# $NetBSD: Makefile,v 1.10 2017/06/05 14:24:16 ryoon Exp $
#

DISTNAME=	Danga-Socket-1.61
PKGNAME=	p5-${DISTNAME}
PKGREVISION=	7
CATEGORIES=	net
MASTER_SITES=	http://search.cpan.org/CPAN/authors/id/B/BR/BRADFITZ/

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://search.cpan.org/CPAN/authors/id/B/BR/BRADFITZ/
COMMENT=	Event loop and event-driven async socket base class
LICENSE=	${PERL5_LICENSE}

DEPENDS+=	p5-Sys-Syscall>=0:../../devel/p5-Sys-Syscall
#DEPENDS+=	{perl>=5.7.3,p5-Time-HiRes>=0}:../../time/p5-Time-HiRes

PERL5_PACKLIST=	auto/Danga/Socket/.packlist
USE_LANGUAGES=	# none

.include "../../lang/perl5/module.mk"
.include "../../mk/bsd.pkg.mk"
