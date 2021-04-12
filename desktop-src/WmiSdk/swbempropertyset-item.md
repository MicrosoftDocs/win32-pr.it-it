---
description: Il metodo Item dell'oggetto SWbemPropertySet ottiene un SWbemProperty denominato dalla raccolta. Questo è il metodo predefinito per questo oggetto.
ms.assetid: 72025676-01dd-4fd7-b000-de6b09ecc6dc
ms.tgt_platform: multiple
title: Metodo SWbemPropertySet. Item (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPropertySet.Item
- ISWbemPropertySet.Item
- ISWbemPropertySet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b4d4dcbbbcb8b5225af038bf71e67c3a14260942
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233796"
---
# <a name="swbempropertysetitem-method"></a><span data-ttu-id="0c670-104">Metodo SWbemPropertySet. Item</span><span class="sxs-lookup"><span data-stu-id="0c670-104">SWbemPropertySet.Item method</span></span>

<span data-ttu-id="0c670-105">Il metodo **Item** dell'oggetto [**SWbemPropertySet**](swbempropertyset.md) ottiene un [**SWbemProperty**](swbemproperty.md) denominato dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="0c670-105">The **Item** method of the [**SWbemPropertySet**](swbempropertyset.md) object gets a named [**SWbemProperty**](swbemproperty.md) from the collection.</span></span> <span data-ttu-id="0c670-106">Questo è il metodo predefinito per questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="0c670-106">This is the default method for this object.</span></span>

<span data-ttu-id="0c670-107">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="0c670-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0c670-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0c670-108">Syntax</span></span>


```VB
objProperty = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="0c670-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="0c670-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c670-110">*strName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0c670-110">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c670-111">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="0c670-111">Required.</span></span> <span data-ttu-id="0c670-112">Nome della proprietà da recuperare.</span><span class="sxs-lookup"><span data-stu-id="0c670-112">Name of the property to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="0c670-113">*iFlags* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="0c670-113">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0c670-114">Riservato.</span><span class="sxs-lookup"><span data-stu-id="0c670-114">Reserved.</span></span> <span data-ttu-id="0c670-115">Se specificato, questo valore deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="0c670-115">This value must be zero if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c670-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0c670-116">Return value</span></span>

<span data-ttu-id="0c670-117">Se l'esito è positivo, viene restituito l'oggetto [**SWbemProperty**](swbemproperty.md) richiesto.</span><span class="sxs-lookup"><span data-stu-id="0c670-117">If successful, the requested [**SWbemProperty**](swbemproperty.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0c670-118">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="0c670-118">Error codes</span></span>

<span data-ttu-id="0c670-119">Dopo il completamento del metodo **Item** , l'oggetto **Err** può contenere uno dei codici di errore elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="0c670-119">After the completion of the **Item** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="0c670-120">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="0c670-120">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="0c670-121">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="0c670-121">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="0c670-122">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="0c670-122">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="0c670-123">È stato specificato un parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="0c670-123">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="0c670-124">**wbemErrOutOfMemory** -2147749896</span><span class="sxs-lookup"><span data-stu-id="0c670-124">**wbemErrOutOfMemory** - 2147749896</span></span>
</dt> <dd>

<span data-ttu-id="0c670-125">Memoria insufficiente per l'esecuzione di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="0c670-125">Not enough memory for this method to execute.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0c670-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0c670-126">Requirements</span></span>



| <span data-ttu-id="0c670-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c670-127">Requirement</span></span> | <span data-ttu-id="0c670-128">Valore</span><span class="sxs-lookup"><span data-stu-id="0c670-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c670-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0c670-129">Minimum supported client</span></span><br/> | <span data-ttu-id="0c670-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0c670-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0c670-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0c670-131">Minimum supported server</span></span><br/> | <span data-ttu-id="0c670-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0c670-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0c670-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0c670-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c670-134"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c670-134"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="0c670-135">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="0c670-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="0c670-136"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0c670-136"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0c670-137">DLL</span><span class="sxs-lookup"><span data-stu-id="0c670-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c670-138"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c670-138"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="0c670-139">CLSID</span><span class="sxs-lookup"><span data-stu-id="0c670-139">CLSID</span></span><br/>                    | <span data-ttu-id="0c670-140">\_SWBEMPROPERTYSET CLSID</span><span class="sxs-lookup"><span data-stu-id="0c670-140">CLSID\_SWbemPropertySet</span></span><br/>                                                      |
| <span data-ttu-id="0c670-141">IID</span><span class="sxs-lookup"><span data-stu-id="0c670-141">IID</span></span><br/>                      | <span data-ttu-id="0c670-142">\_ISWBEMPROPERTYSET IID</span><span class="sxs-lookup"><span data-stu-id="0c670-142">IID\_ISWbemPropertySet</span></span><br/>                                                       |



 

 




