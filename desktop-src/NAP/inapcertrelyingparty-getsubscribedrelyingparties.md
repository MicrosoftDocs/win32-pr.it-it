---
title: Metodo INapCertRelyingParty GetSubscribedRelyingParties (NapCertRelyingParty. h)
description: Ottiene un elenco di relying party che hanno sottoscritto.
ms.assetid: 7eef28fd-71cd-4765-89a5-2c9ce29fdc00
keywords:
- NAP metodo GetSubscribedRelyingParties
- Metodo GetSubscribedRelyingParties NAP, interfaccia INapCertRelyingParty
- Interfaccia INapCertRelyingParty NAP, metodo GetSubscribedRelyingParties
topic_type:
- apiref
api_name:
- INapCertRelyingParty.GetSubscribedRelyingParties
api_location:
- NapCertRelyingParty.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a84871838324c431278d15bb9e78471f48aa1f34
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475490"
---
# <a name="inapcertrelyingpartygetsubscribedrelyingparties-method"></a><span data-ttu-id="f629b-106">Metodo INapCertRelyingParty:: GetSubscribedRelyingParties</span><span class="sxs-lookup"><span data-stu-id="f629b-106">INapCertRelyingParty::GetSubscribedRelyingParties method</span></span>

> [!Note]  
> <span data-ttu-id="f629b-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="f629b-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="f629b-108">Il metodo **GetSubscribedRelyingParties** ottiene un elenco di relying party che hanno sottoscritto.</span><span class="sxs-lookup"><span data-stu-id="f629b-108">The **GetSubscribedRelyingParties** method gets a list of relying parties that have subscribed.</span></span>

## <a name="syntax"></a><span data-ttu-id="f629b-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f629b-109">Syntax</span></span>


```C++
HRESULT GetSubscribedRelyingParties(
  [out] EnforcementEntityCount *count,
  [out]  EnforcementEntityId   **relyingParties
);
```



## <a name="parameters"></a><span data-ttu-id="f629b-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="f629b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f629b-111">*numero* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="f629b-111">*count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f629b-112">Puntatore a un [**EnforcementEntityCount**](nap-datatypes.md) contenente il numero di relying party sottoscritti.</span><span class="sxs-lookup"><span data-stu-id="f629b-112">A pointer to a [**EnforcementEntityCount**](nap-datatypes.md) that contains the number of subscribed relying parties.</span></span>

</dd> <dt>

<span data-ttu-id="f629b-113">*relyingParties* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f629b-113">*relyingParties* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f629b-114">Puntatore a un puntatore a un [**EnforcementEntityId**](nap-datatypes.md) che contiene l'elenco di relying party sottoscritti.</span><span class="sxs-lookup"><span data-stu-id="f629b-114">A pointer to a pointer to an [**EnforcementEntityId**](nap-datatypes.md) that contains the list of subscribed relying parties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f629b-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f629b-115">Return value</span></span>

<span data-ttu-id="f629b-116">Restituisce uno dei seguenti codici di errore in base al risultato di questa operazione.</span><span class="sxs-lookup"><span data-stu-id="f629b-116">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="f629b-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="f629b-117">Return code</span></span>                                                                                     | <span data-ttu-id="f629b-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f629b-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="f629b-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f629b-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="f629b-120">L'operazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="f629b-120">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="f629b-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="f629b-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="f629b-122">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="f629b-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="f629b-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f629b-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="f629b-124">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="f629b-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f629b-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="f629b-125">Remarks</span></span>

<span data-ttu-id="f629b-126">Il chiamante deve liberare il parametro *relyingParties* usando **CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="f629b-126">The caller must free the *relyingParties* parameter using **CoTaskMemFree**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f629b-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f629b-127">Requirements</span></span>



| <span data-ttu-id="f629b-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f629b-128">Requirement</span></span> | <span data-ttu-id="f629b-129">Valore</span><span class="sxs-lookup"><span data-stu-id="f629b-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f629b-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f629b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f629b-131">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f629b-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f629b-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f629b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f629b-133">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f629b-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f629b-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f629b-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="f629b-135"><dt>NapCertRelyingParty. h</dt></span><span class="sxs-lookup"><span data-stu-id="f629b-135"><dt>NapCertRelyingParty.h</dt></span></span> </dl>   |
| <span data-ttu-id="f629b-136">IDL</span><span class="sxs-lookup"><span data-stu-id="f629b-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f629b-137"><dt>NapCertRelyingParty. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f629b-137"><dt>NapCertRelyingParty.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f629b-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f629b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f629b-139">**INapCertRelyingParty**</span><span class="sxs-lookup"><span data-stu-id="f629b-139">**INapCertRelyingParty**</span></span>](inapcertrelyingparty.md)
</dt> </dl>

 

 





