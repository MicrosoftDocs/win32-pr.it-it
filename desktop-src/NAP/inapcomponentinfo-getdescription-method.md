---
title: Metodo GetDescription INapComponentInfo (NapCommon. h)
description: Viene utilizzato dal sistema NAP per ottenere la descrizione di un client di integrità.
ms.assetid: f8d1d5ea-0de6-426d-90eb-b035b5bd0bfd
keywords:
- Metodo GetDescription NAP
- Metodo GetDescription NAP, interfaccia INapComponentInfo
- Interfaccia NAP di INapComponentInfo, metodo GetDescription
topic_type:
- apiref
api_name:
- INapComponentInfo.GetDescription
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 499aee6f7805925cc68c08b580db7b1b72763165
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301067"
---
# <a name="inapcomponentinfogetdescription-method"></a><span data-ttu-id="30439-106">Metodo INapComponentInfo:: GetDescription</span><span class="sxs-lookup"><span data-stu-id="30439-106">INapComponentInfo::GetDescription method</span></span>

> [!Note]  
> <span data-ttu-id="30439-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="30439-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="30439-108">Il metodo di callback **INapComponentInfo:: GetDescription** viene utilizzato dal sistema NAP per ottenere la descrizione di un client di integrità.</span><span class="sxs-lookup"><span data-stu-id="30439-108">The **INapComponentInfo::GetDescription** callback method is used by the NAP System to get the description of a health client.</span></span>

## <a name="syntax"></a><span data-ttu-id="30439-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="30439-109">Syntax</span></span>


```C++
HRESULT GetDescription(
  [out] MessageId *description
);
```



## <a name="parameters"></a><span data-ttu-id="30439-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="30439-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30439-111">*Descrizione* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="30439-111">*description* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="30439-112">Puntatore a un [**MessageID**](nap-datatypes.md) che contiene l'ID risorsa della descrizione.</span><span class="sxs-lookup"><span data-stu-id="30439-112">A pointer to a [**MessageId**](nap-datatypes.md) that contains the resource ID of the description.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30439-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="30439-113">Return value</span></span>

<span data-ttu-id="30439-114">Restituisce uno di questi codici di errore in base al risultato di questa operazione.</span><span class="sxs-lookup"><span data-stu-id="30439-114">Return one of these error codes based on the result of this operation.</span></span>



| <span data-ttu-id="30439-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="30439-115">Return code</span></span>                                                                                     | <span data-ttu-id="30439-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="30439-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="30439-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="30439-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="30439-118">L'operazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="30439-118">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="30439-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="30439-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="30439-120">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="30439-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="30439-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="30439-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="30439-122">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="30439-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="30439-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="30439-123">Requirements</span></span>



| <span data-ttu-id="30439-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="30439-124">Requirement</span></span> | <span data-ttu-id="30439-125">Valore</span><span class="sxs-lookup"><span data-stu-id="30439-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="30439-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="30439-126">Minimum supported client</span></span><br/> | <span data-ttu-id="30439-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="30439-127">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="30439-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="30439-128">Minimum supported server</span></span><br/> | <span data-ttu-id="30439-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="30439-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="30439-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="30439-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="30439-131"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="30439-131"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="30439-132">IDL</span><span class="sxs-lookup"><span data-stu-id="30439-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="30439-133"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="30439-133"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30439-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="30439-134">See also</span></span>

<dl> <span data-ttu-id="30439-135"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="30439-135"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="30439-136">**INapComponentInfo**</span><span class="sxs-lookup"><span data-stu-id="30439-136">**INapComponentInfo**</span></span>](inapcomponentinfo.md)
</dt> </dl>

 

 





