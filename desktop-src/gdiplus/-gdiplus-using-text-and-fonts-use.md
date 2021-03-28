---
description: In Windows GDI+ sono disponibili diverse classi che costituiscono la base per la creazione di testo.
ms.assetid: 12bc38c3-5fbc-4d7b-902c-92a5f5057473
title: Utilizzo di testo e tipi di carattere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f28ec157888dcf45b309237eb0f7eefff17808c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526058"
---
# <a name="using-text-and-fonts"></a>Utilizzo di testo e tipi di carattere

In Windows GDI+ sono disponibili diverse classi che costituiscono la base per la creazione di testo. La classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) presenta diversi metodi [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) che consentono di specificare diverse funzionalità del testo, ad esempio la posizione, il rettangolo di delimitazione, il tipo di carattere e il formato. Altre classi che contribuiscono al rendering del testo includono [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font), [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat), [**InstalledFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-installedfontcollection)e [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection).

Gli argomenti seguenti illustrano il testo e i caratteri in modo più dettagliato:

-   [Creazione di gruppi di caratteri e tipi di carattere](-gdiplus-constructing-font-families-and-fonts-use.md)
-   [Disegno di testo](-gdiplus-drawing-text-use.md)
-   [Formattazione del testo](-gdiplus-formatting-text-use.md)
-   [Enumerazione dei tipi di carattere installati](-gdiplus-enumerating-installed-fonts-use.md)
-   [Creazione di raccolte private di tipi di carattere](-gdiplus-creating-a-private-font-collection-use.md)
-   [Recupero della metrica dei tipi di carattere](-gdiplus-obtaining-font-metrics-use.md)
-   [Anti-aliasing con testo](-gdiplus-antialiasing-with-text-use.md)

 

 



