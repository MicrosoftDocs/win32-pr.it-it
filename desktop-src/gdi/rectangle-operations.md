---
description: La funzione serect crea un rettangolo, la funzione CopyRect esegue una copia di un rettangolo specificato e la funzione SetRectEmpty crea un rettangolo vuoto.
ms.assetid: 982d6283-673b-41a1-abc7-10ef87ff3c6f
title: Operazioni Rectangle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3117fda697000e92258c99cf90af470e8815e237
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344641"
---
# <a name="rectangle-operations"></a>Operazioni Rectangle

La funzione [**serect**](/windows/desktop/api/Winuser/nf-winuser-setrect) crea un rettangolo, la funzione [**CopyRect**](/windows/desktop/api/Winuser/nf-winuser-copyrect) esegue una copia di un rettangolo specificato e la funzione [**SetRectEmpty**](/windows/desktop/api/Winuser/nf-winuser-setrectempty) crea un rettangolo vuoto. Un rettangolo vuoto è qualsiasi rettangolo con larghezza zero, altezza zero o entrambi. La funzione [**IsRectEmpty**](/windows/desktop/api/Winuser/nf-winuser-isrectempty) determina se un rettangolo specificato è vuoto. La funzione [**EqualRect**](/windows/desktop/api/Winuser/nf-winuser-equalrect) determina se due rettangoli sono identici, ovvero se hanno le stesse coordinate.

La funzione [**InflateRect**](/windows/desktop/api/Winuser/nf-winuser-inflaterect) aumenta o diminuisce la larghezza o l'altezza di un rettangolo o di entrambi. Consente di aggiungere o rimuovere larghezza da entrambe le estremità del rettangolo. è possibile aggiungere o rimuovere l'altezza sia dalla parte superiore che dalla parte inferiore del rettangolo.

La funzione [**OffsetRect**](/windows/desktop/api/Winuser/nf-winuser-offsetrect) sposta un rettangolo di una determinata quantità. Sposta il rettangolo aggiungendo gli importi x-amount, y-amount o x-e y delle coordinate d'angolo.

La funzione [**PtInRect**](/windows/desktop/api/Winuser/nf-winuser-ptinrect) determina se un punto specificato si trova all'interno di un rettangolo specificato. Il punto si trova nel rettangolo se si trova sul lato sinistro o superiore oppure è completamente all'interno del rettangolo. Il punto non si trova nel rettangolo se si trova sul lato destro o inferiore.

La funzione [**IntersectRect**](/windows/desktop/api/Winuser/nf-winuser-intersectrect) crea un nuovo rettangolo che rappresenta l'intersezione di due rettangoli esistenti, come illustrato nella figura seguente.

![illustrazione che mostra due rettangoli sovrapposti, con ombreggiatura più scura per indicare l'intersezione ](images/csrec-01.png)

La funzione [**UnionRect**](/windows/desktop/api/Winuser/nf-winuser-unionrect) crea un nuovo rettangolo che rappresenta l'Unione di due rettangoli esistenti, come illustrato nella figura seguente.

![illustrazione di due rettangoli sovrapposti, con ombreggiatura più scura che indica le aree all'interno dell'Unione, ma non all'interno di uno dei due rettangoli](images/csrec-02.png)

Per informazioni sulle funzioni che delineano ellissi e poligoni, vedere [forme compilate](filled-shapes.md).

 

 



