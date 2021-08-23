---
title: IAgentCharacter SetIdleOn
description: IAgentCharacter SetIdleOn
ms.assetid: 397d223a-0970-4535-ad46-2923df6b9975
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde86da6dda12744aedcd780b93d92c45fe2906dd16073bf0e3555848718e747
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665681"
---
# <a name="iagentcharactersetidleon"></a>IAgentCharacter::SetIdleOn

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetIdleOn(
   long bOn  // idle processing flag
);
```

Imposta l'elaborazione inattiva automatica per un carattere.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="bOn"></span><span id="bon"></span><span id="BON"></span>*Bon*
</dt> <dd>

Flag di elaborazione inattivo. Se questo parametro è **True,** Microsoft Agent riproduce automaticamente le animazioni dello stato **idling.**

</dd> </dl>

Il server imposta automaticamente un timeout dopo l'ultima animazione riprodotta per un carattere. Al termine dell'intervallo di questo timer, il server avvia gli stati **idling** per un carattere, riproducendo le animazioni **Idling** associate a intervalli regolari. Se si desidera gestire manualmente le animazioni dello stato **idling,** impostare la proprietà su **False**. Questa proprietà si applica solo all'uso del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.

## <a name="see-also"></a>Vedere anche

[**IAgentCharacter::GetIdleOn**](iagentcharacter--getidleon.md)


 

 




