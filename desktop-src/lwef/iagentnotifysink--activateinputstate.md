---
title: IAgentNotifySink ActivateInputState
description: IAgentNotifySink ActivateInputState
ms.assetid: 2476e475-d80c-47e9-bb60-e0fca41becc9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5821f5943bb87f9c19a66125028604fa5d116a7e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221774"
---
# <a name="iagentnotifysinkactivateinputstate"></a><span data-ttu-id="dd0ab-103">IAgentNotifySink::ActivateInputState</span><span class="sxs-lookup"><span data-stu-id="dd0ab-103">IAgentNotifySink::ActivateInputState</span></span>

<span data-ttu-id="dd0ab-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="dd0ab-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT ActivateInputState(
   long dwCharID,   // character ID
   long bActivated  // input activation flag
);                          
```

<span data-ttu-id="dd0ab-105">Notifica a un'applicazione client che lo stato attivo di input di un carattere è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="dd0ab-105">Notifies a client application that a character's input active state changed.</span></span>

-   <span data-ttu-id="dd0ab-106">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="dd0ab-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="dd0ab-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="dd0ab-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="dd0ab-108">Identificatore del carattere il cui stato di attivazione dell'input è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="dd0ab-108">Identifier of the character whose input activation state changed.</span></span>

</dd> <dt>

<span data-ttu-id="dd0ab-109"><span id="bActivated"></span><span id="bactivated"></span><span id="BACTIVATED"></span>*bActivated*</span><span class="sxs-lookup"><span data-stu-id="dd0ab-109"><span id="bActivated"></span><span id="bactivated"></span><span id="BACTIVATED"></span>*bActivated*</span></span>
</dt> <dd>

<span data-ttu-id="dd0ab-110">Flag attivo di input.</span><span class="sxs-lookup"><span data-stu-id="dd0ab-110">Input active flag.</span></span> <span data-ttu-id="dd0ab-111">Questo valore booleano è **true** se il carattere a cui fa riferimento *dwCharID* è stato attivato come input. e **false** se il carattere ha perso lo stato attivo di input.</span><span class="sxs-lookup"><span data-stu-id="dd0ab-111">This Boolean value is **True** if the character referred to by *dwCharID* became input active; and **False** if the character lost its input active state.</span></span>

</dd> </dl>

 

 




