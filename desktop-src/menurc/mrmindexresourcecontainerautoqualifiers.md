---
title: Funzione MrmIndexResourceContainerAutoQualifiers (MrmResourceIndexer. h)
description: Indicizza le risorse di stringa contenute in un file di risorse (con estensione resw/resjson) o con estensione PRIInfo o prifile, appartenenti a un'app UWP.
ms.assetid: 7FCAA2B5-FF45-4961-84BA-B444B550C91D
keywords:
- Menu della funzione MrmIndexResourceContainerAutoQualifiers e altre risorse
topic_type:
- apiref
api_name:
- MrmIndexResourceContainerAutoQualifiers
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 234566d166e73f75a70b6e613d3f0dfda648ff7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302320"
---
# <a name="mrmindexresourcecontainerautoqualifiers-function"></a><span data-ttu-id="ca744-104">MrmIndexResourceContainerAutoQualifiers (funzione)</span><span class="sxs-lookup"><span data-stu-id="ca744-104">MrmIndexResourceContainerAutoQualifiers function</span></span>

<span data-ttu-id="ca744-105">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="ca744-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ca744-106">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="ca744-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ca744-107">Indicizza le risorse di stringa contenute in un file di risorse (con estensione resw/resjson) o con estensione PRIInfo o prifile, appartenenti a un'app UWP.</span><span class="sxs-lookup"><span data-stu-id="ca744-107">Indexes the string resources contained inside a Resources File (.resw/.resjson), or a .priinfo or .prifile, belonging to a UWP app.</span></span> <span data-ttu-id="ca744-108">Deduce un elenco di qualificatori di risorse dal parametro *containerPath* .</span><span class="sxs-lookup"><span data-stu-id="ca744-108">Infers a list of resource qualifiers from the *containerPath* parameter.</span></span> <span data-ttu-id="ca744-109">Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere [API pri (Package Resource Indexing) e sistemi di compilazione personalizzati](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="ca744-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="ca744-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ca744-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmIndexResourceContainerAutoQualifiers(
  _In_ MrmResourceIndexerHandle indexer,
  _In_ PCWSTR                   containerPath
);
```



## <a name="parameters"></a><span data-ttu-id="ca744-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="ca744-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca744-112">*indicizzatore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ca744-112">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca744-113">Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="ca744-113">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="ca744-114">Handle che identifica l'indicizzatore di risorse che indicizza le risorse di stringa.</span><span class="sxs-lookup"><span data-stu-id="ca744-114">A handle identifying the resource indexer that will index the string resources.</span></span>

</dd> <dt>

<span data-ttu-id="ca744-115">*containerPath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ca744-115">*containerPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca744-116">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="ca744-116">Type: **PCWSTR**</span></span>

<span data-ttu-id="ca744-117">Percorso relativo di un oggetto. resw,. resjson,. PRIInfo o. prifile che contiene le risorse di stringa che si desidera indicizzare.</span><span class="sxs-lookup"><span data-stu-id="ca744-117">A relative path to a .resw, .resjson, .priinfo, or .prifile containing string resources that you want to index.</span></span> <span data-ttu-id="ca744-118">Questo percorso è relativo alla radice del progetto dell'app UWP per cui si generano file PRI.</span><span class="sxs-lookup"><span data-stu-id="ca744-118">This path is relative to the project root of the UWP app for which you are generating PRI files.</span></span> <span data-ttu-id="ca744-119">La radice del progetto corrisponde al valore di *projectRoot* passato a [**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md).</span><span class="sxs-lookup"><span data-stu-id="ca744-119">That project root is the value of *projectRoot* that you passed to [**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca744-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ca744-120">Return value</span></span>

<span data-ttu-id="ca744-121">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ca744-121">Type: **HRESULT**</span></span>

<span data-ttu-id="ca744-122">S \_ OK se la funzione ha avuto esito positivo, in caso contrario un altro valore.</span><span class="sxs-lookup"><span data-stu-id="ca744-122">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="ca744-123">Utilizzare le macro SUCCEEDed () o FAILED () (definite in Winerror. h) per determinare l'esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="ca744-123">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca744-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="ca744-124">Remarks</span></span>

<span data-ttu-id="ca744-125">I qualificatori di risorse vengono dedotti da *containerPath*.</span><span class="sxs-lookup"><span data-stu-id="ca744-125">Resource qualifiers are inferred from *containerPath*.</span></span> <span data-ttu-id="ca744-126">Ad esempio, un valore di L "en-US \\ \\ Resources. resw" aggiunge risorse di stringa con il qualificatore "Language-en-US".</span><span class="sxs-lookup"><span data-stu-id="ca744-126">For example, a value of L"en-US\\\\resources.resw" adds string resources with the qualifier "language-en-US".</span></span>

<span data-ttu-id="ca744-127">Il nome del file di risorse verrà usato come nome del sottoalbero della mappa risorse per queste risorse quando in seguito si genera un file PRI da questo indicizzatore di risorse.</span><span class="sxs-lookup"><span data-stu-id="ca744-127">The name of the Resources File will be used as the resource map subtree name for these resources when you later generate a PRI file from this resource indexer.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca744-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ca744-128">Requirements</span></span>



| <span data-ttu-id="ca744-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca744-129">Requirement</span></span> | <span data-ttu-id="ca744-130">Valore</span><span class="sxs-lookup"><span data-stu-id="ca744-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca744-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca744-131">Minimum supported client</span></span><br/> | <span data-ttu-id="ca744-132">Solo app desktop Windows 10 versione 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="ca744-132">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="ca744-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca744-133">Minimum supported server</span></span><br/> | <span data-ttu-id="ca744-134">\[Solo app desktop Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="ca744-134">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ca744-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ca744-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca744-136"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca744-136"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="ca744-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="ca744-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="ca744-138"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ca744-138"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="ca744-139">DLL</span><span class="sxs-lookup"><span data-stu-id="ca744-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca744-140"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca744-140"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="ca744-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ca744-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca744-142">API per l'indicizzazione delle risorse del pacchetto e sistemi di compilazione personalizzati</span><span class="sxs-lookup"><span data-stu-id="ca744-142">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

