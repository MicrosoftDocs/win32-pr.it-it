---
title: Metodo Wait
description: Metodo Wait
ms.assetid: 968a3f19-6953-473b-ba98-0dc93696e703
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f2e94b0f765a9861c30b254761fbc4dc2e72763
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299606"
---
# <a name="wait-method"></a><span data-ttu-id="5c370-103">Metodo Wait</span><span class="sxs-lookup"><span data-stu-id="5c370-103">Wait Method</span></span>

<span data-ttu-id="5c370-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5c370-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="5c370-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="5c370-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="5c370-106">Fa in modo che la coda dell'animazione per il carattere specificato attenda finché non viene completata la richiesta di animazione specificata.</span><span class="sxs-lookup"><span data-stu-id="5c370-106">Causes the animation queue for the specified character to wait until the specified animation request completes.</span></span>

</dd> <dt>

<span data-ttu-id="5c370-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="5c370-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="5c370-108">*agente ***. Caratteri ("*** CharacterID ***").*** Richiesta di attesa*</span><span class="sxs-lookup"><span data-stu-id="5c370-108">*agent ***.Characters ("*** CharacterID ***").Wait*** Request*</span></span>



| <span data-ttu-id="5c370-109">Parte</span><span class="sxs-lookup"><span data-stu-id="5c370-109">Part</span></span>      | <span data-ttu-id="5c370-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5c370-110">Description</span></span>                                                                     |
|-----------|---------------------------------------------------------------------------------|
| <span data-ttu-id="5c370-111">*Richiesta*</span><span class="sxs-lookup"><span data-stu-id="5c370-111">*Request*</span></span> | <span data-ttu-id="5c370-112">Oggetto [**Request**](/windows/desktop/lwef/the-request-object) che specifica un'animazione particolare.</span><span class="sxs-lookup"><span data-stu-id="5c370-112">A [**Request**](/windows/desktop/lwef/the-request-object) object specifying a particular animation..</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5c370-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="5c370-113">Remarks</span></span>

<span data-ttu-id="5c370-114">Usare questo metodo solo quando sono supportati più caratteri (simultanei) e si sta tentando di sequenziare l'interazione dei caratteri.</span><span class="sxs-lookup"><span data-stu-id="5c370-114">Use this method only when you support multiple (simultaneous) characters and are trying to sequence the interaction of characters.</span></span> <span data-ttu-id="5c370-115">(Per un singolo carattere, ogni richiesta di animazione viene riprodotta in sequenza, dopo il completamento della richiesta precedente). Se si dispone di due caratteri e si desidera che la richiesta di animazione di un carattere attenda il completamento dell'animazione dell'altro carattere, impostare il metodo **wait** sull'oggetto [**richiesta**](/windows/desktop/lwef/the-request-object) di animazione dell'altro carattere.</span><span class="sxs-lookup"><span data-stu-id="5c370-115">(For a single character, each animation request is played sequentially--after the previous request completes.) If you have two characters and you want a character's animation request to wait until the other character's animation completes, set the **Wait** method to the other character's animation [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="5c370-116">Per specificare il parametro request, è necessario creare una variabile e assegnare la richiesta di animazione che si vuole interrompere:</span><span class="sxs-lookup"><span data-stu-id="5c370-116">To specify the request parameter, you must create a variable and assign the animation request you want to interrupt:</span></span>


```
   Dim GenieRequest 
   Dim RobbyRequest 
   Dim Genie 
   Dim Robby 

   Sub window_Onload

   Agent1.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"
   Agent1.Characters.Load "Robby", "https://agent.microsoft.com/characters/v2/robby/robby.acf"

   Set Genie = Agent1.Characters("Genie")
   Set Robby = Agent1.Characters("Robby")

   Genie.Get "State", "Showing"
   Robby.Get "State", "Showing"

   Genie.Get "Animation", "Announce, AnnounceReturn, Pleased, _ 
      PleasedReturn"
   
   Robby.Get "Animation", "Confused, ConfusedReturn, Sad, SadReturn"

   Set Genie = Agent1.Characters ("Genie")
   Set Robby = Agent1.Characters ("Robby")

   Genie.MoveTo 100,100
   Genie.Show

   Robby.MoveTo 250,100
   Robby.Show

   Genie.Play "Announce"
   Set GenieRequest = Genie.Speak ("Why did the chicken cross the road?")
   
   Robby.Wait GenieRequest
   Robby.Play "Confused"
   Set RobbyRequest = Robby.Speak ("I don't know. Why did the chicken _
      cross the road?")
   
   Genie.Wait RobbyRequest
   Genie.Play "Pleased"
   Set GenieRequest = Genie.Speak ("To get to the other side.")
   
   Robby.Wait GenieRequest
   Robby.Play "Sad"
   Robby.Speak "I never should have asked."

   End Sub
```



<span data-ttu-id="5c370-117">È anche possibile semplificare il codice semplicemente chiamando **wait** direttamente, usando una richiesta di animazione specifica.</span><span class="sxs-lookup"><span data-stu-id="5c370-117">You can also streamline your code by just calling **Wait** directly, using a specific animation request.</span></span>


```
   Robby.Wait Genie.Play "GestureRight"
```



<span data-ttu-id="5c370-118">In questo modo si evita di dover dichiarare in modo esplicito un oggetto [**Request**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="5c370-118">This avoids having to explicitly declare a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>

 

 