---
title: Metodo INapSystemHealthAgentCallback CompareSoHRequests (NapSystemHealthAgent. h)
description: Viene usato dall'SHA per confrontare le richieste del rapporto di integrità.
ms.assetid: 14ba189a-e745-44b0-b729-522087d4e08b
keywords:
- NAP metodo CompareSoHRequests
- Metodo CompareSoHRequests NAP, interfaccia INapSystemHealthAgentCallback
- Interfaccia INapSystemHealthAgentCallback NAP, metodo CompareSoHRequests
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.CompareSoHRequests
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c6713f3de47cfbde6df67662f89ab3c094d0674
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301810"
---
# <a name="inapsystemhealthagentcallbackcomparesohrequests-method"></a><span data-ttu-id="abd49-106">Metodo INapSystemHealthAgentCallback:: CompareSoHRequests</span><span class="sxs-lookup"><span data-stu-id="abd49-106">INapSystemHealthAgentCallback::CompareSoHRequests method</span></span>

> [!Note]  
> <span data-ttu-id="abd49-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="abd49-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="abd49-108">Il metodo **INapSystemHealthAgentCallback:: CompareSoHRequests** viene usato dall'SHA per confrontare le richieste del rapporto di integrità.</span><span class="sxs-lookup"><span data-stu-id="abd49-108">The **INapSystemHealthAgentCallback::CompareSoHRequests** method is used by the SHA to compare SoH requests.</span></span>

## <a name="syntax"></a><span data-ttu-id="abd49-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="abd49-109">Syntax</span></span>


```C++
HRESULT CompareSoHRequests(
  [in]  const SoHRequest *lhs,
  [in]  const SoHRequest *rhs,
  [out]       BOOL       *isEqual
);
```



## <a name="parameters"></a><span data-ttu-id="abd49-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="abd49-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abd49-111">*LHS* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="abd49-111">*lhs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abd49-112">Puntatore a [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) a sinistra dell'operazione di confronto.</span><span class="sxs-lookup"><span data-stu-id="abd49-112">A pointer to the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) on the left of the comparison operation.</span></span>

</dd> <dt>

<span data-ttu-id="abd49-113">*RHS* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="abd49-113">*rhs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abd49-114">Puntatore a [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) a destra dell'operazione di confronto.</span><span class="sxs-lookup"><span data-stu-id="abd49-114">A pointer to the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) on the right of the comparison operation.</span></span>

</dd> <dt>

<span data-ttu-id="abd49-115">*è uguale* \[ a out\]</span><span class="sxs-lookup"><span data-stu-id="abd49-115">*isEqual* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="abd49-116">Puntatore a un **bool** che è **true** se *LHS* e *RHS* sono semanticamente uguali e **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="abd49-116">A pointer to a **BOOL** that is **TRUE** if *lhs* and *rhs* are semantically equal, and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abd49-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="abd49-117">Return value</span></span>

<span data-ttu-id="abd49-118">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="abd49-118">This method can return one of these values.</span></span>



| <span data-ttu-id="abd49-119">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="abd49-119">Return code</span></span>                                                                               | <span data-ttu-id="abd49-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="abd49-120">Description</span></span>                                           |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="abd49-121"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="abd49-121"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="abd49-122">Indica l'esito positivo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="abd49-122">Indicates success.</span></span><br/>                         |
| <dl> <span data-ttu-id="abd49-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="abd49-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="abd49-124">Il metodo non è stato implementato dall'SHA.</span><span class="sxs-lookup"><span data-stu-id="abd49-124">The method was not implemented by the SHA.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="abd49-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="abd49-125">Remarks</span></span>

<span data-ttu-id="abd49-126">Questo metodo di callback viene dichiarato dal sistema NAP e deve essere implementato dal writer SHA.</span><span class="sxs-lookup"><span data-stu-id="abd49-126">This callback method is declared by the NAP system and is to be implemented by the SHA writer.</span></span>

<span data-ttu-id="abd49-127">SHA deve confrontare invieranno e restituire **true** se invieranno sono semanticamente uguali.</span><span class="sxs-lookup"><span data-stu-id="abd49-127">The SHA should compare the SoHs and return **TRUE** if the SoHs are semantically equal.</span></span> <span data-ttu-id="abd49-128">NapAgent utilizza queste informazioni per determinare se deve essere avviato un scambio di rapporto di integrità a causa del cambiamento dello stato del computer client.</span><span class="sxs-lookup"><span data-stu-id="abd49-128">The NapAgent uses this information to determine if an SoH exchange should be initiated due to change of state of the client machine.</span></span>

<span data-ttu-id="abd49-129">Se SHAs hanno inserito gli ID incrementali o i timestamp nel rapporto di integrità, invieranno può essere semanticamente uguali (ovvero possono fornire le stesse informazioni sull'integrità), ma possono essere diversi da byte.</span><span class="sxs-lookup"><span data-stu-id="abd49-129">If SHAs have put incremental IDs or time-stamps into their SoH, then SoHs may be semantically equal (i.e. they may convey the same health information), but they may be byte-wise unequal.</span></span> <span data-ttu-id="abd49-130">SHAs deve implementare questa funzione per verificare l'uguaglianza semantica di invieranno.</span><span class="sxs-lookup"><span data-stu-id="abd49-130">SHAs should implement this function to check for semantic equality of SoHs.</span></span>

<span data-ttu-id="abd49-131">Se SHAs non hanno inserito timestamp o ID nei rispettivi invieranno, possono scegliere di non implementare questa funzione e restituire **e \_ NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="abd49-131">If SHAs have not put any time-stamps or Ids into their SoHs, they may choose to not implement this function and return **E\_NOTIMPL**.</span></span> <span data-ttu-id="abd49-132">In questo caso, NapAgent esegue un confronto byte in [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh).</span><span class="sxs-lookup"><span data-stu-id="abd49-132">In this case, the NapAgent performs a byte-wise comparison on the [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span>

## <a name="requirements"></a><span data-ttu-id="abd49-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="abd49-133">Requirements</span></span>



| <span data-ttu-id="abd49-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="abd49-134">Requirement</span></span> | <span data-ttu-id="abd49-135">Valore</span><span class="sxs-lookup"><span data-stu-id="abd49-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abd49-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="abd49-136">Minimum supported client</span></span><br/> | <span data-ttu-id="abd49-137">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="abd49-137">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="abd49-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="abd49-138">Minimum supported server</span></span><br/> | <span data-ttu-id="abd49-139">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="abd49-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="abd49-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="abd49-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="abd49-141"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="abd49-141"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="abd49-142">IDL</span><span class="sxs-lookup"><span data-stu-id="abd49-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="abd49-143"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="abd49-143"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abd49-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="abd49-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abd49-145">**INapSystemHealthAgentCallback**</span><span class="sxs-lookup"><span data-stu-id="abd49-145">**INapSystemHealthAgentCallback**</span></span>](inapsystemhealthagentcallback.md)
</dt> <dt>

[<span data-ttu-id="abd49-146">**Rapporto**</span><span class="sxs-lookup"><span data-stu-id="abd49-146">**SoH**</span></span>](/windows/win32/api/naptypes/ns-naptypes-soh)
</dt> </dl>

 

 





