---
title: Metodo IRemoteDesktopClientEvents OnRemoteDesktopSizeChanged
description: Chiamato quando viene modificata la dimensione del desktop remoto.
ms.assetid: DA641CA7-3214-4DB6-9A7F-75903FE93DB4
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo OnRemoteDesktopSizeChanged
- Metodo OnRemoteDesktopSizeChanged Servizi Desktop remoto, interfaccia IRemoteDesktopClientEvents
- Interfaccia IRemoteDesktopClientEvents Servizi Desktop remoto, metodo OnRemoteDesktopSizeChanged
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnRemoteDesktopSizeChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a7431d1a6f41a6f87bb34fe1486c203168f2c3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741319"
---
# <a name="iremotedesktopclienteventsonremotedesktopsizechanged-method"></a><span data-ttu-id="c2ab8-106">Metodo IRemoteDesktopClientEvents:: OnRemoteDesktopSizeChanged</span><span class="sxs-lookup"><span data-stu-id="c2ab8-106">IRemoteDesktopClientEvents::OnRemoteDesktopSizeChanged method</span></span>

<span data-ttu-id="c2ab8-107">Chiamato quando viene modificata la dimensione del desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="c2ab8-107">Called when the remote desktop size has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2ab8-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c2ab8-108">Syntax</span></span>


```C++
void OnRemoteDesktopSizeChanged(
  [in] long width,
  [in] long height
);
```



## <a name="parameters"></a><span data-ttu-id="c2ab8-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c2ab8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2ab8-110">*larghezza* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c2ab8-110">*width* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="c2ab8-111">*altezza* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c2ab8-111">*height* \[in\]</span></span>
<span data-ttu-id="c2ab8-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="c2ab8-112"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="c2ab8-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c2ab8-113">Return value</span></span>

<span data-ttu-id="c2ab8-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="c2ab8-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2ab8-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c2ab8-115">Requirements</span></span>



| <span data-ttu-id="c2ab8-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2ab8-116">Requirement</span></span> | <span data-ttu-id="c2ab8-117">Valore</span><span class="sxs-lookup"><span data-stu-id="c2ab8-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2ab8-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c2ab8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c2ab8-119">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c2ab8-119">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="c2ab8-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c2ab8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c2ab8-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c2ab8-121">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="c2ab8-122">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="c2ab8-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="c2ab8-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2ab8-123"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="c2ab8-124">DLL</span><span class="sxs-lookup"><span data-stu-id="c2ab8-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2ab8-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2ab8-125"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="c2ab8-126">IID</span><span class="sxs-lookup"><span data-stu-id="c2ab8-126">IID</span></span><br/>                      | <span data-ttu-id="c2ab8-127">DIID \_ IRemoteDesktopClientEvents è definito come 079863B7-6D47-4105-8BFE-0CDCB360E67D</span><span class="sxs-lookup"><span data-stu-id="c2ab8-127">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c2ab8-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c2ab8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2ab8-129">**IRemoteDesktopClientEvents**</span><span class="sxs-lookup"><span data-stu-id="c2ab8-129">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

 





