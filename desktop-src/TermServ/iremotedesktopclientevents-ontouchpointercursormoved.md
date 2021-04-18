---
title: Metodo IRemoteDesktopClientEvents OnTouchPointerCursorMoved
description: Chiamato quando il cursore del puntatore tocco è stato spostato e la proprietà EventsEnabled è impostata su true.
ms.assetid: 55A6AC99-0723-4215-9428-D2DAAC77A74A
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo OnTouchPointerCursorMoved
- Metodo OnTouchPointerCursorMoved Servizi Desktop remoto, interfaccia IRemoteDesktopClientEvents
- Interfaccia IRemoteDesktopClientEvents Servizi Desktop remoto, metodo OnTouchPointerCursorMoved
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnTouchPointerCursorMoved
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae347e19942bf0c82112e5cec6a3fb4fe131349f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301624"
---
# <a name="iremotedesktopclienteventsontouchpointercursormoved-method"></a><span data-ttu-id="41826-106">Metodo IRemoteDesktopClientEvents:: OnTouchPointerCursorMoved</span><span class="sxs-lookup"><span data-stu-id="41826-106">IRemoteDesktopClientEvents::OnTouchPointerCursorMoved method</span></span>

<span data-ttu-id="41826-107">Chiamato quando il cursore del puntatore tocco è stato spostato e la proprietà [**EventsEnabled**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) è impostata su true.</span><span class="sxs-lookup"><span data-stu-id="41826-107">Called when the touch pointer cursor has moved and the [**EventsEnabled**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) property is set to true.</span></span>

## <a name="syntax"></a><span data-ttu-id="41826-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="41826-108">Syntax</span></span>


```C++
void OnTouchPointerCursorMoved(
  [in] long x,
  [in] long y
);
```



## <a name="parameters"></a><span data-ttu-id="41826-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="41826-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41826-110">*x* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41826-110">*x* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="41826-111">*y* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41826-111">*y* \[in\]</span></span>
<span data-ttu-id="41826-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="41826-112"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="41826-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="41826-113">Return value</span></span>

<span data-ttu-id="41826-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="41826-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="41826-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="41826-115">Requirements</span></span>



| <span data-ttu-id="41826-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="41826-116">Requirement</span></span> | <span data-ttu-id="41826-117">Valore</span><span class="sxs-lookup"><span data-stu-id="41826-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41826-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41826-118">Minimum supported client</span></span><br/> | <span data-ttu-id="41826-119">Windows 8</span><span class="sxs-lookup"><span data-stu-id="41826-119">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="41826-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41826-120">Minimum supported server</span></span><br/> | <span data-ttu-id="41826-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="41826-121">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="41826-122">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="41826-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="41826-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41826-123"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="41826-124">DLL</span><span class="sxs-lookup"><span data-stu-id="41826-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41826-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41826-125"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="41826-126">IID</span><span class="sxs-lookup"><span data-stu-id="41826-126">IID</span></span><br/>                      | <span data-ttu-id="41826-127">DIID \_ IRemoteDesktopClientEvents è definito come 079863B7-6D47-4105-8BFE-0CDCB360E67D</span><span class="sxs-lookup"><span data-stu-id="41826-127">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="41826-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="41826-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41826-129">**IRemoteDesktopClientEvents**</span><span class="sxs-lookup"><span data-stu-id="41826-129">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

