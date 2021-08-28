---
description: La funzione SetRect crea un rettangolo, la funzione CopyRect crea una copia di un rettangolo specificato e la funzione SetRectEmpty crea un rettangolo vuoto.
ms.assetid: 982d6283-673b-41a1-abc7-10ef87ff3c6f
title: Operazioni sui rettangoli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 161df56d3534f85cd37701956db0330be59236e3cbbeeed81ef390edd17656bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092761"
---
# <a name="rectangle-operations"></a>Operazioni sui rettangoli

La [**funzione SetRect**](/windows/desktop/api/Winuser/nf-winuser-setrect) crea un rettangolo, la funzione [**CopyRect**](/windows/desktop/api/Winuser/nf-winuser-copyrect) crea una copia di un rettangolo specificato e la [**funzione SetRectEmpty**](/windows/desktop/api/Winuser/nf-winuser-setrectempty) crea un rettangolo vuoto. Un rettangolo vuoto è qualsiasi rettangolo con larghezza zero, altezza zero o entrambi. La [**funzione IsRectEmpty**](/windows/desktop/api/Winuser/nf-winuser-isrectempty) determina se un rettangolo specificato è vuoto. La [**funzione EqualRect**](/windows/desktop/api/Winuser/nf-winuser-equalrect) determina se due rettangoli sono identici, ad esempio se hanno le stesse coordinate.

La [**funzione InflateRect**](/windows/desktop/api/Winuser/nf-winuser-inflaterect) aumenta o riduce la larghezza o l'altezza di un rettangolo o di entrambi. Può aggiungere o rimuovere la larghezza da entrambe le estremità del rettangolo; può aggiungere o rimuovere l'altezza sia dalla parte superiore che dalla parte inferiore del rettangolo.

La [**funzione OffsetRect**](/windows/desktop/api/Winuser/nf-winuser-offsetrect) sposta un rettangolo di una determinata quantità. Sposta il rettangolo aggiungendo le quantità x, y o x e y specificate alle coordinate dell'angolo.

La [**funzione PtInRect**](/windows/desktop/api/Winuser/nf-winuser-ptinrect) determina se un punto specificato si trova all'interno di un rettangolo specificato. Il punto si trova nel rettangolo se si trova sul lato sinistro o superiore o è completamente all'interno del rettangolo. Il punto non si trova nel rettangolo se si trova sul lato destro o inferiore.

La [**funzione IntersectRect**](/windows/desktop/api/Winuser/nf-winuser-intersectrect) crea un nuovo rettangolo che rappresenta l'intersezione di due rettangoli esistenti, come illustrato nella figura seguente.

![Illustrazione che mostra due rettangoli sovrapposti, con ombreggiatura più scura per indicare l'intersezione ](images/csrec-01.png)

La [**funzione UnionRect**](/windows/desktop/api/Winuser/nf-winuser-unionrect) crea un nuovo rettangolo che rappresenta l'unione di due rettangoli esistenti, come illustrato nella figura seguente.

![Illustrazione di due rettangoli sovrapposti, con ombreggiatura più scura che indica le aree all'interno dell'unione, ma non all'interno di uno dei due rettangoli](images/csrec-02.png)

Per informazioni sulle funzioni che disegnano ellissi e poligoni, vedere [Forme riempite.](filled-shapes.md)

 

 



