---
title: Funzione MrmIndexEmbeddedData (MrmResourceIndexer. h)
description: Indicizza una singola risorsa dati incorporata che appartiene a un'app UWP.
ms.assetid: 4DA37CF9-43B6-44EE-8A10-DBD4510D7885
keywords:
- Menu della funzione MrmIndexEmbeddedData e altre risorse
topic_type:
- apiref
api_name:
- MrmIndexEmbeddedData
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 308d08e0e125e7919ad3eb32e6cba2184356fce5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301023"
---
# <a name="mrmindexembeddeddata-function"></a><span data-ttu-id="12525-104">MrmIndexEmbeddedData (funzione)</span><span class="sxs-lookup"><span data-stu-id="12525-104">MrmIndexEmbeddedData function</span></span>

<span data-ttu-id="12525-105">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="12525-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="12525-106">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="12525-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="12525-107">Indicizza una singola risorsa **dati incorporata** che appartiene a un'app UWP.</span><span class="sxs-lookup"><span data-stu-id="12525-107">Indexes a single **embeddeddata** resource belonging to a UWP app.</span></span> <span data-ttu-id="12525-108">Accetta un elenco esplicito (ma facoltativo) di qualificatori di risorse.</span><span class="sxs-lookup"><span data-stu-id="12525-108">Takes an explicit (but optional) list of resource qualifiers.</span></span> <span data-ttu-id="12525-109">Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere [API pri (Package Resource Indexing) e sistemi di compilazione personalizzati](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="12525-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="12525-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="12525-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmIndexEmbeddedData(
  _In_           MrmResourceIndexerHandle indexer,
  _In_           PCWSTR                   resourceUri,
  _In_     const BYTE                     *embeddedData,
  _In_           ULONG                    embeddedDataSize,
  _In_opt_       PCWSTR                   qualifiers
);
```



## <a name="parameters"></a><span data-ttu-id="12525-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="12525-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12525-112">*indicizzatore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="12525-112">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12525-113">Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="12525-113">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="12525-114">Handle che identifica l'indicizzatore di risorse che indicizza il file di risorse.</span><span class="sxs-lookup"><span data-stu-id="12525-114">A handle identifying the resource indexer that will index the resource file.</span></span>

</dd> <dt>

<span data-ttu-id="12525-115">*resourceUri* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="12525-115">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12525-116">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="12525-116">Type: **PCWSTR**</span></span>

<span data-ttu-id="12525-117">URI della risorsa da assegnare alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="12525-117">The resource URI to assign to the resource.</span></span> <span data-ttu-id="12525-118">Il percorso verrà usato come nome del sottoalbero della mappa delle risorse per questa risorsa quando in seguito si genera un file PRI da questo indicizzatore di risorse.</span><span class="sxs-lookup"><span data-stu-id="12525-118">The path will be used as the resource map subtree name for this resource when you later generate a PRI file from this resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="12525-119">*dati incorporata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="12525-119">*embeddedData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12525-120">Tipo: \**const \* byte* _</span><span class="sxs-lookup"><span data-stu-id="12525-120">Type: \**const BYTE\** _</span></span>

<span data-ttu-id="12525-121">Puntatore ai dati della risorsa che si desidera indicizzare.</span><span class="sxs-lookup"><span data-stu-id="12525-121">A pointer to the data of the resource that you want to index.</span></span>

</dd> <dt>

<span data-ttu-id="12525-122">_embeddedDataSize \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="12525-122">_embeddedDataSize\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12525-123">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="12525-123">Type: **ULONG**</span></span>

<span data-ttu-id="12525-124">Dimensione dei dati a cui punta *dati incorporata*.</span><span class="sxs-lookup"><span data-stu-id="12525-124">The size of the data pointed to by *embeddedData*.</span></span>

</dd> <dt>

<span data-ttu-id="12525-125">*qualificatori* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="12525-125">*qualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="12525-126">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="12525-126">Type: **PCWSTR**</span></span>

<span data-ttu-id="12525-127">Elenco facoltativo di qualificatori di risorse, ad esempio L "lingua-en-US \_ scale-100 \_ contrasto-standard".</span><span class="sxs-lookup"><span data-stu-id="12525-127">An optional list of resource qualifiers, for example L"language-en-US\_scale-100\_contrast-standard".</span></span> <span data-ttu-id="12525-128">Una stringa vuota o **nullptr** indica una risorsa neutra.</span><span class="sxs-lookup"><span data-stu-id="12525-128">An empty string or **nullptr** indicates a neutral resource.</span></span> <span data-ttu-id="12525-129">I qualificatori di risorse *non* vengono dedotti da *resourceUri*.</span><span class="sxs-lookup"><span data-stu-id="12525-129">Resource qualifiers are *not* inferred from *resourceUri*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12525-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="12525-130">Return value</span></span>

<span data-ttu-id="12525-131">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="12525-131">Type: **HRESULT**</span></span>

<span data-ttu-id="12525-132">S \_ OK se la funzione ha avuto esito positivo, in caso contrario un altro valore.</span><span class="sxs-lookup"><span data-stu-id="12525-132">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="12525-133">Utilizzare le macro SUCCEEDed () o FAILED () (definite in Winerror. h) per determinare l'esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="12525-133">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="12525-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="12525-134">Remarks</span></span>

<span data-ttu-id="12525-135">Se si desidera specificare i qualificatori delle risorse, passarli nel parametro *Qualifiers* .</span><span class="sxs-lookup"><span data-stu-id="12525-135">If you want to specify any resource qualifiers, then pass them in the *qualifiers* parameter.</span></span> <span data-ttu-id="12525-136">I qualificatori di risorse *non* vengono dedotti da *resourceUri*.</span><span class="sxs-lookup"><span data-stu-id="12525-136">Resource qualifiers are *not* inferred from *resourceUri*.</span></span>

<span data-ttu-id="12525-137">Il segmento di nome file di *resourceUri* viene usato come nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="12525-137">The file name segment of *resourceUri* is used as the resource name.</span></span>

## <a name="requirements"></a><span data-ttu-id="12525-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="12525-138">Requirements</span></span>



| <span data-ttu-id="12525-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="12525-139">Requirement</span></span> | <span data-ttu-id="12525-140">Valore</span><span class="sxs-lookup"><span data-stu-id="12525-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12525-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="12525-141">Minimum supported client</span></span><br/> | <span data-ttu-id="12525-142">Solo app desktop Windows 10 versione 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="12525-142">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="12525-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="12525-143">Minimum supported server</span></span><br/> | <span data-ttu-id="12525-144">\[Solo app desktop Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="12525-144">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="12525-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="12525-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="12525-146"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="12525-146"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="12525-147">Libreria</span><span class="sxs-lookup"><span data-stu-id="12525-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="12525-148"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="12525-148"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="12525-149">DLL</span><span class="sxs-lookup"><span data-stu-id="12525-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12525-150"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12525-150"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="12525-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="12525-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12525-152">API per l'indicizzazione delle risorse del pacchetto e sistemi di compilazione personalizzati</span><span class="sxs-lookup"><span data-stu-id="12525-152">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

