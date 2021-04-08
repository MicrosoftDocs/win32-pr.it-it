---
title: Evento ListenStart
description: Evento ListenStart
ms.assetid: 59feacd6-0b9f-4bf4-b544-48de49384312
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19b8cc19ad727f8e9c4606bbbfba7b2e03e7d638
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856789"
---
# <a name="listenstart-event"></a><span data-ttu-id="dc525-103">Evento ListenStart</span><span class="sxs-lookup"><span data-stu-id="dc525-103">ListenStart Event</span></span>

<span data-ttu-id="dc525-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="dc525-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="dc525-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="dc525-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="dc525-106">Si verifica quando inizia la modalità di ascolto (riconoscimento vocale).</span><span class="sxs-lookup"><span data-stu-id="dc525-106">Occurs when Listening mode (speech recognition) begins.</span></span>

</dd> <dt>

<span data-ttu-id="dc525-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="dc525-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="dc525-108">Agente **secondario** *. \* \* \* ListenStart (ByVal* \*  *CharacterID \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="dc525-108">**Sub** *agent.\*\*\*ListenStart (ByVal*\* *CharacterID\*\*\*)*\*</span></span>



| <span data-ttu-id="dc525-109">Parte</span><span class="sxs-lookup"><span data-stu-id="dc525-109">Part</span></span>          | <span data-ttu-id="dc525-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dc525-110">Description</span></span>                                            |
|---------------|--------------------------------------------------------|
| <span data-ttu-id="dc525-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="dc525-111">*CharacterID*</span></span> | <span data-ttu-id="dc525-112">Restituisce l'ID del carattere di ascolto sotto forma di stringa.</span><span class="sxs-lookup"><span data-stu-id="dc525-112">Returns the ID of the listening character as a string.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="dc525-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="dc525-113">Remarks</span></span>

<span data-ttu-id="dc525-114">Questo evento viene inviato a tutti i client quando viene avviata la modalità di ascolto perché l'utente ha premuto il tasto ascolto o il client di input-attivo denominato metodo [**Listen**](listen-method.md) con **true**.</span><span class="sxs-lookup"><span data-stu-id="dc525-114">This event is sent to all clients when Listening mode begins because the user pressed the Listening key or the input-active client called the [**Listen**](listen-method.md) method with **True**.</span></span> <span data-ttu-id="dc525-115">È possibile usare questo evento per evitare che il carattere parli mentre la modalità di ascolto è attiva.</span><span class="sxs-lookup"><span data-stu-id="dc525-115">You can use this event to avoid having your character speak while the Listening mode is on.</span></span>

<span data-ttu-id="dc525-116">Se si attiva la modalità di ascolto con il metodo [**Listen**](listen-method.md) e quindi l'utente preme il tasto ascolto, la modalità di ascolto viene reimpostata e continua fino a quando non viene completato il timeout della chiave di ascolto, viene rilasciato il tasto di attesa o l'utente termina di parlare, a seconda di quale sarà il momento successivo.</span><span class="sxs-lookup"><span data-stu-id="dc525-116">If you turn on Listening mode with the [**Listen**](listen-method.md) method and then the user presses the Listening key, the Listening mode resets and continues until the Listening key time-out completes, the Listening key is released, or the user finishes speaking, whichever is later.</span></span> <span data-ttu-id="dc525-117">In questa situazione, quando la modalità di ascolto è già attiva, non si otterrà un evento **ListenStart** aggiuntivo quando l'utente preme il tasto di attesa.</span><span class="sxs-lookup"><span data-stu-id="dc525-117">In this situation, when Listening mode is already on, you will not get an additional **ListenStart** event when the user presses the Listening key.</span></span>

<span data-ttu-id="dc525-118">L'evento restituisce il carattere ai client attualmente caricati da questo carattere.</span><span class="sxs-lookup"><span data-stu-id="dc525-118">The event returns the character to the clients that currently have this character loaded.</span></span> <span data-ttu-id="dc525-119">Tutti gli altri client ricevono un carattere null (stringa vuota).</span><span class="sxs-lookup"><span data-stu-id="dc525-119">All other clients receive a null character (empty string).</span></span>

### <a name="see-also"></a><span data-ttu-id="dc525-120">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="dc525-120">See Also</span></span>

<span data-ttu-id="dc525-121">[**Evento ListenComplete**](listencomplete-event.md), [ **metodo Listen**](listen-method.md)</span><span class="sxs-lookup"><span data-stu-id="dc525-121">[**ListenComplete event**](listencomplete-event.md), [**Listen method**](listen-method.md)</span></span>


 

 




