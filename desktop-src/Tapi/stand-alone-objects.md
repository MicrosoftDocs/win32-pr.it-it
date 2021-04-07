---
description: TAPI 3 prevede una serie di oggetti indipendenti dai cinque oggetti TAPI principali (TAPI, Address, Call, CallHub e Terminal).
ms.assetid: 090fa8e5-58a5-46ee-89a3-bd97fcfbf0f0
title: Oggetti Stand-Alone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e71fdea9c7ed4b66f57c3c0fe35625f35656555e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881646"
---
# <a name="stand-alone-objects"></a><span data-ttu-id="4d87c-103">Oggetti Stand-Alone</span><span class="sxs-lookup"><span data-stu-id="4d87c-103">Stand-Alone Objects</span></span>

<span data-ttu-id="4d87c-104">TAPI 3 prevede una serie di oggetti indipendenti dai cinque oggetti TAPI principali (TAPI, Address, Call, CallHub e Terminal).</span><span class="sxs-lookup"><span data-stu-id="4d87c-104">TAPI 3 involves a number of objects that are independent of its five main TAPI objects (TAPI, Address, Call, CallHub, and Terminal).</span></span> <span data-ttu-id="4d87c-105">Le [interfacce di eventi](./event-interfaces.md) e le interfacce di [enumeratore](enumerator-interfaces.md) sono oggetti autonomi e vengono riepilogate separatamente.</span><span class="sxs-lookup"><span data-stu-id="4d87c-105">[Event Interfaces](./event-interfaces.md) and [Enumerator Interfaces](enumerator-interfaces.md) are stand-alone objects, and are summarized separately.</span></span> <span data-ttu-id="4d87c-106">Di seguito vengono riepilogate le interfacce autonome non di eventi e non enumeratori.</span><span class="sxs-lookup"><span data-stu-id="4d87c-106">The following summarizes non-event and non-enumerator stand-alone interfaces.</span></span>



| <span data-ttu-id="4d87c-107">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="4d87c-107">Interface</span></span>                                             | <span data-ttu-id="4d87c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4d87c-108">Description</span></span>                                                                                                                                                                                                   |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4d87c-109">**ITCollection**</span><span class="sxs-lookup"><span data-stu-id="4d87c-109">**ITCollection**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection)                  | <span data-ttu-id="4d87c-110">Fornisce metodi per consentire alle applicazioni client di automazione, ad esempio Visual Basic di recuperare informazioni sulla raccolta.</span><span class="sxs-lookup"><span data-stu-id="4d87c-110">Provides methods to allow Automation client applications such as Visual Basic to retrieve collection information.</span></span>                                                                                             |
| [<span data-ttu-id="4d87c-111">**ITCollection2**</span><span class="sxs-lookup"><span data-stu-id="4d87c-111">**ITCollection2**</span></span>](/windows/desktop/api/Tapi3if/nn-tapi3if-itcollection2)                | <span data-ttu-id="4d87c-112">Estende [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) fornendo metodi aggiuntivi per la modifica delle raccolte.</span><span class="sxs-lookup"><span data-stu-id="4d87c-112">Extends [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) by providing additional methods for modifying collections.</span></span>                                                                                                       |
| [<span data-ttu-id="4d87c-113">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="4d87c-113">**IDispatch**</span></span>](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) | <span data-ttu-id="4d87c-114">Interfaccia COM standard per l'implementazione dell'automazione.</span><span class="sxs-lookup"><span data-stu-id="4d87c-114">Standard COM interface for implementing Automation.</span></span>                                                                                                                                                           |
| [<span data-ttu-id="4d87c-115">**IUnknown**</span><span class="sxs-lookup"><span data-stu-id="4d87c-115">**IUnknown**</span></span>](/windows/win32/api/unknwn/nn-unknwn-iunknown)                         | <span data-ttu-id="4d87c-116">Interfaccia COM standard per ottenere i puntatori alle interfacce di oggetti.</span><span class="sxs-lookup"><span data-stu-id="4d87c-116">Standard COM interface for getting pointers to object interfaces.</span></span>                                                                                                                                             |
| [<span data-ttu-id="4d87c-117">**ITDispatchMapper**</span><span class="sxs-lookup"><span data-stu-id="4d87c-117">**ITDispatchMapper**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itdispatchmapper)          | <span data-ttu-id="4d87c-118">Consente a un'applicazione di recuperare il puntatore di invio di un'altra interfaccia su un oggetto, dato un puntatore [**IDispatch**](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) corrente.</span><span class="sxs-lookup"><span data-stu-id="4d87c-118">Allows an application to retrieve the dispatch pointer of another interface on an object, given a current [**IDispatch**](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) pointer.</span></span> <span data-ttu-id="4d87c-119">Utile per alcuni linguaggi di scripting.</span><span class="sxs-lookup"><span data-stu-id="4d87c-119">Useful for some scripting languages.</span></span> |
| [<span data-ttu-id="4d87c-120">**ITRequest**</span><span class="sxs-lookup"><span data-stu-id="4d87c-120">**ITRequest**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itrequest)                        | <span data-ttu-id="4d87c-121">Fornisce metodi che consentono a un'applicazione TAPI 3 di utilizzare la [telefonia assistita](assisted-telephony-overview.md).</span><span class="sxs-lookup"><span data-stu-id="4d87c-121">Provides methods that allow a TAPI 3 application to use [Assisted Telephony](assisted-telephony-overview.md).</span></span>                                                                                                |



 



| <span data-ttu-id="4d87c-122">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="4d87c-122">Interface</span></span>                                  | <span data-ttu-id="4d87c-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4d87c-123">Description</span></span>                                                                                                                                                                |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4d87c-124">**ITMediaControl**</span><span class="sxs-lookup"><span data-stu-id="4d87c-124">**ITMediaControl**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itmediacontrol)   | <span data-ttu-id="4d87c-125">Avvia, arresta e sospende le azioni correnti, ad esempio una riproduzione.</span><span class="sxs-lookup"><span data-stu-id="4d87c-125">Starts, stops, and pauses current actions, such as a playback.</span></span>                                                                                                             |
| [<span data-ttu-id="4d87c-126">**ITMediaPlayback**</span><span class="sxs-lookup"><span data-stu-id="4d87c-126">**ITMediaPlayback**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) | <span data-ttu-id="4d87c-127">Fornisce metodi specifici per la riproduzione che consentono a un'applicazione di eseguire operazioni come l'impostazione dell'elenco di file da riprodurre e la modifica della velocità di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="4d87c-127">Provides playback-specific methods that allow an application to perform such operations as setting the list of files to play and changing the playback speed.</span></span>              |
| [<span data-ttu-id="4d87c-128">**ITMediaRecord**</span><span class="sxs-lookup"><span data-stu-id="4d87c-128">**ITMediaRecord**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itmediarecord)     | <span data-ttu-id="4d87c-129">Fornisce metodi specifici della registrazione che consentono a un'applicazione di eseguire operazioni come l'impostazione dei nomi dei file da registrare e la modifica della durata di una registrazione.</span><span class="sxs-lookup"><span data-stu-id="4d87c-129">Provides recording-specific methods that allow an application to perform such operations as setting the names of files to record and changing the duration of a recording.</span></span> |



 



| <span data-ttu-id="4d87c-130">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="4d87c-130">Interface</span></span>                                                  | <span data-ttu-id="4d87c-131">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4d87c-131">Description</span></span>                                                                                                                                                         |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4d87c-132">**ITScriptableAudioFormat**</span><span class="sxs-lookup"><span data-stu-id="4d87c-132">**ITScriptableAudioFormat**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itscriptableaudioformat) | <span data-ttu-id="4d87c-133">Recupera il formato audio da o imposta il formato audio per una traccia.</span><span class="sxs-lookup"><span data-stu-id="4d87c-133">Retrieves the audio format from, or sets the audio format for, a track.</span></span>                                                                                             |
| [<span data-ttu-id="4d87c-134">**ITStaticAudioTerminal**</span><span class="sxs-lookup"><span data-stu-id="4d87c-134">**ITStaticAudioTerminal**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itstaticaudioterminal)     | <span data-ttu-id="4d87c-135">Fornisce metodi su oggetti terminali audio statici necessari per supportare i dispositivi telefonici.</span><span class="sxs-lookup"><span data-stu-id="4d87c-135">Provides methods on static audio terminal objects that are needed to support phone devices.</span></span> <span data-ttu-id="4d87c-136">TAPI 3,1 MSPs deve esporre questa interfaccia su tutti i terminali audio statici.</span><span class="sxs-lookup"><span data-stu-id="4d87c-136">TAPI 3.1 MSPs must expose this interface on all static audio terminals.</span></span> |



 

 

 
