---
description: Un'applicazione crea un'area chiamando una funzione associata a una forma specifica. La tabella seguente illustra le funzioni associate a ognuna delle forme standard.
ms.assetid: e94ae371-8365-4e42-ac8c-04c3928fcffb
title: Creazione e selezione dell'area
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75ce2711b2d1ae9dc6641748c72fd586d02e25964102a8c034593d6e60cbaa33
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092691"
---
# <a name="region-creation-and-selection"></a>Creazione e selezione dell'area

Un'applicazione crea un'area chiamando una funzione associata a una forma specifica. La tabella seguente illustra le funzioni associate a ognuna delle forme standard.



| Forma                                   | Funzione                                                                                                                         |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| Area rettangolare                      | [**CreateRectRgn,**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgn) [**CreateRectRgnIndirect,**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgnindirect) [**SetRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-setrectrgn) |
| Area rettangolare con angoli arrotondati | [**CreateRoundRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createroundrectrgn)                                                                                 |
| Area ellittica                       | [**CreateEllipticRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgn), [ **CreateEllipticRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgnindirect)                   |
| Area poligonale                        | [**CreatePolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolygonrgn), [ **CreatePolyPolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolypolygonrgn)                               |



 

Ogni funzione di creazione dell'area restituisce un handle che identifica la nuova area. Un'applicazione può usare questo handle per selezionare l'area in un contesto di dispositivo chiamando la funzione [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) e fornendo questo handle come secondo argomento. Dopo aver selezionato un'area in un contesto di dispositivo, l'applicazione può eseguire varie operazioni su di essa.

 

 



