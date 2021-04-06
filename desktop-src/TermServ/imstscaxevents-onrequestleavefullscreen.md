---
title: Metodo IMsTscAxEvents OnRequestLeaveFullScreen
description: Chiamato quando il client richiede di uscire dalla modalità a schermo intero e la proprietà IMsTscAdvancedSettings put \_ ContainerHandledFullScreen è stata impostata su un valore diverso da zero.
ms.assetid: db6ee012-8288-4360-98b2-12858ea65baa
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo OnRequestLeaveFullScreen
- Metodo OnRequestLeaveFullScreen Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto, metodo OnRequestLeaveFullScreen
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRequestLeaveFullScreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e814d6153e32fdf4fa498a6630fc9ca2908510e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742095"
---
# <a name="imstscaxeventsonrequestleavefullscreen-method"></a><span data-ttu-id="9dd4e-106">Metodo IMsTscAxEvents:: OnRequestLeaveFullScreen</span><span class="sxs-lookup"><span data-stu-id="9dd4e-106">IMsTscAxEvents::OnRequestLeaveFullScreen method</span></span>

<span data-ttu-id="9dd4e-107">Chiamato quando il client richiede di uscire dalla modalità a schermo intero e la proprietà [**IMsTscAdvancedSettings::p UT \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) è stata impostata su un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="9dd4e-107">Called when the client requests to leave full-screen mode and the [**IMsTscAdvancedSettings::put\_ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) property has been set to a nonzero value.</span></span>

## <a name="syntax"></a><span data-ttu-id="9dd4e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9dd4e-108">Syntax</span></span>


```C++
void OnRequestLeaveFullScreen();
```



## <a name="parameters"></a><span data-ttu-id="9dd4e-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="9dd4e-109">Parameters</span></span>

<span data-ttu-id="9dd4e-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="9dd4e-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9dd4e-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9dd4e-111">Return value</span></span>

<span data-ttu-id="9dd4e-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="9dd4e-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9dd4e-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="9dd4e-113">Remarks</span></span>

<span data-ttu-id="9dd4e-114">In modalità a schermo intero gestita dal contenitore il contenitore deve lasciare la modalità standard a schermo intero in risposta a questo evento.</span><span class="sxs-lookup"><span data-stu-id="9dd4e-114">In container-handled full-screen mode, the container should leave standard full-screen mode in response to this event.</span></span>

<span data-ttu-id="9dd4e-115">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="9dd4e-115">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9dd4e-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9dd4e-116">Requirements</span></span>



| <span data-ttu-id="9dd4e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9dd4e-117">Requirement</span></span> | <span data-ttu-id="9dd4e-118">Valore</span><span class="sxs-lookup"><span data-stu-id="9dd4e-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9dd4e-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9dd4e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9dd4e-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9dd4e-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="9dd4e-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9dd4e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9dd4e-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9dd4e-122">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="9dd4e-123">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="9dd4e-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="9dd4e-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9dd4e-124"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9dd4e-125">DLL</span><span class="sxs-lookup"><span data-stu-id="9dd4e-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9dd4e-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9dd4e-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9dd4e-127">IID</span><span class="sxs-lookup"><span data-stu-id="9dd4e-127">IID</span></span><br/>                      | <span data-ttu-id="9dd4e-128">IMsTscAxEvents è definito come 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="9dd4e-128">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="9dd4e-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9dd4e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dd4e-130">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="9dd4e-130">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





