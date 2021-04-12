---
title: IAgentBalloon GetEnabled
description: IAgentBalloon GetEnabled
ms.assetid: 1a5ea6c0-6150-459f-95eb-a9c7598c1d94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfd78245534b942e7972066ec90179172f7b556c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332468"
---
# <a name="iagentballoongetenabled"></a><span data-ttu-id="135c5-103">IAgentBalloon:: GetEnabled</span><span class="sxs-lookup"><span data-stu-id="135c5-103">IAgentBalloon::GetEnabled</span></span>

<span data-ttu-id="135c5-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="135c5-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetEnabled(
  long * pbEnabled  // address of variable for Enabled setting 
);                  // for word balloon
```

<span data-ttu-id="135c5-105">Recupera il valore della proprietà [**Enabled**](enabled-property.md) per un fumetto di Word.</span><span class="sxs-lookup"><span data-stu-id="135c5-105">Retrieves the value of the [**Enabled**](enabled-property.md) property for a word balloon.</span></span>

-   <span data-ttu-id="135c5-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="135c5-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="135c5-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*</span><span class="sxs-lookup"><span data-stu-id="135c5-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="135c5-108">Indirizzo di una variabile che riceve **true** quando il Word Balloon è abilitato e **false** quando è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="135c5-108">The address of a variable that receives **True** when the word balloon is enabled and **False** when it is disabled.</span></span>

</dd> </dl>

<span data-ttu-id="135c5-109">Il server Microsoft Agent Visualizza automaticamente la parola fumetto per l'output parlato, a meno che non sia disabilitato.</span><span class="sxs-lookup"><span data-stu-id="135c5-109">The Microsoft Agent server automatically displays the word balloon for spoken output, unless it is disabled.</span></span> <span data-ttu-id="135c5-110">La parola Balloon può essere disabilitata per un carattere nell'editor dei caratteri di Microsoft Agent oppure (dall'utente) per tutti i caratteri nella finestra delle proprietà di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="135c5-110">The word balloon can be disabled for a character in the Microsoft Agent Character Editor, or (by the user) for all characters in the Microsoft Agent property sheet.</span></span> <span data-ttu-id="135c5-111">Se l'utente disabilita la parola Balloon, il client non potrà ripristinarla.</span><span class="sxs-lookup"><span data-stu-id="135c5-111">If the user disables the word balloon, the client cannot restore it.</span></span>

 

 




