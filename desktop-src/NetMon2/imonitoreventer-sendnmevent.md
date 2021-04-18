---
description: Il metodo SendNMEvent invia eventi a Strumentazione gestione Windows (WMI).
ms.assetid: 85c33a71-72aa-4b0a-8e8b-3a220a080bb2
title: 'Metodo IMonitorEventer:: SendNMEvent (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer.SendNMEvent
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 3286fca4d5b852d4562c13446699c1a6b40f3efe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308659"
---
# <a name="imonitoreventersendnmevent-method"></a><span data-ttu-id="74d29-103">Metodo IMonitorEventer:: SendNMEvent</span><span class="sxs-lookup"><span data-stu-id="74d29-103">IMonitorEventer::SendNMEvent method</span></span>

<span data-ttu-id="74d29-104">Il metodo **SendNMEvent** invia eventi a Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="74d29-104">The **SendNMEvent** method submits events to Windows Management Instrumentation (WMI).</span></span>

## <a name="syntax"></a><span data-ttu-id="74d29-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="74d29-105">Syntax</span></span>


```C++
HRESULT SendNMEvent(
  [in] PNMEVENTDATA pNMEventData
);
```



## <a name="parameters"></a><span data-ttu-id="74d29-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="74d29-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74d29-107">*pNMEventData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74d29-107">*pNMEventData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74d29-108">Puntatore all'evento inviato a WMI.</span><span class="sxs-lookup"><span data-stu-id="74d29-108">Pointer to the event submitted to WMI.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74d29-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="74d29-109">Return value</span></span>

<span data-ttu-id="74d29-110">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="74d29-110">If the method is successful, the return value is S\_OK.</span></span>

<span data-ttu-id="74d29-111">Se il metodo ha esito negativo, il valore restituito è NMERR \_ \_ \_ memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="74d29-111">If the method is unsuccessful, the return value is NMERR\_OUT\_OF\_MEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="74d29-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="74d29-112">Requirements</span></span>



| <span data-ttu-id="74d29-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="74d29-113">Requirement</span></span> | <span data-ttu-id="74d29-114">Valore</span><span class="sxs-lookup"><span data-stu-id="74d29-114">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="74d29-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="74d29-115">Minimum supported client</span></span><br/> | <span data-ttu-id="74d29-116">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="74d29-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="74d29-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="74d29-117">Minimum supported server</span></span><br/> | <span data-ttu-id="74d29-118">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="74d29-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="74d29-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="74d29-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="74d29-120"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="74d29-120"><dt>Netmon.h</dt></span></span> </dl> |



 

 




