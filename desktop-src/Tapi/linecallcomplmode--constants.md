---
description: Le \_ costanti del flag di bit LINECALLCOMPLMODE descrivono i diversi modi in cui è possibile completare una chiamata.
ms.assetid: 68f755a1-586b-4c5b-b8e8-c8b40eb71685
title: Costanti LINECALLCOMPLMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 373a66b6ce13b7bfba00303bea824f542bf0016a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327307"
---
# <a name="linecallcomplmode_-constants"></a><span data-ttu-id="ee174-103">\_Costanti LINECALLCOMPLMODE</span><span class="sxs-lookup"><span data-stu-id="ee174-103">LINECALLCOMPLMODE\_ Constants</span></span>

<span data-ttu-id="ee174-104">Le costanti del flag di bit **LINECALLCOMPLMODE \_** descrivono i diversi modi in cui è possibile completare una chiamata.</span><span class="sxs-lookup"><span data-stu-id="ee174-104">The **LINECALLCOMPLMODE\_** bit-flag constants describe different ways in which a call can be completed.</span></span>

<dl> <dt>

<span data-ttu-id="ee174-105"><span id="LINECALLCOMPLMODE_CALLBACK"></span><span id="linecallcomplmode_callback"></span>**\_callback LINECALLCOMPLMODE**</span><span class="sxs-lookup"><span data-stu-id="ee174-105"><span id="LINECALLCOMPLMODE_CALLBACK"></span><span id="linecallcomplmode_callback"></span>**LINECALLCOMPLMODE\_CALLBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ee174-106">Richiede alla stazione chiamata di restituire la chiamata quando torna inattiva.</span><span class="sxs-lookup"><span data-stu-id="ee174-106">Requests the called station to return the call when it returns to idle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee174-107"><span id="LINECALLCOMPLMODE_CAMPON"></span><span id="linecallcomplmode_campon"></span>**\_campo LINECALLCOMPLMODE**</span><span class="sxs-lookup"><span data-stu-id="ee174-107"><span id="LINECALLCOMPLMODE_CAMPON"></span><span id="linecallcomplmode_campon"></span>**LINECALLCOMPLMODE\_CAMPON**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ee174-108">Accoda la chiamata fino a quando non è possibile completare la chiamata.</span><span class="sxs-lookup"><span data-stu-id="ee174-108">Queues the call until the call can be completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee174-109"><span id="LINECALLCOMPLMODE_INTRUDE"></span><span id="linecallcomplmode_intrude"></span>**LINECALLCOMPLMODE \_ intrusione**</span><span class="sxs-lookup"><span data-stu-id="ee174-109"><span id="LINECALLCOMPLMODE_INTRUDE"></span><span id="linecallcomplmode_intrude"></span>**LINECALLCOMPLMODE\_INTRUDE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ee174-110">Aggiunge l'applicazione alla chiamata esistente nella stazione chiamata (Barge in).</span><span class="sxs-lookup"><span data-stu-id="ee174-110">Adds the application to the existing call at the called station (barge in).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee174-111"><span id="LINECALLCOMPLMODE_MESSAGE"></span><span id="linecallcomplmode_message"></span>**\_messaggio LINECALLCOMPLMODE**</span><span class="sxs-lookup"><span data-stu-id="ee174-111"><span id="LINECALLCOMPLMODE_MESSAGE"></span><span id="linecallcomplmode_message"></span>**LINECALLCOMPLMODE\_MESSAGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ee174-112">Lascia un breve messaggio predefinito per la stazione chiamata (lasciare la chiamata a Word).</span><span class="sxs-lookup"><span data-stu-id="ee174-112">Leaves a short predefined message for the called station (Leave Word Calling).</span></span> <span data-ttu-id="ee174-113">Il messaggio da inviare viene specificato separatamente.</span><span class="sxs-lookup"><span data-stu-id="ee174-113">The message to be sent is specified separately.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ee174-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="ee174-114">Remarks</span></span>

<span data-ttu-id="ee174-115">Nessuna estensibilità.</span><span class="sxs-lookup"><span data-stu-id="ee174-115">No extensibility.</span></span> <span data-ttu-id="ee174-116">Tutti i 32 bit sono riservati.</span><span class="sxs-lookup"><span data-stu-id="ee174-116">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee174-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ee174-117">Requirements</span></span>



| <span data-ttu-id="ee174-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee174-118">Requirement</span></span> | <span data-ttu-id="ee174-119">Valore</span><span class="sxs-lookup"><span data-stu-id="ee174-119">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ee174-120">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="ee174-120">TAPI version</span></span><br/> | <span data-ttu-id="ee174-121">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="ee174-121">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="ee174-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ee174-122">Header</span></span><br/>       | <dl> <span data-ttu-id="ee174-123"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee174-123"><dt>Tapi.h</dt></span></span> </dl> |



 

 




