---
title: Funzione di callback PxeProviderShutdown
description: Chiamato per arrestare il provider.
ms.assetid: 436d7428-18f9-4b73-b346-79c9a0738c31
keywords:
- Funzione di callback PxeProviderShutdown servizi di distribuzione Windows
topic_type:
- apiref
api_name:
- PxeProviderShutdown
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 17698c5fa1f6ce6bd5443d0244ebc6ce6082ec33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301602"
---
# <a name="pxeprovidershutdown-callback-function"></a><span data-ttu-id="e88c0-104">Funzione di callback PxeProviderShutdown</span><span class="sxs-lookup"><span data-stu-id="e88c0-104">PxeProviderShutdown callback function</span></span>

<span data-ttu-id="e88c0-105">Chiamato per arrestare il provider.</span><span class="sxs-lookup"><span data-stu-id="e88c0-105">Called to shutdown the provider.</span></span> <span data-ttu-id="e88c0-106">Questa funzione viene registrata chiamando la funzione [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) con il parametro *CallbackType* impostato sull' **arresto del \_ callback \_ PXE**.</span><span class="sxs-lookup"><span data-stu-id="e88c0-106">This function is registered by calling the [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) function with the *CallbackType* parameter set to **PXE\_CALLBACK\_SHUTDOWN**.</span></span> <span data-ttu-id="e88c0-107">Dopo la chiamata a questa funzione, l'handle *hProvider* passato alla funzione [*PxeProviderInitialize*](pxeproviderinitialize.md) non è più valido.</span><span class="sxs-lookup"><span data-stu-id="e88c0-107">After this function is called, the *hProvider* handle passed to the [*PxeProviderInitialize*](pxeproviderinitialize.md) function is no longer valid.</span></span>

## <a name="syntax"></a><span data-ttu-id="e88c0-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e88c0-108">Syntax</span></span>


```C++
DWORD PXEAPI PxeProviderShutdown(
  _In_ PVOID pContext
);
```



## <a name="parameters"></a><span data-ttu-id="e88c0-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="e88c0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e88c0-110">*pContext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e88c0-110">*pContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e88c0-111">Valore di contesto passato alla funzione [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) .</span><span class="sxs-lookup"><span data-stu-id="e88c0-111">Context value passed to the [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e88c0-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e88c0-112">Return value</span></span>

<span data-ttu-id="e88c0-113">Se l'arresto del provider ha esito positivo, il callback dovrebbe restituire l' **errore \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="e88c0-113">If the provider shutdown succeeds, the callback should return **ERROR\_SUCCESS**.</span></span> <span data-ttu-id="e88c0-114">In caso di errore, dovrebbe essere restituito un codice di errore appropriato.</span><span class="sxs-lookup"><span data-stu-id="e88c0-114">In case of failure, an appropriate error code should be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="e88c0-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e88c0-115">Requirements</span></span>



| <span data-ttu-id="e88c0-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e88c0-116">Requirement</span></span> | <span data-ttu-id="e88c0-117">Valore</span><span class="sxs-lookup"><span data-stu-id="e88c0-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e88c0-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e88c0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e88c0-119">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="e88c0-119">None supported</span></span><br/>                                                          |
| <span data-ttu-id="e88c0-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e88c0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e88c0-121">Windows Server 2008, Windows Server 2003 con \[ solo app desktop SP2\]</span><span class="sxs-lookup"><span data-stu-id="e88c0-121">Windows Server 2008, Windows Server 2003 with SP2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e88c0-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e88c0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e88c0-123">Funzioni server di servizi di distribuzione Windows</span><span class="sxs-lookup"><span data-stu-id="e88c0-123">Windows Deployment Services Server Functions</span></span>](windows-deployment-services-server-functions.md)
</dt> <dt>

[<span data-ttu-id="e88c0-124">*PxeProviderInitialize*</span><span class="sxs-lookup"><span data-stu-id="e88c0-124">*PxeProviderInitialize*</span></span>](pxeproviderinitialize.md)
</dt> <dt>

[<span data-ttu-id="e88c0-125">**PxeRegisterCallback**</span><span class="sxs-lookup"><span data-stu-id="e88c0-125">**PxeRegisterCallback**</span></span>](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)
</dt> </dl>

 

 





