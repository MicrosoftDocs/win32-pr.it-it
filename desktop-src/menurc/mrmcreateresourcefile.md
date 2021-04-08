---
title: Funzione MrmCreateResourceFile (MrmResourceIndexer. h)
description: Crea un file PRI (denominato \ 0034; resources. pri \ 0034;) o file su disco nella cartella specificata. Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere API PRI (Package Resource Indexing) e sistemi di compilazione personalizzati.
ms.assetid: B9CE0638-4650-4E1A-BE5E-4CC7C6614030
keywords:
- Menu della funzione MrmCreateResourceFile e altre risorse
topic_type:
- apiref
api_name:
- MrmCreateResourceFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f80294e5829dbf90c8aa3b0f6485c2da4185add1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743063"
---
# <a name="mrmcreateresourcefile-function"></a><span data-ttu-id="3fb78-105">MrmCreateResourceFile (funzione)</span><span class="sxs-lookup"><span data-stu-id="3fb78-105">MrmCreateResourceFile function</span></span>

<span data-ttu-id="3fb78-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="3fb78-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="3fb78-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="3fb78-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="3fb78-108">Crea un file PRI (denominato "resources. pri") o file su disco nella cartella specificata.</span><span class="sxs-lookup"><span data-stu-id="3fb78-108">Creates a PRI file (named "resources.pri"), or files, on disk in the specified folder.</span></span> <span data-ttu-id="3fb78-109">Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere [API pri (Package Resource Indexing) e sistemi di compilazione personalizzati](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="3fb78-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="3fb78-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3fb78-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateResourceFile(
  _In_ MrmResourceIndexerHandle indexer,
  _In_ MrmPackagingMode         packagingMode,
  _In_ MrmPackagingOptions      packagingOptions,
       PCWSTR                   outputDirectory
);
```



## <a name="parameters"></a><span data-ttu-id="3fb78-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="3fb78-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fb78-112">*indicizzatore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3fb78-112">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fb78-113">Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="3fb78-113">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="3fb78-114">Handle che identifica l'indicizzatore di risorse da cui creare il file PRI.</span><span class="sxs-lookup"><span data-stu-id="3fb78-114">A handle identifying the resource indexer from which to create the PRI file.</span></span>

</dd> <dt>

<span data-ttu-id="3fb78-115">*packagingMode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3fb78-115">*packagingMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fb78-116">Tipo: **[ **MrmPackagingMode**](mrmpackagingmode.md)**</span><span class="sxs-lookup"><span data-stu-id="3fb78-116">Type: **[**MrmPackagingMode**](mrmpackagingmode.md)**</span></span>

<span data-ttu-id="3fb78-117">Specifica se il file PRI deve essere autonomo, suddividerlo automaticamente in base al qualificatore di risorse oppure essere un pacchetto di risorse.</span><span class="sxs-lookup"><span data-stu-id="3fb78-117">Specifies whether the PRI file should be standalone, be automatically split by resource qualifier, or be a resource pack.</span></span>

</dd> <dt>

<span data-ttu-id="3fb78-118">*packagingOptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3fb78-118">*packagingOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fb78-119">Tipo: **[ **MrmPackagingOptions**](mrmpackagingoptions.md)**</span><span class="sxs-lookup"><span data-stu-id="3fb78-119">Type: **[**MrmPackagingOptions**](mrmpackagingoptions.md)**</span></span>

<span data-ttu-id="3fb78-120">Specifica opzioni aggiuntive per il file PRI.</span><span class="sxs-lookup"><span data-stu-id="3fb78-120">Specifies additional options about the PRI file.</span></span>

</dd> <dt>

<span data-ttu-id="3fb78-121">*outputDirectory*</span><span class="sxs-lookup"><span data-stu-id="3fb78-121">*outputDirectory*</span></span> 
</dt> <dd>

<span data-ttu-id="3fb78-122">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="3fb78-122">Type: **PCWSTR**</span></span>

<span data-ttu-id="3fb78-123">Percorso di una cartella in cui salvare il file PRI.</span><span class="sxs-lookup"><span data-stu-id="3fb78-123">A path to a folder in which to save the PRI file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fb78-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3fb78-124">Return value</span></span>

<span data-ttu-id="3fb78-125">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3fb78-125">Type: **HRESULT**</span></span>

<span data-ttu-id="3fb78-126">S \_ OK se la funzione ha avuto esito positivo, in caso contrario un altro valore.</span><span class="sxs-lookup"><span data-stu-id="3fb78-126">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="3fb78-127">Utilizzare le macro SUCCEEDed () o FAILED () (definite in Winerror. h) per determinare l'esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="3fb78-127">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fb78-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3fb78-128">Requirements</span></span>



| <span data-ttu-id="3fb78-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fb78-129">Requirement</span></span> | <span data-ttu-id="3fb78-130">Valore</span><span class="sxs-lookup"><span data-stu-id="3fb78-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fb78-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3fb78-131">Minimum supported client</span></span><br/> | <span data-ttu-id="3fb78-132">Solo app desktop Windows 10 versione 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="3fb78-132">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="3fb78-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3fb78-133">Minimum supported server</span></span><br/> | <span data-ttu-id="3fb78-134">\[Solo app desktop Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="3fb78-134">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3fb78-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3fb78-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="3fb78-136"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="3fb78-136"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="3fb78-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="3fb78-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="3fb78-138"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3fb78-138"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="3fb78-139">DLL</span><span class="sxs-lookup"><span data-stu-id="3fb78-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3fb78-140"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3fb78-140"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="3fb78-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3fb78-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fb78-142">API per l'indicizzazione delle risorse del pacchetto e sistemi di compilazione personalizzati</span><span class="sxs-lookup"><span data-stu-id="3fb78-142">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

