---
description: Il metodo Item dell'oggetto dell'SWbemQualifierSet restituisce un oggetto oggetto SWbemQualifier denominato dalla raccolta. Questo è il metodo predefinito di questo oggetto.
ms.assetid: 5ed3a336-c06f-446d-85d4-243daddc82a5
ms.tgt_platform: multiple
title: Metodo dell'SWbemQualifierSet. Item (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifierSet.Item
- ISWbemQualifierSet.Item
- ISWbemQualifierSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9c89ff554b049e6730a64ebf7e5f017fc8a5652f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885217"
---
# <a name="swbemqualifiersetitem-method"></a><span data-ttu-id="c9eec-104">Metodo dell'SWbemQualifierSet. Item</span><span class="sxs-lookup"><span data-stu-id="c9eec-104">SWbemQualifierSet.Item method</span></span>

<span data-ttu-id="c9eec-105">Il metodo **Item** dell'oggetto [**dell'SWbemQualifierSet**](swbemqualifierset.md) restituisce un oggetto [**oggetto SWbemQualifier**](swbemqualifier.md) denominato dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="c9eec-105">The **Item** method of the [**SWbemQualifierSet**](swbemqualifierset.md) object returns a named [**SWbemQualifier**](swbemqualifier.md) object from the collection.</span></span> <span data-ttu-id="c9eec-106">Questo è il metodo predefinito di questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="c9eec-106">This is the default method of this object.</span></span>

<span data-ttu-id="c9eec-107">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="c9eec-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c9eec-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c9eec-108">Syntax</span></span>


```VB
objQualifier = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="c9eec-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c9eec-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9eec-110">*strName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c9eec-110">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9eec-111">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="c9eec-111">Required.</span></span> <span data-ttu-id="c9eec-112">Nome del qualificatore da recuperare.</span><span class="sxs-lookup"><span data-stu-id="c9eec-112">Name of the qualifier to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="c9eec-113">*iFlags* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="c9eec-113">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c9eec-114">Riservato.</span><span class="sxs-lookup"><span data-stu-id="c9eec-114">Reserved.</span></span> <span data-ttu-id="c9eec-115">Il valore predefinito è 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="c9eec-115">The default value is 0 (zero).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9eec-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c9eec-116">Return value</span></span>

<span data-ttu-id="c9eec-117">Se l'esito è positivo, viene restituito l'oggetto [**oggetto SWbemQualifier**](swbemqualifier.md) richiesto.</span><span class="sxs-lookup"><span data-stu-id="c9eec-117">If successful, the requested [**SWbemQualifier**](swbemqualifier.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c9eec-118">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="c9eec-118">Error codes</span></span>

<span data-ttu-id="c9eec-119">Dopo il completamento del metodo **Item** , l'oggetto **Err** può contenere uno dei codici di errore elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="c9eec-119">After completion of the **Item** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="c9eec-120">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="c9eec-120">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="c9eec-121">Il parametro *iFlags* non è valido.</span><span class="sxs-lookup"><span data-stu-id="c9eec-121">The *iFlags* parameter was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="c9eec-122">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="c9eec-122">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="c9eec-123">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="c9eec-123">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="c9eec-124">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="c9eec-124">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="c9eec-125">Il qualificatore specificato non esiste.</span><span class="sxs-lookup"><span data-stu-id="c9eec-125">Specified qualifier does not exist.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c9eec-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c9eec-126">Requirements</span></span>



| <span data-ttu-id="c9eec-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9eec-127">Requirement</span></span> | <span data-ttu-id="c9eec-128">Valore</span><span class="sxs-lookup"><span data-stu-id="c9eec-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9eec-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c9eec-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c9eec-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c9eec-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c9eec-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c9eec-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c9eec-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c9eec-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c9eec-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c9eec-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9eec-134"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9eec-134"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c9eec-135">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="c9eec-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="c9eec-136"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c9eec-136"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c9eec-137">DLL</span><span class="sxs-lookup"><span data-stu-id="c9eec-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9eec-138"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9eec-138"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c9eec-139">CLSID</span><span class="sxs-lookup"><span data-stu-id="c9eec-139">CLSID</span></span><br/>                    | <span data-ttu-id="c9eec-140">\_Dell'SWBEMQUALIFIERSET CLSID</span><span class="sxs-lookup"><span data-stu-id="c9eec-140">CLSID\_SWbemQualifierSet</span></span><br/>                                                     |
| <span data-ttu-id="c9eec-141">IID</span><span class="sxs-lookup"><span data-stu-id="c9eec-141">IID</span></span><br/>                      | <span data-ttu-id="c9eec-142">\_ISWBEMQUALIFIERSET IID</span><span class="sxs-lookup"><span data-stu-id="c9eec-142">IID\_ISWbemQualifierSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="c9eec-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c9eec-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9eec-144">**Dell'SWbemQualifierSet**</span><span class="sxs-lookup"><span data-stu-id="c9eec-144">**SWbemQualifierSet**</span></span>](swbemqualifierset.md)
</dt> <dt>

[<span data-ttu-id="c9eec-145">**Oggetto SWbemQualifier**</span><span class="sxs-lookup"><span data-stu-id="c9eec-145">**SWbemQualifier**</span></span>](swbemqualifier.md)
</dt> </dl>

 

 




