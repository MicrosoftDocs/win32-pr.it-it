---
title: File Resource-Definition di esempio
description: File script di esempio che definisce le risorse per un'applicazione denominata Shapes.
ms.assetid: 0362b1be-7671-4685-8eb8-bff502224939
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64e6a870b4b63b0e88e5ddcd069e8318e4bdb750
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045055"
---
# <a name="sample-resource-definition-file"></a><span data-ttu-id="64763-103">File Resource-Definition di esempio</span><span class="sxs-lookup"><span data-stu-id="64763-103">Sample Resource-Definition File</span></span>

<span data-ttu-id="64763-104">Nell'esempio seguente viene illustrato un file script che definisce le risorse per un'applicazione denominata Shapes:</span><span class="sxs-lookup"><span data-stu-id="64763-104">The following example shows a script file that defines the resources for an application named Shapes:</span></span>

``` syntax
#include "shapes.h"

ShapesCursor  CURSOR  SHAPES.CUR
ShapesIcon    ICON    SHAPES.ICO

ShapesMenu MENU
{
    POPUP "&Shape"
    {
        MENUITEM "&Clear", ID_CLEAR
        MENUITEM "&Rectangle", ID_RECT
        MENUITEM "&Triangle", ID_TRIANGLE
        MENUITEM "&Star", ID_STAR
        MENUITEM "&Ellipse", ID_ELLIPSE
    }
}
```

<span data-ttu-id="64763-105">L'istruzione [**Cursor**](cursor-resource.md) denomina la risorsa Cursor dell'applicazione ShapesCursor e specifica le forme del file di cursore. CUR, che contiene l'immagine per il cursore.</span><span class="sxs-lookup"><span data-stu-id="64763-105">The [**CURSOR**](cursor-resource.md) statement names the application's cursor resource ShapesCursor and specifies the cursor file SHAPES.CUR, which contains the image for that cursor.</span></span>

<span data-ttu-id="64763-106">L'istruzione [**Icon**](icon-resource.md) denomina la risorsa icona dell'applicazione ShapesIcon e specifica le forme del file icona. ICO, che contiene l'immagine per l'icona.</span><span class="sxs-lookup"><span data-stu-id="64763-106">The [**ICON**](icon-resource.md) statement names the application's icon resource ShapesIcon and specifies the icon file SHAPES.ICO, which contains the image for that icon.</span></span>

<span data-ttu-id="64763-107">L'istruzione [**menu**](menu-resource.md) definisce un menu di applicazione denominato **ShapesMenu**, un menu a comparsa con cinque voci di menu.</span><span class="sxs-lookup"><span data-stu-id="64763-107">The [**MENU**](menu-resource.md) statement defines an application menu named **ShapesMenu**, a pop-up menu with five menu items.</span></span>

<span data-ttu-id="64763-108">Il corpo della definizione di menu, racchiuso tra parentesi graffe o parole chiave **Begin** e **end** , specifica ogni voce di menu e l'identificatore di menu restituito quando l'utente seleziona tale elemento.</span><span class="sxs-lookup"><span data-stu-id="64763-108">The body of the menu definition, enclosed by the curly braces, or the **BEGIN** and **END** keywords, specifies each menu item and the menu identifier that is returned when the user selects that item.</span></span> <span data-ttu-id="64763-109">Ad esempio, il primo elemento nel menu, **Clear**, restituisce l'ID dell'identificatore di menu \_ Clear quando l'utente lo seleziona.</span><span class="sxs-lookup"><span data-stu-id="64763-109">For example, the first item on the menu, **Clear**, returns the menu identifier ID\_CLEAR when the user selects it.</span></span> <span data-ttu-id="64763-110">Gli identificatori di menu vengono definiti nel file di intestazione dell'applicazione, SHAPEs. H.</span><span class="sxs-lookup"><span data-stu-id="64763-110">The menu identifiers are defined in the application header file, SHAPES.H.</span></span>

 

 




