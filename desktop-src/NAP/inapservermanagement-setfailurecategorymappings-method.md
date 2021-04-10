---
title: Metodo INapServerManagement SetFailureCategoryMappings (NapServerManagement. h)
description: Viene utilizzato per impostare i mapping delle categorie di errori di convalida.
ms.assetid: be482f82-c79c-405c-b619-9bcb9b4dc349
keywords:
- NAP metodo SetFailureCategoryMappings
- Metodo SetFailureCategoryMappings NAP, interfaccia INapServerManagement
- Interfaccia INapServerManagement NAP, metodo SetFailureCategoryMappings
topic_type:
- apiref
api_name:
- INapServerManagement.SetFailureCategoryMappings
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a220d6603ef5bbb49377ac0e212d5d98afa4bdd0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964520"
---
# <a name="inapservermanagementsetfailurecategorymappings-method"></a><span data-ttu-id="d88ca-106">Metodo INapServerManagement:: SetFailureCategoryMappings</span><span class="sxs-lookup"><span data-stu-id="d88ca-106">INapServerManagement::SetFailureCategoryMappings method</span></span>

> [!Note]  
> <span data-ttu-id="d88ca-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="d88ca-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="d88ca-108">Il metodo **INapServerManagement:: SetFailureCategoryMappings** viene utilizzato per impostare i mapping delle categorie di errori di convalida.</span><span class="sxs-lookup"><span data-stu-id="d88ca-108">The **INapServerManagement::SetFailureCategoryMappings** method is used to set the SHV's failure category mappings.</span></span>

## <a name="syntax"></a><span data-ttu-id="d88ca-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d88ca-109">Syntax</span></span>


```C++
HRESULT SetFailureCategoryMappings(
  [in]       SystemHealthEntityId   id,
  [in] const FailureCategoryMapping mapping
);
```



## <a name="parameters"></a><span data-ttu-id="d88ca-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="d88ca-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d88ca-111">*ID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d88ca-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d88ca-112">Oggetto [**SystemHealthEntityId**](nap-type-constants.md) che contiene l'identificatore univoco del servizio di convalida dell'integrità di sistema.</span><span class="sxs-lookup"><span data-stu-id="d88ca-112">A [**SystemHealthEntityId**](nap-type-constants.md) that contains the unique identifier of the SHV.</span></span>

</dd> <dt>

<span data-ttu-id="d88ca-113">*mapping* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="d88ca-113">*mapping* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d88ca-114">Struttura [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) che contiene i dati di mapping della categoria degli errori.</span><span class="sxs-lookup"><span data-stu-id="d88ca-114">A [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) structure that contains the failure category mapping data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d88ca-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d88ca-115">Return value</span></span>

<span data-ttu-id="d88ca-116">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="d88ca-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="d88ca-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d88ca-117">Return code</span></span>                                                                                     | <span data-ttu-id="d88ca-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d88ca-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="d88ca-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d88ca-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="d88ca-120">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="d88ca-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="d88ca-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="d88ca-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="d88ca-122">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="d88ca-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="d88ca-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="d88ca-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="d88ca-124">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="d88ca-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d88ca-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d88ca-125">Requirements</span></span>



| <span data-ttu-id="d88ca-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d88ca-126">Requirement</span></span> | <span data-ttu-id="d88ca-127">Valore</span><span class="sxs-lookup"><span data-stu-id="d88ca-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d88ca-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d88ca-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d88ca-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="d88ca-129">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="d88ca-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d88ca-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d88ca-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d88ca-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d88ca-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d88ca-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="d88ca-133"><dt>NapServerManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="d88ca-133"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="d88ca-134">IDL</span><span class="sxs-lookup"><span data-stu-id="d88ca-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d88ca-135"><dt>NapServerManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d88ca-135"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="d88ca-136">DLL</span><span class="sxs-lookup"><span data-stu-id="d88ca-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d88ca-137"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d88ca-137"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="d88ca-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d88ca-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d88ca-139">**INapServerManagement**</span><span class="sxs-lookup"><span data-stu-id="d88ca-139">**INapServerManagement**</span></span>](inapservermanagement.md)
</dt> </dl>

 

 





