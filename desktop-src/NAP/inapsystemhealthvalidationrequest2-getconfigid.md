---
title: Metodo INapSystemHealthValidationRequest2 GetConfigID (NapSystemHealthValidator. h)
description: Utilizzato dai validator di integrità del sistema (SHV) per recuperare l'ID configurazione in una richiesta di convalida.
ms.assetid: 6d5564e4-8386-444b-a859-f0c855e4ee30
keywords:
- NAP metodo GetConfigID
- Metodo GetConfigID NAP, interfaccia INapSystemHealthValidationRequest2
- Interfaccia INapSystemHealthValidationRequest2 NAP, metodo GetConfigID
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest2.GetConfigID
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f3b41d2f08dc117fd28e704d607c628ec73e6ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302580"
---
# <a name="inapsystemhealthvalidationrequest2getconfigid-method"></a><span data-ttu-id="35575-106">Metodo INapSystemHealthValidationRequest2:: GetConfigID</span><span class="sxs-lookup"><span data-stu-id="35575-106">INapSystemHealthValidationRequest2::GetConfigID method</span></span>

> [!Note]  
> <span data-ttu-id="35575-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="35575-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="35575-108">Il metodo **INapSystemHealthValidationRequest2:: GetConfigId** viene usato da convalida integrità sistema (SHV) per recuperare l'ID configurazione in una richiesta di convalida.</span><span class="sxs-lookup"><span data-stu-id="35575-108">The **INapSystemHealthValidationRequest2::GetConfigId** method is used by the System Health Validators (SHVs) to retrieve the configuration ID in a validation request.</span></span>

## <a name="syntax"></a><span data-ttu-id="35575-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="35575-109">Syntax</span></span>


```C++
HRESULT GetConfigID(
  [out] UINT32 *configID
) const;
```



## <a name="parameters"></a><span data-ttu-id="35575-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="35575-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35575-111">*configID* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="35575-111">*configID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="35575-112">Al ritorno, un puntatore a UINT32 che contiene un ID di configurazione di convalida integrità di sistema.</span><span class="sxs-lookup"><span data-stu-id="35575-112">On return, a pointer to UINT32 that contains a configuration ID of the SHV.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35575-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="35575-113">Return value</span></span>

<span data-ttu-id="35575-114">Restituisce uno dei seguenti codici di errore in base al risultato di questa operazione.</span><span class="sxs-lookup"><span data-stu-id="35575-114">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="35575-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="35575-115">Return code</span></span>                                                                                  | <span data-ttu-id="35575-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="35575-116">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="35575-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="35575-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="35575-118">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="35575-118">Operation successful.</span></span><br/>                |
| <dl> <span data-ttu-id="35575-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="35575-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="35575-120">Il parametro configID è **null**.</span><span class="sxs-lookup"><span data-stu-id="35575-120">The configID parameter was **NULL**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="35575-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="35575-121">Requirements</span></span>



| <span data-ttu-id="35575-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="35575-122">Requirement</span></span> | <span data-ttu-id="35575-123">Valore</span><span class="sxs-lookup"><span data-stu-id="35575-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35575-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35575-124">Minimum supported client</span></span><br/> | <span data-ttu-id="35575-125">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="35575-125">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="35575-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35575-126">Minimum supported server</span></span><br/> | <span data-ttu-id="35575-127">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="35575-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="35575-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="35575-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="35575-129"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="35575-129"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="35575-130">IDL</span><span class="sxs-lookup"><span data-stu-id="35575-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="35575-131"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="35575-131"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="35575-132">DLL</span><span class="sxs-lookup"><span data-stu-id="35575-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35575-133"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35575-133"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="35575-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="35575-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35575-135">**INapSystemHealthValidationRequest2**</span><span class="sxs-lookup"><span data-stu-id="35575-135">**INapSystemHealthValidationRequest2**</span></span>](inapsystemhealthvalidationrequest2.md)
</dt> </dl>

 

 





