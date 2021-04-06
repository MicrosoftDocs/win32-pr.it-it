---
title: Funzione MrmCreateResourceIndexerFromPreviousSchemaFile (MrmResourceIndexer. h)
description: Crea un indicizzatore di risorse da un file di schema creato con una chiamata precedente a MrmDumpPriFile. Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere API PRI (Package Resource Indexing) e sistemi di compilazione personalizzati.
ms.assetid: 2ECF355C-C6FD-4949-B455-52E3FF455005
keywords:
- Menu della funzione MrmCreateResourceIndexerFromPreviousSchemaFile e altre risorse
topic_type:
- apiref
api_name:
- MrmCreateResourceIndexerFromPreviousSchemaFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 304e0aebe75ac416623cb1ec1053a7b6ae504194
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743055"
---
# <a name="mrmcreateresourceindexerfrompreviousschemafile-function"></a><span data-ttu-id="068bc-105">MrmCreateResourceIndexerFromPreviousSchemaFile (funzione)</span><span class="sxs-lookup"><span data-stu-id="068bc-105">MrmCreateResourceIndexerFromPreviousSchemaFile function</span></span>

<span data-ttu-id="068bc-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="068bc-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="068bc-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="068bc-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="068bc-108">Crea un indicizzatore di risorse da un file di schema creato con una chiamata precedente a [**MrmDumpPriFile**](mrmdumpprifile.md).</span><span class="sxs-lookup"><span data-stu-id="068bc-108">Creates a resource indexer from a schema file created with a previous call to [**MrmDumpPriFile**](mrmdumpprifile.md).</span></span> <span data-ttu-id="068bc-109">Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere [API pri (Package Resource Indexing) e sistemi di compilazione personalizzati](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="068bc-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="068bc-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="068bc-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateResourceIndexerFromPreviousSchemaFile(
  _In_     PCWSTR                   projectRoot,
  _In_     MrmPlatformVersion       platformVersion,
  _In_opt_ PCWSTR                   defaultQualifiers,
  _In_     PCWSTR                   schemaFile,
  _Inout_  MrmResourceIndexerHandle *indexer
);
```



## <a name="parameters"></a><span data-ttu-id="068bc-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="068bc-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="068bc-112">*projectRoot* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="068bc-112">*projectRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="068bc-113">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="068bc-113">Type: **PCWSTR**</span></span>

<span data-ttu-id="068bc-114">La radice del progetto dell'app UWP per cui verranno generati i file PRI.</span><span class="sxs-lookup"><span data-stu-id="068bc-114">The project root of the UWP app for which you will be generating PRI files.</span></span> <span data-ttu-id="068bc-115">In altre parole, il percorso dei file di risorse dell'app.</span><span class="sxs-lookup"><span data-stu-id="068bc-115">In other words, the path to that app's resource files.</span></span> <span data-ttu-id="068bc-116">Questa impostazione viene specificata in modo che sia possibile specificare i percorsi relativi a tale radice nelle chiamate API successive allo stesso indicizzatore di risorse.</span><span class="sxs-lookup"><span data-stu-id="068bc-116">You specify this so that you can then specify paths relative to that root in subsequent API calls to the same resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="068bc-117">*platformVersion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="068bc-117">*platformVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="068bc-118">Tipo: **[ **MrmPlatformVersion**](mrmplatformversion.md)**</span><span class="sxs-lookup"><span data-stu-id="068bc-118">Type: **[**MrmPlatformVersion**](mrmplatformversion.md)**</span></span>

<span data-ttu-id="068bc-119">Versione della piattaforma di destinazione per l'indicizzatore di risorse.</span><span class="sxs-lookup"><span data-stu-id="068bc-119">The target platform version for the resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="068bc-120">*defaultQualifiers* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="068bc-120">*defaultQualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="068bc-121">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="068bc-121">Type: **PCWSTR**</span></span>

<span data-ttu-id="068bc-122">Elenco di qualificatori di risorse predefiniti.</span><span class="sxs-lookup"><span data-stu-id="068bc-122">A list of default resource qualifiers.</span></span> <span data-ttu-id="068bc-123">Ad esempio, L "lingua-en-US \_ scale-100 \_ contrasto-standard"</span><span class="sxs-lookup"><span data-stu-id="068bc-123">For example, L"language-en-US\_scale-100\_contrast-standard"</span></span>

</dd> <dt>

<span data-ttu-id="068bc-124">*fileschema* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="068bc-124">*schemaFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="068bc-125">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="068bc-125">Type: **PCWSTR**</span></span>

<span data-ttu-id="068bc-126">Percorso di file completo di un file di schema creato da una chiamata precedente a [**MrmDumpPriFile**](mrmdumpprifile.md).</span><span class="sxs-lookup"><span data-stu-id="068bc-126">A full file path to a schema file created by a previous call to [**MrmDumpPriFile**](mrmdumpprifile.md).</span></span>

</dd> <dt>

<span data-ttu-id="068bc-127">*indicizzatore* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="068bc-127">*indexer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="068bc-128">Tipo: \**[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md) \** _</span><span class="sxs-lookup"><span data-stu-id="068bc-128">Type: \**[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)\** _</span></span>

<span data-ttu-id="068bc-129">Puntatore a un handle dell'indicizzatore di risorse.</span><span class="sxs-lookup"><span data-stu-id="068bc-129">A pointer to a resource indexer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="068bc-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="068bc-130">Return value</span></span>

<span data-ttu-id="068bc-131">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="068bc-131">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="068bc-132">S \_ OK se la funzione ha avuto esito positivo, in caso contrario un altro valore.</span><span class="sxs-lookup"><span data-stu-id="068bc-132">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="068bc-133">Utilizzare le macro SUCCEEDed () o FAILED () (definite in Winerror. h) per determinare l'esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="068bc-133">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="068bc-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="068bc-134">Requirements</span></span>



| <span data-ttu-id="068bc-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="068bc-135">Requirement</span></span> | <span data-ttu-id="068bc-136">Valore</span><span class="sxs-lookup"><span data-stu-id="068bc-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="068bc-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="068bc-137">Minimum supported client</span></span><br/> | <span data-ttu-id="068bc-138">Solo app desktop Windows 10 versione 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="068bc-138">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="068bc-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="068bc-139">Minimum supported server</span></span><br/> | <span data-ttu-id="068bc-140">\[Solo app desktop Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="068bc-140">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="068bc-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="068bc-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="068bc-142"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="068bc-142"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="068bc-143">Libreria</span><span class="sxs-lookup"><span data-stu-id="068bc-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="068bc-144"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="068bc-144"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="068bc-145">DLL</span><span class="sxs-lookup"><span data-stu-id="068bc-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="068bc-146"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="068bc-146"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="068bc-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="068bc-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="068bc-148">API per l'indicizzazione delle risorse del pacchetto e sistemi di compilazione personalizzati</span><span class="sxs-lookup"><span data-stu-id="068bc-148">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

