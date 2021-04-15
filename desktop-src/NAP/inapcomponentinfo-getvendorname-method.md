---
title: Metodo getvendorname INapComponentInfo (NapCommon. h)
description: Viene utilizzato dal sistema NAP per ottenere il nome del fornitore di un client di integrità.
ms.assetid: 7083b0b6-38fc-4c24-a5f7-fe0a1ebd5e88
keywords:
- Metodo getvendorname NAP
- Metodo getvendorname NAP, interfaccia INapComponentInfo
- Interfaccia NAP di INapComponentInfo, metodo getvendorname
topic_type:
- apiref
api_name:
- INapComponentInfo.GetVendorName
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3c82f4e7e4f76d827e71421c467a8a223428a3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479360"
---
# <a name="inapcomponentinfogetvendorname-method"></a><span data-ttu-id="14c04-106">Metodo INapComponentInfo:: getvendorname</span><span class="sxs-lookup"><span data-stu-id="14c04-106">INapComponentInfo::GetVendorName method</span></span>

> [!Note]  
> <span data-ttu-id="14c04-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="14c04-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="14c04-108">Il metodo di callback **INapComponentInfo:: Getvendorname** viene utilizzato dal sistema NAP per ottenere il nome del fornitore di un client di integrità.</span><span class="sxs-lookup"><span data-stu-id="14c04-108">The **INapComponentInfo::GetVendorName** callback method is used by the NAP System to get the vendor name of a health client.</span></span>

## <a name="syntax"></a><span data-ttu-id="14c04-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="14c04-109">Syntax</span></span>


```C++
HRESULT GetVendorName(
  [out] MessageId *vendorName
);
```



## <a name="parameters"></a><span data-ttu-id="14c04-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="14c04-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14c04-111">*VendorName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="14c04-111">*vendorName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="14c04-112">Puntatore a un [**MessageID**](nap-datatypes.md) che contiene l'ID risorsa del nome del fornitore.</span><span class="sxs-lookup"><span data-stu-id="14c04-112">A pointer to a [**MessageId**](nap-datatypes.md) that contains the resource ID of the vendor name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14c04-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="14c04-113">Return value</span></span>

<span data-ttu-id="14c04-114">Restituisce uno di questi codici di errore in base al risultato di questa operazione.</span><span class="sxs-lookup"><span data-stu-id="14c04-114">Return one of these error codes based on the result of this operation.</span></span>



| <span data-ttu-id="14c04-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="14c04-115">Return code</span></span>                                                                                     | <span data-ttu-id="14c04-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="14c04-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="14c04-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="14c04-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="14c04-118">L'operazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="14c04-118">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="14c04-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="14c04-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="14c04-120">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="14c04-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="14c04-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="14c04-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="14c04-122">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="14c04-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="14c04-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="14c04-123">Requirements</span></span>



| <span data-ttu-id="14c04-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="14c04-124">Requirement</span></span> | <span data-ttu-id="14c04-125">Valore</span><span class="sxs-lookup"><span data-stu-id="14c04-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="14c04-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14c04-126">Minimum supported client</span></span><br/> | <span data-ttu-id="14c04-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="14c04-127">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="14c04-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14c04-128">Minimum supported server</span></span><br/> | <span data-ttu-id="14c04-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="14c04-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="14c04-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="14c04-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="14c04-131"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="14c04-131"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="14c04-132">IDL</span><span class="sxs-lookup"><span data-stu-id="14c04-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="14c04-133"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="14c04-133"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14c04-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="14c04-134">See also</span></span>

<dl> <span data-ttu-id="14c04-135"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="14c04-135"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="14c04-136">**INapComponentInfo**</span><span class="sxs-lookup"><span data-stu-id="14c04-136">**INapComponentInfo**</span></span>](inapcomponentinfo.md)
</dt> </dl>

 

 





