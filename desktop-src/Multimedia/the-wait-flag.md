---
title: Flag di attesa
description: Flag di attesa
ms.assetid: b971ccd4-0507-4f05-adb3-d4930496034d
keywords:
- MCI_WAIT flag
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 311e1a55e756cfc3c1038f6ab3ccb4b708bb066dde962afff31006dcf39b7c4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117801435"
---
# <a name="the-wait-flag"></a>Flag di attesa

I comandi MCI in genere tornano immediatamente all'utente, anche se sono necessari alcuni minuti per completare l'azione avviata dal comando. È possibile usare il flag "wait" (MCI WAIT) per indirizzare il dispositivo ad attendere il completamento dell'azione richiesta prima di restituire il controllo \_ all'applicazione.

Ad esempio, il comando [**di riproduzione**](play.md) seguente non restituirà il controllo all'applicazione fino al completamento della riproduzione:


```C++
mciSendString("play mydevice from 0 to 100 wait", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



> [!Note]  
> L'utente può annullare un'operazione di attesa premendo un tasto di interruzione. Per impostazione predefinita, questo tasto è CTRL+INTERR. Le applicazioni possono ridefinire questa chiave usando il [**comando break**](break.md) ([**MCI \_ BREAK).**](mci-break.md) (**MCI \_ BREAK** usa la [**struttura MCI BREAK \_ \_ PARMS.**](mci-break-parms.md) Quando un'operazione di attesa viene annullata, MCI tenta di restituire il controllo all'applicazione senza interrompere il comando associato al flag "wait".

 

 

 




