---
title: Funzione MrmCreateResourceIndexer (MrmResourceIndexer. h)
description: Consente di creare un indicizzatore di risorse, usato per generare file di indice delle risorse del pacchetto (PRI) per un'app UWP. Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere API PRI (Package Resource Indexing) e sistemi di compilazione personalizzati.
ms.assetid: 9AE3EF90-4ADC-4646-9C62-87A702333B9A
keywords:
- Menu della funzione MrmCreateResourceIndexer e altre risorse
topic_type:
- apiref
api_name:
- MrmCreateResourceIndexer
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5240112c3fef6e358cfbc90638ef867108aabeb4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400856"
---
# <a name="mrmcreateresourceindexer-function"></a><span data-ttu-id="f7b5a-105">MrmCreateResourceIndexer (funzione)</span><span class="sxs-lookup"><span data-stu-id="f7b5a-105">MrmCreateResourceIndexer function</span></span>

<span data-ttu-id="f7b5a-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="f7b5a-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f7b5a-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="f7b5a-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f7b5a-108">Consente di creare un indicizzatore di risorse, usato per generare file di indice delle risorse del pacchetto (PRI) per un'app UWP.</span><span class="sxs-lookup"><span data-stu-id="f7b5a-108">Creates a resource indexer, used to generate package resource index (PRI) files for a UWP app.</span></span> <span data-ttu-id="f7b5a-109">Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere [API pri (Package Resource Indexing) e sistemi di compilazione personalizzati](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="f7b5a-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="f7b5a-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f7b5a-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateResourceIndexer(
  _In_     PCWSTR                   packageFamilyName,
  _In_     PCWSTR                   projectRoot,
  _In_     MrmPlatformVersion       platformVersion,
  _In_opt_ PCWSTR                   defaultQualifiers,
  _Inout_  MrmResourceIndexerHandle *indexer
);
```



## <a name="parameters"></a><span data-ttu-id="f7b5a-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="f7b5a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7b5a-112">*packageFamilyName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f7b5a-112">*packageFamilyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7b5a-113">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="f7b5a-113">Type: **PCWSTR**</span></span>

<span data-ttu-id="f7b5a-114">Nome della famiglia di pacchetti dell'app UWP per cui verranno generati i file PRI.</span><span class="sxs-lookup"><span data-stu-id="f7b5a-114">The package family name of the UWP app for which you will be generating PRI files.</span></span> <span data-ttu-id="f7b5a-115">Questo valore verrà usato come nome della mappa delle risorse quando in seguito si genera un file PRI da questo indicizzatore di risorse.</span><span class="sxs-lookup"><span data-stu-id="f7b5a-115">This value will be used as the resource map name when you later generate a PRI file from this resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="f7b5a-116">*projectRoot* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f7b5a-116">*projectRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7b5a-117">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="f7b5a-117">Type: **PCWSTR**</span></span>

<span data-ttu-id="f7b5a-118">La radice del progetto dell'app UWP per cui verranno generati i file PRI.</span><span class="sxs-lookup"><span data-stu-id="f7b5a-118">The project root of the UWP app for which you will be generating PRI files.</span></span> <span data-ttu-id="f7b5a-119">In altre parole, il percorso dei file di risorse dell'app.</span><span class="sxs-lookup"><span data-stu-id="f7b5a-119">In other words, the path to that app's resource files.</span></span> <span data-ttu-id="f7b5a-120">Questa impostazione viene specificata in modo che sia possibile specificare i percorsi relativi a tale radice nelle chiamate API successive allo stesso indicizzatore di risorse.</span><span class="sxs-lookup"><span data-stu-id="f7b5a-120">You specify this so that you can then specify paths relative to that root in subsequent API calls to the same resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="f7b5a-121">*platformVersion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f7b5a-121">*platformVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7b5a-122">Tipo: **[ **MrmPlatformVersion**](mrmplatformversion.md)**</span><span class="sxs-lookup"><span data-stu-id="f7b5a-122">Type: **[**MrmPlatformVersion**](mrmplatformversion.md)**</span></span>

<span data-ttu-id="f7b5a-123">Versione della piattaforma di destinazione per l'indicizzatore di risorse.</span><span class="sxs-lookup"><span data-stu-id="f7b5a-123">The target platform version for the resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="f7b5a-124">*defaultQualifiers* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="f7b5a-124">*defaultQualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f7b5a-125">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="f7b5a-125">Type: **PCWSTR**</span></span>

<span data-ttu-id="f7b5a-126">Elenco di qualificatori di risorse predefiniti.</span><span class="sxs-lookup"><span data-stu-id="f7b5a-126">A list of default resource qualifiers.</span></span> <span data-ttu-id="f7b5a-127">Ad esempio, L "lingua-en-US \_ scale-100 \_ contrasto-standard"</span><span class="sxs-lookup"><span data-stu-id="f7b5a-127">For example, L"language-en-US\_scale-100\_contrast-standard"</span></span>

</dd> <dt>

<span data-ttu-id="f7b5a-128">*indicizzatore* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="f7b5a-128">*indexer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f7b5a-129">Tipo: \**[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md) \** _</span><span class="sxs-lookup"><span data-stu-id="f7b5a-129">Type: \**[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)\** _</span></span>

<span data-ttu-id="f7b5a-130">Puntatore a un handle dell'indicizzatore di risorse.</span><span class="sxs-lookup"><span data-stu-id="f7b5a-130">A pointer to a resource indexer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7b5a-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f7b5a-131">Return value</span></span>

<span data-ttu-id="f7b5a-132">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="f7b5a-132">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="f7b5a-133">S \_ OK se la funzione ha avuto esito positivo, in caso contrario un altro valore.</span><span class="sxs-lookup"><span data-stu-id="f7b5a-133">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="f7b5a-134">Utilizzare le macro SUCCEEDed () o FAILED () (definite in Winerror. h) per determinare l'esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="f7b5a-134">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7b5a-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f7b5a-135">Requirements</span></span>



| <span data-ttu-id="f7b5a-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7b5a-136">Requirement</span></span> | <span data-ttu-id="f7b5a-137">Valore</span><span class="sxs-lookup"><span data-stu-id="f7b5a-137">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7b5a-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f7b5a-138">Minimum supported client</span></span><br/> | <span data-ttu-id="f7b5a-139">Solo app desktop Windows 10 versione 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="f7b5a-139">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="f7b5a-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f7b5a-140">Minimum supported server</span></span><br/> | <span data-ttu-id="f7b5a-141">\[Solo app desktop Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="f7b5a-141">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f7b5a-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f7b5a-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7b5a-143"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7b5a-143"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="f7b5a-144">Libreria</span><span class="sxs-lookup"><span data-stu-id="f7b5a-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="f7b5a-145"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f7b5a-145"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="f7b5a-146">DLL</span><span class="sxs-lookup"><span data-stu-id="f7b5a-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7b5a-147"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7b5a-147"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="f7b5a-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f7b5a-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7b5a-149">API per l'indicizzazione delle risorse del pacchetto e sistemi di compilazione personalizzati</span><span class="sxs-lookup"><span data-stu-id="f7b5a-149">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

