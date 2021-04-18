---
description: Il metodo FreeEventData libera lo spazio allocato per la struttura NMEVENTDATA.
ms.assetid: f86dcfd8-5a3b-4ce3-9d45-04545b030a89
title: 'Metodo IMonitorEventer:: FreeEventData (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer.FreeEventData
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: c71b7563e00bfceb220ce1c2bf109339267fbabf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305870"
---
# <a name="imonitoreventerfreeeventdata-method"></a><span data-ttu-id="3c14e-103">Metodo IMonitorEventer:: FreeEventData</span><span class="sxs-lookup"><span data-stu-id="3c14e-103">IMonitorEventer::FreeEventData method</span></span>

<span data-ttu-id="3c14e-104">Il metodo **FreeEventData** libera lo spazio allocato per la struttura [**NMEVENTDATA**](nmeventdata.md) .</span><span class="sxs-lookup"><span data-stu-id="3c14e-104">The **FreeEventData** method frees space allocated for the [**NMEVENTDATA**](nmeventdata.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c14e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3c14e-105">Syntax</span></span>


```C++
HRESULT FreeEventData(
  [in] PNMEVENTDATA pNMEventData
);
```



## <a name="parameters"></a><span data-ttu-id="3c14e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3c14e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c14e-107">*pNMEventData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3c14e-107">*pNMEventData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c14e-108">Indirizzo della struttura [**NMEVENTDATA**](nmeventdata.md) , la cui memoria viene liberata.</span><span class="sxs-lookup"><span data-stu-id="3c14e-108">Address of the [**NMEVENTDATA**](nmeventdata.md) structure, the memory of which is freed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c14e-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3c14e-109">Return value</span></span>

<span data-ttu-id="3c14e-110">Questo metodo restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3c14e-110">This method returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c14e-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="3c14e-111">Remarks</span></span>

<span data-ttu-id="3c14e-112">I monitoraggi chiamano questo metodo per liberare la memoria allocata per la struttura dei dati dell'evento.</span><span class="sxs-lookup"><span data-stu-id="3c14e-112">Monitors call this method to free the memory they allocate for the event data structure.</span></span> <span data-ttu-id="3c14e-113">Tenere presente che, mentre il monitoraggio dispone ancora di un puntatore alle stringhe in una struttura [**NMEVENTDATA**](nmeventdata.md) allocata, è necessario liberare la memoria per queste stringhe prima di chiamare il metodo **FreeEventData** .</span><span class="sxs-lookup"><span data-stu-id="3c14e-113">Be aware that while the monitor still has a pointer to strings in an allocated [**NMEVENTDATA**](nmeventdata.md) structure, the memory for these strings must be freed before the **FreeEventData** method is called.</span></span>

<span data-ttu-id="3c14e-114">Per ulteriori informazioni su come allocare memoria per una struttura [**NMEVENTDATA**](nmeventdata.md) , vedere [**IMonitorEventer:: GetEventData**](imonitoreventer-geteventdata.md).</span><span class="sxs-lookup"><span data-stu-id="3c14e-114">For more information about how to allocate memory for an [**NMEVENTDATA**](nmeventdata.md) structure, see [**IMonitorEventer::GetEventData**](imonitoreventer-geteventdata.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3c14e-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3c14e-115">Requirements</span></span>



| <span data-ttu-id="3c14e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c14e-116">Requirement</span></span> | <span data-ttu-id="3c14e-117">Valore</span><span class="sxs-lookup"><span data-stu-id="3c14e-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3c14e-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c14e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3c14e-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3c14e-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3c14e-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c14e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3c14e-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3c14e-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3c14e-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3c14e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c14e-123"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c14e-123"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c14e-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3c14e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c14e-125">**IMonitorEventer**</span><span class="sxs-lookup"><span data-stu-id="3c14e-125">**IMonitorEventer**</span></span>](imonitoreventer.md)
</dt> <dt>

[<span data-ttu-id="3c14e-126">**IMonitorEventer::GetEventData**</span><span class="sxs-lookup"><span data-stu-id="3c14e-126">**IMonitorEventer::GetEventData**</span></span>](imonitoreventer-geteventdata.md)
</dt> <dt>

[<span data-ttu-id="3c14e-127">**NMEVENTDATA**</span><span class="sxs-lookup"><span data-stu-id="3c14e-127">**NMEVENTDATA**</span></span>](nmeventdata.md)
</dt> </dl>

 

 




