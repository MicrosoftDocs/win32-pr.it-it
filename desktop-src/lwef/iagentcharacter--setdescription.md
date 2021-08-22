---
title: IAgentCharacter SetDescription
description: IAgentCharacter SetDescription
ms.assetid: ae01b9e6-1616-4806-9125-ceb4cb54aab1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d96765d3faddafef00a28826ec5a9fdd92acb6884ac3aa659ad88ba2c091a44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609821"
---
# <a name="iagentcharactersetdescription"></a>IAgentCharacter::SetDescription

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetDescription(
   BSTR bszDescription   // character description
); 
```

Imposta la descrizione del carattere.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="bszDescription"></span><span id="bszdescription"></span><span id="BSZDESCRIPTION"></span>*bszDescription*
</dt> <dd>

Oggetto BSTR che imposta la descrizione per il carattere. La descrizione predefinita di un carattere viene definita quando viene compilato con l'editor di caratteri di Microsoft Agent. L'impostazione della descrizione è facoltativa e non può essere specificata per tutti i caratteri. È possibile modificare la descrizione del carattere **usando IAgentCharacter::setDescription**; tuttavia, questo valore non è persistente (archiviato in modo permanente). La descrizione del carattere ripristina l'impostazione predefinita ogni volta che il carattere viene caricato per la prima volta da un client.

</dd> </dl>

## <a name="see-also"></a>Vedere anche

[**IAgentCharacter::GetDescription**](iagentcharacter--getdescription.md)


 

 




