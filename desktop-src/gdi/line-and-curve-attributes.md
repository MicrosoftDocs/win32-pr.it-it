---
description: Un contesto di dispositivo (DC) contiene attributi che influiscono sull'output della linea e della curva. Gli attributi di linea e curva includono la posizione corrente, lo stile del pennello, il colore del pennello, lo stile della penna, il colore della penna, la trasformazione e così via.
ms.assetid: 9529b389-85f6-421f-8429-9b61cee56ef1
title: Attributi di linea e curva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6ec13ea49a72447045c45ea2837ba40e64e6741
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993949"
---
# <a name="line-and-curve-attributes"></a>Attributi di linea e curva

Un contesto di dispositivo (DC) contiene attributi che influiscono sull'output della linea e della curva. Gli *attributi di linea e curva* includono la posizione corrente, lo stile del pennello, il colore del pennello, lo stile della penna, il colore della penna, la trasformazione e così via.

La posizione corrente predefinita per tutti i controller di dominio si trova nel punto (0,0) nello spazio logico (o mondo). È possibile impostare queste coordinate su una nuova posizione chiamando la funzione [**MoveToEx**](/windows/desktop/api/Wingdi/nf-wingdi-movetoex) e passando un nuovo set di coordinate.

> [!Note]  
> Sono disponibili due set di funzioni di disegno linea e curva. Il primo set mantiene la posizione corrente in un controller di dominio e il secondo set modifica la posizione. È possibile identificare le funzioni che modificano la posizione corrente esaminando il nome della funzione. Se il nome della funzione termina con la preposizione "to", la funzione imposta la posizione corrente sul punto finale dell'ultima riga disegnata ([**LineTo**](/windows/desktop/api/Wingdi/nf-wingdi-lineto), [**ArcTo**](/windows/desktop/api/Wingdi/nf-wingdi-arcto), [**PolyLineTo**](/windows/desktop/api/Wingdi/nf-wingdi-polylineto)o [**PolyBezierTo**](/windows/desktop/api/Wingdi/nf-wingdi-polybezierto)). Se il nome della funzione non termina con questa preposizione, lascia intatta la posizione corrente ([**Arc**](/windows/desktop/api/Wingdi/nf-wingdi-arc), [**polilinea**](/windows/desktop/api/Wingdi/nf-wingdi-polyline)o [**polibezier**](/windows/desktop/api/Wingdi/nf-wingdi-polybezier)).

 

Il pennello predefinito è un pennello bianco a tinta unita. Un'applicazione può creare un nuovo pennello chiamando la funzione [**CreateBrushIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbrushindirect) . Dopo la creazione di un pennello, l'applicazione può selezionarla nel proprio controller di dominio chiamando la funzione [**SelezionaOggetto**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) . Windows offre un set completo di funzioni per creare, selezionare e modificare il pennello nel controller di dominio di un'applicazione. Per ulteriori informazioni su queste funzioni e sui pennelli in generale, vedere [pennelli](brushes.md).

La penna predefinita è un pennarello nero a tinta unita di un pixel di larghezza. Un'applicazione può creare una penna tramite la funzione [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) . Dopo la creazione di una penna, l'applicazione può selezionarla nel proprio controller di dominio chiamando la funzione [**SelezionaOggetto**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) . Windows offre un set completo di funzioni per creare, selezionare e modificare la penna nel controller di dominio di un'applicazione. Per ulteriori informazioni su queste funzioni e sulle penne in generale, vedere [penne](pens.md).

La trasformazione predefinita è la trasformazione Unity (specificata dalla matrice di identità). Un'applicazione può specificare una nuova trasformazione chiamando la funzione [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) . Windows offre un set completo di funzioni per trasformare linee e curve modificando la larghezza, la posizione e l'aspetto generale. Per ulteriori informazioni su queste funzioni, vedere [Coordinate spaces and Transformations](coordinate-spaces-and-transformations.md).

 

 



