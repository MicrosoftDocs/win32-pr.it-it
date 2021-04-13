---
description: Un'applicazione crea un'area chiamando una funzione associata a una forma specifica. Nella tabella seguente vengono illustrate le funzioni associate a ognuna delle forme standard.
ms.assetid: e94ae371-8365-4e42-ac8c-04c3928fcffb
title: Creazione e selezione dell'area
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d27a7887e41a04a62015fa3fc9d82f5beeb01d6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978351"
---
# <a name="region-creation-and-selection"></a>Creazione e selezione dell'area

Un'applicazione crea un'area chiamando una funzione associata a una forma specifica. Nella tabella seguente vengono illustrate le funzioni associate a ognuna delle forme standard.



| Con forme                                   | Funzione                                                                                                                         |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| Area rettangolare                      | [**CreateRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgn), [**CreateRectRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgnindirect), [**SetRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-setrectrgn) |
| Area rettangolare con angoli arrotondati | [**CreateRoundRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createroundrectrgn)                                                                                 |
| Area ellittica                       | [**CreateEllipticRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgn), [ **CreateEllipticRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgnindirect)                   |
| Area poligonale                        | [**CreatePolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolygonrgn), [ **CreatePolyPolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolypolygonrgn)                               |



 

Ogni funzione di creazione dell'area restituisce un handle che identifica la nuova area. Un'applicazione può usare questo handle per selezionare l'area in un contesto di dispositivo chiamando la funzione [**SelezionaOggetto**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) e specificando questo handle come secondo argomento. Dopo aver selezionato un'area in un contesto di dispositivo, l'applicazione può eseguire varie operazioni su di essa.

 

 



