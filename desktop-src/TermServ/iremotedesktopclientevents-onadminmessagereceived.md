---
title: Metodo IRemoteDesktopClientEvents OnAdminMessageReceived
description: Chiamato quando il controllo client riceve un messaggio amministrativo.
ms.assetid: CD580207-CEC1-493B-989E-7C1D4FA71228
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo OnAdminMessageReceived
- Metodo OnAdminMessageReceived Servizi Desktop remoto, interfaccia IRemoteDesktopClientEvents
- Interfaccia IRemoteDesktopClientEvents Servizi Desktop remoto, metodo OnAdminMessageReceived
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnAdminMessageReceived
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 201dd3111dbac0b6395654ef8dfad21318419de3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400783"
---
# <a name="iremotedesktopclienteventsonadminmessagereceived-method"></a><span data-ttu-id="1c936-106">Metodo IRemoteDesktopClientEvents:: OnAdminMessageReceived</span><span class="sxs-lookup"><span data-stu-id="1c936-106">IRemoteDesktopClientEvents::OnAdminMessageReceived method</span></span>

<span data-ttu-id="1c936-107">Chiamato quando il controllo client riceve un messaggio amministrativo.</span><span class="sxs-lookup"><span data-stu-id="1c936-107">Called when the client control receives an administrative message.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c936-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1c936-108">Syntax</span></span>


```C++
void OnAdminMessageReceived(
  [in] BSTR adminMessage
);
```



## <a name="parameters"></a><span data-ttu-id="1c936-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="1c936-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c936-110">*adminMessage* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1c936-110">*adminMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c936-111">Messaggio.</span><span class="sxs-lookup"><span data-stu-id="1c936-111">The message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c936-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1c936-112">Return value</span></span>

<span data-ttu-id="1c936-113">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="1c936-113">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c936-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1c936-114">Requirements</span></span>



| <span data-ttu-id="1c936-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c936-115">Requirement</span></span> | <span data-ttu-id="1c936-116">Valore</span><span class="sxs-lookup"><span data-stu-id="1c936-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c936-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c936-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1c936-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="1c936-118">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="1c936-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c936-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1c936-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1c936-120">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="1c936-121">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="1c936-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="1c936-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c936-122"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="1c936-123">DLL</span><span class="sxs-lookup"><span data-stu-id="1c936-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c936-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c936-124"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="1c936-125">IID</span><span class="sxs-lookup"><span data-stu-id="1c936-125">IID</span></span><br/>                      | <span data-ttu-id="1c936-126">DIID \_ IRemoteDesktopClientEvents è definito come 079863B7-6D47-4105-8BFE-0CDCB360E67D</span><span class="sxs-lookup"><span data-stu-id="1c936-126">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1c936-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1c936-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c936-128">**IRemoteDesktopClientEvents**</span><span class="sxs-lookup"><span data-stu-id="1c936-128">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

 





