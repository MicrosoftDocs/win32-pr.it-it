---
description: Questo argomento elenca i costruttori della classe Font. Per un elenco completo delle classi, vedere classe Font.
ms.assetid: a0169751-50f6-41d9-bd59-3c85aec1bb78
title: Costruttori font. font
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: bdf533e292734956c02d3f8a424ca619cb722c71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233749"
---
# <a name="fontfont-constructors"></a>Costruttori font. font

Questo argomento elenca i costruttori della classe [**font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) . Per un elenco completo delle classi, vedere **classe Font**.

### <a name="overload-list"></a>Elenco di overload



| Costruttore                                                                                                                   | Descrizione                                                                                                                                                                                                                                                                                                  |
|:------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Tipo di carattere (HDC, HFONT)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconsthfont))                                                                | Crea un oggetto [**font:: font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconsthfont)) indirettamente da un tipo di carattere logico GDI usando un handle per una struttura **LOGFONT** di GDI.<br/>                                                                                                                                   |
| [**Tipo di carattere (HDC, LOGFONTA \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconstlogfonta))                                            | Crea un oggetto [**font:: font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconstlogfonta)) direttamente da un tipo di carattere logico GDI. Il tipo di carattere logico GDI è una struttura **LOGFONTA** , che è la versione a un byte di un carattere logico. Questo costruttore viene fornito per la compatibilità con GDI.<br/> |
| [**Tipo di carattere (HDC, Campo LOGFONTW \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconstlogfontw))                                            | Crea un oggetto [**font:: font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconstlogfontw)) direttamente da un tipo di carattere logico GDI. Il tipo di carattere logico GDI è una struttura **Campo LOGFONTW** , che è la versione a caratteri wide di un tipo di carattere logico. Questo costruttore viene fornito per la compatibilità con GDI.<br/>     |
| [**Font (FontFamily \* , Real, int, Unit)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inconstfontfamily_inreal_inint_inunit))                                | Crea un oggetto [**font:: font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inconstfontfamily_inreal_inint_inunit)) basato su un oggetto [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) , una dimensione, uno stile del tipo di carattere e un'unità di misura.<br/>                                                                               |
| [**Font (WCHAR \* , Real, int, Unit, FontCollection \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inconstwchar_inreal_inint_inunit_inconstfontcollection)) | Crea un oggetto [**font:: font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inconstwchar_inreal_inint_inunit_inconstfontcollection)) basato su una famiglia di caratteri, una dimensione, uno stile del tipo di carattere, un'unità di misura e un oggetto [**FontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontcollection) .<br/>                                     |
| [**Tipo di carattere (HDC)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc))                                                                            | Crea un oggetto [**font:: font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc)) basato sull'oggetto del tipo di carattere GDI attualmente selezionato in un contesto di dispositivo specificato. Questo costruttore viene fornito per la compatibilità con GDI. <br/>                                                                           |



 

 
