---
title: IAgentCommandsEx GetDefaultID
description: IAgentCommandsEx GetDefaultID
ms.assetid: 14079ae0-ad2c-4f38-9371-9914f8402e49
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e4380eca62a65758979a94fb23511348b11acdf
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104399024"
---
# <a name="iagentcommandsexgetdefaultid"></a>IAgentCommandsEx::GetDefaultID

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetDefaultID(
   long * pdwID  // address of default command's ID
);
```

Recupera l'ID del comando predefinito in una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) .

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="pdwID"></span><span id="pdwid"></span><span id="PDWID"></span>*pdwID*
</dt> <dd>

Indirizzo di una variabile che riceve l'ID del set di [**comandi**](/windows/desktop/lwef/the-command-object) come predefinito.

</dd> </dl>

Questa proprietà restituisce l'oggetto [**comando**](/windows/desktop/lwef/the-command-object) predefinito corrente nella raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) . Il comando predefinito è in grassetto nel menu a comparsa del carattere. Tuttavia, l'impostazione del comando predefinito non comporta la modifica della gestione dei comandi o degli eventi di doppio clic.

Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.

## <a name="see-also"></a>Vedere anche

[**IAgentCommandsEx::SetDefaultID**](iagentcommandsex--setdefaultid.md)


 

 