---
description: Le \_ costanti del flag di bit PHONESTATUSFLAGS descrivono una serie di informazioni sullo stato dei dispositivi telefonici.
ms.assetid: e94da591-49ab-4932-8621-0a62b8a55dd6
title: Costanti PHONESTATUSFLAGS_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 969c2553274037797bdf9abea3e8bdbc1cd8d018
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326144"
---
# <a name="phonestatusflags_-constants"></a><span data-ttu-id="fbaa0-103">\_Costanti PHONESTATUSFLAGS</span><span class="sxs-lookup"><span data-stu-id="fbaa0-103">PHONESTATUSFLAGS\_ Constants</span></span>

<span data-ttu-id="fbaa0-104">Le costanti del flag di bit **PHONESTATUSFLAGS \_** descrivono una serie di informazioni sullo stato dei dispositivi telefonici.</span><span class="sxs-lookup"><span data-stu-id="fbaa0-104">The **PHONESTATUSFLAGS\_** bit-flag constants describe a variety of phone device status information.</span></span>

<dl> <dt>

<span data-ttu-id="fbaa0-105"><span id="PHONESTATUSFLAGS_CONNECTED"></span><span id="phonestatusflags_connected"></span>**PHONESTATUSFLAGS \_ connesso**</span><span class="sxs-lookup"><span data-stu-id="fbaa0-105"><span id="PHONESTATUSFLAGS_CONNECTED"></span><span id="phonestatusflags_connected"></span>**PHONESTATUSFLAGS\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fbaa0-106">Specifica se il telefono è attualmente connesso a TAPI.</span><span class="sxs-lookup"><span data-stu-id="fbaa0-106">Specifies whether the phone is currently connected to TAPI.</span></span> <span data-ttu-id="fbaa0-107">**True** se connesso; in caso contrario, **false** .</span><span class="sxs-lookup"><span data-stu-id="fbaa0-107">**TRUE** if connected, **FALSE** otherwise.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fbaa0-108"><span id="PHONESTATUSFLAGS_SUSPENDED"></span><span id="phonestatusflags_suspended"></span>**PHONESTATUSFLAGS \_ sospeso**</span><span class="sxs-lookup"><span data-stu-id="fbaa0-108"><span id="PHONESTATUSFLAGS_SUSPENDED"></span><span id="phonestatusflags_suspended"></span>**PHONESTATUSFLAGS\_SUSPENDED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fbaa0-109">Specifica se la manipolazione di TAPI del dispositivo telefonico viene sospesa.</span><span class="sxs-lookup"><span data-stu-id="fbaa0-109">Specifies whether TAPI's manipulation of the phone device is suspended.</span></span> <span data-ttu-id="fbaa0-110">**True** se sospeso; in caso contrario, **false** .</span><span class="sxs-lookup"><span data-stu-id="fbaa0-110">**TRUE** if suspended, **FALSE** otherwise.</span></span> <span data-ttu-id="fbaa0-111">L'uso di un dispositivo telefonico da parte di un'applicazione può essere sospeso temporaneamente quando il Commuter vuole modificare il telefono in modo che non possa tollerare interferenze dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fbaa0-111">An application's use of a phone device can be temporarily suspended when the switch wants to manipulate the phone in a way that cannot tolerate interference from the application.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fbaa0-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="fbaa0-112">Remarks</span></span>

<span data-ttu-id="fbaa0-113">Nessuna estensibilità.</span><span class="sxs-lookup"><span data-stu-id="fbaa0-113">No extensibility.</span></span> <span data-ttu-id="fbaa0-114">Tutti i 32 bit sono riservati.</span><span class="sxs-lookup"><span data-stu-id="fbaa0-114">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbaa0-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fbaa0-115">Requirements</span></span>



| <span data-ttu-id="fbaa0-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbaa0-116">Requirement</span></span> | <span data-ttu-id="fbaa0-117">Valore</span><span class="sxs-lookup"><span data-stu-id="fbaa0-117">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="fbaa0-118">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="fbaa0-118">TAPI version</span></span><br/> | <span data-ttu-id="fbaa0-119">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="fbaa0-119">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="fbaa0-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fbaa0-120">Header</span></span><br/>       | <dl> <span data-ttu-id="fbaa0-121"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbaa0-121"><dt>Tapi.h</dt></span></span> </dl> |



 

 




