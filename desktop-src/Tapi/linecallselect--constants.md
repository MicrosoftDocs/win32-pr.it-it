---
description: Le \_ costanti del flag di bit LINECALLSELECT descrivono quali chiamate devono essere selezionate.
ms.assetid: f19a41bc-403a-4d4b-ab85-240a73514ebb
title: Costanti LINECALLSELECT_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8330b4c4e4e14ac399595d10d4a208a3c67f5b2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332894"
---
# <a name="linecallselect_-constants"></a><span data-ttu-id="f8d10-103">\_Costanti LINECALLSELECT</span><span class="sxs-lookup"><span data-stu-id="f8d10-103">LINECALLSELECT\_ Constants</span></span>

<span data-ttu-id="f8d10-104">Le costanti del flag di bit **LINECALLSELECT \_** descrivono quali chiamate devono essere selezionate.</span><span class="sxs-lookup"><span data-stu-id="f8d10-104">The **LINECALLSELECT\_** bit-flag constants describe which calls are to be selected.</span></span>

<dl> <dt>

<span data-ttu-id="f8d10-105"><span id="LINECALLSELECT_ADDRESS"></span><span id="linecallselect_address"></span>**\_Indirizzo LINECALLSELECT**</span><span class="sxs-lookup"><span data-stu-id="f8d10-105"><span id="LINECALLSELECT_ADDRESS"></span><span id="linecallselect_address"></span>**LINECALLSELECT\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f8d10-106">Seleziona la chiamata sull'indirizzo specificato.</span><span class="sxs-lookup"><span data-stu-id="f8d10-106">Selects call on the specified address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8d10-107"><span id="LINECALLSELECT_CALL"></span><span id="linecallselect_call"></span>**\_chiamata LINECALLSELECT**</span><span class="sxs-lookup"><span data-stu-id="f8d10-107"><span id="LINECALLSELECT_CALL"></span><span id="linecallselect_call"></span>**LINECALLSELECT\_CALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f8d10-108">Seleziona le chiamate correlate alla chiamata specificata.</span><span class="sxs-lookup"><span data-stu-id="f8d10-108">Selects related calls to the specified call.</span></span> <span data-ttu-id="f8d10-109">Ad esempio, le entità in una chiamata di conferenza.</span><span class="sxs-lookup"><span data-stu-id="f8d10-109">For example, the parties in a conference call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8d10-110"><span id="LINECALLSELECT_CALLID"></span><span id="linecallselect_callid"></span>**\_CALLID LINECALLSELECT**</span><span class="sxs-lookup"><span data-stu-id="f8d10-110"><span id="LINECALLSELECT_CALLID"></span><span id="linecallselect_callid"></span>**LINECALLSELECT\_CALLID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f8d10-111">Seleziona le chiamate correlate all'identificatore di chiamata specificato.</span><span class="sxs-lookup"><span data-stu-id="f8d10-111">Selects related calls to the specified call identifier.</span></span> <span data-ttu-id="f8d10-112">Questo flag viene esposto solo alle applicazioni che negoziano una versione di TAPI 3,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="f8d10-112">This flag is exposed only to applications that negotiate a TAPI version of 3.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8d10-113"><span id="LINECALLSELECT_DEVICEID"></span><span id="linecallselect_deviceid"></span>**\_DEVICEID LINECALLSELECT**</span><span class="sxs-lookup"><span data-stu-id="f8d10-113"><span id="LINECALLSELECT_DEVICEID"></span><span id="linecallselect_deviceid"></span>**LINECALLSELECT\_DEVICEID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f8d10-114">Seleziona le chiamate sull'identificatore di dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="f8d10-114">Selects calls on the specified device identifier.</span></span> <span data-ttu-id="f8d10-115">Questo flag viene esposto solo alle applicazioni che negoziano una versione di TAPI 2,1 o successiva.</span><span class="sxs-lookup"><span data-stu-id="f8d10-115">This flag is exposed only to applications that negotiate a TAPI version of 2.1 or higher.</span></span> <span data-ttu-id="f8d10-116">Le applicazioni devono prendere in considerazione l'uso della \_ costante della riga LINECALLSELECT invece di questa.</span><span class="sxs-lookup"><span data-stu-id="f8d10-116">Applications should consider using the LINECALLSELECT\_LINE constant instead of this one.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f8d10-117"><span id="LINECALLSELECT_LINE"></span><span id="linecallselect_line"></span>**\_linea LINECALLSELECT**</span><span class="sxs-lookup"><span data-stu-id="f8d10-117"><span id="LINECALLSELECT_LINE"></span><span id="linecallselect_line"></span>**LINECALLSELECT\_LINE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f8d10-118">Seleziona le chiamate sul dispositivo a linee specificato.</span><span class="sxs-lookup"><span data-stu-id="f8d10-118">Selects calls on the specified line device.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f8d10-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="f8d10-119">Remarks</span></span>

<span data-ttu-id="f8d10-120">Nessuna estensibilità.</span><span class="sxs-lookup"><span data-stu-id="f8d10-120">No extensibility.</span></span> <span data-ttu-id="f8d10-121">Tutti i 32 bit sono riservati.</span><span class="sxs-lookup"><span data-stu-id="f8d10-121">All 32 bits are reserved.</span></span>

<span data-ttu-id="f8d10-122">Questa costante viene utilizzata in [**lineGetNewCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls) e per specificare una selezione (ambito) delle chiamate richieste.</span><span class="sxs-lookup"><span data-stu-id="f8d10-122">This constant is used in [**lineGetNewCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls) and to specify a selection (scope) of the calls that are requested.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8d10-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f8d10-123">Requirements</span></span>



| <span data-ttu-id="f8d10-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8d10-124">Requirement</span></span> | <span data-ttu-id="f8d10-125">Valore</span><span class="sxs-lookup"><span data-stu-id="f8d10-125">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f8d10-126">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="f8d10-126">TAPI version</span></span><br/> | <span data-ttu-id="f8d10-127">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="f8d10-127">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="f8d10-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f8d10-128">Header</span></span><br/>       | <dl> <span data-ttu-id="f8d10-129"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8d10-129"><dt>Tapi.h</dt></span></span> </dl> |



 

 




