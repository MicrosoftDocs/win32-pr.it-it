---
title: Funzione di callback PxeProviderServiceControl
description: Chiamato quando il servizio WDS riceve un codice di controllo del servizio.
ms.assetid: 180ddcda-d111-4c81-9177-db99cbf1449f
keywords:
- Funzione di callback PxeProviderServiceControl servizi di distribuzione Windows
topic_type:
- apiref
api_name:
- PxeProviderServiceControl
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8c8a2c71b7b386254622758efa5f3dc5269a131d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301603"
---
# <a name="pxeproviderservicecontrol-callback-function"></a><span data-ttu-id="71e5a-104">Funzione di callback PxeProviderServiceControl</span><span class="sxs-lookup"><span data-stu-id="71e5a-104">PxeProviderServiceControl callback function</span></span>

<span data-ttu-id="71e5a-105">Chiamato quando il servizio WDS riceve un codice di controllo del servizio.</span><span class="sxs-lookup"><span data-stu-id="71e5a-105">Called when a service control code is received by the WDS service.</span></span> <span data-ttu-id="71e5a-106">Questa funzione di callback viene registrata chiamando la funzione [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) con il parametro *CallbackType* impostato sul **\_ \_ \_ controllo del servizio di callback PXE**.</span><span class="sxs-lookup"><span data-stu-id="71e5a-106">This callback function is registered by calling the [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) function with the *CallbackType* parameter set to **PXE\_CALLBACK\_SERVICE\_CONTROL**.</span></span>

## <a name="syntax"></a><span data-ttu-id="71e5a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="71e5a-107">Syntax</span></span>


```C++
DWORD PXEAPI PxeProviderServiceControl(
  _In_ PVOID pContext,
       DWORD dwControl
);
```



## <a name="parameters"></a><span data-ttu-id="71e5a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="71e5a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71e5a-109">*pContext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="71e5a-109">*pContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71e5a-110">Valore di contesto passato alla funzione [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) .</span><span class="sxs-lookup"><span data-stu-id="71e5a-110">Context value passed to the [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) function.</span></span>

</dd> <dt>

<span data-ttu-id="71e5a-111">*dwControl*</span><span class="sxs-lookup"><span data-stu-id="71e5a-111">*dwControl*</span></span> 
</dt> <dd>

<span data-ttu-id="71e5a-112">Codice di controllo.</span><span class="sxs-lookup"><span data-stu-id="71e5a-112">Control code.</span></span> <span data-ttu-id="71e5a-113">Per l'elenco dei valori possibili, vedere il parametro *dwControl* della funzione [*HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) .</span><span class="sxs-lookup"><span data-stu-id="71e5a-113">For the list of possible values, see the *dwControl* parameter of the [*HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71e5a-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="71e5a-114">Return value</span></span>

<span data-ttu-id="71e5a-115">Se l'arresto del provider ha esito positivo, il callback dovrebbe restituire l' **errore \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="71e5a-115">If the provider shutdown succeeds, the callback should return **ERROR\_SUCCESS**.</span></span> <span data-ttu-id="71e5a-116">In caso di errore, dovrebbe essere restituito un codice di errore appropriato.</span><span class="sxs-lookup"><span data-stu-id="71e5a-116">In case of failure, an appropriate error code should be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="71e5a-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="71e5a-117">Requirements</span></span>



| <span data-ttu-id="71e5a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="71e5a-118">Requirement</span></span> | <span data-ttu-id="71e5a-119">Valore</span><span class="sxs-lookup"><span data-stu-id="71e5a-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="71e5a-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="71e5a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="71e5a-121">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="71e5a-121">None supported</span></span><br/>                                                          |
| <span data-ttu-id="71e5a-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="71e5a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="71e5a-123">Windows Server 2008, Windows Server 2003 con \[ solo app desktop SP2\]</span><span class="sxs-lookup"><span data-stu-id="71e5a-123">Windows Server 2008, Windows Server 2003 with SP2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="71e5a-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="71e5a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71e5a-125">Funzioni server di servizi di distribuzione Windows</span><span class="sxs-lookup"><span data-stu-id="71e5a-125">Windows Deployment Services Server Functions</span></span>](windows-deployment-services-server-functions.md)
</dt> <dt>

[<span data-ttu-id="71e5a-126">**PxeRegisterCallback**</span><span class="sxs-lookup"><span data-stu-id="71e5a-126">**PxeRegisterCallback**</span></span>](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)
</dt> </dl>

 

