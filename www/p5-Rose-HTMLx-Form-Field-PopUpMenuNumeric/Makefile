# $NetBSD: Makefile,v 1.10 2017/06/05 14:25:30 ryoon Exp $

DISTNAME=	Rose-HTMLx-Form-Field-PopUpMenuNumeric-0.001
PKGNAME=	p5-${DISTNAME}
PKGREVISION=	8
CATEGORIES=	devel perl5
MASTER_SITES=	${MASTER_SITE_PERL_CPAN:=Rose/}

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://search.cpan.org/perldoc?Rose::HTMLx::Form::Field::PopUpMenuNumeric
COMMENT=	Extend Rose::HTML::Objects with popup menu for numeric values
LICENSE=	gnu-gpl-v2 # OR artistic

DEPENDS+=	p5-Rose-HTML-Objects-[0-9]*:../../www/p5-Rose-HTML-Objects

USE_LANGUAGES=	# empty
PERL5_PACKLIST=	auto/Rose/HTMLx/Form/Field/PopUpMenuNumeric/.packlist

.include "../../lang/perl5/module.mk"
.include "../../mk/bsd.pkg.mk"
