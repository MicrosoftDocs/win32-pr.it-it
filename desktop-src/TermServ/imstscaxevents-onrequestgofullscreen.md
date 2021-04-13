---
title: Metodo IMsTscAxEvents OnRequestGoFullScreen
description: Chiamato quando il client richiede di passare alla modalità a schermo intero e \_ viene chiamato il metodo IMsTscAdvancedSettings put ContainerHandledFullScreen per impostare la proprietà ContainerHandledFullScreen su un valore diverso da zero.
ms.assetid: f61520dc-a72a-4205-8761-92aaf08b5f90
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo OnRequestGoFullScreen
- Metodo OnRequestGoFullScreen Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto, metodo OnRequestGoFullScreen
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRequestGoFullScreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c865cd27b447743f781b8563956e7fb2d7f5d703
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400733"
---
# <a name="imstscaxeventsonrequestgofullscreen-method"></a><span data-ttu-id="a8b13-106">Metodo IMsTscAxEvents:: OnRequestGoFullScreen</span><span class="sxs-lookup"><span data-stu-id="a8b13-106">IMsTscAxEvents::OnRequestGoFullScreen method</span></span>

<span data-ttu-id="a8b13-107">Chiamato quando il client richiede di passare alla modalità a schermo intero e viene chiamato il metodo [**IMsTscAdvancedSettings::p UT \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) per impostare la proprietà **ContainerHandledFullScreen** su un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="a8b13-107">Called when the client requests to switch to full-screen mode and the [**IMsTscAdvancedSettings::put\_ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) method is called to set the **ContainerHandledFullScreen** property to a nonzero value.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8b13-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a8b13-108">Syntax</span></span>


```C++
void OnRequestGoFullScreen();
```



## <a name="parameters"></a><span data-ttu-id="a8b13-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a8b13-109">Parameters</span></span>

<span data-ttu-id="a8b13-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="a8b13-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a8b13-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a8b13-111">Return value</span></span>

<span data-ttu-id="a8b13-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="a8b13-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8b13-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="a8b13-113">Remarks</span></span>

<span data-ttu-id="a8b13-114">In modalità a schermo intero gestita dal contenitore il contenitore deve immettere la modalità standard a schermo intero in risposta a questo evento.</span><span class="sxs-lookup"><span data-stu-id="a8b13-114">In container-handled full-screen mode, the container should enter standard full-screen mode in response to this event.</span></span>

<span data-ttu-id="a8b13-115">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="a8b13-115">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a8b13-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a8b13-116">Requirements</span></span>



| <span data-ttu-id="a8b13-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8b13-117">Requirement</span></span> | <span data-ttu-id="a8b13-118">Valore</span><span class="sxs-lookup"><span data-stu-id="a8b13-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8b13-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8b13-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a8b13-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a8b13-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a8b13-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8b13-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a8b13-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a8b13-122">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a8b13-123">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="a8b13-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="a8b13-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8b13-124"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a8b13-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a8b13-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8b13-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8b13-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a8b13-127">IID</span><span class="sxs-lookup"><span data-stu-id="a8b13-127">IID</span></span><br/>                      | <span data-ttu-id="a8b13-128">IMsTscAxEvents è definito come 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="a8b13-128">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="a8b13-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a8b13-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8b13-130">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="a8b13-130">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





