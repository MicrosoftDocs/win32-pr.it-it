---
title: IAgentCharacter GetName
description: IAgentCharacter GetName
ms.assetid: 6c013a18-8c56-42a8-8723-31d83b3230cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 107e6fdb6be3e79dee14177d9f56ee7d258f3455d578641e7d3a3b3cf044c741
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962275"
---
# <a name="iagentcharactergetname"></a>IAgentCharacter::GetName

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetName(
   BSTR * pbszName   // address of buffer for character name
);
```

Recupera il nome del carattere.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="pbszName"></span><span id="pbszname"></span><span id="PBSZNAME"></span>*pbszName*
</dt> <dd>

Indirizzo di un BSTR che riceve il valore del nome per il carattere.

</dd> </dl>

Il nome predefinito di un carattere viene definito quando viene compilato con l'editor di caratteri di Microsoft Agent. Il nome di un carattere può variare in base all'ID lingua del carattere. I caratteri possono essere compilati con nomi diversi per linguaggi diversi.

È anche possibile impostare il nome del carattere **usando IAgentCharacter:SetName**; tuttavia, il nome di tutti i client correnti del carattere viene modificato.

## <a name="see-also"></a>Vedere anche

[**IAgentCharacter::SetName**](iagentcharacter--setname.md)


 

 




