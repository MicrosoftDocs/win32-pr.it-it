---
title: Funzione MrmCreateResourceIndexerFromPreviousPriData (MrmResourceIndexer. h)
description: Crea un indicizzatore di risorse dai dati PRI creati da una chiamata precedente a MrmCreateResourceFileInMemory. Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere API PRI (Package Resource Indexing) e sistemi di compilazione personalizzati.
ms.assetid: 945ED98C-8D73-404F-ACE3-7DD314FB405A
keywords:
- Menu della funzione MrmCreateResourceIndexerFromPreviousPriData e altre risorse
topic_type:
- apiref
api_name:
- MrmCreateResourceIndexerFromPreviousPriData
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 152ded28e6158fb80d8157c751026091afb51f65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341012"
---
# <a name="mrmcreateresourceindexerfrompreviouspridata-function"></a><span data-ttu-id="ac5e7-105">MrmCreateResourceIndexerFromPreviousPriData (funzione)</span><span class="sxs-lookup"><span data-stu-id="ac5e7-105">MrmCreateResourceIndexerFromPreviousPriData function</span></span>

<span data-ttu-id="ac5e7-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="ac5e7-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ac5e7-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="ac5e7-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ac5e7-108">Crea un indicizzatore di risorse dai dati PRI creati da una chiamata precedente a [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md).</span><span class="sxs-lookup"><span data-stu-id="ac5e7-108">Creates a resource indexer from PRI data created by a previous call to [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md).</span></span> <span data-ttu-id="ac5e7-109">Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere [API pri (Package Resource Indexing) e sistemi di compilazione personalizzati](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="ac5e7-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="ac5e7-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ac5e7-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateResourceIndexerFromPreviousPriData (
  _In_     PCWSTR                   projectRoot,
  _In_     MrmPlatformVersion       platformVersion,
  _In_opt_ PCWSTR                   defaultQualifiers,
  _In_     BYTE                     *priData,
  _In_     ULONG                    priSize,
  _Inout_  MrmResourceIndexerHandle *indexer
);
```



## <a name="parameters"></a><span data-ttu-id="ac5e7-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="ac5e7-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac5e7-112">*projectRoot* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ac5e7-112">*projectRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac5e7-113">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="ac5e7-113">Type: **PCWSTR**</span></span>

<span data-ttu-id="ac5e7-114">La radice del progetto dell'app UWP per cui verranno generati i file PRI.</span><span class="sxs-lookup"><span data-stu-id="ac5e7-114">The project root of the UWP app for which you will be generating PRI files.</span></span> <span data-ttu-id="ac5e7-115">In altre parole, il percorso dei file di risorse dell'app.</span><span class="sxs-lookup"><span data-stu-id="ac5e7-115">In other words, the path to that app's resource files.</span></span> <span data-ttu-id="ac5e7-116">Questa impostazione viene specificata in modo che sia possibile specificare i percorsi relativi a tale radice nelle chiamate API successive allo stesso indicizzatore di risorse.</span><span class="sxs-lookup"><span data-stu-id="ac5e7-116">You specify this so that you can then specify paths relative to that root in subsequent API calls to the same resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="ac5e7-117">*platformVersion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ac5e7-117">*platformVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac5e7-118">Tipo: **[ **MrmPlatformVersion**](mrmplatformversion.md)**</span><span class="sxs-lookup"><span data-stu-id="ac5e7-118">Type: **[**MrmPlatformVersion**](mrmplatformversion.md)**</span></span>

<span data-ttu-id="ac5e7-119">Versione della piattaforma di destinazione per l'indicizzatore di risorse.</span><span class="sxs-lookup"><span data-stu-id="ac5e7-119">The target platform version for the resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="ac5e7-120">*defaultQualifiers* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="ac5e7-120">*defaultQualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ac5e7-121">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="ac5e7-121">Type: **PCWSTR**</span></span>

<span data-ttu-id="ac5e7-122">Elenco di qualificatori di risorse predefiniti.</span><span class="sxs-lookup"><span data-stu-id="ac5e7-122">A list of default resource qualifiers.</span></span> <span data-ttu-id="ac5e7-123">Ad esempio, L "lingua-en-US \_ scale-100 \_ contrasto-standard"</span><span class="sxs-lookup"><span data-stu-id="ac5e7-123">For example, L"language-en-US\_scale-100\_contrast-standard"</span></span>

</dd> <dt>

<span data-ttu-id="ac5e7-124">*priData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ac5e7-124">*priData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac5e7-125">Tipo: \**byte \** _</span><span class="sxs-lookup"><span data-stu-id="ac5e7-125">Type: \**BYTE\** _</span></span>

<span data-ttu-id="ac5e7-126">Puntatore ai dati PRI creati da una chiamata precedente a [_ *MrmCreateResourceFileInMemory* \*](mrmcreateresourcefileinmemory.md).</span><span class="sxs-lookup"><span data-stu-id="ac5e7-126">A pointer to PRI data created by a previous call to [_ *MrmCreateResourceFileInMemory*\*](mrmcreateresourcefileinmemory.md).</span></span> <span data-ttu-id="ac5e7-127">Non liberare *priData* fino al termine dell'uso dell'indicizzatore di risorse creato da questa funzione.</span><span class="sxs-lookup"><span data-stu-id="ac5e7-127">Don't free *priData* until after you've finished using the resource indexer created by this function.</span></span>

</dd> <dt>

<span data-ttu-id="ac5e7-128">*priSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ac5e7-128">*priSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac5e7-129">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="ac5e7-129">Type: **ULONG**</span></span>

<span data-ttu-id="ac5e7-130">Dimensione dei dati a cui punta *priData*.</span><span class="sxs-lookup"><span data-stu-id="ac5e7-130">The size of the data pointed to by *priData*.</span></span>

</dd> <dt>

<span data-ttu-id="ac5e7-131">*indicizzatore* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="ac5e7-131">*indexer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac5e7-132">Tipo: \**[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md) \** _</span><span class="sxs-lookup"><span data-stu-id="ac5e7-132">Type: \**[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)\** _</span></span>

<span data-ttu-id="ac5e7-133">Puntatore a un handle dell'indicizzatore di risorse.</span><span class="sxs-lookup"><span data-stu-id="ac5e7-133">A pointer to a resource indexer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac5e7-134">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ac5e7-134">Return value</span></span>

<span data-ttu-id="ac5e7-135">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="ac5e7-135">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="ac5e7-136">S \_ OK se la funzione ha avuto esito positivo, in caso contrario un altro valore.</span><span class="sxs-lookup"><span data-stu-id="ac5e7-136">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="ac5e7-137">Utilizzare le macro SUCCEEDed () o FAILED () (definite in Winerror. h) per determinare l'esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="ac5e7-137">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac5e7-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="ac5e7-138">Remarks</span></span>

<span data-ttu-id="ac5e7-139">Non liberare *priData* fino al termine dell'uso dell'indicizzatore di risorse creato da questa funzione.</span><span class="sxs-lookup"><span data-stu-id="ac5e7-139">Don't free *priData* until after you've finished using the resource indexer created by this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac5e7-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ac5e7-140">Requirements</span></span>



| <span data-ttu-id="ac5e7-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac5e7-141">Requirement</span></span> | <span data-ttu-id="ac5e7-142">Valore</span><span class="sxs-lookup"><span data-stu-id="ac5e7-142">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac5e7-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ac5e7-143">Minimum supported client</span></span><br/> | <span data-ttu-id="ac5e7-144">Solo app desktop Windows 10 versione 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="ac5e7-144">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="ac5e7-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ac5e7-145">Minimum supported server</span></span><br/> | <span data-ttu-id="ac5e7-146">\[Solo app desktop Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="ac5e7-146">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ac5e7-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ac5e7-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac5e7-148"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac5e7-148"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="ac5e7-149">Libreria</span><span class="sxs-lookup"><span data-stu-id="ac5e7-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="ac5e7-150"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ac5e7-150"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="ac5e7-151">DLL</span><span class="sxs-lookup"><span data-stu-id="ac5e7-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac5e7-152"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac5e7-152"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="ac5e7-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ac5e7-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac5e7-154">API per l'indicizzazione delle risorse del pacchetto e sistemi di compilazione personalizzati</span><span class="sxs-lookup"><span data-stu-id="ac5e7-154">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

