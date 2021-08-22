---
description: Windows GDI+ fornisce diverse classi che formano le basi per il disegno di testo.
ms.assetid: 12bc38c3-5fbc-4d7b-902c-92a5f5057473
title: Uso di testo e tipi di carattere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2cffc8c36da4c9dd8bbc78c6660a7cc85094071350003c5b23ce4d6a6ce7cad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119359601"
---
# <a name="using-text-and-fonts"></a>Uso di testo e tipi di carattere

Windows GDI+ fornisce diverse classi che formano le basi per il disegno di testo. La [**classe Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) include diversi metodi [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) che consentono di specificare varie funzionalità del testo, ad esempio posizione, rettangolo di delimitazione, tipo di carattere e formato. Altre classi che contribuiscono al rendering del testo includono [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font), [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat), [**InstalledFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-installedfontcollection)e [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection).

Gli argomenti seguenti descrivono il testo e i tipi di carattere in modo più dettagliato:

-   [Costruzione di famiglie di caratteri e tipi di carattere](-gdiplus-constructing-font-families-and-fonts-use.md)
-   [Disegno di testo](-gdiplus-drawing-text-use.md)
-   [Formattazione del testo](-gdiplus-formatting-text-use.md)
-   [Enumerazione dei tipi di carattere installati](-gdiplus-enumerating-installed-fonts-use.md)
-   [Creazione di raccolte private di tipi di carattere](-gdiplus-creating-a-private-font-collection-use.md)
-   [Recupero delle metriche dei tipi di carattere](-gdiplus-obtaining-font-metrics-use.md)
-   [Antialiasing con testo](-gdiplus-antialiasing-with-text-use.md)

 

 



