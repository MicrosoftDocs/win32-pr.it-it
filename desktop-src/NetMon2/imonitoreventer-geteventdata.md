---
description: Il metodo GetEventData alloca spazio per le strutture NMEVENTDATA e NMCOLUMNINFO.
ms.assetid: b24a2a30-4543-4311-87ec-66872463aed7
title: 'Metodo IMonitorEventer:: GetEventData (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer.GetEventData
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: be1654c38f51fa62909e10c12900c087bf0842fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226026"
---
# <a name="imonitoreventergeteventdata-method"></a><span data-ttu-id="1c306-103">Metodo IMonitorEventer:: GetEventData</span><span class="sxs-lookup"><span data-stu-id="1c306-103">IMonitorEventer::GetEventData method</span></span>

<span data-ttu-id="1c306-104">Il metodo **GetEventData** alloca spazio per le strutture [NMEVENTDATA](nmeventdata.md) e [NMCOLUMNINFO](nmcolumninfo.md) .</span><span class="sxs-lookup"><span data-stu-id="1c306-104">The **GetEventData** method allocates space for the [NMEVENTDATA](nmeventdata.md) and [NMCOLUMNINFO](nmcolumninfo.md) structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c306-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1c306-105">Syntax</span></span>


```C++
HRESULT GetEventData(
  [in]  BYTE         bNumColumns,
  [out] PNMEVENTDATA *ppNMEventData
);
```



## <a name="parameters"></a><span data-ttu-id="1c306-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1c306-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c306-107">*bNumColumns* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1c306-107">*bNumColumns* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c306-108">Numero di strutture **NMCOLUMNINFO** necessarie.</span><span class="sxs-lookup"><span data-stu-id="1c306-108">Number of **NMCOLUMNINFO** structures needed.</span></span>

</dd> <dt>

<span data-ttu-id="1c306-109">*ppNMEventData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1c306-109">*ppNMEventData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1c306-110">Indirizzo della struttura **NMEVENTDATA** restituita.</span><span class="sxs-lookup"><span data-stu-id="1c306-110">Address of the **NMEVENTDATA** structure that is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c306-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1c306-111">Return value</span></span>

<span data-ttu-id="1c306-112">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1c306-112">If the method is successful, the return value is S\_OK.</span></span>

<span data-ttu-id="1c306-113">Se il metodo ha esito negativo, il valore restituito è NMERR \_ \_ \_ memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="1c306-113">If the method is unsuccessful, the return value is NMERR\_OUT\_OF\_MEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c306-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="1c306-114">Remarks</span></span>

<span data-ttu-id="1c306-115">I monitoraggi chiamano questo metodo per allocare memoria per le strutture di dati dell'evento e delle informazioni sulle colonne.</span><span class="sxs-lookup"><span data-stu-id="1c306-115">Monitors call this method to allocate memory for the event data and column information structures.</span></span> <span data-ttu-id="1c306-116">Per liberare la memoria allocata per una struttura **NMEVENTDATA** , vedere [IMonitorEventer:: FreeEventData](imonitoreventer-freeeventdata.md).</span><span class="sxs-lookup"><span data-stu-id="1c306-116">To free memory allocated for an **NMEVENTDATA** structure, see [IMonitorEventer::FreeEventData](imonitoreventer-freeeventdata.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1c306-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1c306-117">Requirements</span></span>



| <span data-ttu-id="1c306-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c306-118">Requirement</span></span> | <span data-ttu-id="1c306-119">Valore</span><span class="sxs-lookup"><span data-stu-id="1c306-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1c306-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c306-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1c306-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1c306-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="1c306-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c306-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1c306-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1c306-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="1c306-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1c306-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c306-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c306-125"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c306-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1c306-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c306-127">IMonitorEventer</span><span class="sxs-lookup"><span data-stu-id="1c306-127">IMonitorEventer</span></span>](imonitoreventer.md)
</dt> <dt>

[<span data-ttu-id="1c306-128">IMonitorEventer::FreeEventData</span><span class="sxs-lookup"><span data-stu-id="1c306-128">IMonitorEventer::FreeEventData</span></span>](imonitoreventer-freeeventdata.md)
</dt> <dt>

[<span data-ttu-id="1c306-129">NMEVENTDATA</span><span class="sxs-lookup"><span data-stu-id="1c306-129">NMEVENTDATA</span></span>](nmeventdata.md)
</dt> <dt>

[<span data-ttu-id="1c306-130">NMCOLUMNINFO</span><span class="sxs-lookup"><span data-stu-id="1c306-130">NMCOLUMNINFO</span></span>](nmcolumninfo.md)
</dt> </dl>

 

 




