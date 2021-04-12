---
title: Metodo ITsSbResourcePluginStoreEx AcquireTargetLock
description: Blocca una destinazione.
ms.assetid: 76707f1d-1f13-4d81-8954-2acf05cda2cd
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo AcquireTargetLock
- Metodo AcquireTargetLock Servizi Desktop remoto, interfaccia ITsSbResourcePluginStoreEx
- Interfaccia ITsSbResourcePluginStoreEx Servizi Desktop remoto, metodo AcquireTargetLock
topic_type:
- apiref
api_name:
- ITsSbResourcePluginStoreEx.AcquireTargetLock
api_location:
- SbTsV.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c18be0a544ebcea2d2cecb40dcea3a08e4bd35b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119262"
---
# <a name="itssbresourcepluginstoreexacquiretargetlock-method"></a><span data-ttu-id="2b425-106">Metodo ITsSbResourcePluginStoreEx:: AcquireTargetLock</span><span class="sxs-lookup"><span data-stu-id="2b425-106">ITsSbResourcePluginStoreEx::AcquireTargetLock method</span></span>

<span data-ttu-id="2b425-107">Blocca una destinazione.</span><span class="sxs-lookup"><span data-stu-id="2b425-107">Locks a target.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b425-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2b425-108">Syntax</span></span>


```C++
HRESULT AcquireTargetLock(
  [in]  BSTR     targetName,
  [in]  DWORD    dwTimeout,
  [out] IUnknown **ppContext
);
```



## <a name="parameters"></a><span data-ttu-id="2b425-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="2b425-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b425-110">*TargetName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2b425-110">*targetName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b425-111">Nome della destinazione da bloccare.</span><span class="sxs-lookup"><span data-stu-id="2b425-111">The name of the target to lock.</span></span>

</dd> <dt>

<span data-ttu-id="2b425-112">*dwTimeOut* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2b425-112">*dwTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b425-113">Timeout per l'operazione, espresso in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="2b425-113">The timeout for the operation, in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="2b425-114">*ppContext* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2b425-114">*ppContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b425-115">Restituisce un puntatore al contesto del blocco.</span><span class="sxs-lookup"><span data-stu-id="2b425-115">Returns a pointer to the context of the lock.</span></span> <span data-ttu-id="2b425-116">Per rilasciare il blocco, fornire questo puntatore al metodo [**ReleaseTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) .</span><span class="sxs-lookup"><span data-stu-id="2b425-116">To release the lock, supply this pointer to the [**ReleaseTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b425-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2b425-117">Return value</span></span>

<span data-ttu-id="2b425-118">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2b425-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2b425-119">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2b425-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b425-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="2b425-120">Remarks</span></span>

<span data-ttu-id="2b425-121">Una volta acquisito il blocco, si presuppone che il thread chiamante disponga dell'accesso esclusivo all'oggetto di destinazione e che pertanto nessun altro thread (all'interno della stessa macchina) possa aggiornarlo.</span><span class="sxs-lookup"><span data-stu-id="2b425-121">After the lock is acquired, the calling thread is assumed to have exclusive access to the target object and therefore no other thread (within the same machine) can update it.</span></span> <span data-ttu-id="2b425-122">Pertanto, il thread chiamante deve chiamare il metodo [**ReleaseTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) non appena ha effettuato gli aggiornamenti necessari per l'oggetto di destinazione.</span><span class="sxs-lookup"><span data-stu-id="2b425-122">Therefore the calling thread must call the [**ReleaseTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) method as soon as it has made the necessary updates to the target object.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2b425-123">Questo blocco non impedisce completamente la modifica esterna degli oggetti di destinazione se nella distribuzione è presente più di un broker di connessione.</span><span class="sxs-lookup"><span data-stu-id="2b425-123">this lock does not completely prevent target objects from being modified externally if more than one Connection Broker exists in the deployment.</span></span> <span data-ttu-id="2b425-124">Il thread chiamante deve essere preparato per gestire correttamente un errore e ripetere l'aggiornamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="2b425-124">The calling thread must be prepared to handle a failure gracefully and retry the target update.</span></span>

 

<span data-ttu-id="2b425-125">Questo metodo è disponibile in Windows Server 2012 R2 con [KB3091411](https://support.microsoft.com/kb/3091411) installato nell'interfaccia [**ITsSbResourcePluginStoreEx**](itssbresourcepluginstoreex.md) .</span><span class="sxs-lookup"><span data-stu-id="2b425-125">This method is available on Windows Server 2012 R2 with [KB3091411](https://support.microsoft.com/kb/3091411) installed in the [**ITsSbResourcePluginStoreEx**](itssbresourcepluginstoreex.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b425-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2b425-126">Requirements</span></span>



| <span data-ttu-id="2b425-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b425-127">Requirement</span></span> | <span data-ttu-id="2b425-128">Valore</span><span class="sxs-lookup"><span data-stu-id="2b425-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b425-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2b425-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2b425-130">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="2b425-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2b425-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2b425-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2b425-132">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="2b425-132">Windows Server 2012 R2</span></span><br/>                                                             |
| <span data-ttu-id="2b425-133">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="2b425-133">End of server support</span></span><br/>    | <span data-ttu-id="2b425-134">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="2b425-134">Windows Server 2012 R2</span></span><br/>                                                             |
| <span data-ttu-id="2b425-135">IDL</span><span class="sxs-lookup"><span data-stu-id="2b425-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2b425-136"><dt>SbTsV. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2b425-136"><dt>SbTsV.idl</dt></span></span> </dl>          |
| <span data-ttu-id="2b425-137">IID</span><span class="sxs-lookup"><span data-stu-id="2b425-137">IID</span></span><br/>                      | <span data-ttu-id="2b425-138">IID \_ ITsSbResourcePluginStoreEx è definito come 80b83ffd-625d-11e5-bea1-a0481c7e9064</span><span class="sxs-lookup"><span data-stu-id="2b425-138">IID\_ITsSbResourcePluginStoreEx is defined as 80b83ffd-625d-11e5-bea1-a0481c7e9064</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2b425-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2b425-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b425-140">**ITsSbResourcePluginStoreEx**</span><span class="sxs-lookup"><span data-stu-id="2b425-140">**ITsSbResourcePluginStoreEx**</span></span>](itssbresourcepluginstoreex.md)
</dt> </dl>

 

 





