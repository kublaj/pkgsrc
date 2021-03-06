# $NetBSD: Makefile,v 1.1 2018/07/04 06:46:49 adam Exp $

DISTNAME=	tables-3.4.4
PKGNAME=	${PYPKGPREFIX}-${DISTNAME}
CATEGORIES=	math python
MASTER_SITES=	${MASTER_SITE_PYPI:=t/tables/}

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://www.pytables.org/
COMMENT=	Database package for large amounts of data
LICENSE=	modified-bsd

PYSETUPBUILDARGS+=	--blosc=${BUILDLINK_PREFIX.blosc}
PYSETUPBUILDARGS+=	--bzip2=${BUILDLINK_PREFIX.bzip2}
PYSETUPBUILDARGS+=	--hdf5=${BUILDLINK_PREFIX.hdf5}
PYSETUPBUILDARGS+=	--lzo=${BUILDLINK_PREFIX.lzo}

DEPENDS+=	${PYPKGPREFIX}-cython-[0-9]*:../../devel/py-cython
DEPENDS+=	${PYPKGPREFIX}-numexpr>=2.5.2:../../math/py-numexpr
DEPENDS+=	${PYPKGPREFIX}-six>=1.9.0:../../lang/py-six

USE_LANGUAGES=		c c++

post-install:
	cd ${DESTDIR}${PREFIX}/bin && \
		${MV} pt2to3 pt2to3${PYVERSSUFFIX} && \
		${MV} ptdump ptdump${PYVERSSUFFIX} && \
		${MV} ptrepack ptrepack${PYVERSSUFFIX} && \
		${MV} pttree pttree${PYVERSSUFFIX} || ${TRUE}

do-test:
	cd ${WRKSRC}/tables/tests && ${PYTHONBIN} test_all.py

.include "../../archivers/bzip2/buildlink3.mk"
.include "../../archivers/lzo/buildlink3.mk"
.include "../../devel/blosc/buildlink3.mk"
.include "../../devel/hdf5/buildlink3.mk"
.include "../../devel/zlib/buildlink3.mk"
.include "../../math/py-numpy/buildlink3.mk"
.include "../../lang/python/egg.mk"
.include "../../mk/bsd.pkg.mk"
