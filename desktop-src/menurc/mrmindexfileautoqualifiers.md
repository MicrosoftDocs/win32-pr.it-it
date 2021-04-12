---
title: Funzione MrmIndexFileAutoQualifiers (MrmResourceIndexer. h)
description: Indicizza un file di risorse appartenente a un'app UWP. Deduce un elenco di qualificatori di risorse dal parametro FilePath. Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere API PRI (Package Resource Indexing) e sistemi di compilazione personalizzati.
ms.assetid: CEA4D845-987C-48D6-B80E-9F055363FFE0
keywords:
- Menu della funzione MrmIndexFileAutoQualifiers e altre risorse
topic_type:
- apiref
api_name:
- MrmIndexFileAutoQualifiers
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65254a8715073060e9b4fc1578b68d54ae987958
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119098"
---
# <a name="mrmindexfileautoqualifiers-function"></a><span data-ttu-id="2ca01-106">MrmIndexFileAutoQualifiers (funzione)</span><span class="sxs-lookup"><span data-stu-id="2ca01-106">MrmIndexFileAutoQualifiers function</span></span>

<span data-ttu-id="2ca01-107">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="2ca01-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2ca01-108">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="2ca01-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2ca01-109">Indicizza un file di risorse appartenente a un'app UWP.</span><span class="sxs-lookup"><span data-stu-id="2ca01-109">Indexes a resource file belonging to a UWP app.</span></span> <span data-ttu-id="2ca01-110">Deduce un elenco di qualificatori di risorse dal parametro *filePath* .</span><span class="sxs-lookup"><span data-stu-id="2ca01-110">Infers a list of resource qualifiers from the *filePath* parameter.</span></span> <span data-ttu-id="2ca01-111">Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere [API pri (Package Resource Indexing) e sistemi di compilazione personalizzati](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="2ca01-111">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="2ca01-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2ca01-112">Syntax</span></span>


```C++
HRESULT HRESULT MrmIndexFileAutoQualifiers(
  _In_ MrmResourceIndexerHandle indexer,
  _In_ PCWSTR                   filePath
);
```



## <a name="parameters"></a><span data-ttu-id="2ca01-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="2ca01-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ca01-114">*indicizzatore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2ca01-114">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ca01-115">Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="2ca01-115">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="2ca01-116">Handle che identifica l'indicizzatore di risorse che indicizza il file di risorse.</span><span class="sxs-lookup"><span data-stu-id="2ca01-116">A handle identifying the resource indexer that will index the resource file.</span></span>

</dd> <dt>

<span data-ttu-id="2ca01-117">*filePath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2ca01-117">*filePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ca01-118">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="2ca01-118">Type: **PCWSTR**</span></span>

<span data-ttu-id="2ca01-119">Percorso relativo di un file contenente una risorsa che si desidera indicizzare.</span><span class="sxs-lookup"><span data-stu-id="2ca01-119">A relative path to a file containing a resource that you want to index.</span></span> <span data-ttu-id="2ca01-120">Questo percorso è relativo alla radice del progetto dell'app UWP per cui si generano file PRI.</span><span class="sxs-lookup"><span data-stu-id="2ca01-120">This path is relative to the project root of the UWP app for which you are generating PRI files.</span></span> <span data-ttu-id="2ca01-121">La radice del progetto corrisponde al valore di *projectRoot* passato a [**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md).</span><span class="sxs-lookup"><span data-stu-id="2ca01-121">That project root is the value of *projectRoot* that you passed to [**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ca01-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2ca01-122">Return value</span></span>

<span data-ttu-id="2ca01-123">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="2ca01-123">Type: **HRESULT**</span></span>

<span data-ttu-id="2ca01-124">S \_ OK se la funzione ha avuto esito positivo, in caso contrario un altro valore.</span><span class="sxs-lookup"><span data-stu-id="2ca01-124">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="2ca01-125">Utilizzare le macro SUCCEEDed () o FAILED () (definite in Winerror. h) per determinare l'esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="2ca01-125">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ca01-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="2ca01-126">Remarks</span></span>

<span data-ttu-id="2ca01-127">Il segmento di nome file di *filePath* viene usato come nome della risorsa; i qualificatori di risorse e vengono derivati dal percorso.</span><span class="sxs-lookup"><span data-stu-id="2ca01-127">The file name segment of *filePath* is used as the resource name; and resource qualifiers are derived from its path.</span></span> <span data-ttu-id="2ca01-128">Se ad esempio si passa L "images \\ de-de \\ scale-100 \\background.png" a *filePath* , l'indicizzatore di risorse aggiunge una risorsa denominata "background.png" con i qualificatori di risorse "Language-de-de" e "scale-100".</span><span class="sxs-lookup"><span data-stu-id="2ca01-128">For example, if you pass L"Images\\de-DE\\scale-100\\background.png" to *filePath* then the resource indexer adds a resource named "background.png" with resource qualifiers "language-de-DE" and "scale-100".</span></span>

<span data-ttu-id="2ca01-129">L "files" verrà usato come nome del sottoalbero della mappa delle risorse per questa risorsa quando in seguito si genera un file PRI da questo indicizzatore di risorse.</span><span class="sxs-lookup"><span data-stu-id="2ca01-129">L"Files" will be used as the resource map subtree name for this resource when you later generate a PRI file from this resource indexer.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ca01-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2ca01-130">Requirements</span></span>



| <span data-ttu-id="2ca01-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ca01-131">Requirement</span></span> | <span data-ttu-id="2ca01-132">Valore</span><span class="sxs-lookup"><span data-stu-id="2ca01-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ca01-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2ca01-133">Minimum supported client</span></span><br/> | <span data-ttu-id="2ca01-134">Solo app desktop Windows 10 versione 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="2ca01-134">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="2ca01-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2ca01-135">Minimum supported server</span></span><br/> | <span data-ttu-id="2ca01-136">\[Solo app desktop Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="2ca01-136">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2ca01-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2ca01-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ca01-138"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ca01-138"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="2ca01-139">Libreria</span><span class="sxs-lookup"><span data-stu-id="2ca01-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="2ca01-140"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2ca01-140"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="2ca01-141">DLL</span><span class="sxs-lookup"><span data-stu-id="2ca01-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ca01-142"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ca01-142"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="2ca01-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2ca01-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ca01-144">API per l'indicizzazione delle risorse del pacchetto e sistemi di compilazione personalizzati</span><span class="sxs-lookup"><span data-stu-id="2ca01-144">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

