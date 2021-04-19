---
description: Le \_ costanti del flag di bit LINEANSWERMODE descrivono in che modo una chiamata attiva esistente su un dispositivo linea è interessata dalla risposta di un'altra chiamata all'offerta sulla stessa riga.
ms.assetid: 35f63d92-970f-4fb8-aba9-179fc7de70f4
title: Costanti LINEANSWERMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 658d5b1265d28f8cb719719e4303fde97d3fff3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332906"
---
# <a name="lineanswermode_-constants"></a><span data-ttu-id="75270-103">\_Costanti LINEANSWERMODE</span><span class="sxs-lookup"><span data-stu-id="75270-103">LINEANSWERMODE\_ Constants</span></span>

<span data-ttu-id="75270-104">Le costanti del flag di bit **LINEANSWERMODE \_** descrivono in che modo una chiamata attiva esistente su un dispositivo linea è interessata dalla risposta di un'altra chiamata all' *offerta* sulla stessa riga.</span><span class="sxs-lookup"><span data-stu-id="75270-104">The **LINEANSWERMODE\_** bit-flag constants describe how an existing active call on a line device is affected by answering another *offering* call on the same line.</span></span>

<dl> <dt>

<span data-ttu-id="75270-105"><span id="LINEANSWERMODE_DROP"></span><span id="lineanswermode_drop"></span>**LINEANSWERMODE \_ Drop**</span><span class="sxs-lookup"><span data-stu-id="75270-105"><span id="LINEANSWERMODE_DROP"></span><span id="lineanswermode_drop"></span>**LINEANSWERMODE\_DROP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="75270-106">La chiamata attualmente attiva verrà eliminata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="75270-106">The currently active call will automatically be dropped.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="75270-107"><span id="LINEANSWERMODE_HOLD"></span><span id="lineanswermode_hold"></span>**LINEANSWERMODE in \_ attesa**</span><span class="sxs-lookup"><span data-stu-id="75270-107"><span id="LINEANSWERMODE_HOLD"></span><span id="lineanswermode_hold"></span>**LINEANSWERMODE\_HOLD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="75270-108">La chiamata attualmente attiva verrà automaticamente messa in attesa.</span><span class="sxs-lookup"><span data-stu-id="75270-108">The currently active call will automatically be placed on hold.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="75270-109"><span id="LINEANSWERMODE_NONE"></span><span id="lineanswermode_none"></span>**LINEANSWERMODE \_ None**</span><span class="sxs-lookup"><span data-stu-id="75270-109"><span id="LINEANSWERMODE_NONE"></span><span id="lineanswermode_none"></span>**LINEANSWERMODE\_NONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="75270-110">La risposta a un'altra chiamata sulla stessa riga non ha alcun effetto sulla chiamata attiva esistente sulla riga.</span><span class="sxs-lookup"><span data-stu-id="75270-110">Answering another call on the same line has no effect on the existing active call on the line.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="75270-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="75270-111">Remarks</span></span>

<span data-ttu-id="75270-112">Nessuna estensibilità.</span><span class="sxs-lookup"><span data-stu-id="75270-112">No extensibility.</span></span> <span data-ttu-id="75270-113">Tutti i 32 bit sono riservati.</span><span class="sxs-lookup"><span data-stu-id="75270-113">All 32 bits are reserved.</span></span>

<span data-ttu-id="75270-114">Se una chiamata viene offerta (disponibile) quando un'altra chiamata è già attiva, la nuova chiamata viene connessa a richiamando [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer).</span><span class="sxs-lookup"><span data-stu-id="75270-114">If a call comes in (is offered) at the time another call is already active, the new call is connected to by invoking [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer).</span></span> <span data-ttu-id="75270-115">L'effetto presente sulla chiamata attiva esistente dipende dalle funzionalità del dispositivo della linea.</span><span class="sxs-lookup"><span data-stu-id="75270-115">The effect this has on the existing active call depends on the line's device capabilities.</span></span> <span data-ttu-id="75270-116">La prima chiamata potrebbe non essere interessata, è possibile che venga eliminata automaticamente o che venga automaticamente messa in attesa.</span><span class="sxs-lookup"><span data-stu-id="75270-116">The first call may be unaffected, it may automatically be dropped, or it may automatically be placed on hold.</span></span>

## <a name="requirements"></a><span data-ttu-id="75270-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="75270-117">Requirements</span></span>



| <span data-ttu-id="75270-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="75270-118">Requirement</span></span> | <span data-ttu-id="75270-119">Valore</span><span class="sxs-lookup"><span data-stu-id="75270-119">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="75270-120">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="75270-120">TAPI version</span></span><br/> | <span data-ttu-id="75270-121">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="75270-121">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="75270-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="75270-122">Header</span></span><br/>       | <dl> <span data-ttu-id="75270-123"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="75270-123"><dt>Tapi.h</dt></span></span> </dl> |



 

 




