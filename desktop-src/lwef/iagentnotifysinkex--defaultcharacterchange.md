---
title: IAgentNotifySinkEx DefaultCharacterChange
description: IAgentNotifySinkEx DefaultCharacterChange
ms.assetid: 13acb502-e247-433f-abf3-2d78a2d6a4a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ec212887d17d1aa59d942ece79b3e6928900ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298493"
---
# <a name="iagentnotifysinkexdefaultcharacterchange"></a>IAgentNotifySinkEx::D efaultCharacterChange

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT DefaultCharacterChange(
   BSTR bszGUID  // character identifier
);
```

Notifica a un'applicazione client quando viene modificato il carattere predefinito.

-   Nessun valore restituito.

<dl> <dt>

<span id="bszGUID"></span><span id="bszguid"></span><span id="BSZGUID"></span>*bszGUID*
</dt> <dd>

Identificatore univoco per il carattere.

</dd> </dl>

Quando l'utente modifica il carattere assegnato come carattere predefinito dell'utente, il server invia questo evento ai client che hanno caricato il carattere predefinito. L'evento restituisce l'identificatore univoco (GUID) del carattere formattato con parentesi graffe e trattini, che viene definito quando il carattere viene compilato con l'editor dei caratteri di Microsoft Agent.

Quando viene visualizzato il nuovo carattere, assume le stesse dimensioni di qualsiasi istanza già caricata del carattere o del carattere predefinito precedente (in quell'ordine).

## <a name="see-also"></a>Vedere anche

[**IAgent:: Load**](iagent--load.md)


 

 




