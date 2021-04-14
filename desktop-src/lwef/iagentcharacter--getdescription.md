---
title: IAgentCharacter GetDescription
description: IAgentCharacter GetDescription
ms.assetid: 729f54ac-1c60-4a7b-b993-5682a6ea2b3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 423cd1f5c799cc1f0177f6d3d7922d5d14de1dbe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396994"
---
# <a name="iagentcharactergetdescription"></a>IAgentCharacter:: GetDescription

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetDescription(
   BSTR * pbszDescription   // address of buffer for character description
); 
```

Recupera la descrizione del carattere.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="pbszDescription"></span><span id="pbszdescription"></span><span id="PBSZDESCRIPTION"></span>*pbszDescription*
</dt> <dd>

Indirizzo di un BSTR che riceve il valore della descrizione per il carattere. La descrizione di un carattere viene definita quando viene compilata con l'editor dei caratteri di Microsoft Agent. L'impostazione della descrizione è facoltativa e non può essere specificata per tutti i caratteri.

</dd> </dl>

 

 




