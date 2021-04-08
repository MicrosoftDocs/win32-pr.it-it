---
title: Funzione MrmDumpPriFile (MrmResourceIndexer. h)
description: Consente di eseguire il dump di un file PRI (binario) al relativo equivalente XML (come file su disco), in modo da renderlo più facilmente leggibile.
ms.assetid: FE1982AB-881C-4F07-8B9E-E3770E5B5099
keywords:
- Menu della funzione MrmDumpPriFile e altre risorse
topic_type:
- apiref
api_name:
- MrmDumpPriFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba254cbac0dd8afd328e0d7e04f573138f14b588
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741826"
---
# <a name="mrmdumpprifile-function"></a><span data-ttu-id="15dff-104">MrmDumpPriFile (funzione)</span><span class="sxs-lookup"><span data-stu-id="15dff-104">MrmDumpPriFile function</span></span>

<span data-ttu-id="15dff-105">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="15dff-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="15dff-106">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="15dff-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="15dff-107">Consente di eseguire il dump di un file PRI (binario) al relativo equivalente XML (come file su disco), in modo da renderlo più facilmente leggibile.</span><span class="sxs-lookup"><span data-stu-id="15dff-107">Dumps a PRI file (which is binary) to its XML equivalent (as a file on disk), in order to make it more easily readable.</span></span> <span data-ttu-id="15dff-108">Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere [API pri (Package Resource Indexing) e sistemi di compilazione personalizzati](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="15dff-108">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="15dff-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="15dff-109">Syntax</span></span>


```C++
HRESULT HRESULT MrmDumpPriFile(
  _In_     PCWSTR      indexFileName,
  _In_opt_ PCWSTR      schemaPriFile,
  _In_     MrmDumpType dumpType,
  _In_     PCWSTR      outputXmlFile
);
```



## <a name="parameters"></a><span data-ttu-id="15dff-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="15dff-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15dff-111">*indexFileName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15dff-111">*indexFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15dff-112">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="15dff-112">Type: **PCWSTR**</span></span>

<span data-ttu-id="15dff-113">Percorso di file completo di un file PRI.</span><span class="sxs-lookup"><span data-stu-id="15dff-113">A full file path to a PRI file.</span></span> <span data-ttu-id="15dff-114">Si tratta del file PRI di cui verrà eseguito il dump in XML.</span><span class="sxs-lookup"><span data-stu-id="15dff-114">This is the PRI file that will be dumped to XML.</span></span>

</dd> <dt>

<span data-ttu-id="15dff-115">*schemaPriFile* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="15dff-115">*schemaPriFile* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="15dff-116">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="15dff-116">Type: **PCWSTR**</span></span>

<span data-ttu-id="15dff-117">Percorso file completo facoltativo di un file di schema o di un file PRI che rappresenta uno schema. vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="15dff-117">An optional full file path to a schema file (or to a PRI file representing a schema; see Remarks).</span></span>

</dd> <dt>

<span data-ttu-id="15dff-118">*dumpType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15dff-118">*dumpType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15dff-119">Tipo: **[ **MrmDumpType**](mrmdumptype.md)**</span><span class="sxs-lookup"><span data-stu-id="15dff-119">Type: **[**MrmDumpType**](mrmdumptype.md)**</span></span>

<span data-ttu-id="15dff-120">Specifica il modo in cui il dump XML deve essere dettagliato o se deve essere eseguito il dump di uno schema.</span><span class="sxs-lookup"><span data-stu-id="15dff-120">Specifies how detailed the XML dump should be, or whether a schema should be dumped.</span></span>

</dd> <dt>

<span data-ttu-id="15dff-121">*outputXmlFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15dff-121">*outputXmlFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15dff-122">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="15dff-122">Type: **PCWSTR**</span></span>

<span data-ttu-id="15dff-123">Percorso di un file XML da creare.</span><span class="sxs-lookup"><span data-stu-id="15dff-123">The path of an XML file to create.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15dff-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="15dff-124">Return value</span></span>

<span data-ttu-id="15dff-125">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="15dff-125">Type: **HRESULT**</span></span>

<span data-ttu-id="15dff-126">S \_ OK se la funzione ha avuto esito positivo, in caso contrario un altro valore.</span><span class="sxs-lookup"><span data-stu-id="15dff-126">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="15dff-127">Utilizzare le macro SUCCEEDed () o FAILED () (definite in Winerror. h) per determinare l'esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="15dff-127">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="15dff-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="15dff-128">Remarks</span></span>

<span data-ttu-id="15dff-129">Un pacchetto di risorse senza schema è uno creato con l'argomento [**MrmPackagingOptionsOmitSchemaFromResourcePacks**](mrmpackagingoptions.md) passato a [**MrmCreateResourceFile**](mrmcreateresourcefile.md) o [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) (oppure con l'opzione *omitSchemaFromResourcePacks* nel file di configurazione pri).</span><span class="sxs-lookup"><span data-stu-id="15dff-129">A schema-free resource pack is one that was created with the [**MrmPackagingOptionsOmitSchemaFromResourcePacks**](mrmpackagingoptions.md) argument passed to [**MrmCreateResourceFile**](mrmcreateresourcefile.md) or [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) (or with the *omitSchemaFromResourcePacks* switch in the PRI config file).</span></span> <span data-ttu-id="15dff-130">Per eseguire il dump di un pacchetto di risorse senza schema, passare il percorso ai dati PRI del pacchetto principale come argomento per il parametro *schemaPriFile* .</span><span class="sxs-lookup"><span data-stu-id="15dff-130">To dump a schema-free resource pack, pass the path to your main package PRI data as the argument for the *schemaPriFile* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="15dff-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="15dff-131">Requirements</span></span>



| <span data-ttu-id="15dff-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="15dff-132">Requirement</span></span> | <span data-ttu-id="15dff-133">Valore</span><span class="sxs-lookup"><span data-stu-id="15dff-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15dff-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="15dff-134">Minimum supported client</span></span><br/> | <span data-ttu-id="15dff-135">Solo app desktop Windows 10 versione 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="15dff-135">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="15dff-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="15dff-136">Minimum supported server</span></span><br/> | <span data-ttu-id="15dff-137">\[Solo app desktop Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="15dff-137">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="15dff-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="15dff-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="15dff-139"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="15dff-139"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="15dff-140">Libreria</span><span class="sxs-lookup"><span data-stu-id="15dff-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="15dff-141"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="15dff-141"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="15dff-142">DLL</span><span class="sxs-lookup"><span data-stu-id="15dff-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15dff-143"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15dff-143"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="15dff-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="15dff-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15dff-145">API per l'indicizzazione delle risorse del pacchetto e sistemi di compilazione personalizzati</span><span class="sxs-lookup"><span data-stu-id="15dff-145">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

