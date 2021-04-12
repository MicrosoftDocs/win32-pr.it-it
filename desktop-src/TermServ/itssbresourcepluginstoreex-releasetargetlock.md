---
title: Metodo ITsSbResourcePluginStoreEx ReleaseTargetLock
description: Rilascia un blocco su una destinazione.
ms.assetid: ab2ae9f3-2d38-4b31-9889-58297c574bd4
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo ReleaseTargetLock
- Metodo ReleaseTargetLock Servizi Desktop remoto, interfaccia ITsSbResourcePluginStoreEx
- Interfaccia ITsSbResourcePluginStoreEx Servizi Desktop remoto, metodo ReleaseTargetLock
topic_type:
- apiref
api_name:
- ITsSbResourcePluginStoreEx.ReleaseTargetLock
api_location:
- SbTsV.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fbc34bdb27e40316ea1271bf0faa5d8c6b0abfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120183"
---
# <a name="itssbresourcepluginstoreexreleasetargetlock-method"></a><span data-ttu-id="38071-106">Metodo ITsSbResourcePluginStoreEx:: ReleaseTargetLock</span><span class="sxs-lookup"><span data-stu-id="38071-106">ITsSbResourcePluginStoreEx::ReleaseTargetLock method</span></span>

<span data-ttu-id="38071-107">Rilascia un blocco su una destinazione.</span><span class="sxs-lookup"><span data-stu-id="38071-107">Releases a lock on a target.</span></span>

## <a name="syntax"></a><span data-ttu-id="38071-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="38071-108">Syntax</span></span>


```C++
HRESULT ReleaseTargetLock(
  [in] IUnknown *pContext
);
```



## <a name="parameters"></a><span data-ttu-id="38071-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="38071-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38071-110">*pContext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="38071-110">*pContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38071-111">Puntatore al contesto restituito dal metodo [**AcquireTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-acquiretargetlock) .</span><span class="sxs-lookup"><span data-stu-id="38071-111">A pointer to the context returned by the [**AcquireTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-acquiretargetlock) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38071-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="38071-112">Return value</span></span>

<span data-ttu-id="38071-113">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="38071-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="38071-114">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="38071-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="38071-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="38071-115">Remarks</span></span>

<span data-ttu-id="38071-116">Questo metodo è disponibile solo in Windows Server 2012 R2 con [KB3091411](https://support.microsoft.com/kb/3091411) installato nell'interfaccia [**ITsSbResourcePluginStoreEx**](itssbresourcepluginstoreex.md) .</span><span class="sxs-lookup"><span data-stu-id="38071-116">This method is only available on Windows Server 2012 R2 with [KB3091411](https://support.microsoft.com/kb/3091411) installed in the [**ITsSbResourcePluginStoreEx**](itssbresourcepluginstoreex.md) interface.</span></span> <span data-ttu-id="38071-117">Questo metodo è disponibile nell'interfaccia [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) a partire da Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="38071-117">This method is available on the [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) interface starting with Windows Server 2016.</span></span>

## <a name="requirements"></a><span data-ttu-id="38071-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="38071-118">Requirements</span></span>



| <span data-ttu-id="38071-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="38071-119">Requirement</span></span> | <span data-ttu-id="38071-120">Valore</span><span class="sxs-lookup"><span data-stu-id="38071-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="38071-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="38071-121">Minimum supported client</span></span><br/> | <span data-ttu-id="38071-122">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="38071-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="38071-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="38071-123">Minimum supported server</span></span><br/> | <span data-ttu-id="38071-124">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="38071-124">Windows Server 2012 R2</span></span><br/>                                                             |
| <span data-ttu-id="38071-125">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="38071-125">End of server support</span></span><br/>    | <span data-ttu-id="38071-126">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="38071-126">Windows Server 2012 R2</span></span><br/>                                                             |
| <span data-ttu-id="38071-127">IDL</span><span class="sxs-lookup"><span data-stu-id="38071-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="38071-128"><dt>SbTsV. idl</dt></span><span class="sxs-lookup"><span data-stu-id="38071-128"><dt>SbTsV.idl</dt></span></span> </dl>          |
| <span data-ttu-id="38071-129">IID</span><span class="sxs-lookup"><span data-stu-id="38071-129">IID</span></span><br/>                      | <span data-ttu-id="38071-130">IID \_ ITsSbResourcePluginStoreEx è definito come 80b83ffd-625d-11e5-bea1-a0481c7e9064</span><span class="sxs-lookup"><span data-stu-id="38071-130">IID\_ITsSbResourcePluginStoreEx is defined as 80b83ffd-625d-11e5-bea1-a0481c7e9064</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="38071-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="38071-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38071-132">**ITsSbResourcePluginStoreEx**</span><span class="sxs-lookup"><span data-stu-id="38071-132">**ITsSbResourcePluginStoreEx**</span></span>](itssbresourcepluginstoreex.md)
</dt> </dl>

 

 





