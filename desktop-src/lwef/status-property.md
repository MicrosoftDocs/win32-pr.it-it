---
title: Proprietà Status
description: Proprietà Status
ms.assetid: vs|msagent|~\pacontrol_8xd6.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 402e88185e1024aa5958d06936a6529ae4012622
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298461"
---
# <a name="status-property"></a><span data-ttu-id="2dc60-103">Proprietà Status</span><span class="sxs-lookup"><span data-stu-id="2dc60-103">Status Property</span></span>

<span data-ttu-id="2dc60-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2dc60-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="2dc60-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="2dc60-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="2dc60-106">Restituisce lo stato del canale di output audio.</span><span class="sxs-lookup"><span data-stu-id="2dc60-106">Returns the status of the audio output channel.</span></span>

</dd> <dt>

<span data-ttu-id="2dc60-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="2dc60-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="2dc60-108">*agente \* \* *. AudioOutput. status**</span><span class="sxs-lookup"><span data-stu-id="2dc60-108">*agent\*\*\*.AudioOutput.Status*\*</span></span>



| <span data-ttu-id="2dc60-109">Valore</span><span class="sxs-lookup"><span data-stu-id="2dc60-109">Value</span></span> | <span data-ttu-id="2dc60-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2dc60-110">Description</span></span>                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2dc60-111">0</span><span class="sxs-lookup"><span data-stu-id="2dc60-111">0</span></span>     | <span data-ttu-id="2dc60-112">Il canale di output audio è disponibile (non occupato).</span><span class="sxs-lookup"><span data-stu-id="2dc60-112">The audio output channel is available (not busy).</span></span>                                                                 |
| <span data-ttu-id="2dc60-113">1</span><span class="sxs-lookup"><span data-stu-id="2dc60-113">1</span></span>     | <span data-ttu-id="2dc60-114">Non è disponibile alcun supporto per l'output audio. ad esempio, perché non è presente alcuna scheda audio.</span><span class="sxs-lookup"><span data-stu-id="2dc60-114">There is no support for audio output; for example, because there is no sound card.</span></span>                                |
| <span data-ttu-id="2dc60-115">2</span><span class="sxs-lookup"><span data-stu-id="2dc60-115">2</span></span>     | <span data-ttu-id="2dc60-116">Non è possibile aprire il canale di output audio (è occupato); ad esempio, perché un'altra applicazione sta riproducendo audio.</span><span class="sxs-lookup"><span data-stu-id="2dc60-116">The audio output channel can't be opened (is busy); for example, because some other application is playing audio.</span></span> |
| <span data-ttu-id="2dc60-117">3</span><span class="sxs-lookup"><span data-stu-id="2dc60-117">3</span></span>     | <span data-ttu-id="2dc60-118">Il canale di output audio è occupato perché il server sta elaborando l'input vocale dell'utente.</span><span class="sxs-lookup"><span data-stu-id="2dc60-118">The audio output channel is busy because the server is processing user speech input.</span></span>                              |
| <span data-ttu-id="2dc60-119">4</span><span class="sxs-lookup"><span data-stu-id="2dc60-119">4</span></span>     | <span data-ttu-id="2dc60-120">Il canale di output audio è occupato perché è in corso un carattere.</span><span class="sxs-lookup"><span data-stu-id="2dc60-120">The audio output channel is busy because a character is currently speaking.</span></span>                                       |
| <span data-ttu-id="2dc60-121">5</span><span class="sxs-lookup"><span data-stu-id="2dc60-121">5</span></span>     | <span data-ttu-id="2dc60-122">Il canale di output audio non è occupato, ma è in attesa dell'input vocale dell'utente.</span><span class="sxs-lookup"><span data-stu-id="2dc60-122">The audio output channel is not busy, but it is waiting for user speech input.</span></span>                                    |
| <span data-ttu-id="2dc60-123">6</span><span class="sxs-lookup"><span data-stu-id="2dc60-123">6</span></span>     | <span data-ttu-id="2dc60-124">Si è verificato un altro problema (sconosciuto) durante il tentativo di accedere al canale di output audio.</span><span class="sxs-lookup"><span data-stu-id="2dc60-124">There was some other (unknown) problem in attempting to access the audio output channel.</span></span>                          |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2dc60-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="2dc60-125">Remarks</span></span>

<span data-ttu-id="2dc60-126">Questa impostazione consente all'applicazione client di eseguire una query sul canale di output audio, restituendo un valore integer che indica lo stato del canale di output audio.</span><span class="sxs-lookup"><span data-stu-id="2dc60-126">This setting enables your client application to query the audio output channel, returning an Integer value that indicates the status of the audio output channel.</span></span> <span data-ttu-id="2dc60-127">È possibile usare questo valore per determinare se è opportuno che il carattere parli o se è appropriato provare ad attivare la modalità di ascolto (usando il metodo [**Listen**](listen-method.md) ).</span><span class="sxs-lookup"><span data-stu-id="2dc60-127">You can use this to determine whether it is appropriate to have your character speak or whether it is appropriate to try to turn on Listening mode (using the [**Listen**](listen-method.md) method).</span></span>

## <a name="see-also"></a><span data-ttu-id="2dc60-128">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="2dc60-128">See Also</span></span>

[<span data-ttu-id="2dc60-129">**Evento ListenComplete**</span><span class="sxs-lookup"><span data-stu-id="2dc60-129">**ListenComplete event**</span></span>](listencomplete-event.md)


 

 




