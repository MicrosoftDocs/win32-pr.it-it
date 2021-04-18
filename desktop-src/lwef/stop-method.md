---
title: Metodo Stop (funzionalità legacy dell'ambiente Windows)
description: Metodo Stop
ms.assetid: 68372f72-db9c-447c-a3e4-488940c730d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20192634c197559ca54bb8af3d8a29f37beb53e2
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300856"
---
# <a name="stop-method-legacy-windows-environment-features"></a><span data-ttu-id="a8e50-103">Metodo Stop (funzionalità legacy dell'ambiente Windows)</span><span class="sxs-lookup"><span data-stu-id="a8e50-103">Stop Method (Legacy Windows Environment Features)</span></span>

<span data-ttu-id="a8e50-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a8e50-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="a8e50-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="a8e50-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="a8e50-106">Arresta l'animazione per il carattere specificato.</span><span class="sxs-lookup"><span data-stu-id="a8e50-106">Stops the animation for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="a8e50-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="a8e50-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="a8e50-108">\*agente \***. Caratteri ("**_CharacterID_\*_"). Arresta_ \*  \[ *richiesta*\]</span><span class="sxs-lookup"><span data-stu-id="a8e50-108">*agent\***.Characters ("**_CharacterID_*_").Stop_\* \[*Request*\]</span></span>



| <span data-ttu-id="a8e50-109">Parte</span><span class="sxs-lookup"><span data-stu-id="a8e50-109">Part</span></span>      | <span data-ttu-id="a8e50-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a8e50-110">Description</span></span>                                                                                   |
|-----------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8e50-111">*Richiesta*</span><span class="sxs-lookup"><span data-stu-id="a8e50-111">*Request*</span></span> | <span data-ttu-id="a8e50-112">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="a8e50-112">Optional.</span></span> <span data-ttu-id="a8e50-113">Oggetto [**Request**](/windows/desktop/lwef/the-request-object) che specifica una particolare chiamata di animazione.</span><span class="sxs-lookup"><span data-stu-id="a8e50-113">A [**Request**](/windows/desktop/lwef/the-request-object) object specifying a particular animation call.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a8e50-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="a8e50-114">Remarks</span></span>

<span data-ttu-id="a8e50-115">Per specificare il parametro request, è necessario creare una variabile e assegnare la richiesta di animazione che si desidera arrestare.</span><span class="sxs-lookup"><span data-stu-id="a8e50-115">To specify the request parameter, you must create a variable and assign the animation request you want to stop.</span></span> <span data-ttu-id="a8e50-116">Se non si imposta il parametro **Request** , il server interrompe tutte le animazioni per il carattere, incluse le chiamate [**Get**](get-method.md) in coda, e cancella la coda delle animazioni, a meno che il carattere non stia attualmente **eseguendo l'animazione o la** **visualizzazione** .</span><span class="sxs-lookup"><span data-stu-id="a8e50-116">If you don't set the **Request** parameter, the server stops all animations for the character, including queued [**Get**](get-method.md) calls, and clears its animation queue unless the character is currently playing its **Hiding** or **Showing** animation.</span></span> <span data-ttu-id="a8e50-117">Questo metodo non interrompe le chiamate **Get** non in coda.</span><span class="sxs-lookup"><span data-stu-id="a8e50-117">This method does not stop non-queued **Get** calls.</span></span>

<span data-ttu-id="a8e50-118">Per arrestare un'animazione o una chiamata [**Get**](get-method.md) specifica, dichiarare una variabile oggetto e assegnare la richiesta di animazione alla variabile:</span><span class="sxs-lookup"><span data-stu-id="a8e50-118">To stop a specific animation or [**Get**](get-method.md) call, declare an object variable and assign your animation request to that variable:</span></span>


```
   Dim MyRequest
   Dim Genie

   Agent1.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"

   Set Genie = Agent1.Characters ("Genie")

   Genie.Get "state", "Showing"
   Genie.Get "animation", "Greet, GreetReturn"

   Genie.Show
   
   'This animation will never play
   Set MyRequest = Genie.Play ("Greet")
   
   Genie.Stop MyRequest
```



<span data-ttu-id="a8e50-119">Questo metodo non genererà un oggetto [**Request**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="a8e50-119">This method will not generate a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>

## <a name="see-also"></a><span data-ttu-id="a8e50-120">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="a8e50-120">See Also</span></span>

[<span data-ttu-id="a8e50-121">**Metodo StopAll**</span><span class="sxs-lookup"><span data-stu-id="a8e50-121">**StopAll method**</span></span>](stopall-method.md)


 

 
