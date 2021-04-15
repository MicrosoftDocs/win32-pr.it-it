---
title: Funzione MrmIndexFile (MrmResourceIndexer. h)
description: Indicizza un file di risorse appartenente a un'app UWP. Accetta un elenco esplicito (ma facoltativo) di qualificatori di risorse. Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere API PRI (Package Resource Indexing) e sistemi di compilazione personalizzati.
ms.assetid: C9F245B4-D2D3-4863-BB64-72619FC73D3C
keywords:
- Menu della funzione MrmIndexFile e altre risorse
topic_type:
- apiref
api_name:
- MrmIndexFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9db3e0521f954a2d5d5e0286fb6f21b8e5f55eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478646"
---
# <a name="mrmindexfile-function"></a><span data-ttu-id="a1a07-106">MrmIndexFile (funzione)</span><span class="sxs-lookup"><span data-stu-id="a1a07-106">MrmIndexFile function</span></span>

<span data-ttu-id="a1a07-107">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="a1a07-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a1a07-108">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="a1a07-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a1a07-109">Indicizza un file di risorse appartenente a un'app UWP.</span><span class="sxs-lookup"><span data-stu-id="a1a07-109">Indexes a resource file belonging to a UWP app.</span></span> <span data-ttu-id="a1a07-110">Accetta un elenco esplicito (ma facoltativo) di qualificatori di risorse.</span><span class="sxs-lookup"><span data-stu-id="a1a07-110">Takes an explicit (but optional) list of resource qualifiers.</span></span> <span data-ttu-id="a1a07-111">Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere [API pri (Package Resource Indexing) e sistemi di compilazione personalizzati](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="a1a07-111">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="a1a07-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a1a07-112">Syntax</span></span>


```C++
HRESULT HRESULT MrmIndexFile(
  _In_     MrmResourceIndexerHandle indexer,
  _In_     PCWSTR                   resourceUri,
  _In_     PCWSTR                   filePath,
  _In_opt_ PCWSTR                   qualifiers
);
```



## <a name="parameters"></a><span data-ttu-id="a1a07-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="a1a07-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1a07-114">*indicizzatore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a1a07-114">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1a07-115">Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="a1a07-115">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="a1a07-116">Handle che identifica l'indicizzatore di risorse che indicizza il file di risorse.</span><span class="sxs-lookup"><span data-stu-id="a1a07-116">A handle identifying the resource indexer that will index the resource file.</span></span>

</dd> <dt>

<span data-ttu-id="a1a07-117">*resourceUri* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a1a07-117">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1a07-118">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="a1a07-118">Type: **PCWSTR**</span></span>

<span data-ttu-id="a1a07-119">URI della risorsa da assegnare alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="a1a07-119">The resource URI to assign to the resource.</span></span> <span data-ttu-id="a1a07-120">Il percorso verrà usato come nome del sottoalbero della mappa delle risorse per questa risorsa quando in seguito si genera un file PRI da questo indicizzatore di risorse.</span><span class="sxs-lookup"><span data-stu-id="a1a07-120">The path will be used as the resource map subtree name for this resource when you later generate a PRI file from this resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="a1a07-121">*filePath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a1a07-121">*filePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1a07-122">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="a1a07-122">Type: **PCWSTR**</span></span>

<span data-ttu-id="a1a07-123">Percorso relativo di un file contenente una risorsa che si desidera indicizzare.</span><span class="sxs-lookup"><span data-stu-id="a1a07-123">A relative path to a file containing a resource that you want to index.</span></span> <span data-ttu-id="a1a07-124">Questo percorso è relativo alla radice del progetto dell'app UWP per cui si generano file PRI.</span><span class="sxs-lookup"><span data-stu-id="a1a07-124">This path is relative to the project root of the UWP app for which you are generating PRI files.</span></span> <span data-ttu-id="a1a07-125">La radice del progetto corrisponde al valore di *projectRoot* passato a [**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md).</span><span class="sxs-lookup"><span data-stu-id="a1a07-125">That project root is the value of *projectRoot* that you passed to [**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md).</span></span>

</dd> <dt>

<span data-ttu-id="a1a07-126">*qualificatori* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="a1a07-126">*qualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a1a07-127">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="a1a07-127">Type: **PCWSTR**</span></span>

<span data-ttu-id="a1a07-128">Elenco facoltativo di qualificatori di risorse, ad esempio L "lingua-en-US \_ scale-100 \_ contrasto-standard".</span><span class="sxs-lookup"><span data-stu-id="a1a07-128">An optional list of resource qualifiers, for example L"language-en-US\_scale-100\_contrast-standard".</span></span> <span data-ttu-id="a1a07-129">Una stringa vuota o **nullptr** indica una risorsa neutra.</span><span class="sxs-lookup"><span data-stu-id="a1a07-129">An empty string or **nullptr** indicates a neutral resource.</span></span> <span data-ttu-id="a1a07-130">I qualificatori di risorse *non* vengono dedotti da *resourceUri* né da *containerPath*.</span><span class="sxs-lookup"><span data-stu-id="a1a07-130">Resource qualifiers are *not* inferred from *resourceUri* nor from *containerPath*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1a07-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a1a07-131">Return value</span></span>

<span data-ttu-id="a1a07-132">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a1a07-132">Type: **HRESULT**</span></span>

<span data-ttu-id="a1a07-133">S \_ OK se la funzione ha avuto esito positivo, in caso contrario un altro valore.</span><span class="sxs-lookup"><span data-stu-id="a1a07-133">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="a1a07-134">Utilizzare le macro SUCCEEDed () o FAILED () (definite in Winerror. h) per determinare l'esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="a1a07-134">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1a07-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="a1a07-135">Remarks</span></span>

<span data-ttu-id="a1a07-136">Se si desidera specificare i qualificatori delle risorse, passarli nel parametro *Qualifiers* .</span><span class="sxs-lookup"><span data-stu-id="a1a07-136">If you want to specify any resource qualifiers, then pass them in the *qualifiers* parameter.</span></span> <span data-ttu-id="a1a07-137">I qualificatori di risorse *non* vengono dedotti da *resourceUri* né da *filePath*.</span><span class="sxs-lookup"><span data-stu-id="a1a07-137">Resource qualifiers are *not* inferred from *resourceUri* nor from *filePath*.</span></span>

<span data-ttu-id="a1a07-138">Il segmento di nome file di *resourceUri* (non *filePath*) viene usato come nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="a1a07-138">The file name segment of *resourceUri* (not *filePath*) is used as the resource name.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1a07-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a1a07-139">Requirements</span></span>



| <span data-ttu-id="a1a07-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1a07-140">Requirement</span></span> | <span data-ttu-id="a1a07-141">Valore</span><span class="sxs-lookup"><span data-stu-id="a1a07-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1a07-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a1a07-142">Minimum supported client</span></span><br/> | <span data-ttu-id="a1a07-143">Solo app desktop Windows 10 versione 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="a1a07-143">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="a1a07-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a1a07-144">Minimum supported server</span></span><br/> | <span data-ttu-id="a1a07-145">\[Solo app desktop Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="a1a07-145">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a1a07-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a1a07-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1a07-147"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1a07-147"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="a1a07-148">Libreria</span><span class="sxs-lookup"><span data-stu-id="a1a07-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="a1a07-149"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a1a07-149"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="a1a07-150">DLL</span><span class="sxs-lookup"><span data-stu-id="a1a07-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1a07-151"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1a07-151"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="a1a07-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a1a07-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1a07-153">API per l'indicizzazione delle risorse del pacchetto e sistemi di compilazione personalizzati</span><span class="sxs-lookup"><span data-stu-id="a1a07-153">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

