---
description: Un contesto di dispositivo contiene attributi che influiscono sull'output di linee e curve. Gli attributi di linea e curva includono la posizione corrente, lo stile del pennello, il colore del pennello, lo stile della penna, il colore della penna, la trasformazione e così via.
ms.assetid: 9529b389-85f6-421f-8429-9b61cee56ef1
title: Attributi di linea e curva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d5ab8758cf6e77b28568cacafd8c57312c052d9e9415211f034e3d1a70b6c09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831611"
---
# <a name="line-and-curve-attributes"></a>Attributi di linea e curva

Un contesto di dispositivo contiene attributi che influiscono sull'output di linee e curve. Gli *attributi di linea e curva* includono la posizione corrente, lo stile del pennello, il colore del pennello, lo stile della penna, il colore della penna, la trasformazione e così via.

La posizione corrente predefinita per qualsiasi controller di dominio si trova nel punto (0,0) nello spazio logico (o mondo). È possibile impostare queste coordinate su una nuova posizione chiamando la [**funzione MoveToEx**](/windows/desktop/api/Wingdi/nf-wingdi-movetoex) e passando un nuovo set di coordinate.

> [!Note]  
> Esistono due set di funzioni di disegno a linee e a curva. Il primo set mantiene la posizione corrente in un controller di dominio e il secondo set modifica la posizione. È possibile identificare le funzioni che modificano la posizione corrente esaminando il nome della funzione. Se il nome della funzione termina con la preposizione "A", la funzione imposta la posizione corrente sul punto finale dell'ultima riga disegnata ([**LineTo**](/windows/desktop/api/Wingdi/nf-wingdi-lineto), [**ArcTo**](/windows/desktop/api/Wingdi/nf-wingdi-arcto), [**PolylineTo**](/windows/desktop/api/Wingdi/nf-wingdi-polylineto)o [**PolyBezierTo**](/windows/desktop/api/Wingdi/nf-wingdi-polybezierto)). Se il nome della funzione non termina con questa preposizione, lascia intatta la posizione corrente [**(Arco,**](/windows/desktop/api/Wingdi/nf-wingdi-arc) [**Polilinea**](/windows/desktop/api/Wingdi/nf-wingdi-polyline)o [**PolyBezier).**](/windows/desktop/api/Wingdi/nf-wingdi-polybezier)

 

Il pennello predefinito è un pennello bianco a tinta unita. Un'applicazione può creare un nuovo pennello chiamando la [**funzione CreateBrushIndirect.**](/windows/desktop/api/Wingdi/nf-wingdi-createbrushindirect) Dopo aver creato un pennello, l'applicazione può selezionarlo nel relativo controller di dominio chiamando la [**funzione SelectObject.**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) Windows fornisce un set completo di funzioni per creare, selezionare e modificare il pennello nel controller di dominio di un'applicazione. Per altre informazioni su queste funzioni e sui pennelli in generale, vedere [Pennelli.](brushes.md)

La penna predefinita è una penna nera a tinta unita con larghezza di un pixel. Un'applicazione può creare una penna usando la [**funzione ExtCreatePen.**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) Dopo aver creato una penna, l'applicazione può selezionarla nel relativo controller di dominio chiamando la [**funzione SelectObject.**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) Windows fornisce un set completo di funzioni per creare, selezionare e modificare la penna nel controller di dominio di un'applicazione. Per altre informazioni su queste funzioni e sulle penne in generale, vedere [Penn](pens.md).

La trasformazione predefinita è la trasformazione Unity (specificata dalla matrice di identità). Un'applicazione può specificare una nuova trasformazione chiamando la [**funzione SetWorldTransform.**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) Windows fornisce un set completo di funzioni per trasformare linee e curve modificandone larghezza, posizione e aspetto generale. Per altre informazioni su queste funzioni, vedere [Coordinate Spaces and Transformations](coordinate-spaces-and-transformations.md).

 

 



