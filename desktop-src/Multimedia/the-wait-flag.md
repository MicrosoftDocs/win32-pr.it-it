---
title: Flag di attesa
description: Flag di attesa
ms.assetid: b971ccd4-0507-4f05-adb3-d4930496034d
keywords:
- Flag di MCI_WAIT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e552650aca9cf104d2c87d7faddd0b6c85b5a6b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045372"
---
# <a name="the-wait-flag"></a>Flag di attesa

I comandi MCI in genere restituiscono immediatamente l'utente, anche se sono necessari alcuni minuti per completare l'azione iniziata dal comando. È possibile usare il flag di attesa (MCI \_ Wait) per indirizzare il dispositivo in modo che attenda che l'azione richiesta venga completata prima di restituire il controllo all'applicazione.

Ad esempio, il comando [**Play**](play.md) seguente non restituirà il controllo all'applicazione fino a quando non viene completata la riproduzione:


```C++
mciSendString("play mydevice from 0 to 100 wait", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



> [!Note]  
> L'utente può annullare un'operazione di attesa premendo un tasto di interruzione. Per impostazione predefinita, questa chiave è CTRL + INTERr. Le applicazioni possono ridefinire questa chiave utilizzando il comando [**break**](break.md) ([**MCI \_ break**](mci-break.md)). (**L' \_ interruzioni MCI** utilizza la struttura [**\_ \_ parametri di MCI break**](mci-break-parms.md) ). Quando viene annullata un'operazione di attesa, MCI tenta di restituire il controllo all'applicazione senza interrompere il comando associato al flag "Wait".

 

 

 




