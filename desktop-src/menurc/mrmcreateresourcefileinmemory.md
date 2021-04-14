---
title: Funzione MrmCreateResourceFileInMemory (MrmResourceIndexer. h)
description: Crea informazioni PRI come BLOB in memoria, non come file su disco.
ms.assetid: 68BDAD27-545A-4DC6-B909-4242A0863690
keywords:
- Menu della funzione MrmCreateResourceFileInMemory e altre risorse
topic_type:
- apiref
api_name:
- MrmCreateResourceFileInMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17bbe36a55b5be18f9f4005b4e0ae24d3d610bd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478652"
---
# <a name="mrmcreateresourcefileinmemory-function"></a><span data-ttu-id="6552e-104">MrmCreateResourceFileInMemory (funzione)</span><span class="sxs-lookup"><span data-stu-id="6552e-104">MrmCreateResourceFileInMemory function</span></span>

<span data-ttu-id="6552e-105">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="6552e-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="6552e-106">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="6552e-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="6552e-107">Crea informazioni PRI come BLOB in memoria, non come file su disco.</span><span class="sxs-lookup"><span data-stu-id="6552e-107">Creates PRI info as a blob in memory, not as a file on disk.</span></span> <span data-ttu-id="6552e-108">La funzione alloca memoria e restituisce un puntatore a tale memoria in *outputPriData*.</span><span class="sxs-lookup"><span data-stu-id="6552e-108">The function allocates memory and returns a pointer to that memory in *outputPriData*.</span></span> <span data-ttu-id="6552e-109">Chiamare [**MrmFreeMemory**](mrmfreememory.md) con lo stesso puntatore per liberare la memoria.</span><span class="sxs-lookup"><span data-stu-id="6552e-109">Call [**MrmFreeMemory**](mrmfreememory.md) with the same pointer to free that memory.</span></span> <span data-ttu-id="6552e-110">Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere [API pri (Package Resource Indexing) e sistemi di compilazione personalizzati](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="6552e-110">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="6552e-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6552e-111">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateResourceFileInMemory(
  _In_  MrmResourceIndexerHandle indexer,
  _In_  MrmPackagingMode         packagingMode,
  _In_  MrmPackagingOptions      packagingOptions,
  _Out_ BYTE                     **outputPriData,
  _Out_ ULONG                    *outputPriSize
);
```



## <a name="parameters"></a><span data-ttu-id="6552e-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="6552e-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6552e-113">*indicizzatore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6552e-113">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6552e-114">Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="6552e-114">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="6552e-115">Handle che identifica l'indicizzatore di risorse da cui creare le informazioni PRI.</span><span class="sxs-lookup"><span data-stu-id="6552e-115">A handle identifying the resource indexer from which to create the PRI info.</span></span>

</dd> <dt>

<span data-ttu-id="6552e-116">*packagingMode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6552e-116">*packagingMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6552e-117">Tipo: **[ **MrmPackagingMode**](mrmpackagingmode.md)**</span><span class="sxs-lookup"><span data-stu-id="6552e-117">Type: **[**MrmPackagingMode**](mrmpackagingmode.md)**</span></span>

<span data-ttu-id="6552e-118">Specifica se le informazioni PRI devono essere autonome o essere un pacchetto di risorse.</span><span class="sxs-lookup"><span data-stu-id="6552e-118">Specifies whether the PRI info should be standalone, or be a resource pack.</span></span> <span data-ttu-id="6552e-119">**MrmPackagingModeAutoSplit** non è supportato.</span><span class="sxs-lookup"><span data-stu-id="6552e-119">**MrmPackagingModeAutoSplit** is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="6552e-120">*packagingOptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6552e-120">*packagingOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6552e-121">Tipo: **[ **MrmPackagingOptions**](mrmpackagingoptions.md)**</span><span class="sxs-lookup"><span data-stu-id="6552e-121">Type: **[**MrmPackagingOptions**](mrmpackagingoptions.md)**</span></span>

<span data-ttu-id="6552e-122">Specifica opzioni aggiuntive per le informazioni sul PRI.</span><span class="sxs-lookup"><span data-stu-id="6552e-122">Specifies additional options about the PRI info.</span></span>

</dd> <dt>

<span data-ttu-id="6552e-123">*outputPriData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6552e-123">*outputPriData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6552e-124">Tipo: **byte \* \***</span><span class="sxs-lookup"><span data-stu-id="6552e-124">Type: **BYTE\*\***</span></span>

<span data-ttu-id="6552e-125">Indirizzo di un puntatore a BYTE.</span><span class="sxs-lookup"><span data-stu-id="6552e-125">The address of a pointer to BYTE.</span></span> <span data-ttu-id="6552e-126">La funzione alloca memoria e restituisce un puntatore a tale memoria in *outputPriData*.</span><span class="sxs-lookup"><span data-stu-id="6552e-126">The function allocates memory and returns a pointer to that memory in *outputPriData*.</span></span> <span data-ttu-id="6552e-127">Chiamare [**MrmFreeMemory**](mrmfreememory.md) con il puntatore a byte per liberare la memoria.</span><span class="sxs-lookup"><span data-stu-id="6552e-127">Call [**MrmFreeMemory**](mrmfreememory.md) with your pointer to BYTE to free that memory.</span></span>

</dd> <dt>

<span data-ttu-id="6552e-128">*outputPriSize* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6552e-128">*outputPriSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6552e-129">Tipo: \**ULONG \** _</span><span class="sxs-lookup"><span data-stu-id="6552e-129">Type: \**ULONG\** _</span></span>

<span data-ttu-id="6552e-130">Indirizzo di ULONG.</span><span class="sxs-lookup"><span data-stu-id="6552e-130">The address of a ULONG.</span></span> <span data-ttu-id="6552e-131">In _outputPriSize \*, la funzione restituisce le dimensioni della memoria allocata a cui punta *outputPriData*.</span><span class="sxs-lookup"><span data-stu-id="6552e-131">In _outputPriSize\*, the function returns the size of the allocated memory pointed to by *outputPriData*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6552e-132">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6552e-132">Return value</span></span>

<span data-ttu-id="6552e-133">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6552e-133">Type: **HRESULT**</span></span>

<span data-ttu-id="6552e-134">S \_ OK se la funzione ha avuto esito positivo, in caso contrario un altro valore.</span><span class="sxs-lookup"><span data-stu-id="6552e-134">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="6552e-135">Utilizzare le macro SUCCEEDed () o FAILED () (definite in Winerror. h) per determinare l'esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="6552e-135">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="6552e-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="6552e-136">Remarks</span></span>

<span data-ttu-id="6552e-137">Se si passa *outputPriData* a [**MrmCreateResourceIndexerFromPreviousPriData**](mrmcreateresourceindexerfrompreviouspridata-.md), non liberare la memoria fino a quando non viene terminato di usare l'indicizzatore di risorse.</span><span class="sxs-lookup"><span data-stu-id="6552e-137">If you pass *outputPriData* to [**MrmCreateResourceIndexerFromPreviousPriData**](mrmcreateresourceindexerfrompreviouspridata-.md), then don't free the memory until after you've finished using the resource indexer.</span></span>

## <a name="requirements"></a><span data-ttu-id="6552e-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6552e-138">Requirements</span></span>



| <span data-ttu-id="6552e-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="6552e-139">Requirement</span></span> | <span data-ttu-id="6552e-140">Valore</span><span class="sxs-lookup"><span data-stu-id="6552e-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6552e-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6552e-141">Minimum supported client</span></span><br/> | <span data-ttu-id="6552e-142">Solo app desktop Windows 10 versione 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="6552e-142">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="6552e-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6552e-143">Minimum supported server</span></span><br/> | <span data-ttu-id="6552e-144">\[Solo app desktop Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="6552e-144">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6552e-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6552e-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="6552e-146"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="6552e-146"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="6552e-147">Libreria</span><span class="sxs-lookup"><span data-stu-id="6552e-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="6552e-148"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6552e-148"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="6552e-149">DLL</span><span class="sxs-lookup"><span data-stu-id="6552e-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6552e-150"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6552e-150"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="6552e-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6552e-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6552e-152">API per l'indicizzazione delle risorse del pacchetto e sistemi di compilazione personalizzati</span><span class="sxs-lookup"><span data-stu-id="6552e-152">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

