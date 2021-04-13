---
title: Evento ListenComplete
description: Evento ListenComplete
ms.assetid: 29e3f424-17b4-4287-b644-ed62b80e0035
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dbfe0fac272b50af3f82efdc8a422bebddbf786
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396699"
---
# <a name="listencomplete-event"></a><span data-ttu-id="feb13-103">Evento ListenComplete</span><span class="sxs-lookup"><span data-stu-id="feb13-103">ListenComplete Event</span></span>

<span data-ttu-id="feb13-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="feb13-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="feb13-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="feb13-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="feb13-106">Si verifica quando la modalità di ascolto (riconoscimento vocale) è terminata.</span><span class="sxs-lookup"><span data-stu-id="feb13-106">Occurs when Listening mode (speech recognition) has ended.</span></span>

</dd> <dt>

<span data-ttu-id="feb13-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="feb13-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="feb13-108"> *Agente secondario.\ *\ *\ * ListenComplete (ByVal*\ *  *CharacterID*, **ByVal** *cause\ *\ * *)**</span><span class="sxs-lookup"><span data-stu-id="feb13-108">**Sub** *agent.\*\*\*ListenComplete (ByVal*\* *CharacterID*, **ByVal** *Cause\*\*\*)*\*</span></span>



| <span data-ttu-id="feb13-109">Parte</span><span class="sxs-lookup"><span data-stu-id="feb13-109">Part</span></span>          | <span data-ttu-id="feb13-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="feb13-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="feb13-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="feb13-111">*CharacterID*</span></span> | <span data-ttu-id="feb13-112">Restituisce l'ID del carattere di ascolto sotto forma di stringa.</span><span class="sxs-lookup"><span data-stu-id="feb13-112">Returns the ID of the listening character as a string.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="feb13-113">*Causa*</span><span class="sxs-lookup"><span data-stu-id="feb13-113">*Cause*</span></span>       | <span data-ttu-id="feb13-114">Restituisce la parte dell'evento completo come numero intero che può essere uno dei seguenti: 1 la modalità di ascolto è stata disattivata dal codice del programma.</span><span class="sxs-lookup"><span data-stu-id="feb13-114">Returns the cause of the complete event as an integer that may be one of the following: 1 Listening mode was turned off by program code.</span></span><br/> <span data-ttu-id="feb13-115">si è verificato un timeout di 2 modalità di ascolto (attivata dal codice del programma).</span><span class="sxs-lookup"><span data-stu-id="feb13-115">2 Listening mode (turned on by program code) timed out.</span></span><br/> <span data-ttu-id="feb13-116">si è verificato un timeout di 3 modalità di ascolto (attivata dal tasto di attesa).</span><span class="sxs-lookup"><span data-stu-id="feb13-116">3 Listening mode (turned on by the Listening key) timed out.</span></span><br/> <span data-ttu-id="feb13-117">4 la modalità di ascolto è stata disattivata perché l'utente ha rilasciato il tasto di attesa.</span><span class="sxs-lookup"><span data-stu-id="feb13-117">4 Listening mode was turned off because the user released the Listening key.</span></span><br/> <span data-ttu-id="feb13-118">5 modalità di ascolto terminata perché l'utente ha terminato di parlare.</span><span class="sxs-lookup"><span data-stu-id="feb13-118">5 Listening mode ended because the user finished speaking.</span></span><br/> <span data-ttu-id="feb13-119">6 modalità di ascolto terminata perché il client di input-attivo è stato disattivato.</span><span class="sxs-lookup"><span data-stu-id="feb13-119">6 Listening mode ended because the input-active client was deactivated.</span></span><br/> <span data-ttu-id="feb13-120">7 modalità di ascolto terminata perché il carattere predefinito è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="feb13-120">7 Listening mode ended because the default character was changed.</span></span><br/> <span data-ttu-id="feb13-121">8 modalità di ascolto terminata perché l'utente ha disabilitato l'input vocale.</span><span class="sxs-lookup"><span data-stu-id="feb13-121">8 Listening mode ended because the user disabled speech input.</span></span><br/> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="feb13-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="feb13-122">Remarks</span></span>

<span data-ttu-id="feb13-123">Questo evento viene inviato a tutti i client quando termina il timeout della modalità di ascolto, dopo che l'utente rilascia il tasto di attesa, quando il client attivo di input chiama il metodo [**Listen**](listen-method.md) con **false** oppure l'utente ha terminato di parlare.</span><span class="sxs-lookup"><span data-stu-id="feb13-123">This event is sent to all clients when the Listening mode time-out ends, after the user releases the Listening key, when the input active client calls the [**Listen**](listen-method.md) method with **False**, or the user finished speaking.</span></span> <span data-ttu-id="feb13-124">È possibile usare questo evento per determinare quando riavviare l'output di tipo carattere parlato.</span><span class="sxs-lookup"><span data-stu-id="feb13-124">You can use this event to determine when to resume character spoken (audio) output.</span></span>

<span data-ttu-id="feb13-125">Se si attiva la modalità di ascolto utilizzando il metodo [**Listen**](listen-method.md) e quindi l'utente preme il tasto ascolto, la modalità di ascolto viene reimpostata e continua fino a quando non viene completato il timeout della chiave di ascolto, viene rilasciata la chiave in ascolto o l'utente termina di parlare, a seconda di quale dei più tardi.</span><span class="sxs-lookup"><span data-stu-id="feb13-125">If you turn on Listening mode using the [**Listen**](listen-method.md) method and then the user presses the Listening key, the Listening mode resets and continues until the Listening key time-out completes, the Listening key is released, or the user finishes speaking, whichever is later.</span></span> <span data-ttu-id="feb13-126">In questa situazione, non si riceverà un evento **ListenComplete** fino al completamento della modalità della chiave di ascolto.</span><span class="sxs-lookup"><span data-stu-id="feb13-126">In this situation, you will not receive a **ListenComplete** event until the listening key's mode completes.</span></span>

<span data-ttu-id="feb13-127">L'evento restituisce il carattere ai client attualmente caricati da questo carattere.</span><span class="sxs-lookup"><span data-stu-id="feb13-127">The event returns the character to the clients that currently have this character loaded.</span></span> <span data-ttu-id="feb13-128">Tutti gli altri client ricevono un carattere null (stringa vuota).</span><span class="sxs-lookup"><span data-stu-id="feb13-128">All other clients receive a null character (empty string).</span></span>

### <a name="see-also"></a><span data-ttu-id="feb13-129">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="feb13-129">See Also</span></span>

<span data-ttu-id="feb13-130">[**Evento ListenStart**](listenstart-event.md), [ **metodo Listen**](listen-method.md)</span><span class="sxs-lookup"><span data-stu-id="feb13-130">[**ListenStart event**](listenstart-event.md), [**Listen method**](listen-method.md)</span></span>


 

 





