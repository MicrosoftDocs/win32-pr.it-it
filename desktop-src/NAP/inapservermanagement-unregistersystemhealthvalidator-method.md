---
title: Metodo INapServerManagement UnregisterSystemHealthValidator (NapServerManagement. h)
description: Viene utilizzato per annullare la registrazione di un servizio di convalida integrità di sistema con il server NAP.
ms.assetid: f4148df1-a230-4845-ac8b-9e04be9e0d6c
keywords:
- NAP metodo UnregisterSystemHealthValidator
- Metodo UnregisterSystemHealthValidator NAP, interfaccia INapServerManagement
- Interfaccia INapServerManagement NAP, metodo UnregisterSystemHealthValidator
topic_type:
- apiref
api_name:
- INapServerManagement.UnregisterSystemHealthValidator
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0715445504b862d9ae9e8478b543f8e80378f08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518628"
---
# <a name="inapservermanagementunregistersystemhealthvalidator-method"></a><span data-ttu-id="fa329-106">Metodo INapServerManagement:: UnregisterSystemHealthValidator</span><span class="sxs-lookup"><span data-stu-id="fa329-106">INapServerManagement::UnregisterSystemHealthValidator method</span></span>

> [!Note]  
> <span data-ttu-id="fa329-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="fa329-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="fa329-108">Il metodo **INapServerManagement:: UnregisterSystemHealthValidator** viene usato per annullare la registrazione di un servizio di convalida dell'integrità di sistema con il server NAP.</span><span class="sxs-lookup"><span data-stu-id="fa329-108">The **INapServerManagement::UnregisterSystemHealthValidator** method is used to unregister an SHV with the NAP server.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa329-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fa329-109">Syntax</span></span>


```C++
HRESULT UnregisterSystemHealthValidator(
  [in] SystemHealthEntityId id
);
```



## <a name="parameters"></a><span data-ttu-id="fa329-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="fa329-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa329-111">*ID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fa329-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa329-112">Oggetto [**SystemHealthEntityId**](nap-type-constants.md) che contiene l'identificatore univoco del servizio di convalida dell'integrità di cui annullare la registrazione.</span><span class="sxs-lookup"><span data-stu-id="fa329-112">A [**SystemHealthEntityId**](nap-type-constants.md) that contains the unique identifier of the SHV to unregister.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa329-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fa329-113">Return value</span></span>

<span data-ttu-id="fa329-114">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="fa329-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="fa329-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="fa329-115">Return code</span></span>                                                                                     | <span data-ttu-id="fa329-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fa329-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="fa329-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fa329-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="fa329-118">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="fa329-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="fa329-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="fa329-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="fa329-120">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="fa329-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="fa329-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="fa329-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="fa329-122">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="fa329-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fa329-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="fa329-123">Remarks</span></span>

<span data-ttu-id="fa329-124">Se sono presenti chiamate asincrone in sospeso per il servizio di convalida dell'integrità di sistema, verranno completate in un secondo momento e verranno ignorate.</span><span class="sxs-lookup"><span data-stu-id="fa329-124">If there are any asynchronous calls pending on the SHV, they will complete at a later time and will be discarded.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa329-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fa329-125">Requirements</span></span>



| <span data-ttu-id="fa329-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa329-126">Requirement</span></span> | <span data-ttu-id="fa329-127">Valore</span><span class="sxs-lookup"><span data-stu-id="fa329-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa329-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fa329-128">Minimum supported client</span></span><br/> | <span data-ttu-id="fa329-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="fa329-129">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="fa329-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fa329-130">Minimum supported server</span></span><br/> | <span data-ttu-id="fa329-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fa329-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="fa329-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fa329-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa329-133"><dt>NapServerManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa329-133"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="fa329-134">IDL</span><span class="sxs-lookup"><span data-stu-id="fa329-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fa329-135"><dt>NapServerManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fa329-135"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="fa329-136">DLL</span><span class="sxs-lookup"><span data-stu-id="fa329-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa329-137"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa329-137"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="fa329-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fa329-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa329-139">**INapServerManagement**</span><span class="sxs-lookup"><span data-stu-id="fa329-139">**INapServerManagement**</span></span>](inapservermanagement.md)
</dt> </dl>

 

 





