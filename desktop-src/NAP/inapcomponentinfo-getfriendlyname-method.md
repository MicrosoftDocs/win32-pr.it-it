---
title: Metodo GetFriendlyName INapComponentInfo (NapCommon. h)
description: Viene utilizzato dal sistema NAP per ottenere il nome descrittivo di un client di integrità.
ms.assetid: 28614f06-a250-4f92-abf2-422675efd8a0
keywords:
- Metodo GetFriendlyName NAP
- Metodo GetFriendlyName NAP, interfaccia INapComponentInfo
- INapComponentInfo Interface NAP, metodo GetFriendlyName
topic_type:
- apiref
api_name:
- INapComponentInfo.GetFriendlyName
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3848f8fb8365f91bceb5a44c498578f04a1776b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478916"
---
# <a name="inapcomponentinfogetfriendlyname-method"></a><span data-ttu-id="3287f-106">Metodo INapComponentInfo:: GetFriendlyName</span><span class="sxs-lookup"><span data-stu-id="3287f-106">INapComponentInfo::GetFriendlyName method</span></span>

> [!Note]  
> <span data-ttu-id="3287f-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="3287f-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="3287f-108">Il metodo di callback **INapComponentInfo:: GetFriendlyName** viene utilizzato dal sistema NAP per ottenere il nome descrittivo di un client di integrità.</span><span class="sxs-lookup"><span data-stu-id="3287f-108">The **INapComponentInfo::GetFriendlyName** callback method is used by the NAP System to get the friendly name of a health client.</span></span>

## <a name="syntax"></a><span data-ttu-id="3287f-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3287f-109">Syntax</span></span>


```C++
HRESULT GetFriendlyName(
  [out] MessageId *friendlyName
);
```



## <a name="parameters"></a><span data-ttu-id="3287f-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="3287f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3287f-111">*FriendlyName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3287f-111">*friendlyName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3287f-112">Puntatore a un [**MessageID**](nap-datatypes.md) che contiene l'ID risorsa del nome descrittivo.</span><span class="sxs-lookup"><span data-stu-id="3287f-112">A pointer to a [**MessageId**](nap-datatypes.md) that contains the resource ID of the friendly name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3287f-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3287f-113">Return value</span></span>

<span data-ttu-id="3287f-114">Restituisce uno di questi codici di errore in base al risultato di questa operazione.</span><span class="sxs-lookup"><span data-stu-id="3287f-114">Return one of these error codes based on the result of this operation.</span></span>



| <span data-ttu-id="3287f-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="3287f-115">Return code</span></span>                                                                                     | <span data-ttu-id="3287f-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3287f-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="3287f-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3287f-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="3287f-118">L'operazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="3287f-118">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="3287f-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="3287f-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="3287f-120">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="3287f-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="3287f-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="3287f-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="3287f-122">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="3287f-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3287f-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3287f-123">Requirements</span></span>



| <span data-ttu-id="3287f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="3287f-124">Requirement</span></span> | <span data-ttu-id="3287f-125">Valore</span><span class="sxs-lookup"><span data-stu-id="3287f-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3287f-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3287f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3287f-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3287f-127">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3287f-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3287f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3287f-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3287f-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3287f-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3287f-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="3287f-131"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="3287f-131"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="3287f-132">IDL</span><span class="sxs-lookup"><span data-stu-id="3287f-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3287f-133"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3287f-133"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3287f-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3287f-134">See also</span></span>

<dl> <span data-ttu-id="3287f-135"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="3287f-135"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="3287f-136">**INapComponentInfo**</span><span class="sxs-lookup"><span data-stu-id="3287f-136">**INapComponentInfo**</span></span>](inapcomponentinfo.md)
</dt> </dl>

 

 





