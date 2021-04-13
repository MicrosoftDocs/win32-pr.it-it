---
title: IAgentCommandsEx SetDefaultID
description: IAgentCommandsEx SetDefaultID
ms.assetid: 056ec518-bf0b-403f-adc6-9b53b0c044a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37754eb61df7879511a03dde705936d36f905376
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398927"
---
# <a name="iagentcommandsexsetdefaultid"></a>IAgentCommandsEx::SetDefaultID

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetDefaultID(
   long dwID,  // default command's ID
);
```

Imposta l'ID del comando predefinito in una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) .

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="dwID"></span><span id="dwid"></span><span id="DWID"></span>*dwID*
</dt> <dd>

ID del [**comando**](/windows/desktop/lwef/the-command-object) da impostare come valore predefinito.

</dd> </dl>

Questa proprietà imposta il set di oggetti [**comando**](/windows/desktop/lwef/the-command-object) predefinito nella raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) . Il comando predefinito è in grassetto nel menu a comparsa del carattere. Tuttavia, l'impostazione del comando predefinito non modifica effettivamente la gestione dei comandi o gli eventi di doppio clic.

Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.

## <a name="see-also"></a>Vedere anche

[**IAgentCommandsEx::GetDefaultID**](iagentcommandsex--getdefaultid.md)


 

 