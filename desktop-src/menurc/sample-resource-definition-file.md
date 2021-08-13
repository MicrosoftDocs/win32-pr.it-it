---
title: File di Resource-Definition di esempio
description: File di script di esempio che definisce le risorse per un'applicazione denominata Shapes.
ms.assetid: 0362b1be-7671-4685-8eb8-bff502224939
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 141258148b4e7a21d625a44b7f03d5e383c318d10447e050891f32b397c4283d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119226001"
---
# <a name="sample-resource-definition-file"></a>File di Resource-Definition di esempio

L'esempio seguente illustra un file script che definisce le risorse per un'applicazione denominata Shapes:

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

[**L'istruzione CURSOR**](cursor-resource.md) specifica il nome shapesCursor della risorsa cursore dell'applicazione e specifica il file di cursore SHAPES. CUR, che contiene l'immagine per il cursore.

[**L'istruzione ICON**](icon-resource.md) specifica il nome shapesIcon della risorsa icona dell'applicazione e specifica il file dell'icona SHAPES. ICO, che contiene l'immagine per l'icona.

[**L'istruzione MENU**](menu-resource.md) definisce un menu dell'applicazione denominato **ShapesMenu**, un menu a comparsa con cinque voci di menu.

Il corpo della definizione di menu, racchiuso tra parentesi graffe o le parole chiave **BEGIN** ed **END,** specifica ogni voce di menu e l'identificatore di menu restituito quando l'utente seleziona tale voce. Ad esempio, la prima voce del menu, **Cancella**, restituisce l'ID di menu \_ CLEAR quando l'utente lo seleziona. Gli identificatori di menu sono definiti nel file di intestazione dell'applicazione SHAPES.H.

 

 




