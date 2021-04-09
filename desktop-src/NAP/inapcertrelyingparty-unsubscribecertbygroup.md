---
title: Metodo INapCertRelyingParty UnSubscribeCertByGroup (NapCertRelyingParty. h)
description: Annulla la sottoscrizione da un server dei certificati di integrità (HCS).
ms.assetid: 2b26b110-8aba-487e-bd49-c6afc6af11f8
keywords:
- NAP metodo UnSubscribeCertByGroup
- Metodo UnSubscribeCertByGroup NAP, interfaccia INapCertRelyingParty
- Interfaccia INapCertRelyingParty NAP, metodo UnSubscribeCertByGroup
topic_type:
- apiref
api_name:
- INapCertRelyingParty.UnSubscribeCertByGroup
api_location:
- NapCertRelyingParty.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b01bbad5ef48b5f709f93f018c56b5798907d08c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964362"
---
# <a name="inapcertrelyingpartyunsubscribecertbygroup-method"></a><span data-ttu-id="8197a-106">Metodo INapCertRelyingParty:: UnSubscribeCertByGroup</span><span class="sxs-lookup"><span data-stu-id="8197a-106">INapCertRelyingParty::UnSubscribeCertByGroup method</span></span>

> [!Note]  
> <span data-ttu-id="8197a-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="8197a-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="8197a-108">Il metodo **UnSubscribeCertByGroup** Annulla la sottoscrizione da un server dei certificati di integrità (HCS).</span><span class="sxs-lookup"><span data-stu-id="8197a-108">The **UnSubscribeCertByGroup** method unsubscribes from a health certificate server (HCS).</span></span>

## <a name="syntax"></a><span data-ttu-id="8197a-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8197a-109">Syntax</span></span>


```C++
HRESULT UnSubscribeCertByGroup(
  [in]        EnforcementEntityId   id,
  [in] const  VARIANT             * reserved
);
```



## <a name="parameters"></a><span data-ttu-id="8197a-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="8197a-110">Parameters</span></span>

<dl> <dt>

 <span data-ttu-id="8197a-111">*ID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8197a-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8197a-112">Oggetto [**EnforcementEntityId**](nap-datatypes.md) che contiene l'ID del client di imposizione che sta annullando la sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="8197a-112">An [**EnforcementEntityId**](nap-datatypes.md) that contains the ID of the enforcement client that is unsubscribing.</span></span>

</dd> <dt>

 <span data-ttu-id="8197a-113">*riservato* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8197a-113">*reserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8197a-114">Deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="8197a-114">Must be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8197a-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8197a-115">Return value</span></span>

<span data-ttu-id="8197a-116">Restituisce uno dei seguenti codici di errore in base al risultato di questa operazione.</span><span class="sxs-lookup"><span data-stu-id="8197a-116">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="8197a-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="8197a-117">Return code</span></span>                                                                                     | <span data-ttu-id="8197a-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8197a-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="8197a-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8197a-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="8197a-120">L'operazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="8197a-120">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="8197a-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="8197a-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="8197a-122">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="8197a-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="8197a-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="8197a-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="8197a-124">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="8197a-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8197a-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="8197a-125">Remarks</span></span>

<span data-ttu-id="8197a-126">Se non sono presenti altri Sottoscrittori di HCS, NapAgent eliminerà i certificati di integrità corrispondenti dall'archivio del computer locale.</span><span class="sxs-lookup"><span data-stu-id="8197a-126">If there are no other subscribers to the HCS, the NapAgent will delete the corresponding health certificates from the local machine store.</span></span>

<span data-ttu-id="8197a-127">Prima di chiamare questo metodo, chiamare [**SubscribeCertByGroup**](inapcertrelyingparty-subscribecertbygroup.md).</span><span class="sxs-lookup"><span data-stu-id="8197a-127">Before calling this method, call [**SubscribeCertByGroup**](inapcertrelyingparty-subscribecertbygroup.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8197a-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8197a-128">Requirements</span></span>



| <span data-ttu-id="8197a-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="8197a-129">Requirement</span></span> | <span data-ttu-id="8197a-130">Valore</span><span class="sxs-lookup"><span data-stu-id="8197a-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8197a-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8197a-131">Minimum supported client</span></span><br/> | <span data-ttu-id="8197a-132">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8197a-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8197a-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8197a-133">Minimum supported server</span></span><br/> | <span data-ttu-id="8197a-134">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8197a-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="8197a-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8197a-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="8197a-136"><dt>NapCertRelyingParty. h</dt></span><span class="sxs-lookup"><span data-stu-id="8197a-136"><dt>NapCertRelyingParty.h</dt></span></span> </dl>   |
| <span data-ttu-id="8197a-137">IDL</span><span class="sxs-lookup"><span data-stu-id="8197a-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8197a-138"><dt>NapCertRelyingParty. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8197a-138"><dt>NapCertRelyingParty.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8197a-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8197a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8197a-140">**INapCertRelyingParty**</span><span class="sxs-lookup"><span data-stu-id="8197a-140">**INapCertRelyingParty**</span></span>](inapcertrelyingparty.md)
</dt> </dl>

 

 





