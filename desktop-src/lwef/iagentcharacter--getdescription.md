---
title: IAgentCharacter GetDescription
description: IAgentCharacter GetDescription
ms.assetid: 729f54ac-1c60-4a7b-b993-5682a6ea2b3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23216f1a7b013a54de1e64351c2a9d3a3d3359d90e0516cd6852a003baa047c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716191"
---
# <a name="iagentcharactergetdescription"></a>IAgentCharacter::GetDescription

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetDescription(
   BSTR * pbszDescription   // address of buffer for character description
); 
```

Recupera la descrizione del carattere.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="pbszDescription"></span><span id="pbszdescription"></span><span id="PBSZDESCRIPTION"></span>*pbszDescription*
</dt> <dd>

Indirizzo di un BSTR che riceve il valore della descrizione per il carattere. La descrizione di un carattere viene definita quando viene compilata con l'editor di caratteri di Microsoft Agent. L'impostazione della descrizione è facoltativa e non può essere specificata per tutti i caratteri.

</dd> </dl>

 

 




