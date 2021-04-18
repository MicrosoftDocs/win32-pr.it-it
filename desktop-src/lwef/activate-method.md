---
title: Metodo Activate
description: Metodo Activate
ms.assetid: 8111139d-1453-416e-8f08-38c06669ff4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21df1965abaeed35e9e440a0f559f5e12d68d6fe
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299652"
---
# <a name="activate-method"></a><span data-ttu-id="5eccb-103">Metodo Activate</span><span class="sxs-lookup"><span data-stu-id="5eccb-103">Activate Method</span></span>

<span data-ttu-id="5eccb-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5eccb-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="5eccb-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>[**Descrizione**](../wmformat/description.md)</span><span class="sxs-lookup"><span data-stu-id="5eccb-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>[**Description**](../wmformat/description.md)</span></span>
</dt> <dd>

<span data-ttu-id="5eccb-106">Imposta il client o il carattere attivo.</span><span class="sxs-lookup"><span data-stu-id="5eccb-106">Sets the active client or character.</span></span>

</dd> <dt>

<span data-ttu-id="5eccb-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="5eccb-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="5eccb-108">\*agente ***. Caratteri ("*** CharacterID \* \* *"). Attiva* \*  \[ *stato*\]</span><span class="sxs-lookup"><span data-stu-id="5eccb-108">*agent ***.Characters ("*** CharacterID\*\*\*").Activate*\* \[*State*\]</span></span>



| <span data-ttu-id="5eccb-109">Parte</span><span class="sxs-lookup"><span data-stu-id="5eccb-109">Part</span></span>    | <span data-ttu-id="5eccb-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5eccb-110">Description</span></span>                                                                                                                                                                           |
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5eccb-111">*State*</span><span class="sxs-lookup"><span data-stu-id="5eccb-111">*State*</span></span> | <span data-ttu-id="5eccb-112">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="5eccb-112">Optional.</span></span> <span data-ttu-id="5eccb-113">Per questo parametro è possibile specificare i valori seguenti: 0 non è il client attivo.</span><span class="sxs-lookup"><span data-stu-id="5eccb-113">You can specify the following values for this parameter: 0 Not the active client.</span></span><br/> <span data-ttu-id="5eccb-114">1 il client attivo.</span><span class="sxs-lookup"><span data-stu-id="5eccb-114">1 The active client.</span></span> <br/> <span data-ttu-id="5eccb-115">2 (impostazione predefinita) carattere superiore.</span><span class="sxs-lookup"><span data-stu-id="5eccb-115">2 (Default) The topmost character.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5eccb-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="5eccb-116">Remarks</span></span>

<span data-ttu-id="5eccb-117">Quando sono visibili più caratteri, solo uno dei caratteri riceve l'input vocale alla volta.</span><span class="sxs-lookup"><span data-stu-id="5eccb-117">When multiple characters are visible, only one of the characters receives speech input at a time.</span></span> <span data-ttu-id="5eccb-118">Analogamente, quando più applicazioni client condividono lo stesso carattere, solo uno dei client riceve l'input del mouse (ad esempio, gli eventi di clic o di trascinamento del controllo agente Microsoft).</span><span class="sxs-lookup"><span data-stu-id="5eccb-118">Similarly, when multiple client applications share the same character, only one of the clients receives mouse input (for example, Microsoft Agent control click or drag events).</span></span> <span data-ttu-id="5eccb-119">Il set di caratteri per ricevere input da mouse e vocale è il carattere superiore e il client che riceve l'input è il client attivo di tale carattere.</span><span class="sxs-lookup"><span data-stu-id="5eccb-119">The character set to receive mouse and speech input is the topmost character and the client that receives the input is the active client of that character.</span></span> <span data-ttu-id="5eccb-120">La finestra del carattere superiore viene visualizzata anche nella parte superiore dell'ordine z della finestra dei caratteri. In genere, l'utente determina il carattere superiore selezionando in modo esplicito il carattere.</span><span class="sxs-lookup"><span data-stu-id="5eccb-120">(The topmost character's window also appears at the top of the character window's z-order.) Typically, the user determines the topmost character by explicitly selecting the character.</span></span> <span data-ttu-id="5eccb-121">Tuttavia, l'attivazione in primo piano cambia anche quando un carattere viene visualizzato o nascosto (il carattere diventa o non è più in primo piano, rispettivamente).</span><span class="sxs-lookup"><span data-stu-id="5eccb-121">However, topmost activation also changes when a character is shown or hidden (the character becomes or is no longer topmost, respectively.)</span></span>

<span data-ttu-id="5eccb-122">È anche possibile usare questo metodo per gestire in modo esplicito quando il client riceve input indirizzato al carattere, ad esempio quando l'applicazione stessa diventa attiva.</span><span class="sxs-lookup"><span data-stu-id="5eccb-122">You can also use this method to explicitly manage when your client receives input directed to the character such as when your application itself becomes active.</span></span> <span data-ttu-id="5eccb-123">Se, ad esempio, si imposta *lo stato* su 2, il carattere è in primo piano e il client riceve tutti gli eventi di input del mouse e vocale generati dall'interazione dell'utente con il carattere.</span><span class="sxs-lookup"><span data-stu-id="5eccb-123">For example, setting *State* to 2 makes the character topmost and your client receives all mouse and speech input events generated from user interaction with the character.</span></span> <span data-ttu-id="5eccb-124">Quindi, rende il client anche il client di input-attivo del carattere.</span><span class="sxs-lookup"><span data-stu-id="5eccb-124">Therefore, it also makes your client the input-active client of the character.</span></span>

<span data-ttu-id="5eccb-125">Tuttavia, è anche possibile impostare se stessi come client attivo per un carattere senza rendere il carattere superiore, impostando *stato* su 1.</span><span class="sxs-lookup"><span data-stu-id="5eccb-125">However, you can also set yourself to be the active client for a character without making the character topmost, by setting *State* to 1.</span></span> <span data-ttu-id="5eccb-126">Ciò consente al client di ricevere input indirizzato a tale carattere quando il carattere diventa più in alto.</span><span class="sxs-lookup"><span data-stu-id="5eccb-126">This enables your client to receive input directed to that character when the character becomes topmost.</span></span> <span data-ttu-id="5eccb-127">Analogamente, è possibile impostare il client su non come client attivo (non per ricevere input) quando il carattere diventa in primo piano, impostando *stato* su 0.</span><span class="sxs-lookup"><span data-stu-id="5eccb-127">Similarly, you can set your client to not be the active client (not to receive input) when the character becomes topmost, by setting *State* to 0.</span></span>

<span data-ttu-id="5eccb-128">Evitare di chiamare questo metodo direttamente dopo un metodo [**show**](/previous-versions/visualstudio/foxpro/d79z7xxa(v=vs.71)) .</span><span class="sxs-lookup"><span data-stu-id="5eccb-128">Avoid calling this method directly after a [**Show**](/previous-versions/visualstudio/foxpro/d79z7xxa(v=vs.71)) method.</span></span> <span data-ttu-id="5eccb-129">**Mostra** imposta automaticamente il client attivo di input.</span><span class="sxs-lookup"><span data-stu-id="5eccb-129">**Show** automatically sets the input-active client.</span></span> <span data-ttu-id="5eccb-130">Quando il carattere è nascosto, la chiamata [**Activate**](/previous-versions/visualstudio/foxpro/01ayxx68(v=vs.71)) potrebbe non riuscire se viene elaborata prima del completamento del metodo **show** .</span><span class="sxs-lookup"><span data-stu-id="5eccb-130">When the character is hidden, the [**Activate**](/previous-versions/visualstudio/foxpro/01ayxx68(v=vs.71)) call may fail if it gets processed before the **Show** method completes.</span></span>

<span data-ttu-id="5eccb-131">Se si chiama questo metodo in una funzione, viene restituito un valore booleano che indica se il metodo ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="5eccb-131">If you call this method to a function, it returns a Boolean value that indicates whether the method succeeded.</span></span> <span data-ttu-id="5eccb-132">Il tentativo di chiamare questo metodo con il parametro *state* impostato su 2 quando il carattere specificato è nascosto avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="5eccb-132">Attempting to call this method with the *State* parameter set to 2 when the specified character is hidden will fail.</span></span> <span data-ttu-id="5eccb-133">Analogamente, se si imposta *lo stato* su 0 e l'applicazione è l'unico client, questa chiamata ha esito negativo perché un carattere deve avere sempre un client in primo piano.</span><span class="sxs-lookup"><span data-stu-id="5eccb-133">Similarly, if you set *State* to 0 and your application is the only client, this call fails because a character must always have a topmost client.</span></span>


```
   Dim Genie as Object

   Sub FormLoad()

   Agent1.Characters.Load "Genie", "Genie.acs"

   Set Genie = Agent1.Characters ("Genie")

   If (Genie. Activate = True) Then
      'I'm active

   Else
      'I must be hidden or something

   End If 
   
   End Sub
```



> [!Note]  
> <span data-ttu-id="5eccb-134">La chiamata a questo metodo con *stato* impostato su 1 in genere non genera un evento [**ActivateInput**](https://www.bing.com/search?q=**ActivateInput**) a meno che non ci siano altri caratteri caricati o che l'applicazione sia già in input-Active.</span><span class="sxs-lookup"><span data-stu-id="5eccb-134">Calling this method with *State* set to 1 does not typically generate an [**ActivateInput**](https://www.bing.com/search?q=**ActivateInput**) event unless there are no other characters loaded or your application is already input-active.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="5eccb-135">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="5eccb-135">See Also</span></span>

<span data-ttu-id="5eccb-136">[**Evento ActivateInput**](activateinput-event.md), [ **evento DeactivateInput**](deactivateinput-event.md)</span><span class="sxs-lookup"><span data-stu-id="5eccb-136">[**ActivateInput event**](activateinput-event.md), [**DeactivateInput event**](deactivateinput-event.md)</span></span>


 

