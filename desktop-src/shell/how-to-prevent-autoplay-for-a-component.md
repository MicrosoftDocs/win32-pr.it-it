---
description: Illustra quale chiave del Registro di sistema deve essere impostata per impedire AutoPlay.
ms.assetid: E0A25DC2-0991-45D6-9185-019DB4C040AD
title: Come impedire La riproduzione automatica per un componente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d3b44817f6803c25bbf506a5f76c8b068c683af4b5d4c7536482c30cd3aee2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117859688"
---
# <a name="how-to-prevent-autoplay-for-a-component"></a>Come impedire La riproduzione automatica per un componente

Illustra quale chiave del Registro di sistema deve essere impostata per impedire AutoPlay.

## <a name="instructions"></a>Istruzioni


Per impedire l'avvio di AutoPlay in risposta a un evento, aggiungere il valore **\_ REG SZ** seguente, come illustrato in questo esempio.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     CancelAutoplay
                        CLSID
                           00000000-0000-0000-0000-000000000000
```

Il valore è l'identificatore di classe (CLSID) noto dal componente che genera l'evento nella tabella degli oggetti in esecuzione (ROT). Il valore non contiene dati.

> [!IMPORTANT]
> In questa chiave i CLSID non sono racchiusi tra parentesi graffe ( {} ).

 

 

 



