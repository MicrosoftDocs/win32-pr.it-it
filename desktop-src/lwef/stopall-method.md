---
title: Metodo StopAll
description: Metodo StopAll
ms.assetid: 2ce32ff8-4908-45b1-9b83-4d558f67417c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76c99a687c2481d9686e84b7fa5c198e7a4273a2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299594"
---
# <a name="stopall-method"></a><span data-ttu-id="36ae4-103">Metodo StopAll</span><span class="sxs-lookup"><span data-stu-id="36ae4-103">StopAll Method</span></span>

<span data-ttu-id="36ae4-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="36ae4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="36ae4-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="36ae4-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="36ae4-106">Arresta tutte le richieste di animazione o i tipi di richieste specificati per il carattere specificato.</span><span class="sxs-lookup"><span data-stu-id="36ae4-106">Stops all animation requests or specified types of requests for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="36ae4-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="36ae4-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="36ae4-108">\*agente ***. Caratteri ("*** CharacterID \* \* *").* \*  \[ *Tipo* stopAll\]</span><span class="sxs-lookup"><span data-stu-id="36ae4-108">*agent ***.Characters ("*** CharacterID\*\*\*").StopAll*\* \[*Type*\]</span></span>



| <span data-ttu-id="36ae4-109">Parte</span><span class="sxs-lookup"><span data-stu-id="36ae4-109">Part</span></span>   | <span data-ttu-id="36ae4-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="36ae4-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36ae4-111">*Tipo*</span><span class="sxs-lookup"><span data-stu-id="36ae4-111">*Type*</span></span> | <span data-ttu-id="36ae4-112">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="36ae4-112">Optional.</span></span> <span data-ttu-id="36ae4-113">Per utilizzare questo parametro, è possibile utilizzare uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="36ae4-113">To use this parameter you can use any of the following values.</span></span> <span data-ttu-id="36ae4-114">È anche possibile specificare più tipi separandoli con virgole.</span><span class="sxs-lookup"><span data-stu-id="36ae4-114">You can also specify multiple types by separating them with commas.</span></span> <br/> <span data-ttu-id="36ae4-115">"**Get**"</span><span class="sxs-lookup"><span data-stu-id="36ae4-115">"**Get**"</span></span> <br/> <span data-ttu-id="36ae4-116">Per arrestare tutte le richieste [**Get**](get-method.md) in coda.</span><span class="sxs-lookup"><span data-stu-id="36ae4-116">To stop all queued [**Get**](get-method.md) requests.</span></span><br/> <span data-ttu-id="36ae4-117">"**NonQueuedGet**"</span><span class="sxs-lookup"><span data-stu-id="36ae4-117">"**NonQueuedGet**"</span></span> <br/> <span data-ttu-id="36ae4-118">Per arrestare tutte le richieste [**Get**](get-method.md) non accodate (metodo **Get** con parametro **queue** impostato su **false**).</span><span class="sxs-lookup"><span data-stu-id="36ae4-118">To stop all non-queued [**Get**](get-method.md) requests (**Get** method with **Queue** parameter set to **False**).</span></span><br/> <span data-ttu-id="36ae4-119">"**Sposta**"</span><span class="sxs-lookup"><span data-stu-id="36ae4-119">"**Move**"</span></span> <br/> <span data-ttu-id="36ae4-120">Per arrestare tutte le richieste [**movete**](moveto-method.md) in coda.</span><span class="sxs-lookup"><span data-stu-id="36ae4-120">To stop all queued [**MoveTo**](moveto-method.md) requests.</span></span><br/> <span data-ttu-id="36ae4-121">"**Riproduci**"</span><span class="sxs-lookup"><span data-stu-id="36ae4-121">"**Play**"</span></span> <br/> <span data-ttu-id="36ae4-122">Per arrestare tutte le richieste di [**riproduzione**](play-method.md) in coda.</span><span class="sxs-lookup"><span data-stu-id="36ae4-122">To stop all queued [**Play**](play-method.md) requests.</span></span><br/> <span data-ttu-id="36ae4-123">"**Pronuncia**"</span><span class="sxs-lookup"><span data-stu-id="36ae4-123">"**Speak**"</span></span> <br/> <span data-ttu-id="36ae4-124">Per arrestare tutte le richieste [**Speak**](speak-method.md) in coda.</span><span class="sxs-lookup"><span data-stu-id="36ae4-124">To stop all queued [**Speak**](speak-method.md) requests.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="36ae4-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="36ae4-125">Remarks</span></span>

<span data-ttu-id="36ae4-126">Se non si imposta il parametro di **tipo** , il server interrompe tutte le animazioni per il carattere, incluse le richieste [**Get**](get-method.md) in coda e non accodate, e cancella la coda di animazioni.</span><span class="sxs-lookup"><span data-stu-id="36ae4-126">If you don't set the **Type** parameter, the server stops all animations for the character, including queued and non-queued [**Get**](get-method.md) requests, and clears its animation queue.</span></span> <span data-ttu-id="36ae4-127">Interrompe inoltre la riproduzione dell'animazione di un carattere o di una visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="36ae4-127">It also stops playing a character's Hiding or Showing animation.</span></span>

<span data-ttu-id="36ae4-128">Questo metodo non genererà un oggetto [**Request**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="36ae4-128">This method will not generate a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>

## <a name="see-also"></a><span data-ttu-id="36ae4-129">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="36ae4-129">See Also</span></span>

[<span data-ttu-id="36ae4-130">**Metodo Stop**</span><span class="sxs-lookup"><span data-stu-id="36ae4-130">**Stop method**</span></span>](stop-method.md)


 

