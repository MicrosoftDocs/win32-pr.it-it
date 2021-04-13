---
title: Metodo GetVersion INapComponentInfo (NapCommon. h)
description: Viene utilizzato dal sistema NAP per ottenere la versione di un client di integrità.
ms.assetid: aabd13d9-d2ad-4554-a9f6-7845e6775ccd
keywords:
- Metodo GetVersion NAP
- Metodo GetVersion NAP, interfaccia INapComponentInfo
- Interfaccia INapComponentInfo NAP, Metodo GetVersion
topic_type:
- apiref
api_name:
- INapComponentInfo.GetVersion
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa1d62c22acf778430bfc2f9dc0e969887c7b306
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519181"
---
# <a name="inapcomponentinfogetversion-method"></a><span data-ttu-id="956b2-106">Metodo INapComponentInfo:: GetVersion</span><span class="sxs-lookup"><span data-stu-id="956b2-106">INapComponentInfo::GetVersion method</span></span>

> [!Note]  
> <span data-ttu-id="956b2-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="956b2-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="956b2-108">Il metodo di callback **INapComponentInfo:: GetVersion** viene utilizzato dal sistema NAP per ottenere la versione di un client di integrità.</span><span class="sxs-lookup"><span data-stu-id="956b2-108">The **INapComponentInfo::GetVersion** callback method is used by the NAP System to get the version of a health client.</span></span>

## <a name="syntax"></a><span data-ttu-id="956b2-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="956b2-109">Syntax</span></span>


```C++
HRESULT GetVersion(
  [out] MessageId *version
);
```



## <a name="parameters"></a><span data-ttu-id="956b2-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="956b2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="956b2-111">*versione* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="956b2-111">*version* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="956b2-112">Puntatore a un [**MessageID**](nap-datatypes.md) che contiene l'ID risorsa della versione.</span><span class="sxs-lookup"><span data-stu-id="956b2-112">A pointer to a [**MessageId**](nap-datatypes.md) that contains the resource ID of the version.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="956b2-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="956b2-113">Return value</span></span>

<span data-ttu-id="956b2-114">Restituisce uno di questi codici di errore in base al risultato di questa operazione.</span><span class="sxs-lookup"><span data-stu-id="956b2-114">Return one of these error codes based on the result of this operation.</span></span>



| <span data-ttu-id="956b2-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="956b2-115">Return code</span></span>                                                                                     | <span data-ttu-id="956b2-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="956b2-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="956b2-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="956b2-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="956b2-118">L'operazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="956b2-118">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="956b2-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="956b2-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="956b2-120">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="956b2-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="956b2-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="956b2-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="956b2-122">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="956b2-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="956b2-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="956b2-123">Requirements</span></span>



| <span data-ttu-id="956b2-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="956b2-124">Requirement</span></span> | <span data-ttu-id="956b2-125">Valore</span><span class="sxs-lookup"><span data-stu-id="956b2-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="956b2-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="956b2-126">Minimum supported client</span></span><br/> | <span data-ttu-id="956b2-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="956b2-127">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="956b2-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="956b2-128">Minimum supported server</span></span><br/> | <span data-ttu-id="956b2-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="956b2-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="956b2-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="956b2-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="956b2-131"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="956b2-131"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="956b2-132">IDL</span><span class="sxs-lookup"><span data-stu-id="956b2-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="956b2-133"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="956b2-133"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="956b2-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="956b2-134">See also</span></span>

<dl> <span data-ttu-id="956b2-135"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="956b2-135"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="956b2-136">**INapComponentInfo**</span><span class="sxs-lookup"><span data-stu-id="956b2-136">**INapComponentInfo**</span></span>](inapcomponentinfo.md)
</dt> </dl>

 

 





