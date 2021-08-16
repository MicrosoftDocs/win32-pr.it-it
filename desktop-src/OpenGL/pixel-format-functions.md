---
title: Funzioni di formato pixel
description: Le funzioni Windows seguenti gestiscono i formati pixel.
ms.assetid: 78a6be75-72f6-4aef-a6bc-5f052c6fe2e9
keywords:
- Funzioni WGL, formato pixel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46c4b82a2b6cd91dd007cecf78065fa0c01204ecf468017ec7e121bd764c9ff2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119486331"
---
# <a name="pixel-format-functions"></a>Funzioni di formato pixel

Le funzioni Windows seguenti gestiscono i formati pixel.



| Windows Funzione                                               | Descrizione                                                                                                                                                           |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)                 | Ottiene il formato pixel del contesto di dispositivo che corrisponde più vicino a un formato pixel specificato.                                                                      |
| [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat)                       | Imposta il formato pixel corrente di un contesto di dispositivo sul formato pixel specificato da un indice del formato pixel.                                                                   |
| [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat)                       | Ottiene l'indice del formato pixel del formato pixel corrente di un contesto di dispositivo.                                                                                            |
| [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat)             | Dati un contesto di dispositivo e un indice di formato pixel, inserisce una struttura di dati [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) con le proprietà del formato pixel. |
| [**GetEnhMetaFilePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getenhmetafilepixelformat) | Recupera le informazioni sul formato pixel per un metafile avanzato.                                                                                                          |



 

La [**funzione ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat) restituisce un indice in formato pixel in base uno che identifica la corrispondenza migliore dai formati pixel supportati dal contesto di dispositivo.

La [**funzione SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat) identifica il formato desiderato usando un indice in formato pixel basato su uno. In genere, si chiama **ChoosePixelFormat** per trovare un formato pixel più adatto e quindi si chiama **SetPixelFormat** con il risultato **di ChoosePixelFormat**.

Se si chiama **SetPixelFormat per** un contesto di dispositivo che fa riferimento a una finestra, **SetPixelFormat** modifica anche il formato pixel della finestra. L'impostazione del formato pixel di una finestra più volte può causare complicazioni significative per Gestione finestre e per le applicazioni multithread, quindi non è consentito. È possibile impostare il formato pixel di una finestra una sola volta; Successivamente, il formato pixel della finestra non può essere modificato.

La [**funzione GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat) restituisce un indice in formato pixel in base uno.

La [**funzione DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) accetta quanto segue come parametri:

-   Handle per un contesto di dispositivo
-   Indice in formato pixel
-   Puntatore a una struttura di [**dati PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor)

La [**funzione DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) restituisce con i membri di **PIXELFORMATDESCRIPTOR** impostati in modo appropriato.

La **funzione GetEnhMetaFilePixelFormat** restituisce le dimensioni del formato pixel di un metafile e recupera le informazioni sul formato pixel del metafile.

 

 




