---
title: Metodo INapServerInfo GetFailureCategoryMappings (NapServerManagement. h)
description: Recupera i mapping delle categorie di errore per un SHA o un servizio di convalida dell'integrità specificato.
ms.assetid: 89b89003-40b3-4763-aec8-01cd0c307649
keywords:
- NAP metodo GetFailureCategoryMappings
- Metodo GetFailureCategoryMappings NAP, interfaccia INapServerInfo
- Interfaccia INapServerInfo NAP, metodo GetFailureCategoryMappings
topic_type:
- apiref
api_name:
- INapServerInfo.GetFailureCategoryMappings
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7ba830dd8a35a2c60b14c4feec14846125223e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479342"
---
# <a name="inapserverinfogetfailurecategorymappings-method"></a><span data-ttu-id="45a11-106">Metodo INapServerInfo:: GetFailureCategoryMappings</span><span class="sxs-lookup"><span data-stu-id="45a11-106">INapServerInfo::GetFailureCategoryMappings method</span></span>

> [!Note]  
> <span data-ttu-id="45a11-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="45a11-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="45a11-108">Il metodo **INapServerInfo:: GetFailureCategoryMappings** recupera i mapping delle categorie di errore per un SHA o un servizio di convalida dell'integrità specificato.</span><span class="sxs-lookup"><span data-stu-id="45a11-108">The **INapServerInfo::GetFailureCategoryMappings** method retrieves the failure category mappings for a specified SHA or SHV.</span></span>

## <a name="syntax"></a><span data-ttu-id="45a11-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="45a11-109">Syntax</span></span>


```C++
HRESULT GetFailureCategoryMappings(
  [in]  SystemHealthEntityId   id,
  [out] FailureCategoryMapping *mapping
);
```



## <a name="parameters"></a><span data-ttu-id="45a11-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="45a11-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45a11-111">*ID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="45a11-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45a11-112">Oggetto [**SystemHealthEntityId**](nap-type-constants.md) che contiene l'identificatore univoco dell'oggetto SHA o del servizio di convalida dell'integrità.</span><span class="sxs-lookup"><span data-stu-id="45a11-112">A [**SystemHealthEntityId**](nap-type-constants.md) that contains the unique identifier of the SHA or the SHV.</span></span>

</dd> <dt>

<span data-ttu-id="45a11-113">*mapping* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="45a11-113">*mapping* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="45a11-114">Puntatore a un [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) che contiene i dati di mapping.</span><span class="sxs-lookup"><span data-stu-id="45a11-114">A pointer to a [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) that contains the mapping data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45a11-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="45a11-115">Return value</span></span>

<span data-ttu-id="45a11-116">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="45a11-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="45a11-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="45a11-117">Return code</span></span>                                                                                     | <span data-ttu-id="45a11-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="45a11-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="45a11-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="45a11-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="45a11-120">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="45a11-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="45a11-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="45a11-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="45a11-122">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="45a11-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="45a11-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="45a11-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="45a11-124">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="45a11-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="45a11-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="45a11-125">Requirements</span></span>



| <span data-ttu-id="45a11-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="45a11-126">Requirement</span></span> | <span data-ttu-id="45a11-127">Valore</span><span class="sxs-lookup"><span data-stu-id="45a11-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45a11-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="45a11-128">Minimum supported client</span></span><br/> | <span data-ttu-id="45a11-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="45a11-129">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="45a11-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="45a11-130">Minimum supported server</span></span><br/> | <span data-ttu-id="45a11-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="45a11-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="45a11-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="45a11-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="45a11-133"><dt>NapServerManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="45a11-133"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="45a11-134">IDL</span><span class="sxs-lookup"><span data-stu-id="45a11-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="45a11-135"><dt>NapServerManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="45a11-135"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="45a11-136">DLL</span><span class="sxs-lookup"><span data-stu-id="45a11-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45a11-137"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45a11-137"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="45a11-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="45a11-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45a11-139">**INapServerInfo**</span><span class="sxs-lookup"><span data-stu-id="45a11-139">**INapServerInfo**</span></span>](inapserverinfo.md)
</dt> </dl>

 

 





