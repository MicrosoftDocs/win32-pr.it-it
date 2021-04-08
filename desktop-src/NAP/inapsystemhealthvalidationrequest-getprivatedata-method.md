---
title: Metodo INapSystemHealthValidationRequest GetPrivateData (NapSystemHealthValidator. h)
description: Consente al NapServer di recuperare le informazioni sullo stato.
ms.assetid: f85026ca-852b-4eb1-9a8c-7e03cd1765f2
keywords:
- NAP metodo GetPrivateData
- Metodo GetPrivateData NAP, interfaccia INapSystemHealthValidationRequest
- Interfaccia INapSystemHealthValidationRequest NAP, metodo GetPrivateData
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetPrivateData
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d78cceba42cd503ef8a875ece8f4ed196eaeff8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743346"
---
# <a name="inapsystemhealthvalidationrequestgetprivatedata-method"></a><span data-ttu-id="a789b-106">Metodo INapSystemHealthValidationRequest:: GetPrivateData</span><span class="sxs-lookup"><span data-stu-id="a789b-106">INapSystemHealthValidationRequest::GetPrivateData method</span></span>

> [!Note]  
> <span data-ttu-id="a789b-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="a789b-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="a789b-108">Il metodo **INapSystemHealthValidationRequest:: GetPrivateData** consente al NapServer di recuperare le informazioni sullo stato.</span><span class="sxs-lookup"><span data-stu-id="a789b-108">The **INapSystemHealthValidationRequest::GetPrivateData** method allows the NapServer to retrieve state information.</span></span>

## <a name="syntax"></a><span data-ttu-id="a789b-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a789b-109">Syntax</span></span>


```C++
HRESULT GetPrivateData(
  [out] PrivateData **privateData
);
```



## <a name="parameters"></a><span data-ttu-id="a789b-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="a789b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a789b-111">*PrivateData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a789b-111">*privateData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a789b-112">Puntatore a un puntatore a un BLOB di dati opachi [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) che contiene le informazioni sullo stato.</span><span class="sxs-lookup"><span data-stu-id="a789b-112">A pointer to a pointer to [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) opaque data blob that contains state information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a789b-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a789b-113">Return value</span></span>

<span data-ttu-id="a789b-114">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="a789b-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="a789b-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="a789b-115">Return code</span></span>                                                                                     | <span data-ttu-id="a789b-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a789b-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="a789b-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a789b-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="a789b-118">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="a789b-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="a789b-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="a789b-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="a789b-120">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="a789b-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="a789b-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a789b-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="a789b-122">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="a789b-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a789b-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="a789b-123">Remarks</span></span>

<span data-ttu-id="a789b-124">Solo NapServer può interpretare il BLOB di dati.</span><span class="sxs-lookup"><span data-stu-id="a789b-124">Only the NapServer can interpret the data blob.</span></span>

## <a name="requirements"></a><span data-ttu-id="a789b-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a789b-125">Requirements</span></span>



| <span data-ttu-id="a789b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a789b-126">Requirement</span></span> | <span data-ttu-id="a789b-127">Valore</span><span class="sxs-lookup"><span data-stu-id="a789b-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a789b-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a789b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a789b-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a789b-129">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="a789b-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a789b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a789b-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a789b-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a789b-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a789b-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="a789b-133"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="a789b-133"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="a789b-134">IDL</span><span class="sxs-lookup"><span data-stu-id="a789b-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a789b-135"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a789b-135"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="a789b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a789b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a789b-137"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a789b-137"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="a789b-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a789b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a789b-139">**INapSystemHealthValidationRequest**</span><span class="sxs-lookup"><span data-stu-id="a789b-139">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





