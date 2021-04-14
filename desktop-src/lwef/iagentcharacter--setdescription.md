---
title: IAgentCharacter Descrizione
description: IAgentCharacter Descrizione
ms.assetid: ae01b9e6-1616-4806-9125-ceb4cb54aab1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce9815e5c0e01537c7db2b400326f86da37af003
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396978"
---
# <a name="iagentcharactersetdescription"></a>IAgentCharacter:: FileDescription

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetDescription(
   BSTR bszDescription   // character description
); 
```

Imposta la descrizione del carattere.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="bszDescription"></span><span id="bszdescription"></span><span id="BSZDESCRIPTION"></span>*bszDescription*
</dt> <dd>

BSTR che imposta la descrizione per il carattere. La descrizione predefinita di un carattere viene definita quando viene compilata con l'editor dei caratteri di Microsoft Agent. L'impostazione della descrizione è facoltativa e non può essere specificata per tutti i caratteri. È possibile modificare la descrizione del carattere usando **IAgentCharacter:: FileDescription**; Tuttavia, questo valore non è permanente (archiviato in modo permanente). La descrizione del carattere viene ripristinata l'impostazione predefinita ogni volta che il carattere viene caricato per la prima volta da un client.

</dd> </dl>

## <a name="see-also"></a>Vedere anche

[**IAgentCharacter:: GetDescription**](iagentcharacter--getdescription.md)


 

 




