---
title: Interfaccia IBackgroundCopyError (Deliveryoptimization. h)
description: Utilizzare l'interfaccia IBackgroundCopyError per determinare la provocazione di un errore e se il processo di trasferimento può proseguire.
ms.assetid: 7DCB63CF-4180-4DC3-9093-07C4F8CF7A8E
keywords:
- Interfaccia IBackgroundCopyError
- Interfaccia IBackgroundCopyError, descritta
topic_type:
- apiref
api_name:
- IBackgroundCopyError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1f35365d56ce9391a746e479e1b59034342ebf62
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476372"
---
# <a name="ibackgroundcopyerror-interface"></a><span data-ttu-id="8bdaa-105">Interfaccia IBackgroundCopyError</span><span class="sxs-lookup"><span data-stu-id="8bdaa-105">IBackgroundCopyError interface</span></span>

<span data-ttu-id="8bdaa-106">Utilizzare l'interfaccia **IBackgroundCopyError** per determinare la provocazione di un errore e se il processo di trasferimento può proseguire.</span><span class="sxs-lookup"><span data-stu-id="8bdaa-106">Use the **IBackgroundCopyError** interface to determine the cause of an error and if the transfer process can proceed.</span></span>

<span data-ttu-id="8bdaa-107">Viene creato un oggetto Error solo quando lo stato del processo è BG_JOB_STATE_ERROR o BG_JOB_STATE_TRANSIENT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="8bdaa-107">DO creates an error object only when the state of the job is BG_JOB_STATE_ERROR or BG_JOB_STATE_TRANSIENT_ERROR.</span></span> <span data-ttu-id="8bdaa-108">Non crea un oggetto Error quando un metodo di interfaccia **IBackgroundCopyXXXX** ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="8bdaa-108">DO does not create an error object when an **IBackgroundCopyXXXX** interface method fails.</span></span> <span data-ttu-id="8bdaa-109">L'oggetto Error è disponibile fino a quando non inizia il trasferimento dei dati (lo stato del processo viene modificato in BG_JOB_STATE_TRANSFERRING) per il processo.</span><span class="sxs-lookup"><span data-stu-id="8bdaa-109">The error object is available until DO begins transferring data (the state of the job changes to BG_JOB_STATE_TRANSFERRING) for the job.</span></span>

<span data-ttu-id="8bdaa-110">Per ottenere un oggetto **IBackgroundCopyError** , chiamare il metodo [**Metodo ibackgroundcopyjob:: GetError**](ibackgroundcopyjob-geterror.md) .</span><span class="sxs-lookup"><span data-stu-id="8bdaa-110">To get an **IBackgroundCopyError** object, call the [**IBackgroundCopyJob::GetError**](ibackgroundcopyjob-geterror.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="8bdaa-111">Membri</span><span class="sxs-lookup"><span data-stu-id="8bdaa-111">Members</span></span>

<span data-ttu-id="8bdaa-112">L'interfaccia **IBackgroundCopyError** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="8bdaa-112">The **IBackgroundCopyError** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8bdaa-113">**IBackgroundCopyError** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="8bdaa-113">**IBackgroundCopyError** also has these types of members:</span></span>

-   [<span data-ttu-id="8bdaa-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="8bdaa-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8bdaa-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="8bdaa-115">Methods</span></span>

<span data-ttu-id="8bdaa-116">L'interfaccia **IBackgroundCopyError** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="8bdaa-116">The **IBackgroundCopyError** interface has these methods.</span></span>



| <span data-ttu-id="8bdaa-117">Metodo</span><span class="sxs-lookup"><span data-stu-id="8bdaa-117">Method</span></span>                                                   | <span data-ttu-id="8bdaa-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8bdaa-118">Description</span></span>                                                                                 |
|:---------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8bdaa-119">**GetError**</span><span class="sxs-lookup"><span data-stu-id="8bdaa-119">**GetError**</span></span>](ibackgroundcopyerror-geterror-method.md) | <span data-ttu-id="8bdaa-120">Recupera il codice di errore e identifica il contesto in cui si è verificato l'errore.</span><span class="sxs-lookup"><span data-stu-id="8bdaa-120">Retrieves the error code and identifies the context in which the error occurred.</span></span><br/> |
| [<span data-ttu-id="8bdaa-121">**GetFile**</span><span class="sxs-lookup"><span data-stu-id="8bdaa-121">**GetFile**</span></span>](ibackgroundcopyerror-getfile-method.md)   | <span data-ttu-id="8bdaa-122">Recupera un puntatore di interfaccia all'oggetto file associato all'errore.</span><span class="sxs-lookup"><span data-stu-id="8bdaa-122">Retrieves an interface pointer to the file object associated with the error.</span></span><br/>     |



 

## <a name="requirements"></a><span data-ttu-id="8bdaa-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8bdaa-123">Requirements</span></span>



| <span data-ttu-id="8bdaa-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="8bdaa-124">Requirement</span></span> | <span data-ttu-id="8bdaa-125">Valore</span><span class="sxs-lookup"><span data-stu-id="8bdaa-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bdaa-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8bdaa-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8bdaa-127">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="8bdaa-127">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="8bdaa-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8bdaa-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8bdaa-129">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8bdaa-129">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="8bdaa-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8bdaa-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="8bdaa-131"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="8bdaa-131"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="8bdaa-132">IDL</span><span class="sxs-lookup"><span data-stu-id="8bdaa-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8bdaa-133"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8bdaa-133"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="8bdaa-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="8bdaa-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="8bdaa-135"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8bdaa-135"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="8bdaa-136">DLL</span><span class="sxs-lookup"><span data-stu-id="8bdaa-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8bdaa-137"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8bdaa-137"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="8bdaa-138">IID</span><span class="sxs-lookup"><span data-stu-id="8bdaa-138">IID</span></span><br/>                      | <span data-ttu-id="8bdaa-139">IID_IBackgroundCopyError viene definito come 19C613A0-FCB8-4F28-81AE-897C3D078F81</span><span class="sxs-lookup"><span data-stu-id="8bdaa-139">IID_IBackgroundCopyError is defined as 19C613A0-FCB8-4F28-81AE-897C3D078F81</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="8bdaa-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8bdaa-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bdaa-141">**BG_JOB_STATE**</span><span class="sxs-lookup"><span data-stu-id="8bdaa-141">**BG_JOB_STATE**</span></span>](bg-job-state-.md)
</dt> <dt>

[<span data-ttu-id="8bdaa-142">**Metodo ibackgroundcopyjob:: GetError**</span><span class="sxs-lookup"><span data-stu-id="8bdaa-142">**IBackgroundCopyJob::GetError**</span></span>](ibackgroundcopyjob-geterror.md)
</dt> <dt>

[<span data-ttu-id="8bdaa-143">**Metodo ibackgroundcopyjob:: GetState**</span><span class="sxs-lookup"><span data-stu-id="8bdaa-143">**IBackgroundCopyJob::GetState**</span></span>](ibackgroundcopyjob-getstate.md)
</dt> <dt>

[<span data-ttu-id="8bdaa-144">**IBackgroundCopyCallback::JobError**</span><span class="sxs-lookup"><span data-stu-id="8bdaa-144">**IBackgroundCopyCallback::JobError**</span></span>](ibackgroundcopycallback-joberror-method.md)
</dt> </dl>

 

