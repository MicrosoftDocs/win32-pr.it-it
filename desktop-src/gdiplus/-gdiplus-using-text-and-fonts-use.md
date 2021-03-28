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
# <a name="using-text-and-fonts"></a><span data-ttu-id="95cec-103">Utilizzo di testo e tipi di carattere</span><span class="sxs-lookup"><span data-stu-id="95cec-103">Using Text and Fonts</span></span>

<span data-ttu-id="95cec-104">In Windows GDI+ sono disponibili diverse classi che costituiscono la base per la creazione di testo.</span><span class="sxs-lookup"><span data-stu-id="95cec-104">Windows GDI+ provides several classes that form the foundation for drawing text.</span></span> <span data-ttu-id="95cec-105">La classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) presenta diversi metodi [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) che consentono di specificare diverse funzionalità del testo, ad esempio la posizione, il rettangolo di delimitazione, il tipo di carattere e il formato.</span><span class="sxs-lookup"><span data-stu-id="95cec-105">The [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class has several [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) methods that allow you to specify various features of text, such as location, bounding rectangle, font, and format.</span></span> <span data-ttu-id="95cec-106">Altre classi che contribuiscono al rendering del testo includono [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font), [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat), [**InstalledFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-installedfontcollection)e [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection).</span><span class="sxs-lookup"><span data-stu-id="95cec-106">Other classes that contribute to text rendering include [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font), [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat), [**InstalledFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-installedfontcollection), and [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection).</span></span>

<span data-ttu-id="95cec-107">Gli argomenti seguenti illustrano il testo e i caratteri in modo più dettagliato:</span><span class="sxs-lookup"><span data-stu-id="95cec-107">The following topics cover text and fonts in more detail:</span></span>

-   [<span data-ttu-id="95cec-108">Creazione di gruppi di caratteri e tipi di carattere</span><span class="sxs-lookup"><span data-stu-id="95cec-108">Constructing Font Families and Fonts</span></span>](-gdiplus-constructing-font-families-and-fonts-use.md)
-   [<span data-ttu-id="95cec-109">Disegno di testo</span><span class="sxs-lookup"><span data-stu-id="95cec-109">Drawing Text</span></span>](-gdiplus-drawing-text-use.md)
-   [<span data-ttu-id="95cec-110">Formattazione del testo</span><span class="sxs-lookup"><span data-stu-id="95cec-110">Formatting Text</span></span>](-gdiplus-formatting-text-use.md)
-   [<span data-ttu-id="95cec-111">Enumerazione dei tipi di carattere installati</span><span class="sxs-lookup"><span data-stu-id="95cec-111">Enumerating Installed Fonts</span></span>](-gdiplus-enumerating-installed-fonts-use.md)
-   [<span data-ttu-id="95cec-112">Creazione di raccolte private di tipi di carattere</span><span class="sxs-lookup"><span data-stu-id="95cec-112">Creating a Private Font Collection</span></span>](-gdiplus-creating-a-private-font-collection-use.md)
-   [<span data-ttu-id="95cec-113">Recupero della metrica dei tipi di carattere</span><span class="sxs-lookup"><span data-stu-id="95cec-113">Obtaining Font Metrics</span></span>](-gdiplus-obtaining-font-metrics-use.md)
-   [<span data-ttu-id="95cec-114">Anti-aliasing con testo</span><span class="sxs-lookup"><span data-stu-id="95cec-114">Antialiasing with Text</span></span>](-gdiplus-antialiasing-with-text-use.md)

 

 



