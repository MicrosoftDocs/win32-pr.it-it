---
description: Associa un'implementazione di ITransactionProxy al contesto corrente.
ms.assetid: 64009632-b536-41fb-95ac-b23e2cbf18da
title: 'Metodo IContextTransactionInfo:: RegisterTransactionProxy'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextTransactionInfo.RegisterTransactionProxy
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7b559453b0d4ed75f92f7a421be4c3a47e07fdf7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342391"
---
# <a name="icontexttransactioninforegistertransactionproxy-method"></a><span data-ttu-id="c8240-103">Metodo IContextTransactionInfo:: RegisterTransactionProxy</span><span class="sxs-lookup"><span data-stu-id="c8240-103">IContextTransactionInfo::RegisterTransactionProxy method</span></span>

<span data-ttu-id="c8240-104">Associa un'implementazione di [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) al contesto corrente.</span><span class="sxs-lookup"><span data-stu-id="c8240-104">Associates an [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) implementation with the current context.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8240-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c8240-105">Syntax</span></span>


```C++
HRESULT RegisterTransactionProxy(
  [in]  ITransactionProxy *pProxy,
  [out] GUID              *pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="c8240-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c8240-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8240-107">*pProxy* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c8240-107">*pProxy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8240-108">Implementazione di [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) da associare al contesto corrente.</span><span class="sxs-lookup"><span data-stu-id="c8240-108">An [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) implementation to associate with the current context.</span></span>

</dd> <dt>

<span data-ttu-id="c8240-109">*pGuid* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c8240-109">*pGuid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8240-110">GUID che identifica il proxy di transazione.</span><span class="sxs-lookup"><span data-stu-id="c8240-110">A GUID that identifies the transaction proxy.</span></span> <span data-ttu-id="c8240-111">COM+ utilizza questo GUID quando viene chiamato [**ITransactionProxy:: commit**](/windows/desktop/api/ComSvcs/nf-comsvcs-itransactionproxy-commit) sul proxy di transazione.</span><span class="sxs-lookup"><span data-stu-id="c8240-111">COM+ uses this GUID when calling [**ITransactionProxy::Commit**](/windows/desktop/api/ComSvcs/nf-comsvcs-itransactionproxy-commit) on the transaction proxy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8240-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c8240-112">Return value</span></span>

<span data-ttu-id="c8240-113">Questo metodo può restituire i valori restituiti standard E \_ INVALIDARG, e \_ OutOfMemory e e \_ imprevisto, oltre ai valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="c8240-113">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, and E\_UNEXPECTED, as well as the following values.</span></span>



| <span data-ttu-id="c8240-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="c8240-114">Return code</span></span>                                                                                                     | <span data-ttu-id="c8240-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c8240-115">Description</span></span>                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c8240-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c8240-116"><dt>**S\_OK**</dt></span></span> </dl>                            | <span data-ttu-id="c8240-117">Metodo completato correttamente.</span><span class="sxs-lookup"><span data-stu-id="c8240-117">The method completed successfully.</span></span><br/>                                                                           |
| <dl> <span data-ttu-id="c8240-118"><dt>**CONTESTO \_ E \_ ALREADYINTRANSACTION**</dt></span><span class="sxs-lookup"><span data-stu-id="c8240-118"><dt>**CONTEXT\_E\_ALREADYINTRANSACTION**</dt></span></span> </dl> | <span data-ttu-id="c8240-119">Al contesto corrente è già associata un'implementazione di [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) .</span><span class="sxs-lookup"><span data-stu-id="c8240-119">The current context already has an associated [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) implementation.</span></span><br/> |
| <dl> <span data-ttu-id="c8240-120"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="c8240-120"><dt>**E\_NOTIMPL**</dt></span></span> </dl>                       | <span data-ttu-id="c8240-121">Il contesto corrente ospita una transazione BYOT (Bring Your Own Transaction) o una transazione non radice.</span><span class="sxs-lookup"><span data-stu-id="c8240-121">The current context is hosting a Bring Your Own Transaction (BYOT) transaction or a non-root transaction.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="c8240-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="c8240-122">Remarks</span></span>

<span data-ttu-id="c8240-123">Il metodo **RegisterTransactionProxy** può essere chiamato solo se il contesto corrente è un contesto di transazione radice.</span><span class="sxs-lookup"><span data-stu-id="c8240-123">The **RegisterTransactionProxy** method can only be called if the current context is a root transaction context.</span></span> <span data-ttu-id="c8240-124">Non può essere chiamato se il contesto ospita una transazione BYOT o una transazione non radice.</span><span class="sxs-lookup"><span data-stu-id="c8240-124">It cannot be called if the context is hosting a BYOT transaction or a non-root transaction.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8240-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c8240-125">Requirements</span></span>



| <span data-ttu-id="c8240-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8240-126">Requirement</span></span> | <span data-ttu-id="c8240-127">Valore</span><span class="sxs-lookup"><span data-stu-id="c8240-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="c8240-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8240-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c8240-129">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="c8240-129">Windows XP with SP2 \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="c8240-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8240-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c8240-131">Windows Server 2003 con \[ solo app desktop SP1\]</span><span class="sxs-lookup"><span data-stu-id="c8240-131">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c8240-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c8240-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8240-133">**IContextTransactionInfo**</span><span class="sxs-lookup"><span data-stu-id="c8240-133">**IContextTransactionInfo**</span></span>](icontexttransactioninfo.md)
</dt> </dl>

 

 




