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
# <a name="sample-resource-definition-file"></a>File Resource-Definition di esempio

Nell'esempio seguente viene illustrato un file script che definisce le risorse per un'applicazione denominata Shapes:

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

L'istruzione [**Cursor**](cursor-resource.md) denomina la risorsa Cursor dell'applicazione ShapesCursor e specifica le forme del file di cursore. CUR, che contiene l'immagine per il cursore.

L'istruzione [**Icon**](icon-resource.md) denomina la risorsa icona dell'applicazione ShapesIcon e specifica le forme del file icona. ICO, che contiene l'immagine per l'icona.

L'istruzione [**menu**](menu-resource.md) definisce un menu di applicazione denominato **ShapesMenu**, un menu a comparsa con cinque voci di menu.

Il corpo della definizione di menu, racchiuso tra parentesi graffe o parole chiave **Begin** e **end** , specifica ogni voce di menu e l'identificatore di menu restituito quando l'utente seleziona tale elemento. Ad esempio, il primo elemento nel menu, **Clear**, restituisce l'ID dell'identificatore di menu \_ Clear quando l'utente lo seleziona. Gli identificatori di menu vengono definiti nel file di intestazione dell'applicazione, SHAPEs. H.

 

 




