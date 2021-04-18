---
title: Nome IAgentCharacter
description: Nome IAgentCharacter
ms.assetid: 4944f910-60e9-446b-82e9-2794f445789a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec058e338adfa8c998bf26a1223ae71f0c7de3d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298975"
---
# <a name="iagentcharactersetname"></a>IAgentCharacter:: nome

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetName(
   BSTR bszName   // character name
);
```

Imposta il nome del carattere.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*
</dt> <dd>

BSTR che imposta il nome del carattere. Il nome predefinito di un carattere viene definito quando viene compilato con l'editor dei caratteri di Microsoft Agent. È possibile modificarlo utilizzando **IAgentCharacter:: Sename**; Tuttavia, modifica il nome del carattere per tutti i client correnti del carattere. Questa proprietà non è permanente (archiviata in modo permanente). Il nome del carattere viene ripristinato con il nome predefinito ogni volta che il carattere viene caricato per la prima volta da un client.

Il nome del carattere può inoltre dipendere dall'ID della lingua. I caratteri possono essere compilati con nomi diversi per le diverse lingue.

Il server utilizza l'impostazione del nome del carattere in parti dell'interfaccia dell'agente Microsoft, ad esempio il titolo della finestra comandi vocali quando il carattere è input-attivo e nel menu a comparsa della barra delle applicazioni di Microsoft Agent.

</dd> </dl>

## <a name="see-also"></a>Vedere anche

[**IAgentCharacter:: GetName**](iagentcharacter--getname.md)


 

 




