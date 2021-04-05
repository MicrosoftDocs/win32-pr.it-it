---
description: Il metodo clone dell'oggetto SWbemNamedValueSet restituisce un nuovo oggetto che è un clone della raccolta corrente.
ms.assetid: 0e7fab2e-8175-45e5-aa70-1109502e2b3f
ms.tgt_platform: multiple
title: Metodo SWbemNamedValueSet. Clone (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.Clone
- ISWbemNamedValueSet.Clone
- ISWbemNamedValueSet.Clone
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 17678d36a553c84c008f606c647d7ff1fa9dfadc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103756974"
---
# <a name="swbemnamedvaluesetclone-method"></a><span data-ttu-id="0dd46-103">Metodo SWbemNamedValueSet. Clone</span><span class="sxs-lookup"><span data-stu-id="0dd46-103">SWbemNamedValueSet.Clone method</span></span>

<span data-ttu-id="0dd46-104">Il metodo **Clone** dell'oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) restituisce un nuovo oggetto che è un clone della raccolta corrente.</span><span class="sxs-lookup"><span data-stu-id="0dd46-104">The **Clone** method of the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object returns a new object that is a clone of the current collection.</span></span>

<span data-ttu-id="0dd46-105">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="0dd46-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0dd46-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0dd46-106">Syntax</span></span>


```VB
objwbemNamedValueSet = .Clone( _
)
```



## <a name="parameters"></a><span data-ttu-id="0dd46-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="0dd46-107">Parameters</span></span>

<span data-ttu-id="0dd46-108">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="0dd46-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0dd46-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0dd46-109">Return value</span></span>

<span data-ttu-id="0dd46-110">Se l'esito è positivo, viene restituito un nuovo oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) .</span><span class="sxs-lookup"><span data-stu-id="0dd46-110">If successful, a new [**SWbemNamedValueSet**](swbemnamedvalueset.md) object returns.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0dd46-111">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="0dd46-111">Error codes</span></span>

<span data-ttu-id="0dd46-112">Al termine del metodo **Clone** , l'oggetto **Err** può contenere uno dei codici di errore riportati di seguito.</span><span class="sxs-lookup"><span data-stu-id="0dd46-112">Upon completion of the **Clone** method, the **Err** object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="0dd46-113">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="0dd46-113">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="0dd46-114">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="0dd46-114">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="0dd46-115">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="0dd46-115">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="0dd46-116">Memoria insufficiente per clonare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0dd46-116">Not enough memory to clone the object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0dd46-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="0dd46-117">Remarks</span></span>

<span data-ttu-id="0dd46-118">Utilizzare questo metodo per duplicare una raccolta [**SWbemNamedValueSet**](swbemnamedvalueset.md) .</span><span class="sxs-lookup"><span data-stu-id="0dd46-118">Use this method to duplicate an [**SWbemNamedValueSet**](swbemnamedvalueset.md) collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="0dd46-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0dd46-119">Requirements</span></span>



| <span data-ttu-id="0dd46-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0dd46-120">Requirement</span></span> | <span data-ttu-id="0dd46-121">Valore</span><span class="sxs-lookup"><span data-stu-id="0dd46-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0dd46-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0dd46-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0dd46-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0dd46-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0dd46-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0dd46-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0dd46-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0dd46-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0dd46-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0dd46-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0dd46-127"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0dd46-127"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="0dd46-128">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="0dd46-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="0dd46-129"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0dd46-129"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0dd46-130">DLL</span><span class="sxs-lookup"><span data-stu-id="0dd46-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0dd46-131"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0dd46-131"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="0dd46-132">CLSID</span><span class="sxs-lookup"><span data-stu-id="0dd46-132">CLSID</span></span><br/>                    | <span data-ttu-id="0dd46-133">\_SWBEMNAMEDVALUESET CLSID</span><span class="sxs-lookup"><span data-stu-id="0dd46-133">CLSID\_SWbemNamedValueSet</span></span><br/>                                                    |
| <span data-ttu-id="0dd46-134">IID</span><span class="sxs-lookup"><span data-stu-id="0dd46-134">IID</span></span><br/>                      | <span data-ttu-id="0dd46-135">\_ISWBEMNAMEDVALUESET IID</span><span class="sxs-lookup"><span data-stu-id="0dd46-135">IID\_ISWbemNamedValueSet</span></span><br/>                                                     |



## <a name="see-also"></a><span data-ttu-id="0dd46-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0dd46-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0dd46-137">**SWbemNamedValueSet**</span><span class="sxs-lookup"><span data-stu-id="0dd46-137">**SWbemNamedValueSet**</span></span>](swbemnamedvalueset.md)
</dt> </dl>

 

 




