---
description: Il metodo Item dell'oggetto SWbemMethodSet restituisce un oggetto SWbemMethod denominato dalla raccolta.
ms.assetid: 4c1bbecc-b38b-4869-9c8c-b9321536b23e
ms.tgt_platform: multiple
title: Metodo SWbemMethodSet. Item (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethodSet.Item
- ISWbemMethodSet.Item
- ISWbemMethodSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 89d20dc652189abe3354f5d1b51c03279d3f74c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309839"
---
# <a name="swbemmethodsetitem-method"></a><span data-ttu-id="f7797-103">Metodo SWbemMethodSet. Item</span><span class="sxs-lookup"><span data-stu-id="f7797-103">SWbemMethodSet.Item method</span></span>

<span data-ttu-id="f7797-104">Il metodo **Item** dell'oggetto [**SWbemMethodSet**](swbemmethodset.md) restituisce un oggetto [**SWbemMethod**](swbemmethod.md) denominato dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="f7797-104">The **Item** method of the [**SWbemMethodSet**](swbemmethodset.md) object returns a named [**SWbemMethod**](swbemmethod.md) object from the collection.</span></span>

<span data-ttu-id="f7797-105">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="f7797-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f7797-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f7797-106">Syntax</span></span>


```VB
objMethod = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="f7797-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="f7797-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7797-108">*strName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f7797-108">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7797-109">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="f7797-109">Required.</span></span> <span data-ttu-id="f7797-110">Nome del metodo da recuperare.</span><span class="sxs-lookup"><span data-stu-id="f7797-110">Name of the method to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="f7797-111">*iFlags* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="f7797-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f7797-112">Riservato.</span><span class="sxs-lookup"><span data-stu-id="f7797-112">Reserved.</span></span> <span data-ttu-id="f7797-113">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="f7797-113">The default value is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7797-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f7797-114">Return value</span></span>

<span data-ttu-id="f7797-115">In caso di esito positivo, l'oggetto [**SWbemMethod**](swbemmethod.md) richiesto restituisce.</span><span class="sxs-lookup"><span data-stu-id="f7797-115">If successful, the requested [**SWbemMethod**](swbemmethod.md) object returns.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f7797-116">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="f7797-116">Error codes</span></span>

<span data-ttu-id="f7797-117">Al termine del metodo **Item** , l'oggetto **Err** può contenere uno dei codici di errore elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="f7797-117">Upon completion of the **Item** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="f7797-118">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="f7797-118">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="f7797-119">Il parametro *iFlags* non è valido.</span><span class="sxs-lookup"><span data-stu-id="f7797-119">The *iFlags* parameter was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="f7797-120">**wbemErrFailed** -2147749894</span><span class="sxs-lookup"><span data-stu-id="f7797-120">**wbemErrFailed** - 2147749894</span></span>
</dt> <dd>

<span data-ttu-id="f7797-121">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="f7797-121">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="f7797-122">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="f7797-122">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="f7797-123">Il metodo specificato non esiste.</span><span class="sxs-lookup"><span data-stu-id="f7797-123">The specified method does not exist.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f7797-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f7797-124">Requirements</span></span>



| <span data-ttu-id="f7797-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7797-125">Requirement</span></span> | <span data-ttu-id="f7797-126">Valore</span><span class="sxs-lookup"><span data-stu-id="f7797-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7797-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f7797-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f7797-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f7797-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f7797-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f7797-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f7797-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f7797-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f7797-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f7797-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7797-132"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7797-132"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f7797-133">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="f7797-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="f7797-134"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f7797-134"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f7797-135">DLL</span><span class="sxs-lookup"><span data-stu-id="f7797-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7797-136"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7797-136"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f7797-137">CLSID</span><span class="sxs-lookup"><span data-stu-id="f7797-137">CLSID</span></span><br/>                    | <span data-ttu-id="f7797-138">\_SWBEMMETHODSET CLSID</span><span class="sxs-lookup"><span data-stu-id="f7797-138">CLSID\_SWbemMethodSet</span></span><br/>                                                        |
| <span data-ttu-id="f7797-139">IID</span><span class="sxs-lookup"><span data-stu-id="f7797-139">IID</span></span><br/>                      | <span data-ttu-id="f7797-140">\_ISWBEMMETHODSET IID</span><span class="sxs-lookup"><span data-stu-id="f7797-140">IID\_ISWbemMethodSet</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="f7797-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f7797-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7797-142">**SWbemMethodSet**</span><span class="sxs-lookup"><span data-stu-id="f7797-142">**SWbemMethodSet**</span></span>](swbemmethodset.md)
</dt> <dt>

[<span data-ttu-id="f7797-143">**SWbemMethod**</span><span class="sxs-lookup"><span data-stu-id="f7797-143">**SWbemMethod**</span></span>](swbemmethod.md)
</dt> </dl>

 

 




