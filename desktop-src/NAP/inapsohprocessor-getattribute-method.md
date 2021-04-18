---
title: Metodo GetAttribute INapSoHProcessor (NapProtocol. h)
description: Recupera il tipo di attributo e il valore, in base alla posizione dell'attributo.
ms.assetid: 0d7bc655-428b-4a31-b03f-445e80a6d194
keywords:
- Metodo GetAttribute NAP
- Metodo GetAttribute NAP, interfaccia INapSoHProcessor
- Interfaccia NAP di INapSoHProcessor, metodo GetAttribute
topic_type:
- apiref
api_name:
- INapSoHProcessor.GetAttribute
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ed2d7d9cbafa5a44e0f6c24f4c42959c456722a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301066"
---
# <a name="inapsohprocessorgetattribute-method"></a><span data-ttu-id="5021c-106">Metodo INapSoHProcessor:: GetAttribute</span><span class="sxs-lookup"><span data-stu-id="5021c-106">INapSoHProcessor::GetAttribute method</span></span>

> [!Note]  
> <span data-ttu-id="5021c-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="5021c-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="5021c-108">Il metodo **INapSoHProcessor:: GetAttribute** Recupera il tipo e il valore dell'attributo, data la posizione dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="5021c-108">The **INapSoHProcessor::GetAttribute** method retrieves the attribute type and value, given the attribute location.</span></span>

## <a name="syntax"></a><span data-ttu-id="5021c-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5021c-109">Syntax</span></span>


```C++
HRESULT GetAttribute(
  [in]  UINT16            attributeLocation,
  [out] SoHAttributeType  *type,
  [out] SoHAttributeValue **value
);
```



## <a name="parameters"></a><span data-ttu-id="5021c-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="5021c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5021c-111">*attributeLocation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5021c-111">*attributeLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5021c-112">Posizione (indice) dell'attributo di cui devono essere recuperati il tipo e il valore.</span><span class="sxs-lookup"><span data-stu-id="5021c-112">The location (index) of the attribute whose type and value are to be retrieved.</span></span> <span data-ttu-id="5021c-113">Il valore di *attributeLocation* viene restituito da una chiamata precedente a [**INapSoHProcessor:: FindNextAttribute**](inapsohprocessor-findnextattribute-method.md).</span><span class="sxs-lookup"><span data-stu-id="5021c-113">The value of *attributeLocation* is returned from a prior call to [**INapSoHProcessor::FindNextAttribute**](inapsohprocessor-findnextattribute-method.md).</span></span>

</dd> <dt>

<span data-ttu-id="5021c-114">*tipo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="5021c-114">*type* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5021c-115">Puntatore a una struttura [**SoHAttributeType**](sohattributetype-enum.md) che specifica il tipo di attributo in *value*.</span><span class="sxs-lookup"><span data-stu-id="5021c-115">A pointer to an [**SoHAttributeType**](sohattributetype-enum.md) structure that specifies the attribute's type in *value*.</span></span>

</dd> <dt>

<span data-ttu-id="5021c-116">*valore* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="5021c-116">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5021c-117">Puntatore a un puntatore a una struttura [**SoHAttributeValue**](sohattributevalue-union.md) che contiene il valore dell'attributo in base a quanto definito dal *tipo*.</span><span class="sxs-lookup"><span data-stu-id="5021c-117">A pointer to a pointer to a [**SoHAttributeValue**](sohattributevalue-union.md) structure that contains the attribute's value as defined by *type*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5021c-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5021c-118">Return value</span></span>

<span data-ttu-id="5021c-119">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="5021c-119">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="5021c-120">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="5021c-120">Return code</span></span>                                                                                     | <span data-ttu-id="5021c-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5021c-121">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="5021c-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5021c-122"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="5021c-123">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="5021c-123">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="5021c-124"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="5021c-124"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="5021c-125">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="5021c-125">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="5021c-126"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="5021c-126"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="5021c-127">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="5021c-127">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5021c-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5021c-128">Requirements</span></span>



| <span data-ttu-id="5021c-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="5021c-129">Requirement</span></span> | <span data-ttu-id="5021c-130">Valore</span><span class="sxs-lookup"><span data-stu-id="5021c-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="5021c-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5021c-131">Minimum supported client</span></span><br/> | <span data-ttu-id="5021c-132">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5021c-132">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="5021c-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5021c-133">Minimum supported server</span></span><br/> | <span data-ttu-id="5021c-134">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5021c-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="5021c-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5021c-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="5021c-136"><dt>NapProtocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="5021c-136"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="5021c-137">IDL</span><span class="sxs-lookup"><span data-stu-id="5021c-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5021c-138"><dt>NapProtocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5021c-138"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="5021c-139">DLL</span><span class="sxs-lookup"><span data-stu-id="5021c-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5021c-140"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5021c-140"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="5021c-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5021c-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5021c-142">**INapSoHProcessor**</span><span class="sxs-lookup"><span data-stu-id="5021c-142">**INapSoHProcessor**</span></span>](inapsohprocessor.md)
</dt> </dl>

 

 





