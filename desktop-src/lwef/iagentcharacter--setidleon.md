---
title: IAgentCharacter SetIdleOn
description: IAgentCharacter SetIdleOn
ms.assetid: 397d223a-0970-4535-ad46-2923df6b9975
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98db30c9c440ed0564b98977d33e15e390cf57d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396975"
---
# <a name="iagentcharactersetidleon"></a>IAgentCharacter::SetIdleOn

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetIdleOn(
   long bOn  // idle processing flag
);
```

Imposta l'elaborazione inattiva automatica per un carattere.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="bOn"></span><span id="bon"></span><span id="BON"></span>*bOn*
</dt> <dd>

Flag di elaborazione inattiva. Se questo parametro è impostato su **true**, l'agente Microsoft riproduce automaticamente le animazioni di stato al **minimo** .

</dd> </dl>

Il server imposta automaticamente un timeout dopo l'ultima animazione riprodotta per un carattere. Quando l'intervallo di questo timer è completo, il server inizia gli Stati di **minimo** per un carattere, eseguendo le animazioni al **minimo** associate a intervalli regolari. Se si desidera gestire manualmente le animazioni **dello stato di** inattivo, impostare la proprietà su **false**. Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.

## <a name="see-also"></a>Vedere anche

[**IAgentCharacter::GetIdleOn**](iagentcharacter--getidleon.md)


 

 




