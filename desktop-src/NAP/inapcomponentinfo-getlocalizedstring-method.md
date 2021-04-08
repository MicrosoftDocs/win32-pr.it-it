---
title: Metodo INapComponentInfo GetLocalizedString (NapCommon. h)
description: Viene utilizzato dal sistema NAP per ottenere le stringhe localizzate.
ms.assetid: ad5be180-6329-4c91-b4d1-871a4d83c323
keywords:
- NAP metodo GetLocalizedString
- Metodo GetLocalizedString NAP, interfaccia INapComponentInfo
- Interfaccia INapComponentInfo NAP, metodo GetLocalizedString
topic_type:
- apiref
api_name:
- INapComponentInfo.GetLocalizedString
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 781e4e8c93f58039c72a98f40a529243e5722d23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964984"
---
# <a name="inapcomponentinfogetlocalizedstring-method"></a><span data-ttu-id="f16bd-106">Metodo INapComponentInfo:: GetLocalizedString</span><span class="sxs-lookup"><span data-stu-id="f16bd-106">INapComponentInfo::GetLocalizedString method</span></span>

> [!Note]  
> <span data-ttu-id="f16bd-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="f16bd-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="f16bd-108">Il metodo di callback **INapComponentInfo:: GetLocalizedString** viene utilizzato dal sistema NAP per ottenere le stringhe localizzate.</span><span class="sxs-lookup"><span data-stu-id="f16bd-108">The **INapComponentInfo::GetLocalizedString** callback method is used by the NAP System to get localized strings.</span></span>

## <a name="syntax"></a><span data-ttu-id="f16bd-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f16bd-109">Syntax</span></span>


```C++
HRESULT GetLocalizedString(
  [in]  MessageId     msgId,
  [out] CountedString **string
);
```



## <a name="parameters"></a><span data-ttu-id="f16bd-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="f16bd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f16bd-111">*msgid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f16bd-111">*msgId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f16bd-112">[**MessageID**](nap-datatypes.md) che contiene l'ID risorsa della stringa da localizzare.</span><span class="sxs-lookup"><span data-stu-id="f16bd-112">A [**MessageId**](nap-datatypes.md) that contains the resource ID of the string to localize.</span></span>

</dd> <dt>

<span data-ttu-id="f16bd-113">*stringa* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="f16bd-113">*string* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f16bd-114">Puntatore a un puntatore a un [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) che contiene la versione localizzata del messaggio.</span><span class="sxs-lookup"><span data-stu-id="f16bd-114">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) that contains the localized version of the message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f16bd-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f16bd-115">Return value</span></span>

<span data-ttu-id="f16bd-116">Restituisce uno di questi codici di errore in base al risultato di questa operazione.</span><span class="sxs-lookup"><span data-stu-id="f16bd-116">Return one of these error codes based on the result of this operation.</span></span>



| <span data-ttu-id="f16bd-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="f16bd-117">Return code</span></span>                                                                                     | <span data-ttu-id="f16bd-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f16bd-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="f16bd-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f16bd-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="f16bd-120">L'operazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="f16bd-120">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="f16bd-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="f16bd-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="f16bd-122">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="f16bd-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="f16bd-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f16bd-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="f16bd-124">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="f16bd-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f16bd-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="f16bd-125">Remarks</span></span>

<span data-ttu-id="f16bd-126">Le stringhe devono essere localizzate in base all'ID lingua del thread chiamante.</span><span class="sxs-lookup"><span data-stu-id="f16bd-126">Strings should be localized according to the calling thread's language-id.</span></span>

## <a name="requirements"></a><span data-ttu-id="f16bd-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f16bd-127">Requirements</span></span>



| <span data-ttu-id="f16bd-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f16bd-128">Requirement</span></span> | <span data-ttu-id="f16bd-129">Valore</span><span class="sxs-lookup"><span data-stu-id="f16bd-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f16bd-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f16bd-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f16bd-131">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f16bd-131">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f16bd-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f16bd-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f16bd-133">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f16bd-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f16bd-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f16bd-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="f16bd-135"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f16bd-135"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="f16bd-136">IDL</span><span class="sxs-lookup"><span data-stu-id="f16bd-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f16bd-137"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f16bd-137"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f16bd-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f16bd-138">See also</span></span>

<dl> <span data-ttu-id="f16bd-139"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="f16bd-139"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="f16bd-140">**INapComponentInfo**</span><span class="sxs-lookup"><span data-stu-id="f16bd-140">**INapComponentInfo**</span></span>](inapcomponentinfo.md)
</dt> </dl>

 

 





