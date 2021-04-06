---
title: IAgentAudioOutputProperties GetEnabled
description: IAgentAudioOutputProperties GetEnabled
ms.assetid: a1e555e1-98f1-4a3d-b6ba-4cd35348db2b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e86b82c720971ae1e14ee294e6d097fd35ca80a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044672"
---
# <a name="iagentaudiooutputpropertiesgetenabled"></a><span data-ttu-id="aa8d4-103">IAgentAudioOutputProperties:: GetEnabled</span><span class="sxs-lookup"><span data-stu-id="aa8d4-103">IAgentAudioOutputProperties::GetEnabled</span></span>

<span data-ttu-id="aa8d4-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="aa8d4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetEnabled(
long * pbEnabled  // address of variable for audio output Enabled setting 
);                      
```

<span data-ttu-id="aa8d4-105">Recupera un valore che indica se l'output del riconoscimento vocale del carattere è abilitato.</span><span class="sxs-lookup"><span data-stu-id="aa8d4-105">Retrieves a value indicating whether character speech output is enabled.</span></span>

-   <span data-ttu-id="aa8d4-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="aa8d4-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="aa8d4-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*</span><span class="sxs-lookup"><span data-stu-id="aa8d4-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="aa8d4-108">Indirizzo di una variabile che riceve **true** se l'output vocale è attualmente abilitato e **false** se disabilitato.</span><span class="sxs-lookup"><span data-stu-id="aa8d4-108">Address of a variable that receives **True** if the speech output is currently enabled and **False** if disabled.</span></span>

</dd> </dl>

<span data-ttu-id="aa8d4-109">Poiché questa impostazione influiscono sull'output parlato (TTS e file audio) per tutti i caratteri, solo l'utente può modificare questa proprietà nella finestra delle proprietà di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="aa8d4-109">Because this setting affects spoken output (TTS and sound file) for all characters, only the user can change this property in the Microsoft Agent property sheet.</span></span>

 

 




