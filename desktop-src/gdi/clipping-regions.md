---
description: Un'area di ridimensionamento è uno degli oggetti grafici che un'applicazione può selezionare in un contesto di dispositivo (DC).
ms.assetid: d9238ee5-3305-4e85-aef3-2c5c8b74aacd
title: Aree di ridimensionamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a830e05b2a9ce709183f23fad66f937c8c512acd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130830"
---
# <a name="clipping-regions"></a>Aree di ridimensionamento

Un'area di ridimensionamento è uno degli oggetti grafici che un'applicazione può selezionare in un contesto di dispositivo (DC). È in genere rettangolare. Alcuni contesti di dispositivo forniscono un'area di visualizzazione predefinita o predefinita, mentre altri no. Se, ad esempio, si ottiene un handle del contesto di dispositivo dalla funzione [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) , il controller di dominio contiene un'area di ritaglio rettangolare predefinita che corrisponde al rettangolo non valido che richiede il ridisegno. Tuttavia, quando si ottiene un handle del contesto di dispositivo chiamando la funzione [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) con un parametro _HWND_ **null** oppure chiamando la funzione [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) , il controller di dominio non contiene un'area di visualizzazione predefinita. Per altre informazioni sui contesti di dispositivo restituiti dalla funzione **BeginPaint** , vedere [disegno e disegno](painting-and-drawing.md) . Per altre informazioni sui contesti di dispositivo restituiti dalle funzioni **CreateDC** e **GetDC** , vedere [contesti di dispositivo](device-contexts.md).

Le applicazioni possono eseguire una serie di operazioni sulle aree di ritaglio. Alcune di queste operazioni richiedono un handle che identifichi l'area e altre no. Ad esempio, un'applicazione può eseguire le operazioni seguenti direttamente in un'area di visualizzazione del contesto di dispositivo.

-   Determinare se l'output grafico viene visualizzato all'interno dei bordi dell'area passando le coordinate della forma riga, arco, bitmap, testo o riempimento corrispondente alla funzione [**PtVisible**](/windows/desktop/api/Wingdi/nf-wingdi-ptvisible) .
-   Determinare se parte dell'area client interseca un'area chiamando la funzione [**RectVisible**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible) .
-   Spostare l'area esistente in base a un offset specificato chiamando la funzione [**OffsetClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-offsetcliprgn) .
-   Escludere una parte rettangolare dell'area client dall'area di ritaglio corrente chiamando la funzione [**ExcludeClipRect**](/windows/desktop/api/Wingdi/nf-wingdi-excludecliprect) .
-   Combinare una parte rettangolare dell'area client con l'area di ritaglio corrente chiamando la funzione [**IntersectClipRect**](/windows/desktop/api/Wingdi/nf-wingdi-intersectcliprect) .

Dopo avere ottenuto un handle che identifica l'area di visualizzazione, un'applicazione può eseguire qualsiasi operazione comune con le aree, ad esempio:

-   Combinazione di una copia dell'area di visualizzazione corrente con una seconda area chiamando la funzione [**CombineRgn**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn) .
-   Confrontare una copia dell'area di visualizzazione corrente con una seconda area chiamando la funzione [**EqualRgn**](/windows/desktop/api/Wingdi/nf-wingdi-equalrgn) .
-   Determinare se un punto si trova all'interno di una copia dell'area di ritaglio corrente chiamando la funzione [**PtInRegion**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion) .

 

 



