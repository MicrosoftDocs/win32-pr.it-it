---
title: Proprietà SRStatus
description: Proprietà SRStatus
ms.assetid: 67618a35-05e4-4bb3-b910-c75de6e32578
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64cb6ba16bc024a52b65efa98c22fd089ad79da
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045382"
---
# <a name="srstatus-property"></a><span data-ttu-id="1e92d-103">Proprietà SRStatus</span><span class="sxs-lookup"><span data-stu-id="1e92d-103">SRStatus Property</span></span>

<span data-ttu-id="1e92d-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1e92d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="1e92d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="1e92d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="1e92d-106">Restituisce un valore che indica se è possibile avviare l'input vocale per il carattere.</span><span class="sxs-lookup"><span data-stu-id="1e92d-106">Returns whether speech input can be started for the character.</span></span>

</dd> <dt>

<span data-ttu-id="1e92d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="1e92d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="1e92d-108">*agente. ***Caratteri ("*** CharacterID \* \* *"). SRStatus**</span><span class="sxs-lookup"><span data-stu-id="1e92d-108">*agent.\*\*\*Characters("*\*\* CharacterID\***").SRStatus**</span></span>



| <span data-ttu-id="1e92d-109">Valore</span><span class="sxs-lookup"><span data-stu-id="1e92d-109">Value</span></span> | <span data-ttu-id="1e92d-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1e92d-110">Description</span></span>                                                                                                                                                                                                                               |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e92d-111">0</span><span class="sxs-lookup"><span data-stu-id="1e92d-111">0</span></span>     | <span data-ttu-id="1e92d-112">Le condizioni supportano l'input vocale.</span><span class="sxs-lookup"><span data-stu-id="1e92d-112">Conditions support speech input.</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="1e92d-113">1</span><span class="sxs-lookup"><span data-stu-id="1e92d-113">1</span></span>     | <span data-ttu-id="1e92d-114">Nessun dispositivo di input audio disponibile nel sistema.</span><span class="sxs-lookup"><span data-stu-id="1e92d-114">There is no audio input device available on this system.</span></span> <span data-ttu-id="1e92d-115">Si noti che questo non rileva se un microfono è installato; può solo rilevare se l'utente dispone di una scheda audio abilitata per l'input correttamente installata con un driver funzionante.</span><span class="sxs-lookup"><span data-stu-id="1e92d-115">(Note that this does not detect whether a microphone is installed; it can only detect whether the user has a properly installed input-enabled sound card with a working driver.)</span></span> |
| <span data-ttu-id="1e92d-116">2</span><span class="sxs-lookup"><span data-stu-id="1e92d-116">2</span></span>     | <span data-ttu-id="1e92d-117">Un altro client è il client attivo di questo carattere oppure il carattere corrente non è in primo piano.</span><span class="sxs-lookup"><span data-stu-id="1e92d-117">Another client is the active client of this character, or the current character is not topmost.</span></span>                                                                                                                                           |
| <span data-ttu-id="1e92d-118">3</span><span class="sxs-lookup"><span data-stu-id="1e92d-118">3</span></span>     | <span data-ttu-id="1e92d-119">Il canale di input o di output audio è attualmente occupato, un'applicazione sta usando audio.</span><span class="sxs-lookup"><span data-stu-id="1e92d-119">The audio input or output channel is currently busy, an application is using audio.</span></span>                                                                                                                                                       |
| <span data-ttu-id="1e92d-120">4</span><span class="sxs-lookup"><span data-stu-id="1e92d-120">4</span></span>     | <span data-ttu-id="1e92d-121">Si è verificato un errore non specificato durante il processo di inizializzazione del sottosistema di riconoscimento vocale.</span><span class="sxs-lookup"><span data-stu-id="1e92d-121">An unspecified error occurred in the process of initializing the speech recognition subsystem.</span></span> <span data-ttu-id="1e92d-122">Ciò include la possibilità che non sia disponibile un motore di riconoscimento vocale corrispondente all'impostazione della lingua del carattere.</span><span class="sxs-lookup"><span data-stu-id="1e92d-122">This includes the possibility that there is no speech engine available matching the character's language setting.</span></span>                          |
| <span data-ttu-id="1e92d-123">5</span><span class="sxs-lookup"><span data-stu-id="1e92d-123">5</span></span>     | <span data-ttu-id="1e92d-124">L'utente ha disabilitato l'input vocale nelle opzioni dei caratteri avanzati.</span><span class="sxs-lookup"><span data-stu-id="1e92d-124">The user has disabled speech input in the Advanced Character Options.</span></span>                                                                                                                                                                     |
| <span data-ttu-id="1e92d-125">6</span><span class="sxs-lookup"><span data-stu-id="1e92d-125">6</span></span>     | <span data-ttu-id="1e92d-126">Si è verificato un errore durante il controllo dello stato dell'audio, ma la cause dell'errore non è stata restituita dal sistema.</span><span class="sxs-lookup"><span data-stu-id="1e92d-126">An error occurred in checking the audio status, but the cause of the error was not returned by the system.</span></span>                                                                                                                                |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1e92d-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="1e92d-127">Remarks</span></span>

<span data-ttu-id="1e92d-128">Questa proprietà restituisce le condizioni necessarie per supportare l'input vocale, incluso lo stato del dispositivo audio.</span><span class="sxs-lookup"><span data-stu-id="1e92d-128">This property returns the conditions necessary to support speech input, including the status of the audio device.</span></span> <span data-ttu-id="1e92d-129">È possibile controllare questa proprietà prima di chiamare il metodo [**Listen**](listen-method.md) per garantirne l'esito positivo.</span><span class="sxs-lookup"><span data-stu-id="1e92d-129">You can check this property before you call the [**Listen**](listen-method.md) method to better ensure its success.</span></span>

<span data-ttu-id="1e92d-130">Quando l'input vocale è abilitato nella finestra delle proprietà dell'agente (Opzioni carattere avanzate), l'esecuzione di una query su questa proprietà caricherà il motore associato, se non è già caricato, e avvierà servizi vocali.</span><span class="sxs-lookup"><span data-stu-id="1e92d-130">When speech input is enabled in the Agent property sheet (Advanced Character Options), querying this property will load the associated engine, if it is not already loaded, and start speech services.</span></span> <span data-ttu-id="1e92d-131">Ovvero, la chiave di ascolto è disponibile e il suggerimento di ascolto è automaticamente visualizzabile.</span><span class="sxs-lookup"><span data-stu-id="1e92d-131">That is, the Listening key is available, and the Listening Tip is automatically displayable.</span></span> <span data-ttu-id="1e92d-132">(Il tasto di attesa e il suggerimento di ascolto sono abilitati solo se sono abilitati anche nelle opzioni dei caratteri avanzati). Tuttavia, se si esegue una query sulla proprietà quando la voce Speech è disabilitata, il server non avvia i servizi di riconoscimento vocale.</span><span class="sxs-lookup"><span data-stu-id="1e92d-132">(The Listening key and Listening Tip are only enabled if they are also enabled in Advanced Character Options.) However, if you query the property when speech is disabled, the server does not start speech services.</span></span>

<span data-ttu-id="1e92d-133">Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="1e92d-133">This property only applies to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="1e92d-134">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="1e92d-134">See Also</span></span>

[<span data-ttu-id="1e92d-135">**Listen (metodo)**</span><span class="sxs-lookup"><span data-stu-id="1e92d-135">**Listen method**</span></span>](listen-method.md)


 

 




