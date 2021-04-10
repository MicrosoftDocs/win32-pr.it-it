---
title: Metodo IMsTscAxEvents OnMouseInputModeChanged
description: Chiamato quando viene modificata la modalità di input del mouse.
ms.assetid: d0554c59-967d-4181-98cd-9e88dde32752
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo OnMouseInputModeChanged
- Metodo OnMouseInputModeChanged Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto, metodo OnMouseInputModeChanged
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnMouseInputModeChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dbfef19aa79ba634a13d92b8d11866b8016e893
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120198"
---
# <a name="imstscaxeventsonmouseinputmodechanged-method"></a><span data-ttu-id="f849c-106">Metodo IMsTscAxEvents:: OnMouseInputModeChanged</span><span class="sxs-lookup"><span data-stu-id="f849c-106">IMsTscAxEvents::OnMouseInputModeChanged method</span></span>

<span data-ttu-id="f849c-107">Chiamato quando viene modificata la modalità di input del mouse.</span><span class="sxs-lookup"><span data-stu-id="f849c-107">Called when the mouse input mode has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="f849c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f849c-108">Syntax</span></span>


```C++
void OnMouseInputModeChanged(
  [in] VARIANT_BOOL fMouseModeRelative
);
```



## <a name="parameters"></a><span data-ttu-id="f849c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f849c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f849c-110">*fMouseModeRelative* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f849c-110">*fMouseModeRelative* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f849c-111">Indica se il mouse è in modalità relativa.</span><span class="sxs-lookup"><span data-stu-id="f849c-111">Indicates whether the mouse is in relative mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f849c-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f849c-112">Return value</span></span>

<span data-ttu-id="f849c-113">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="f849c-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f849c-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="f849c-114">Remarks</span></span>

<span data-ttu-id="f849c-115">Implementare questo metodo nel sink di evento per ricevere una notifica che la modalità di input del mouse è cambiata.</span><span class="sxs-lookup"><span data-stu-id="f849c-115">Implement this method in your event sink to receive notification that the mouse input mode has changed.</span></span>

## <a name="requirements"></a><span data-ttu-id="f849c-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f849c-116">Requirements</span></span>



| <span data-ttu-id="f849c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f849c-117">Requirement</span></span> | <span data-ttu-id="f849c-118">Valore</span><span class="sxs-lookup"><span data-stu-id="f849c-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f849c-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f849c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f849c-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f849c-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f849c-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f849c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f849c-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f849c-122">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f849c-123">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="f849c-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="f849c-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f849c-124"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f849c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f849c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f849c-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f849c-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f849c-127">IID</span><span class="sxs-lookup"><span data-stu-id="f849c-127">IID</span></span><br/>                      | <span data-ttu-id="f849c-128">IMsTscAxEvents è definito come 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="f849c-128">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="f849c-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f849c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f849c-130">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="f849c-130">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





