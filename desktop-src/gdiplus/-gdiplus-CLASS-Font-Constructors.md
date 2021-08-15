---
description: Questo argomento elenca i costruttori della classe Font. Per un elenco completo delle classi, vedere Classe Font.
ms.assetid: a0169751-50f6-41d9-bd59-3c85aec1bb78
title: Costruttori di Font.Font
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: ff876120655adcf58318a471ed66ddfa4502d625305d9fda37f01c966e19e0cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977901"
---
# <a name="fontfont-constructors"></a>Costruttori di Font.Font

Questo argomento elenca i costruttori della [**classe Font.**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) Per un elenco completo delle classi, vedere **Classe Font**.

### <a name="overload-list"></a>Elenco di overload



| Costruttore                                                                                                                   | Descrizione                                                                                                                                                                                                                                                                                                  |
|:------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Font(HDC, HFONT)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconsthfont))                                                                | Crea un [**oggetto Font::Font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconsthfont)) indirettamente da un tipo di carattere logico GDI usando un handle per una struttura **GDI LOGFONT.**<br/>                                                                                                                                   |
| [**Font(HDC,LOGFONTA \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconstlogfonta))                                            | Crea un [**oggetto Font::Font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconstlogfonta)) direttamente da un tipo di carattere logico GDI. Il tipo di carattere logico GDI è una **struttura LOGFONTA,** ovvero la versione di un carattere a un byte di un tipo di carattere logico. Questo costruttore viene fornito per la compatibilità con GDI.<br/> |
| [**Font(HDC,LOGFONTW \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconstlogfontw))                                            | Crea un [**oggetto Font::Font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconstlogfontw)) direttamente da un tipo di carattere logico GDI. Il tipo di carattere logico GDI è una **struttura LOGFONTW,** ovvero la versione di caratteri wide di un tipo di carattere logico. Questo costruttore viene fornito per la compatibilità con GDI.<br/>     |
| [**\*Font(FontFamily,REAL,INT,Unit)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inconstfontfamily_inreal_inint_inunit))                                | Crea un [**oggetto Font::Font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inconstfontfamily_inreal_inint_inunit)) basato su un [**oggetto FontFamily,**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) una dimensione, uno stile del carattere e un'unità di misura.<br/>                                                                               |
| [**\*Font(WCHAR,REAL,INT,Unit,FontCollection \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inconstwchar_inreal_inint_inunit_inconstfontcollection)) | Crea un [**oggetto Font::Font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inconstwchar_inreal_inint_inunit_inconstfontcollection)) basato su una famiglia di caratteri, una dimensione, uno stile del carattere, un'unità di misura e un [**oggetto FontCollection.**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontcollection)<br/>                                     |
| [**Font (HDC)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc))                                                                            | Crea un [**oggetto Font::Font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc)) basato sull'oggetto tipo di carattere GDI attualmente selezionato in un contesto di dispositivo specificato. Questo costruttore viene fornito per la compatibilità con GDI. <br/>                                                                           |



 

 
