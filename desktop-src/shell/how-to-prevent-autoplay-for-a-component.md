---
description: Viene illustrata la chiave del registro di sistema da impostare per impedire AutoPlay.
ms.assetid: E0A25DC2-0991-45D6-9185-019DB4C040AD
title: Come impedire AutoPlay per un componente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ebe03473ce7c5eb441ec428cbe4d060dc62f042
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979530"
---
# <a name="how-to-prevent-autoplay-for-a-component"></a>Come impedire AutoPlay per un componente

Viene illustrata la chiave del registro di sistema da impostare per impedire AutoPlay.

## <a name="instructions"></a>Istruzioni


Per impedire l'avvio di AutoPlay in risposta a un evento, aggiungere il seguente valore **reg \_ SZ** , come illustrato in questo esempio.

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

Il valore è l'identificatore di classe (CLSID) in base al quale il componente che genera l'evento è noto nella tabella degli oggetti in esecuzione (ROT). Il valore non contiene dati.

> [!IMPORTANT]
> Sotto questa chiave, i CLSID non sono racchiusi tra parentesi graffe ( {} ).

 

 

 



