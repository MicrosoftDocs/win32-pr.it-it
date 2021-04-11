---
title: GetExtraData IAgentCharacter
description: GetExtraData IAgentCharacter
ms.assetid: 83f69bae-0ae3-45c5-ba0d-71610993da60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea854479ab85630abc3d110c9c193716ddedd004
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116937"
---
# <a name="iagentcharactergetextradata"></a>IAgentCharacter:: GetExtraData

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetExtraData(
   BSTR * pbszExtraData   // address of buffer for additional character data
); 
```

Recupera dati aggiuntivi archiviati come parte del carattere.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="pbszExtraData"></span><span id="pbszextradata"></span><span id="PBSZEXTRADATA"></span>*pbszExtraData*
</dt> <dd>

Indirizzo di un BSTR che riceve il valore dei dati aggiuntivi per il carattere. I dati aggiuntivi di un carattere vengono definiti quando vengono compilati con l'editor dei caratteri di Microsoft Agent. Uno sviluppatore di caratteri può fornire questa stringa modificando. File ACD per un carattere. L'impostazione è facoltativa e non può essere specificata per tutti i caratteri, né i dati possono essere definiti o modificati in fase di esecuzione. Inoltre, il significato dei dati forniti viene definito dallo sviluppatore di caratteri.

</dd> </dl>

 

 




