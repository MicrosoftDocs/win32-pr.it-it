---
description: Dopo che un'applicazione ha creato un controller di dominio di visualizzazione o stampante, può iniziare a disegnare sul dispositivo associato o, nel caso del controller di dominio di memoria, può iniziare a disegnare sulla bitmap archiviata in memoria.
ms.assetid: 73657a66-9415-4db0-a800-463c3d639240
title: Operazioni sugli oggetti grafici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 104ae7467e04f53196c839b6daa72482ab73845c3185208eb3cb886cb0ce6a44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965621"
---
# <a name="operations-on-graphic-objects"></a>Operazioni sugli oggetti grafici

Dopo che un'applicazione ha creato un controller di dominio di visualizzazione o stampante, può iniziare a disegnare sul dispositivo associato o, nel caso del controller di dominio di memoria, può iniziare a disegnare sulla bitmap archiviata in memoria. Tuttavia, prima dell'inizio del disegno e talvolta mentre è in corso il disegno, è spesso necessario sostituire gli oggetti predefiniti con nuovi oggetti.

Un'applicazione può esaminare gli attributi di un oggetto predefinito chiamando le [**funzioni GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) [**e GetObject.**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) La **funzione GetCurrentObject** restituisce un handle che identifica la penna, il pennello, la tavolozza, la bitmap o il tipo di carattere corrente e la funzione **GetObject** inizializza una struttura contenente gli attributi dell'oggetto.

Alcune stampanti forniscono pennari, pennelli e tipi di carattere residenti che possono essere usati per migliorare la velocità di disegno in un'applicazione. Per enumerare questi oggetti è possibile usare due funzioni: [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) ed [**EnumFontFamilies**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa). Se l'applicazione deve enumerare penna o pennelli residenti, può chiamare la **funzione EnumObjects** per esaminare gli attributi corrispondenti. Se l'applicazione deve enumerare i tipi di carattere residenti, può chiamare la **funzione EnumFontFamilies** (che può enumerare anche i tipi di carattere GDI).

Quando un'applicazione determina che un oggetto predefinito deve essere sostituito, crea un nuovo oggetto chiamando una delle funzioni di creazione seguenti.



| Oggetto grafico | Funzione                                                                                                                                                                                                                                                                                                                                                             |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bitmap         | [**CreateBitmap,**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap) [**CreateBitmapIndirect,**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect) [**CreateCompatibleBitmap,**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) [**CreateDiscardableBitmap,**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap) [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap)                                                                                                           |
| Brush          | [**CreateBrushIndirect,**](/windows/desktop/api/Wingdi/nf-wingdi-createbrushindirect) [**CreateDIBPatternBrush,**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrush) [**CreateDIBPatternBrushPt,**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrushpt) [**CreateHatchBrush,**](/windows/desktop/api/Wingdi/nf-wingdi-createhatchbrush) [**CreatePatternBrush,**](/windows/desktop/api/Wingdi/nf-wingdi-createpatternbrush) [**CreateSolidBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createsolidbrush)                                                 |
| Tavolozza dei colori  | [**CreatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-createpalette)                                                                                                                                                                                                                                                                                                                               |
| Carattere           | [**CreateFont**](/windows/desktop/api/Wingdi/nf-wingdi-createfonta), [ **CreateFontIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createfontindirecta)                                                                                                                                                                                                                                                                                   |
| Penna            | [**CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect), [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen)                                                                                                                                                                                                                                                 |
| Region         | [**CreateEllipticRgn,**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgn) [**CreateEllipticRgnIndirect,**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgnindirect) [**CreatePolygonRgn,**](/windows/desktop/api/Wingdi/nf-wingdi-createpolygonrgn) [**CreatePolyPolygonRgn,**](/windows/desktop/api/Wingdi/nf-wingdi-createpolypolygonrgn) [**CreateRectRgn,**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgn) [**CreateRectRgnIndirect,**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgnindirect) [**CreateRoundRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createroundrectrgn) |



 

Ognuna di queste funzioni restituisce un handle che identifica un nuovo oggetto. Dopo che un'applicazione recupera un handle, deve chiamare la [**funzione SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) per sostituire l'oggetto predefinito. Tuttavia, l'applicazione deve salvare l'handle che identifica l'oggetto predefinito e usare questo handle per sostituire il nuovo oggetto quando non è più necessario. Quando l'applicazione termina di disegnare con il nuovo oggetto, deve ripristinare l'oggetto predefinito chiamando la funzione **SelectObject** e quindi eliminare il nuovo oggetto chiamando la [**funzione DeleteObject.**](/windows/desktop/api/Wingdi/nf-wingdi-deleteobject) La mancata eliminazione di oggetti causa gravi problemi di prestazioni.

 

 



