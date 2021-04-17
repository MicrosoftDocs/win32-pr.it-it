---
title: Metodo OnComplete INapServerCallback (NapSystemHealthValidator. h)
description: Usato da SHV per segnalare il completamento della richiesta asincrona.
ms.assetid: 959ee4ac-7c29-4013-a174-24abc6a580c7
keywords:
- Metodo OnComplete NAP
- Metodo OnComplete NAP, interfaccia INapServerCallback
- Interfaccia NAP di INapServerCallback, metodo OnComplete
topic_type:
- apiref
api_name:
- INapServerCallback.OnComplete
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ef846d3d9dc2d6618f0eca9f097d74222606eb4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479343"
---
# <a name="inapservercallbackoncomplete-method"></a><span data-ttu-id="61a5a-106">Metodo INapServerCallback:: OnComplete</span><span class="sxs-lookup"><span data-stu-id="61a5a-106">INapServerCallback::OnComplete method</span></span>

> [!Note]  
> <span data-ttu-id="61a5a-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="61a5a-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="61a5a-108">Il metodo **INapServerCallback:: OnComplete** viene usato da SHV per segnalare il completamento della richiesta asincrona.</span><span class="sxs-lookup"><span data-stu-id="61a5a-108">The **INapServerCallback::OnComplete** method is used by SHVs to signal asynchronous request completion.</span></span>

## <a name="syntax"></a><span data-ttu-id="61a5a-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="61a5a-109">Syntax</span></span>


```C++
HRESULT OnComplete(
  [in] INapSystemHealthValidationRequest *request,
  [in] HRESULT                           errorCode
);
```



## <a name="parameters"></a><span data-ttu-id="61a5a-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="61a5a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61a5a-111">*richiesta* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="61a5a-111">*request* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61a5a-112">Puntatore a un oggetto [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) che rappresenta una richiesta di convalida.</span><span class="sxs-lookup"><span data-stu-id="61a5a-112">A pointer to an [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) object that represents a validation request.</span></span>

</dd> <dt>

<span data-ttu-id="61a5a-113">Codice errore  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="61a5a-113">*errorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61a5a-114">[**Codice di errore di protezione accesso alla rete**](nap-error-constants.md) che indica il motivo per cui non è stato possibile eseguire la convalida.</span><span class="sxs-lookup"><span data-stu-id="61a5a-114">A [**NAP error code**](nap-error-constants.md) that indicates the reason why the validation could not be performed.</span></span>

> [!Note]  
> <span data-ttu-id="61a5a-115">In genere, il valore restituito del metodo [**INapSystemHealthValidationRequest:: SetSoHResponse**](inapsystemhealthvalidationrequest-setsohresponse-method.md) viene passato a questo parametro.</span><span class="sxs-lookup"><span data-stu-id="61a5a-115">Typically, the return value of the [**INapSystemHealthValidationRequest::SetSoHResponse**](inapsystemhealthvalidationrequest-setsohresponse-method.md) method is passed to this parameter.</span></span> <span data-ttu-id="61a5a-116">Tuttavia, se non è possibile chiamare **SetSoHResponse** a causa di un errore di rielaborazione, viene passato il valore restituito dal comando non riuscito.</span><span class="sxs-lookup"><span data-stu-id="61a5a-116">However, if **SetSoHResponse** could not be called due to a reprocessing failure, the value returned by the failed command is passed.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61a5a-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="61a5a-117">Return value</span></span>

<span data-ttu-id="61a5a-118">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="61a5a-118">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="61a5a-119">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="61a5a-119">Return code</span></span>                                                                                     | <span data-ttu-id="61a5a-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="61a5a-120">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="61a5a-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="61a5a-121"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="61a5a-122">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="61a5a-122">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="61a5a-123"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="61a5a-123"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="61a5a-124">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="61a5a-124">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="61a5a-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="61a5a-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="61a5a-126">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="61a5a-126">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="61a5a-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="61a5a-127">Remarks</span></span>

<span data-ttu-id="61a5a-128">I validator devono restituire S \_ OK se la convalida [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) può essere completata, indipendentemente dal fatto che il **SoHRequest** abbia superato il controllo di integrità.</span><span class="sxs-lookup"><span data-stu-id="61a5a-128">Validators must return S\_OK if the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) validation could be completed, regardless of whether the **SoHRequest** passed the health check.</span></span>

## <a name="requirements"></a><span data-ttu-id="61a5a-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="61a5a-129">Requirements</span></span>



| <span data-ttu-id="61a5a-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="61a5a-130">Requirement</span></span> | <span data-ttu-id="61a5a-131">Valore</span><span class="sxs-lookup"><span data-stu-id="61a5a-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61a5a-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="61a5a-132">Minimum supported client</span></span><br/> | <span data-ttu-id="61a5a-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="61a5a-133">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="61a5a-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="61a5a-134">Minimum supported server</span></span><br/> | <span data-ttu-id="61a5a-135">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="61a5a-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="61a5a-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="61a5a-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="61a5a-137"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="61a5a-137"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="61a5a-138">IDL</span><span class="sxs-lookup"><span data-stu-id="61a5a-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="61a5a-139"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="61a5a-139"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="61a5a-140">DLL</span><span class="sxs-lookup"><span data-stu-id="61a5a-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61a5a-141"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61a5a-141"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="61a5a-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="61a5a-142">See also</span></span>

<dl> <span data-ttu-id="61a5a-143"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="61a5a-143"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="61a5a-144">**INapServerCallback**</span><span class="sxs-lookup"><span data-stu-id="61a5a-144">**INapServerCallback**</span></span>](inapservercallback.md)
</dt> <dt>

[<span data-ttu-id="61a5a-145">**INapSystemHealthValidationRequest**</span><span class="sxs-lookup"><span data-stu-id="61a5a-145">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





