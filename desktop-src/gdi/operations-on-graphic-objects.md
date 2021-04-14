---
description: Dopo che un'applicazione ha creato un controller di dominio di visualizzazione o di stampa, può iniziare a disegnare sul dispositivo associato o, nel caso del controller di dominio della memoria, può iniziare a disegnare sulla bitmap archiviata in memoria.
ms.assetid: 73657a66-9415-4db0-a800-463c3d639240
title: Operazioni sugli oggetti grafici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec0574b8527dbf83b4cb4a38163dcf7b33017336
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978490"
---
# <a name="operations-on-graphic-objects"></a>Operazioni sugli oggetti grafici

Dopo che un'applicazione ha creato un controller di dominio di visualizzazione o di stampa, può iniziare a disegnare sul dispositivo associato o, nel caso del controller di dominio della memoria, può iniziare a disegnare sulla bitmap archiviata in memoria. Tuttavia, prima dell'inizio del disegno e talvolta durante il disegno è in corso, spesso è necessario sostituire gli oggetti predefiniti con i nuovi oggetti.

Un'applicazione può esaminare gli attributi di un oggetto predefinito chiamando le funzioni [**GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) e [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) . La funzione **GetCurrentObject** restituisce un handle che identifica la penna, il pennello, la tavolozza, la bitmap o il tipo di carattere corrente e la funzione **GetObject** Inizializza una struttura che contiene gli attributi dell'oggetto.

Alcune stampanti forniscono penne, pennelli e tipi di carattere residenti che possono essere utilizzati per migliorare la velocità di disegno in un'applicazione. Per enumerare questi oggetti, è possibile usare due funzioni: [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) e [**EnumFontFamilies**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa). Se l'applicazione deve enumerare le penne o i pennelli residenti, può chiamare la funzione **EnumObjects** per esaminare gli attributi corrispondenti. Se l'applicazione deve enumerare i tipi di carattere residenti, può chiamare la funzione **EnumFontFamilies** , che può anche enumerare i tipi di carattere GDI.

Una volta che un'applicazione ha determinato che è necessario sostituire un oggetto predefinito, viene creato un nuovo oggetto chiamando una delle funzioni di creazione seguenti.



| Oggetto grafico | Funzione                                                                                                                                                                                                                                                                                                                                                             |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bitmap         | [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap), [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect), [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap), [**CreateDiscardableBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap), [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap)                                                                                                           |
| Brush          | [**CreateBrushIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbrushindirect), [**CreateDIBPatternBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrush), [**CreateDIBPatternBrushPt**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrushpt), [**CreateHatchBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createhatchbrush), [**CreatePatternBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createpatternbrush), [**CreateSolidBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createsolidbrush)                                                 |
| Tavolozza dei colori  | [**CreatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-createpalette)                                                                                                                                                                                                                                                                                                                               |
| Carattere           | [**CreateFont**](/windows/desktop/api/Wingdi/nf-wingdi-createfonta), [ **CreateFontIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createfontindirecta)                                                                                                                                                                                                                                                                                   |
| Penna            | [**CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect), [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen)                                                                                                                                                                                                                                                 |
| Region         | [**CreateEllipticRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgn), [**CreateEllipticRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgnindirect), [**CreatePolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolygonrgn), [**CreatePolyPolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolypolygonrgn), [**CreateRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgn), [**CreateRectRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgnindirect), [**CreateRoundRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createroundrectrgn) |



 

Ognuna di queste funzioni restituisce un handle che identifica un nuovo oggetto. Quando un'applicazione recupera un handle, deve chiamare la funzione [**SelezionaOggetto**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) per sostituire l'oggetto predefinito. Tuttavia, l'applicazione deve salvare l'handle che identifica l'oggetto predefinito e utilizzare questo handle per sostituire il nuovo oggetto quando non è più necessario. Quando l'applicazione termina il disegno con il nuovo oggetto, deve ripristinare l'oggetto predefinito chiamando la funzione **SelezionaOggetto** e quindi eliminare il nuovo oggetto chiamando la funzione [**DeleteObject**](/windows/desktop/api/Wingdi/nf-wingdi-deleteobject) . La mancata eliminazione degli oggetti causa gravi problemi di prestazioni.

 

 



