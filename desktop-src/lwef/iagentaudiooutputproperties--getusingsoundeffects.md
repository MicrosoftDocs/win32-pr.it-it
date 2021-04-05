---
title: IAgentAudioOutputProperties GetUsingSoundEffects
description: IAgentAudioOutputProperties GetUsingSoundEffects
ms.assetid: 3ccf90b1-a2aa-482a-9f96-85d735532c11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e83314acfc67ce8bea4a0f0d305f6d5d490a92e5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710639"
---
# <a name="iagentaudiooutputpropertiesgetusingsoundeffects"></a><span data-ttu-id="4d9b2-103">IAgentAudioOutputProperties::GetUsingSoundEffects</span><span class="sxs-lookup"><span data-stu-id="4d9b2-103">IAgentAudioOutputProperties::GetUsingSoundEffects</span></span>

<span data-ttu-id="4d9b2-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4d9b2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetUsingSoundEffects(
long * pbUsingSoundEffects  // address of variable sound effects output 
);                          // setting 
```

<span data-ttu-id="4d9b2-105">Recupera un valore che indica se l'output degli effetti audio è abilitato.</span><span class="sxs-lookup"><span data-stu-id="4d9b2-105">Retrieves a value indicating whether sound effects output is enabled.</span></span>

-   <span data-ttu-id="4d9b2-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="4d9b2-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="4d9b2-107"><span id="pbUsingSoundEffects"></span><span id="pbusingsoundeffects"></span><span id="PBUSINGSOUNDEFFECTS"></span>*pbUsingSoundEffects*</span><span class="sxs-lookup"><span data-stu-id="4d9b2-107"><span id="pbUsingSoundEffects"></span><span id="pbusingsoundeffects"></span><span id="PBUSINGSOUNDEFFECTS"></span>*pbUsingSoundEffects*</span></span>
</dt> <dd>

<span data-ttu-id="4d9b2-108">Indirizzo di una variabile che riceve **true** se l'output degli effetti audio è attualmente abilitato e **false** se disabilitato.</span><span class="sxs-lookup"><span data-stu-id="4d9b2-108">Address of a variable that receives **True** if the sound effects output is currently enabled and **False** if disabled.</span></span>

</dd> </dl>

<span data-ttu-id="4d9b2-109">Gli effetti audio per l'animazione di un carattere vengono assegnati nell'editor dei caratteri di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="4d9b2-109">Sound effects for a character's animation are assigned in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="4d9b2-110">Poiché questa impostazione influisce sull'output degli effetti audio per tutti i caratteri, solo l'utente può modificare questa proprietà nella finestra delle proprietà di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="4d9b2-110">Because this setting affects sound effects output for all characters, only the user can change this property in the Microsoft Agent property sheet.</span></span>

 

 




