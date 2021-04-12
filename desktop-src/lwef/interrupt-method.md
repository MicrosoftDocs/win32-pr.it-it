---
title: Metodo interrupt
description: Metodo interrupt
ms.assetid: b8442e25-a629-47c7-acdd-1d28e74d78a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d58050e181525cc4a4b9f35ec169e92d91ab28e7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104399031"
---
# <a name="interrupt-method"></a><span data-ttu-id="c991e-103">Metodo interrupt</span><span class="sxs-lookup"><span data-stu-id="c991e-103">Interrupt Method</span></span>

<span data-ttu-id="c991e-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c991e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="c991e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="c991e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="c991e-106">Interrompe l'animazione per il carattere specificato.</span><span class="sxs-lookup"><span data-stu-id="c991e-106">Interrupts the animation for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="c991e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="c991e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="c991e-108">\*agente ***. Caratteri ("*** CharacterID \* \* *").* \*  *Richiesta* di interrupt</span><span class="sxs-lookup"><span data-stu-id="c991e-108">*agent ***.Characters ("*** CharacterID\*\*\*").Interrupt*\* *Request*</span></span>



| <span data-ttu-id="c991e-109">Parte</span><span class="sxs-lookup"><span data-stu-id="c991e-109">Part</span></span>      | <span data-ttu-id="c991e-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c991e-110">Description</span></span>                                                                  |
|-----------|------------------------------------------------------------------------------|
| <span data-ttu-id="c991e-111">*Richiesta*</span><span class="sxs-lookup"><span data-stu-id="c991e-111">*Request*</span></span> | <span data-ttu-id="c991e-112">Oggetto [**Request**](/windows/desktop/lwef/the-request-object) per una particolare chiamata di animazione.</span><span class="sxs-lookup"><span data-stu-id="c991e-112">A [**Request**](/windows/desktop/lwef/the-request-object) object for a particular animation call.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c991e-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="c991e-113">Remarks</span></span>

<span data-ttu-id="c991e-114">È possibile usarlo per sincronizzare l'animazione tra caratteri.</span><span class="sxs-lookup"><span data-stu-id="c991e-114">You can use this to sync up animation between characters.</span></span> <span data-ttu-id="c991e-115">Se, ad esempio, un altro carattere si trova in un'animazione di ciclo, questo metodo arresterà il ciclo e passerà all'animazione successiva nella coda del carattere.</span><span class="sxs-lookup"><span data-stu-id="c991e-115">For example, if another character is in a looping animation, this method will stop the loop and move to the next animation in the character's queue.</span></span> <span data-ttu-id="c991e-116">Non è possibile interrompere un'animazione di caratteri che non si sta usando (che non è stata caricata).</span><span class="sxs-lookup"><span data-stu-id="c991e-116">You cannot interrupt a character animation that you are not using (that you have not loaded).</span></span>

<span data-ttu-id="c991e-117">Per specificare il parametro request, è necessario creare una variabile e assegnare la richiesta di animazione che si vuole interrompere:</span><span class="sxs-lookup"><span data-stu-id="c991e-117">To specify the request parameter, you must create a variable and assign the animation request you want to interrupt:</span></span>


```
   Dim GenieRequest as Object
   Dim RobbyRequest as Object
   Dim Genie as Object
   Dim Robby as Object

   Sub FormLoad()

      MyAgent1.Characters.Load "Genie", "Genie.acs"

      MyAgent1.Characters.Load "Robby", "Robby.acs"

      Set Genie = MyAgent1.Characters ("Genie")
      Set Robby = MyAgent1.Characters ("Robby")

      Genie.Show

      Genie.Speak "Just a moment"

      Set GenieRequest = Genie.Play ("Processing")

      Robby.Show
      Robby.Play "confused"
      Robby.Speak "Hey, Genie. What are you doing?"
      Robby.Interrupt GenieRequest

      Genie.Speak "I was just checking on something."

   End Sub
```



<span data-ttu-id="c991e-118">Non è possibile interrompere l'animazione dello stesso carattere specificato in questo metodo perché il server accoda il metodo **interrupt** nella coda di animazione di tale carattere.</span><span class="sxs-lookup"><span data-stu-id="c991e-118">You cannot interrupt the animation of the same character you specify in this method because the server queues the **Interrupt** method in that character's animation queue.</span></span> <span data-ttu-id="c991e-119">Pertanto, è possibile utilizzare solo **interrupt** per arrestare l'animazione di un altro carattere caricato.</span><span class="sxs-lookup"><span data-stu-id="c991e-119">Therefore, you can only use **Interrupt** to halt the animation of another character you have loaded.</span></span>

<span data-ttu-id="c991e-120">Se si dichiara un riferimento a un oggetto e lo si imposta su questo metodo, viene restituito un oggetto [**Request**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="c991e-120">If you declare an object reference and set it to this method, it returns a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>

> [!Note]  
> <span data-ttu-id="c991e-121">L' **interrupt** non Scarica la coda del carattere; arresta l'animazione esistente e passa all'animazione successiva nella coda del carattere.</span><span class="sxs-lookup"><span data-stu-id="c991e-121">**Interrupt** does not flush the character's queue; it halts the existing animation and moves on to the next animation in the character's queue.</span></span> <span data-ttu-id="c991e-122">Per arrestare e scaricare la coda di un carattere, usare il metodo [**Stop**](stop-method.md) .</span><span class="sxs-lookup"><span data-stu-id="c991e-122">To halt and flush a character's queue, use the [**Stop**](stop-method.md) method.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="c991e-123">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="c991e-123">See Also</span></span>

[<span data-ttu-id="c991e-124">**Metodo Stop**</span><span class="sxs-lookup"><span data-stu-id="c991e-124">**Stop method**</span></span>](stop-method.md)


 

 