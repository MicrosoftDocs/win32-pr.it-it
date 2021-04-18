---
description: Le \_ costanti del flag di bit LINECALLHUBTRACKING descrivono il tipo di rilevamento dell'hub di chiamata fornito.
ms.assetid: ad3c8d2e-f074-4db0-bb72-fb2181cbf687
title: Costanti LINECALLHUBTRACKING_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bfae61e36551a7d186408c2c87e0727503540a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327882"
---
# <a name="linecallhubtracking_-constants"></a><span data-ttu-id="25538-103">\_Costanti LINECALLHUBTRACKING</span><span class="sxs-lookup"><span data-stu-id="25538-103">LINECALLHUBTRACKING\_ Constants</span></span>

<span data-ttu-id="25538-104">Le costanti del flag di bit **LINECALLHUBTRACKING \_** descrivono il tipo di rilevamento dell'hub di chiamata fornito.</span><span class="sxs-lookup"><span data-stu-id="25538-104">The **LINECALLHUBTRACKING\_** bit-flag constants describe the type of call hub tracking provided.</span></span>

<dl> <dt>

<span data-ttu-id="25538-105"><span id="LINECALLHUBTRACKING_ALLCALLS"></span><span id="linecallhubtracking_allcalls"></span>**\_ALLCALLS LINECALLHUBTRACKING**</span><span class="sxs-lookup"><span data-stu-id="25538-105"><span id="LINECALLHUBTRACKING_ALLCALLS"></span><span id="linecallhubtracking_allcalls"></span>**LINECALLHUBTRACKING\_ALLCALLS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="25538-106">Il rilevamento dell'hub chiamate viene fornito a livello di chiamata.</span><span class="sxs-lookup"><span data-stu-id="25538-106">Call hub tracking is provided at the call level.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="25538-107"><span id="LINECALLHUBTRACKING_NONE"></span><span id="linecallhubtracking_none"></span>**LINECALLHUBTRACKING \_ None**</span><span class="sxs-lookup"><span data-stu-id="25538-107"><span id="LINECALLHUBTRACKING_NONE"></span><span id="linecallhubtracking_none"></span>**LINECALLHUBTRACKING\_NONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="25538-108">Nessun rilevamento dell'hub di chiamata specificato.</span><span class="sxs-lookup"><span data-stu-id="25538-108">No call hub tracking is provided.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="25538-109"><span id="LINECALLHUBTRACKING_PROVIDERLEVEL"></span><span id="linecallhubtracking_providerlevel"></span>**\_PROVIDERLEVEL LINECALLHUBTRACKING**</span><span class="sxs-lookup"><span data-stu-id="25538-109"><span id="LINECALLHUBTRACKING_PROVIDERLEVEL"></span><span id="linecallhubtracking_providerlevel"></span>**LINECALLHUBTRACKING\_PROVIDERLEVEL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="25538-110">Gli hub di chiamata vengono rilevati a livello del provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="25538-110">Call hubs are tracked at the service provider level.</span></span> <span data-ttu-id="25538-111">Le modifiche della chiamata da una chiamata non vengono segnalate.</span><span class="sxs-lookup"><span data-stu-id="25538-111">Call by call changes are not reported.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="25538-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="25538-112">Remarks</span></span>

<span data-ttu-id="25538-113">Nessuna estensibilità.</span><span class="sxs-lookup"><span data-stu-id="25538-113">No extensibility.</span></span> <span data-ttu-id="25538-114">Tutti i 32 bit sono riservati.</span><span class="sxs-lookup"><span data-stu-id="25538-114">All 32 bits are reserved.</span></span>

<span data-ttu-id="25538-115">Quando si verificano modifiche in questa struttura di dati, all'applicazione viene inviato un messaggio di [**riga \_ CALLINFO**](line-callinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="25538-115">When changes occur in this data structure, a [**LINE\_CALLINFO**](line-callinfo.md) message is sent to the application.</span></span> <span data-ttu-id="25538-116">I parametri di questo messaggio sono un handle per la chiamata e un'indicazione dell'elemento informazioni che è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="25538-116">The parameters to this message are a handle to the call and an indication of the information item that has changed.</span></span> <span data-ttu-id="25538-117">La struttura dei dati [**LINECALLHUBTRACKINGINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallhubtrackinginfo) indica il tipo di rilevamento fornito.</span><span class="sxs-lookup"><span data-stu-id="25538-117">The [**LINECALLHUBTRACKINGINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallhubtrackinginfo) data structure indicates which tracking type is provided.</span></span>

## <a name="requirements"></a><span data-ttu-id="25538-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="25538-118">Requirements</span></span>



| <span data-ttu-id="25538-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="25538-119">Requirement</span></span> | <span data-ttu-id="25538-120">Valore</span><span class="sxs-lookup"><span data-stu-id="25538-120">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="25538-121">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="25538-121">TAPI version</span></span><br/> | <span data-ttu-id="25538-122">Richiede TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="25538-122">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="25538-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="25538-123">Header</span></span><br/>       | <dl> <span data-ttu-id="25538-124"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="25538-124"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25538-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="25538-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25538-126">**LINEA \_ CALLINFO**</span><span class="sxs-lookup"><span data-stu-id="25538-126">**LINE\_CALLINFO**</span></span>](line-callinfo.md)
</dt> <dt>

[<span data-ttu-id="25538-127">**LINECALLHUBTRACKINGINFO**</span><span class="sxs-lookup"><span data-stu-id="25538-127">**LINECALLHUBTRACKINGINFO**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallhubtrackinginfo)
</dt> <dt>

[<span data-ttu-id="25538-128">**LINECALLINFO**</span><span class="sxs-lookup"><span data-stu-id="25538-128">**LINECALLINFO**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)
</dt> </dl>

 

 




