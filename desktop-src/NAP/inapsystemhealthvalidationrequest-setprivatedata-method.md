---
title: Metodo INapSystemHealthValidationRequest SetPrivateData (NapSystemHealthValidator. h)
description: Consente all'NapServer di archiviare le informazioni sullo stato.
ms.assetid: 128f9beb-e5da-4b20-bf5e-fcf064209da3
keywords:
- NAP metodo SetPrivateData
- Metodo SetPrivateData NAP, interfaccia INapSystemHealthValidationRequest
- Interfaccia INapSystemHealthValidationRequest NAP, metodo SetPrivateData
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.SetPrivateData
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da50ca236c08388632e17916decee162b3b71743
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742223"
---
# <a name="inapsystemhealthvalidationrequestsetprivatedata-method"></a><span data-ttu-id="50eaa-106">Metodo INapSystemHealthValidationRequest:: SetPrivateData</span><span class="sxs-lookup"><span data-stu-id="50eaa-106">INapSystemHealthValidationRequest::SetPrivateData method</span></span>

> [!Note]  
> <span data-ttu-id="50eaa-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="50eaa-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="50eaa-108">Il metodo **INapSystemHealthValidationRequest:: SetPrivateData** consente al NapServer di archiviare le informazioni sullo stato.</span><span class="sxs-lookup"><span data-stu-id="50eaa-108">The **INapSystemHealthValidationRequest::SetPrivateData** method allows the NapServer to store state information.</span></span>

## <a name="syntax"></a><span data-ttu-id="50eaa-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="50eaa-109">Syntax</span></span>


```C++
HRESULT SetPrivateData(
  [in] const PrivateData *privateData
);
```



## <a name="parameters"></a><span data-ttu-id="50eaa-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="50eaa-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50eaa-111">*PrivateData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="50eaa-111">*privateData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50eaa-112">Puntatore a un BLOB di dati [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) che contiene le informazioni sullo stato opaco.</span><span class="sxs-lookup"><span data-stu-id="50eaa-112">A pointer to a [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) data blob that contains the opaque state information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50eaa-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="50eaa-113">Return value</span></span>

<span data-ttu-id="50eaa-114">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="50eaa-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="50eaa-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="50eaa-115">Return code</span></span>                                                                                     | <span data-ttu-id="50eaa-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="50eaa-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="50eaa-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="50eaa-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="50eaa-118">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="50eaa-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="50eaa-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="50eaa-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="50eaa-120">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="50eaa-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="50eaa-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="50eaa-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="50eaa-122">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="50eaa-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="50eaa-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="50eaa-123">Remarks</span></span>

<span data-ttu-id="50eaa-124">Solo NapServer può interpretare il BLOB di dati.</span><span class="sxs-lookup"><span data-stu-id="50eaa-124">Only the NapServer can interpret the data blob.</span></span>

## <a name="requirements"></a><span data-ttu-id="50eaa-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="50eaa-125">Requirements</span></span>



| <span data-ttu-id="50eaa-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="50eaa-126">Requirement</span></span> | <span data-ttu-id="50eaa-127">Valore</span><span class="sxs-lookup"><span data-stu-id="50eaa-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50eaa-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="50eaa-128">Minimum supported client</span></span><br/> | <span data-ttu-id="50eaa-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="50eaa-129">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="50eaa-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="50eaa-130">Minimum supported server</span></span><br/> | <span data-ttu-id="50eaa-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="50eaa-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="50eaa-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="50eaa-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="50eaa-133"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="50eaa-133"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="50eaa-134">IDL</span><span class="sxs-lookup"><span data-stu-id="50eaa-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="50eaa-135"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="50eaa-135"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="50eaa-136">DLL</span><span class="sxs-lookup"><span data-stu-id="50eaa-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50eaa-137"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50eaa-137"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="50eaa-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="50eaa-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50eaa-139">**INapSystemHealthValidationRequest**</span><span class="sxs-lookup"><span data-stu-id="50eaa-139">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





