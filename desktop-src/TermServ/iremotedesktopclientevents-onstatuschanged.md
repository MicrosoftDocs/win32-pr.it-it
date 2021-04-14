---
title: Metodo IRemoteDesktopClientEvents OnStatusChanged (LocationApi. h)
description: Chiamato quando il controllo client ha aggiornato il proprio stato.
ms.assetid: AAFBDC9E-C8B5-4924-AA69-82EF09996AF7
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo OnStatusChanged
- Metodo OnStatusChanged Servizi Desktop remoto, interfaccia IRemoteDesktopClientEvents
- Interfaccia IRemoteDesktopClientEvents Servizi Desktop remoto, metodo OnStatusChanged
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnStatusChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b17e42e75072033f952c7ef790365d6a363a5b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478880"
---
# <a name="iremotedesktopclienteventsonstatuschanged-method"></a><span data-ttu-id="6be7d-106">Metodo IRemoteDesktopClientEvents:: OnStatusChanged</span><span class="sxs-lookup"><span data-stu-id="6be7d-106">IRemoteDesktopClientEvents::OnStatusChanged method</span></span>

<span data-ttu-id="6be7d-107">Chiamato quando il controllo client ha aggiornato il proprio stato.</span><span class="sxs-lookup"><span data-stu-id="6be7d-107">Called when the client control has updated its status.</span></span>

## <a name="syntax"></a><span data-ttu-id="6be7d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6be7d-108">Syntax</span></span>


```C++
void OnStatusChanged(
   long statusCode,
   BSTR statusMessage
);
```



## <a name="parameters"></a><span data-ttu-id="6be7d-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="6be7d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6be7d-110">*statusCode*</span><span class="sxs-lookup"><span data-stu-id="6be7d-110">*statusCode*</span></span> 
</dt> <dd>

<span data-ttu-id="6be7d-111">Nuovo codice di stato.</span><span class="sxs-lookup"><span data-stu-id="6be7d-111">The new status code.</span></span>

</dd> <dt>

<span data-ttu-id="6be7d-112">*statusMessage*</span><span class="sxs-lookup"><span data-stu-id="6be7d-112">*statusMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="6be7d-113">Testo del messaggio di stato.</span><span class="sxs-lookup"><span data-stu-id="6be7d-113">The status message text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6be7d-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6be7d-114">Return value</span></span>

<span data-ttu-id="6be7d-115">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="6be7d-115">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6be7d-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6be7d-116">Requirements</span></span>



| <span data-ttu-id="6be7d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6be7d-117">Requirement</span></span> | <span data-ttu-id="6be7d-118">Valore</span><span class="sxs-lookup"><span data-stu-id="6be7d-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6be7d-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6be7d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6be7d-120">Windows 8</span><span class="sxs-lookup"><span data-stu-id="6be7d-120">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="6be7d-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6be7d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6be7d-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6be7d-122">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="6be7d-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6be7d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6be7d-124"><dt>LocationApi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6be7d-124"><dt>Locationapi.h</dt></span></span> </dl>       |
| <span data-ttu-id="6be7d-125">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="6be7d-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="6be7d-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6be7d-126"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="6be7d-127">DLL</span><span class="sxs-lookup"><span data-stu-id="6be7d-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6be7d-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6be7d-128"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="6be7d-129">IID</span><span class="sxs-lookup"><span data-stu-id="6be7d-129">IID</span></span><br/>                      | <span data-ttu-id="6be7d-130">DIID \_ IRemoteDesktopClientEvents è definito come 079863B7-6D47-4105-8BFE-0CDCB360E67D</span><span class="sxs-lookup"><span data-stu-id="6be7d-130">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6be7d-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6be7d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6be7d-132">**IRemoteDesktopClientEvents**</span><span class="sxs-lookup"><span data-stu-id="6be7d-132">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

 





