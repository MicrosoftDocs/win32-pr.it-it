---
title: IAgentCommandsEx GetDefaultID
description: IAgentCommandsEx GetDefaultID
ms.assetid: 14079ae0-ad2c-4f38-9371-9914f8402e49
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e4dabfb1c957031b353303775921a352bf40d984ac5de1ee9c933f79a5e02cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105227"
---
# <a name="iagentcommandsexgetdefaultid"></a>IAgentCommandsEx::GetDefaultID

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetDefaultID(
   long * pdwID  // address of default command's ID
);
```

Recupera l'ID del comando predefinito in una [**raccolta Commands.**](/windows/desktop/lwef/the-commands-collection-object)

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="pdwID"></span><span id="pdwid"></span><span id="PDWID"></span>*pdwID*
</dt> <dd>

Indirizzo di una variabile che riceve l'ID del set [**di**](/windows/desktop/lwef/the-command-object) comandi come predefinito.

</dd> </dl>

Questa proprietà restituisce l'oggetto [**Command**](/windows/desktop/lwef/the-command-object) predefinito corrente nella [**raccolta Commands.**](/windows/desktop/lwef/the-commands-collection-object) Il comando predefinito è in grassetto nel menu a comparsa del carattere. Tuttavia, l'impostazione del comando predefinito non modifica la gestione dei comandi o gli eventi di doppio clic.

Questa proprietà si applica solo all'uso del carattere da parte dell'applicazione client. L'impostazione non influisce su altri client del carattere o di altri caratteri dell'applicazione client.

## <a name="see-also"></a>Vedere anche

[**IAgentCommandsEx::SetDefaultID**](iagentcommandsex--setdefaultid.md)


 

 