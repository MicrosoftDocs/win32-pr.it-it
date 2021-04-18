---
title: Metodo INapCertRelyingParty SubscribeCertByGroup (NapCertRelyingParty. h)
description: Sottoscrive un server di certificazione integrità (HCS).
ms.assetid: 6fce113d-e183-45d7-8fb5-e04b6f4afcca
keywords:
- NAP metodo SubscribeCertByGroup
- Metodo SubscribeCertByGroup NAP, interfaccia INapCertRelyingParty
- Interfaccia INapCertRelyingParty NAP, metodo SubscribeCertByGroup
topic_type:
- apiref
api_name:
- INapCertRelyingParty.SubscribeCertByGroup
api_location:
- NapCertRelyingParty.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 053c3c2dbf00e706003988bd5769cb2aa9201c41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301814"
---
# <a name="inapcertrelyingpartysubscribecertbygroup-method"></a><span data-ttu-id="7dca0-106">Metodo INapCertRelyingParty:: SubscribeCertByGroup</span><span class="sxs-lookup"><span data-stu-id="7dca0-106">INapCertRelyingParty::SubscribeCertByGroup method</span></span>

> [!Note]  
> <span data-ttu-id="7dca0-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="7dca0-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="7dca0-108">Il metodo **SubscribeCertByGroup** sottoscrive un server dei certificati di integrità (HCS).</span><span class="sxs-lookup"><span data-stu-id="7dca0-108">The **SubscribeCertByGroup** method subscribes to a health certificate server (HCS).</span></span> <span data-ttu-id="7dca0-109">HCS deve essere già registrato prima della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="7dca0-109">The HCS must already be registered before subscribing.</span></span>

## <a name="syntax"></a><span data-ttu-id="7dca0-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7dca0-110">Syntax</span></span>


```C++
HRESULT SubscribeCertByGroup(
  [in]        EnforcementEntityId  id,
  [in]  const BSTR                subscriberName,
  [in]  const  VARIANT            *reserved,
  [out]       BOOL                *certExists
);
```



## <a name="parameters"></a><span data-ttu-id="7dca0-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="7dca0-111">Parameters</span></span>

<dl> <dt>

 <span data-ttu-id="7dca0-112">*ID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7dca0-112">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7dca0-113">Oggetto [**EnforcementEntityId**](nap-datatypes.md) che contiene l'ID del client di imposizione che sta sottoscrivendo.</span><span class="sxs-lookup"><span data-stu-id="7dca0-113">An [**EnforcementEntityId**](nap-datatypes.md) that contains the ID of the enforcement client that is subscribing.</span></span>

</dd> <dt>

<span data-ttu-id="7dca0-114">*subscriberName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7dca0-114">*subscriberName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7dca0-115">Nome del Sottoscrittore.</span><span class="sxs-lookup"><span data-stu-id="7dca0-115">The name of the subscriber.</span></span>

> [!Note]  
> <span data-ttu-id="7dca0-116">Attualmente viene usato solo a scopo di registrazione.</span><span class="sxs-lookup"><span data-stu-id="7dca0-116">This is currently only used for logging purposes.</span></span>

 

</dd> <dt>

<span data-ttu-id="7dca0-117">*riservato* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7dca0-117">*reserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7dca0-118">Deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="7dca0-118">Must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7dca0-119">*certExists* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7dca0-119">*certExists* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7dca0-120">Indica se un certificato di integrità di questo HCS è già gestito da NapAgent ed è presente nell'archivio del computer.</span><span class="sxs-lookup"><span data-stu-id="7dca0-120">Indicates whether a health certificate from this HCS is already being maintained by the NapAgent and is present in the machine store.</span></span> <span data-ttu-id="7dca0-121">Se **true**, un certificato di integrità è già in fase di manutenzione ed è presente.</span><span class="sxs-lookup"><span data-stu-id="7dca0-121">If **TRUE**, a health certificate is already being maintained and is present.</span></span> <span data-ttu-id="7dca0-122">Se **false**, un certificato di integrità non viene attualmente mantenuto e presente.</span><span class="sxs-lookup"><span data-stu-id="7dca0-122">If **FALSE**, a health certificate is not currently being maintained and present.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7dca0-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7dca0-123">Return value</span></span>

<span data-ttu-id="7dca0-124">Restituisce uno dei seguenti codici di errore in base al risultato di questa operazione.</span><span class="sxs-lookup"><span data-stu-id="7dca0-124">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="7dca0-125">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="7dca0-125">Return code</span></span>                                                                                     | <span data-ttu-id="7dca0-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7dca0-126">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="7dca0-127"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7dca0-127"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="7dca0-128">L'operazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="7dca0-128">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="7dca0-129"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="7dca0-129"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="7dca0-130">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="7dca0-130">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="7dca0-131"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="7dca0-131"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="7dca0-132">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="7dca0-132">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7dca0-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7dca0-133">Requirements</span></span>



| <span data-ttu-id="7dca0-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="7dca0-134">Requirement</span></span> | <span data-ttu-id="7dca0-135">Valore</span><span class="sxs-lookup"><span data-stu-id="7dca0-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7dca0-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7dca0-136">Minimum supported client</span></span><br/> | <span data-ttu-id="7dca0-137">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7dca0-137">Windows Vista \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7dca0-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7dca0-138">Minimum supported server</span></span><br/> | <span data-ttu-id="7dca0-139">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7dca0-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7dca0-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7dca0-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="7dca0-141"><dt>NapCertRelyingParty. h</dt></span><span class="sxs-lookup"><span data-stu-id="7dca0-141"><dt>NapCertRelyingParty.h</dt></span></span> </dl>   |
| <span data-ttu-id="7dca0-142">IDL</span><span class="sxs-lookup"><span data-stu-id="7dca0-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7dca0-143"><dt>NapCertRelyingParty. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7dca0-143"><dt>NapCertRelyingParty.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7dca0-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7dca0-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7dca0-145">**INapCertRelyingParty**</span><span class="sxs-lookup"><span data-stu-id="7dca0-145">**INapCertRelyingParty**</span></span>](inapcertrelyingparty.md)
</dt> </dl>

 

 





