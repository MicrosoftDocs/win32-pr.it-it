---
title: Metodo INapComponentInfo ConvertErrorCodeToMessageId (NapCommon. h)
description: Viene utilizzato dal sistema NAP per richiedere che il client di integrità converta un codice di errore HRESULT in un ID messaggio.
ms.assetid: 760dd039-5b9c-4227-9939-ad6ea23f5b81
keywords:
- NAP metodo ConvertErrorCodeToMessageId
- Metodo ConvertErrorCodeToMessageId NAP, interfaccia INapComponentInfo
- Interfaccia INapComponentInfo NAP, metodo ConvertErrorCodeToMessageId
topic_type:
- apiref
api_name:
- INapComponentInfo.ConvertErrorCodeToMessageId
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7ed8eee06ed6bd553ffcce68e76e375dd706238
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478917"
---
# <a name="inapcomponentinfoconverterrorcodetomessageid-method"></a><span data-ttu-id="d5a24-106">Metodo INapComponentInfo:: ConvertErrorCodeToMessageId</span><span class="sxs-lookup"><span data-stu-id="d5a24-106">INapComponentInfo::ConvertErrorCodeToMessageId method</span></span>

> [!Note]  
> <span data-ttu-id="d5a24-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="d5a24-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="d5a24-108">Il metodo di callback **INapComponentInfo:: ConvertErrorCodeToMessageId** viene utilizzato dal sistema NAP per richiedere che il client di integrità converta un codice di errore HRESULT in un ID messaggio.</span><span class="sxs-lookup"><span data-stu-id="d5a24-108">The **INapComponentInfo::ConvertErrorCodeToMessageId** callback method is used by the NAP System to request the health client convert an HRESULT error code into a message ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5a24-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d5a24-109">Syntax</span></span>


```C++
HRESULT ConvertErrorCodeToMessageId(
  [in]  HRESULT   errorCode,
  [out] MessageId *msgId
);
```



## <a name="parameters"></a><span data-ttu-id="d5a24-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="d5a24-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5a24-111">Codice errore  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d5a24-111">*errorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5a24-112">[**Codice di errore**](nap-error-constants.md) del sistema NAP che deve essere convertito in un **MessageID**.</span><span class="sxs-lookup"><span data-stu-id="d5a24-112">The [**error code**](nap-error-constants.md) from the NAP System that is to be converted into a **MessageId**.</span></span>

</dd> <dt>

<span data-ttu-id="d5a24-113">*msgid* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d5a24-113">*msgId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5a24-114">Puntatore a un [**MessageID**](nap-datatypes.md) che contiene l'ID risorsa della stringa localizzata corrispondente.</span><span class="sxs-lookup"><span data-stu-id="d5a24-114">A pointer to a [**MessageId**](nap-datatypes.md) that contains the resource ID of the corresponding localized string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5a24-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d5a24-115">Return value</span></span>

<span data-ttu-id="d5a24-116">Restituisce uno di questi codici di errore in base al risultato di questa operazione.</span><span class="sxs-lookup"><span data-stu-id="d5a24-116">Return one of these error codes based on the result of this operation.</span></span>



| <span data-ttu-id="d5a24-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d5a24-117">Return code</span></span>                                                                                     | <span data-ttu-id="d5a24-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d5a24-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="d5a24-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d5a24-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="d5a24-120">L'operazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="d5a24-120">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="d5a24-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="d5a24-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="d5a24-122">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="d5a24-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="d5a24-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="d5a24-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="d5a24-124">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="d5a24-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d5a24-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="d5a24-125">Remarks</span></span>

<span data-ttu-id="d5a24-126">Il **MessageID** restituito viene utilizzato dal sistema NAP per recuperare una stringa localizzata.</span><span class="sxs-lookup"><span data-stu-id="d5a24-126">The returned **MessageId** is used by the NAP System to retrieve a localized string.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5a24-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d5a24-127">Requirements</span></span>



| <span data-ttu-id="d5a24-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5a24-128">Requirement</span></span> | <span data-ttu-id="d5a24-129">Valore</span><span class="sxs-lookup"><span data-stu-id="d5a24-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5a24-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d5a24-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d5a24-131">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d5a24-131">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d5a24-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d5a24-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d5a24-133">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d5a24-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d5a24-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d5a24-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5a24-135"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5a24-135"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="d5a24-136">IDL</span><span class="sxs-lookup"><span data-stu-id="d5a24-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d5a24-137"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d5a24-137"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5a24-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d5a24-138">See also</span></span>

<dl> <span data-ttu-id="d5a24-139"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="d5a24-139"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="d5a24-140">**INapComponentInfo**</span><span class="sxs-lookup"><span data-stu-id="d5a24-140">**INapComponentInfo**</span></span>](inapcomponentinfo.md)
</dt> </dl>

 

 





