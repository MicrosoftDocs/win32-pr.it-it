---
title: Funzione MrmCreateResourceIndexerFromPreviousSchemaData (MrmResourceIndexer. h)
description: Crea un indicizzatore di risorse da dati dello schema in memoria creati con una chiamata precedente a MrmDumpPriFileInMemory o MrmDumpPriDataInMemory.
ms.assetid: D9C90C12-CEFE-4794-9553-8BFBE9E43D99
keywords:
- Menu della funzione MrmCreateResourceIndexerFromPreviousSchemaData e altre risorse
topic_type:
- apiref
api_name:
- MrmCreateResourceIndexerFromPreviousSchemaData
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 621500f8f35714daad0e259e6a718c25129987dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477153"
---
# <a name="mrmcreateresourceindexerfrompreviousschemadata-function"></a><span data-ttu-id="2800e-104">MrmCreateResourceIndexerFromPreviousSchemaData (funzione)</span><span class="sxs-lookup"><span data-stu-id="2800e-104">MrmCreateResourceIndexerFromPreviousSchemaData function</span></span>

<span data-ttu-id="2800e-105">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="2800e-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2800e-106">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="2800e-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2800e-107">Crea un indicizzatore di risorse da dati dello schema in memoria creati con una chiamata precedente a [**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md) o [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md).</span><span class="sxs-lookup"><span data-stu-id="2800e-107">Creates a resource indexer from in-memory schema data created with a previous call to either [**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md) or [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md).</span></span> <span data-ttu-id="2800e-108">Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere [API pri (Package Resource Indexing) e sistemi di compilazione personalizzati](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="2800e-108">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="2800e-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2800e-109">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateResourceIndexerFromPreviousSchemaData(
  _In_     PCWSTR                   projectRoot,
  _In_     MrmPlatformVersion       platformVersion,
  _In_opt_ PCWSTR                   defaultQualifiers,
  _In_     BYTE                     *schemaXmlData,
  _In_     ULONG                    schemaXmlSize,
  _Inout_  MrmResourceIndexerHandle *indexer
);
```



## <a name="parameters"></a><span data-ttu-id="2800e-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="2800e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2800e-111">*projectRoot* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2800e-111">*projectRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2800e-112">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="2800e-112">Type: **PCWSTR**</span></span>

<span data-ttu-id="2800e-113">La radice del progetto dell'app UWP per cui verranno generati i file PRI.</span><span class="sxs-lookup"><span data-stu-id="2800e-113">The project root of the UWP app for which you will be generating PRI files.</span></span> <span data-ttu-id="2800e-114">In altre parole, il percorso dei file di risorse dell'app.</span><span class="sxs-lookup"><span data-stu-id="2800e-114">In other words, the path to that app's resource files.</span></span> <span data-ttu-id="2800e-115">Questa impostazione viene specificata in modo che sia possibile specificare i percorsi relativi a tale radice nelle chiamate API successive allo stesso indicizzatore di risorse.</span><span class="sxs-lookup"><span data-stu-id="2800e-115">You specify this so that you can then specify paths relative to that root in subsequent API calls to the same resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="2800e-116">*platformVersion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2800e-116">*platformVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2800e-117">Tipo: **[ **MrmPlatformVersion**](mrmplatformversion.md)**</span><span class="sxs-lookup"><span data-stu-id="2800e-117">Type: **[**MrmPlatformVersion**](mrmplatformversion.md)**</span></span>

<span data-ttu-id="2800e-118">Versione della piattaforma di destinazione per l'indicizzatore di risorse.</span><span class="sxs-lookup"><span data-stu-id="2800e-118">The target platform version for the resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="2800e-119">*defaultQualifiers* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="2800e-119">*defaultQualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2800e-120">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="2800e-120">Type: **PCWSTR**</span></span>

<span data-ttu-id="2800e-121">Elenco di qualificatori di risorse predefiniti.</span><span class="sxs-lookup"><span data-stu-id="2800e-121">A list of default resource qualifiers.</span></span> <span data-ttu-id="2800e-122">Ad esempio, L "lingua-en-US \_ scale-100 \_ contrasto-standard"</span><span class="sxs-lookup"><span data-stu-id="2800e-122">For example, L"language-en-US\_scale-100\_contrast-standard"</span></span>

</dd> <dt>

<span data-ttu-id="2800e-123">*schemaXmlData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2800e-123">*schemaXmlData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2800e-124">Tipo: \**byte \** _</span><span class="sxs-lookup"><span data-stu-id="2800e-124">Type: \**BYTE\** _</span></span>

<span data-ttu-id="2800e-125">Puntatore ai dati dello schema creati da una precedente chiamata a [_ *MrmDumpPriFileInMemory* \*](mrmdumpprifileinmemory.md) o [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md).</span><span class="sxs-lookup"><span data-stu-id="2800e-125">A pointer to schema data created by a previous call to either [_ *MrmDumpPriFileInMemory*\*](mrmdumpprifileinmemory.md) or [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md).</span></span> <span data-ttu-id="2800e-126">Non liberare *schemaXmlData* fino al termine dell'uso dell'indicizzatore di risorse creato da questa funzione.</span><span class="sxs-lookup"><span data-stu-id="2800e-126">Don't free *schemaXmlData* until after you've finished using the resource indexer created by this function.</span></span>

</dd> <dt>

<span data-ttu-id="2800e-127">*schemaXmlSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2800e-127">*schemaXmlSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2800e-128">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="2800e-128">Type: **ULONG**</span></span>

<span data-ttu-id="2800e-129">Dimensione dei dati a cui punta *schemaXmlData*.</span><span class="sxs-lookup"><span data-stu-id="2800e-129">The size of the data pointed to by *schemaXmlData*.</span></span>

</dd> <dt>

<span data-ttu-id="2800e-130">*indicizzatore* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="2800e-130">*indexer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2800e-131">Tipo: \**[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md) \** _</span><span class="sxs-lookup"><span data-stu-id="2800e-131">Type: \**[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)\** _</span></span>

<span data-ttu-id="2800e-132">Puntatore a un handle dell'indicizzatore di risorse.</span><span class="sxs-lookup"><span data-stu-id="2800e-132">A pointer to a resource indexer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2800e-133">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2800e-133">Return value</span></span>

<span data-ttu-id="2800e-134">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="2800e-134">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="2800e-135">S \_ OK se la funzione ha avuto esito positivo, in caso contrario un altro valore.</span><span class="sxs-lookup"><span data-stu-id="2800e-135">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="2800e-136">Utilizzare le macro SUCCEEDed () o FAILED () (definite in Winerror. h) per determinare l'esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="2800e-136">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="2800e-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="2800e-137">Remarks</span></span>

<span data-ttu-id="2800e-138">Non liberare *schemaXmlData* fino al termine dell'uso dell'indicizzatore di risorse creato da questa funzione.</span><span class="sxs-lookup"><span data-stu-id="2800e-138">Don't free *schemaXmlData* until after you've finished using the resource indexer created by this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="2800e-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2800e-139">Requirements</span></span>



| <span data-ttu-id="2800e-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="2800e-140">Requirement</span></span> | <span data-ttu-id="2800e-141">Valore</span><span class="sxs-lookup"><span data-stu-id="2800e-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2800e-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2800e-142">Minimum supported client</span></span><br/> | <span data-ttu-id="2800e-143">Solo app desktop Windows 10 versione 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="2800e-143">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="2800e-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2800e-144">Minimum supported server</span></span><br/> | <span data-ttu-id="2800e-145">\[Solo app desktop Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="2800e-145">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2800e-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2800e-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="2800e-147"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="2800e-147"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="2800e-148">Libreria</span><span class="sxs-lookup"><span data-stu-id="2800e-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="2800e-149"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2800e-149"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="2800e-150">DLL</span><span class="sxs-lookup"><span data-stu-id="2800e-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2800e-151"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2800e-151"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="2800e-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2800e-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2800e-153">API per l'indicizzazione delle risorse del pacchetto e sistemi di compilazione personalizzati</span><span class="sxs-lookup"><span data-stu-id="2800e-153">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

