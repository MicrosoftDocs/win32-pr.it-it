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
# <a name="iagentnotifysinkexdefaultcharacterchange"></a><span data-ttu-id="a737e-103">IAgentNotifySinkEx::D efaultCharacterChange</span><span class="sxs-lookup"><span data-stu-id="a737e-103">IAgentNotifySinkEx::DefaultCharacterChange</span></span>

<span data-ttu-id="a737e-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a737e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT DefaultCharacterChange(
   BSTR bszGUID  // character identifier
);
```

<span data-ttu-id="a737e-105">Notifica a un'applicazione client quando viene modificato il carattere predefinito.</span><span class="sxs-lookup"><span data-stu-id="a737e-105">Notifies a client application when the default character changes.</span></span>

-   <span data-ttu-id="a737e-106">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="a737e-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="a737e-107"><span id="bszGUID"></span><span id="bszguid"></span><span id="BSZGUID"></span>*bszGUID*</span><span class="sxs-lookup"><span data-stu-id="a737e-107"><span id="bszGUID"></span><span id="bszguid"></span><span id="BSZGUID"></span>*bszGUID*</span></span>
</dt> <dd>

<span data-ttu-id="a737e-108">Identificatore univoco per il carattere.</span><span class="sxs-lookup"><span data-stu-id="a737e-108">The unique identifier for the character.</span></span>

</dd> </dl>

<span data-ttu-id="a737e-109">Quando l'utente modifica il carattere assegnato come carattere predefinito dell'utente, il server invia questo evento ai client che hanno caricato il carattere predefinito.</span><span class="sxs-lookup"><span data-stu-id="a737e-109">When the user changes the character assigned as the user's default character, the server sends this event to clients that have loaded the default character.</span></span> <span data-ttu-id="a737e-110">L'evento restituisce l'identificatore univoco (GUID) del carattere formattato con parentesi graffe e trattini, che viene definito quando il carattere viene compilato con l'editor dei caratteri di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="a737e-110">The event returns the character's unique identifier (GUID) formatted with braces and dashes, which is defined when the character is built with the Microsoft Agent Character Editor.</span></span>

<span data-ttu-id="a737e-111">Quando viene visualizzato il nuovo carattere, assume le stesse dimensioni di qualsiasi istanza già caricata del carattere o del carattere predefinito precedente (in quell'ordine).</span><span class="sxs-lookup"><span data-stu-id="a737e-111">When the new character appears, it assumes the same size as any already loaded instance of the character or the previous default character (in that order).</span></span>

## <a name="see-also"></a><span data-ttu-id="a737e-112">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="a737e-112">See Also</span></span>

[<span data-ttu-id="a737e-113">**IAgent:: Load**</span><span class="sxs-lookup"><span data-stu-id="a737e-113">**IAgent::Load**</span></span>](iagent--load.md)


 

 




