---
title: GetName IAgentCharacter
description: GetName IAgentCharacter
ms.assetid: 6c013a18-8c56-42a8-8723-31d83b3230cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33679577cfb5179a799ee61207f7ecd9b2be8a21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332764"
---
# <a name="iagentcharactergetname"></a>IAgentCharacter:: GetName

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetName(
   BSTR * pbszName   // address of buffer for character name
);
```

Recupera il nome del carattere.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="pbszName"></span><span id="pbszname"></span><span id="PBSZNAME"></span>*pbszName*
</dt> <dd>

Indirizzo di un BSTR che riceve il valore del nome per il carattere.

</dd> </dl>

Il nome predefinito di un carattere viene definito quando viene compilato con l'editor dei caratteri di Microsoft Agent. Il nome di un carattere può variare in base all'ID lingua del carattere. I caratteri possono essere compilati con nomi diversi per le diverse lingue.

È anche possibile impostare il nome del carattere usando **IAgentCharacter: Sename**; Tuttavia, modifica il nome per tutti i client correnti del carattere.

## <a name="see-also"></a>Vedere anche

[**IAgentCharacter:: nome**](iagentcharacter--setname.md)


 

 




