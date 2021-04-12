---
title: Funzione MrmIndexString (MrmResourceIndexer. h)
description: Indicizza una singola risorsa di stringa che appartiene a un'app UWP.
ms.assetid: 098F47E7-4BEC-452F-A33C-111F3F524E67
keywords:
- Menu della funzione MrmIndexString e altre risorse
topic_type:
- apiref
api_name:
- MrmIndexString
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec0c81155ae2484dd38f29e332a5f0093b07cd9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119095"
---
# <a name="mrmindexstring-function"></a><span data-ttu-id="4f448-104">MrmIndexString (funzione)</span><span class="sxs-lookup"><span data-stu-id="4f448-104">MrmIndexString function</span></span>

<span data-ttu-id="4f448-105">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="4f448-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="4f448-106">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="4f448-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="4f448-107">Indicizza una singola risorsa di stringa che appartiene a un'app UWP.</span><span class="sxs-lookup"><span data-stu-id="4f448-107">Indexes a single string resource belonging to a UWP app.</span></span> <span data-ttu-id="4f448-108">Accetta un elenco esplicito (ma facoltativo) di qualificatori di risorse.</span><span class="sxs-lookup"><span data-stu-id="4f448-108">Takes an explicit (but optional) list of resource qualifiers.</span></span> <span data-ttu-id="4f448-109">Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere [API pri (Package Resource Indexing) e sistemi di compilazione personalizzati](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="4f448-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="4f448-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4f448-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmIndexString(
  _In_     MrmResourceIndexerHandle indexer,
  _In_     PCWSTR                   resourceUri,
  _In_     PCWSTR                   resourceString,
  _In_opt_ PCWSTR                   qualifiers
);
```



## <a name="parameters"></a><span data-ttu-id="4f448-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="4f448-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f448-112">*indicizzatore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4f448-112">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f448-113">Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="4f448-113">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="4f448-114">Handle che identifica l'indicizzatore di risorse che indicizza le risorse di stringa.</span><span class="sxs-lookup"><span data-stu-id="4f448-114">A handle identifying the resource indexer that will index the string resources.</span></span>

</dd> <dt>

<span data-ttu-id="4f448-115">*resourceUri* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4f448-115">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f448-116">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="4f448-116">Type: **PCWSTR**</span></span>

<span data-ttu-id="4f448-117">URI della risorsa da assegnare alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="4f448-117">The resource URI to assign to the resource.</span></span> <span data-ttu-id="4f448-118">Il percorso verrà usato come nome del sottoalbero della mappa delle risorse per questa risorsa quando in seguito si genera un file PRI da questo indicizzatore di risorse.</span><span class="sxs-lookup"><span data-stu-id="4f448-118">The path will be used as the resource map subtree name for this resource when you later generate a PRI file from this resource indexer.</span></span>

</dd> <dt>

<span data-ttu-id="4f448-119">*resourceString* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4f448-119">*resourceString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f448-120">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="4f448-120">Type: **PCWSTR**</span></span>

<span data-ttu-id="4f448-121">Valore della risorsa di stringa.</span><span class="sxs-lookup"><span data-stu-id="4f448-121">The value of the string resource.</span></span>

</dd> <dt>

<span data-ttu-id="4f448-122">*qualificatori* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="4f448-122">*qualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4f448-123">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="4f448-123">Type: **PCWSTR**</span></span>

<span data-ttu-id="4f448-124">Elenco facoltativo di qualificatori di risorse, ad esempio L "lingua-en-US \_ scale-100 \_ contrasto-standard".</span><span class="sxs-lookup"><span data-stu-id="4f448-124">An optional list of resource qualifiers, for example L"language-en-US\_scale-100\_contrast-standard".</span></span> <span data-ttu-id="4f448-125">Una stringa vuota o **nullptr** indica una risorsa neutra.</span><span class="sxs-lookup"><span data-stu-id="4f448-125">An empty string or **nullptr** indicates a neutral resource.</span></span> <span data-ttu-id="4f448-126">I qualificatori di risorse *non* vengono dedotti da *resourceUri*.</span><span class="sxs-lookup"><span data-stu-id="4f448-126">Resource qualifiers are *not* inferred from *resourceUri*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f448-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4f448-127">Return value</span></span>

<span data-ttu-id="4f448-128">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4f448-128">Type: **HRESULT**</span></span>

<span data-ttu-id="4f448-129">S \_ OK se la funzione ha avuto esito positivo, in caso contrario un altro valore.</span><span class="sxs-lookup"><span data-stu-id="4f448-129">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="4f448-130">Utilizzare le macro SUCCEEDed () o FAILED () (definite in Winerror. h) per determinare l'esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="4f448-130">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f448-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="4f448-131">Remarks</span></span>

<span data-ttu-id="4f448-132">Se si desidera specificare i qualificatori delle risorse, passarli nel parametro *Qualifiers* .</span><span class="sxs-lookup"><span data-stu-id="4f448-132">If you want to specify any resource qualifiers, then pass them in the *qualifiers* parameter.</span></span> <span data-ttu-id="4f448-133">I qualificatori di risorse *non* vengono dedotti da *resourceUri*.</span><span class="sxs-lookup"><span data-stu-id="4f448-133">Resource qualifiers are *not* inferred from *resourceUri*.</span></span>

<span data-ttu-id="4f448-134">Il segmento di nome file di *resourceUri* viene usato come nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="4f448-134">The file name segment of *resourceUri* is used as the resource name.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f448-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4f448-135">Requirements</span></span>



| <span data-ttu-id="4f448-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f448-136">Requirement</span></span> | <span data-ttu-id="4f448-137">Valore</span><span class="sxs-lookup"><span data-stu-id="4f448-137">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f448-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f448-138">Minimum supported client</span></span><br/> | <span data-ttu-id="4f448-139">Solo app desktop Windows 10 versione 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="4f448-139">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="4f448-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f448-140">Minimum supported server</span></span><br/> | <span data-ttu-id="4f448-141">\[Solo app desktop Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="4f448-141">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4f448-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4f448-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f448-143"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f448-143"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="4f448-144">Libreria</span><span class="sxs-lookup"><span data-stu-id="4f448-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="4f448-145"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4f448-145"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="4f448-146">DLL</span><span class="sxs-lookup"><span data-stu-id="4f448-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f448-147"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f448-147"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="4f448-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4f448-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f448-149">API per l'indicizzazione delle risorse del pacchetto e sistemi di compilazione personalizzati</span><span class="sxs-lookup"><span data-stu-id="4f448-149">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

