---
title: Enumerazione ControlCloseStatus
description: Indica se l'applicazione che contiene il controllo può chiudere immediatamente il controllo.
ms.assetid: ac2e1c68-81b1-4b51-aa7e-0ff703e619a2
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto enumerazione ControlCloseStatus
topic_type:
- apiref
api_name:
- ControlCloseStatus
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6b94e0ce5cd040a2ade970f566897d2eac339dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963853"
---
# <a name="controlclosestatus-enumeration"></a><span data-ttu-id="33f21-104">Enumerazione ControlCloseStatus</span><span class="sxs-lookup"><span data-stu-id="33f21-104">ControlCloseStatus enumeration</span></span>

<span data-ttu-id="33f21-105">Indica se l'applicazione che contiene il controllo può chiudere immediatamente il controllo.</span><span class="sxs-lookup"><span data-stu-id="33f21-105">Indicates whether the application containing the control can close the control immediately.</span></span>

## <a name="syntax"></a><span data-ttu-id="33f21-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="33f21-106">Syntax</span></span>


```C++
enum ControlCloseStatus {
  controlCloseCanProceed     = 0x0000, 
  controlCloseWaitForEvents  = 0x0001 

};
```



## <a name="constants"></a><span data-ttu-id="33f21-107">Costanti</span><span class="sxs-lookup"><span data-stu-id="33f21-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="33f21-108"><span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>**controlCloseCanProceed**</span><span class="sxs-lookup"><span data-stu-id="33f21-108"><span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>**controlCloseCanProceed**</span></span>
</dt> <dd>

<span data-ttu-id="33f21-109">Il contenitore può procedere immediatamente con Close.</span><span class="sxs-lookup"><span data-stu-id="33f21-109">Container can go ahead with close immediately.</span></span> <span data-ttu-id="33f21-110">Questo problema può verificarsi se il controllo non è connesso.</span><span class="sxs-lookup"><span data-stu-id="33f21-110">This can happen if the control is not connected.</span></span>

</dd> <dt>

<span data-ttu-id="33f21-111"><span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>**controlCloseWaitForEvents**</span><span class="sxs-lookup"><span data-stu-id="33f21-111"><span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>**controlCloseWaitForEvents**</span></span>
</dt> <dd>

<span data-ttu-id="33f21-112">Il contenitore deve attendere gli eventi [**IMsTscAxEvents:: disconnected**](imstscaxevents-ondisconnected.md) o [**IMsTscAxEvents:: OnConfirmClose**](imstscaxevents-onconfirmclose.md).</span><span class="sxs-lookup"><span data-stu-id="33f21-112">Container should wait for events [**IMsTscAxEvents::OnDisconnected**](imstscaxevents-ondisconnected.md) or [**IMsTscAxEvents::OnConfirmClose**](imstscaxevents-onconfirmclose.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="33f21-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="33f21-113">Requirements</span></span>



| <span data-ttu-id="33f21-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="33f21-114">Requirement</span></span> | <span data-ttu-id="33f21-115">Valore</span><span class="sxs-lookup"><span data-stu-id="33f21-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="33f21-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33f21-116">Minimum supported client</span></span><br/> | <span data-ttu-id="33f21-117">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="33f21-117">Windows 8.1</span></span><br/>                                                                 |
| <span data-ttu-id="33f21-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33f21-118">Minimum supported server</span></span><br/> | <span data-ttu-id="33f21-119">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="33f21-119">Windows Server 2012 R2</span></span><br/>                                                      |
| <span data-ttu-id="33f21-120">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="33f21-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="33f21-121"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33f21-121"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33f21-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="33f21-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33f21-123">**IMsRdpClient:: RequestClose**</span><span class="sxs-lookup"><span data-stu-id="33f21-123">**IMsRdpClient::RequestClose**</span></span>](imsrdpclient-requestclose.md)
</dt> <dt>

[<span data-ttu-id="33f21-124">**IMsTscAxEvents::OnConfirmClose**</span><span class="sxs-lookup"><span data-stu-id="33f21-124">**IMsTscAxEvents::OnConfirmClose**</span></span>](imstscaxevents-onconfirmclose.md)
</dt> <dt>

[<span data-ttu-id="33f21-125">**IMsTscAxEvents:: disconnected**</span><span class="sxs-lookup"><span data-stu-id="33f21-125">**IMsTscAxEvents::OnDisconnected**</span></span>](imstscaxevents-ondisconnected.md)
</dt> </dl>

 

 





