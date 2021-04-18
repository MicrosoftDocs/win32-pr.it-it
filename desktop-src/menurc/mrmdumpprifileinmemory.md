---
title: Funzione MrmDumpPriFileInMemory (MrmResourceIndexer. h)
description: Consente di eseguire il dump di un file PRI (binario) al relativo equivalente XML (come dati in memoria), in modo da renderlo più facilmente leggibile.
ms.assetid: 04FD048F-1473-47B1-9CAB-03FEF98A9B48
keywords:
- Menu della funzione MrmDumpPriFileInMemory e altre risorse
topic_type:
- apiref
api_name:
- MrmDumpPriFileInMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 253db38bf1e272f21ff66210bdbd07d5a33f4c60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301024"
---
# <a name="mrmdumpprifileinmemory-function"></a><span data-ttu-id="36581-104">MrmDumpPriFileInMemory (funzione)</span><span class="sxs-lookup"><span data-stu-id="36581-104">MrmDumpPriFileInMemory function</span></span>

<span data-ttu-id="36581-105">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="36581-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="36581-106">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="36581-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="36581-107">Consente di eseguire il dump di un file PRI (binario) al relativo equivalente XML (come dati in memoria), in modo da renderlo più facilmente leggibile.</span><span class="sxs-lookup"><span data-stu-id="36581-107">Dumps a PRI file (which is binary) to its XML equivalent (as in-memory data), in order to make it more easily readable.</span></span> <span data-ttu-id="36581-108">La funzione alloca memoria e restituisce un puntatore a tale memoria in *outputXmlData*.</span><span class="sxs-lookup"><span data-stu-id="36581-108">The function allocates memory and returns a pointer to that memory in *outputXmlData*.</span></span> <span data-ttu-id="36581-109">Chiamare [**MrmFreeMemory**](mrmfreememory.md) con lo stesso puntatore per liberare la memoria.</span><span class="sxs-lookup"><span data-stu-id="36581-109">Call [**MrmFreeMemory**](mrmfreememory.md) with the same pointer to free that memory.</span></span> <span data-ttu-id="36581-110">Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere [API pri (Package Resource Indexing) e sistemi di compilazione personalizzati](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="36581-110">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="36581-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="36581-111">Syntax</span></span>


```C++
HRESULT HRESULT MrmDumpPriFileInMemory(
  _In_     PCWSTR      indexFileName,
  _In_opt_ PCWSTR      schemaPriFile,
  _In_     MrmDumpType dumpType,
  _Out_    BYTE        **outputXmlData,
  _Out_    ULONG       *outputXmlSize
);
```



## <a name="parameters"></a><span data-ttu-id="36581-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="36581-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36581-113">*indexFileName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="36581-113">*indexFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36581-114">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="36581-114">Type: **PCWSTR**</span></span>

<span data-ttu-id="36581-115">Percorso di file completo di un file PRI.</span><span class="sxs-lookup"><span data-stu-id="36581-115">A full file path to a PRI file.</span></span> <span data-ttu-id="36581-116">Si tratta del file PRI di cui verrà eseguito il dump in XML.</span><span class="sxs-lookup"><span data-stu-id="36581-116">This is the PRI file that will be dumped to XML.</span></span>

</dd> <dt>

<span data-ttu-id="36581-117">*schemaPriFile* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="36581-117">*schemaPriFile* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="36581-118">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="36581-118">Type: **PCWSTR**</span></span>

<span data-ttu-id="36581-119">Percorso file completo facoltativo di un file di schema o di un file PRI che rappresenta uno schema. vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="36581-119">An optional full file path to a schema file (or to a PRI file representing a schema; see Remarks).</span></span>

</dd> <dt>

<span data-ttu-id="36581-120">*dumpType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="36581-120">*dumpType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36581-121">Tipo: **[ **MrmDumpType**](mrmdumptype.md)**</span><span class="sxs-lookup"><span data-stu-id="36581-121">Type: **[**MrmDumpType**](mrmdumptype.md)**</span></span>

<span data-ttu-id="36581-122">Specifica il modo in cui il dump XML deve essere dettagliato o se deve essere eseguito il dump di uno schema.</span><span class="sxs-lookup"><span data-stu-id="36581-122">Specifies how detailed the XML dump should be, or whether a schema should be dumped.</span></span>

</dd> <dt>

<span data-ttu-id="36581-123">*outputXmlData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="36581-123">*outputXmlData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="36581-124">Tipo: **byte \* \***</span><span class="sxs-lookup"><span data-stu-id="36581-124">Type: **BYTE\*\***</span></span>

<span data-ttu-id="36581-125">Indirizzo di un puntatore a BYTE.</span><span class="sxs-lookup"><span data-stu-id="36581-125">The address of a pointer to BYTE.</span></span> <span data-ttu-id="36581-126">La funzione alloca memoria e restituisce un puntatore a tale memoria in *outputXmlData*.</span><span class="sxs-lookup"><span data-stu-id="36581-126">The function allocates memory and returns a pointer to that memory in *outputXmlData*.</span></span> <span data-ttu-id="36581-127">Chiamare [**MrmFreeMemory**](mrmfreememory.md) con il puntatore a byte per liberare la memoria.</span><span class="sxs-lookup"><span data-stu-id="36581-127">Call [**MrmFreeMemory**](mrmfreememory.md) with your pointer to BYTE to free that memory.</span></span>

</dd> <dt>

<span data-ttu-id="36581-128">*outputXmlSize* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="36581-128">*outputXmlSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="36581-129">Tipo: \**ULONG \** _</span><span class="sxs-lookup"><span data-stu-id="36581-129">Type: \**ULONG\** _</span></span>

<span data-ttu-id="36581-130">Indirizzo di ULONG.</span><span class="sxs-lookup"><span data-stu-id="36581-130">The address of a ULONG.</span></span> <span data-ttu-id="36581-131">In _outputXmlSize \*, la funzione restituisce le dimensioni della memoria allocata a cui punta *outputXmlData*.</span><span class="sxs-lookup"><span data-stu-id="36581-131">In _outputXmlSize\*, the function returns the size of the allocated memory pointed to by *outputXmlData*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36581-132">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="36581-132">Return value</span></span>

<span data-ttu-id="36581-133">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="36581-133">Type: **HRESULT**</span></span>

<span data-ttu-id="36581-134">S \_ OK se la funzione ha avuto esito positivo, in caso contrario un altro valore.</span><span class="sxs-lookup"><span data-stu-id="36581-134">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="36581-135">Utilizzare le macro SUCCEEDed () o FAILED () (definite in Winerror. h) per determinare l'esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="36581-135">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="36581-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="36581-136">Remarks</span></span>

<span data-ttu-id="36581-137">Un pacchetto di risorse senza schema è uno creato con l'argomento [**MrmPackagingOptionsOmitSchemaFromResourcePacks**](mrmpackagingoptions.md) passato a [**MrmCreateResourceFile**](mrmcreateresourcefile.md) o [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) (oppure con l'opzione *omitSchemaFromResourcePacks* nel file di configurazione pri).</span><span class="sxs-lookup"><span data-stu-id="36581-137">A schema-free resource pack is one that was created with the [**MrmPackagingOptionsOmitSchemaFromResourcePacks**](mrmpackagingoptions.md) argument passed to [**MrmCreateResourceFile**](mrmcreateresourcefile.md) or [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) (or with the *omitSchemaFromResourcePacks* switch in the PRI config file).</span></span> <span data-ttu-id="36581-138">Per eseguire il dump di un pacchetto di risorse senza schema, passare il percorso ai dati PRI del pacchetto principale come argomento per il parametro *schemaPriFile* .</span><span class="sxs-lookup"><span data-stu-id="36581-138">To dump a schema-free resource pack, pass the path to your main package PRI data as the argument for the *schemaPriFile* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="36581-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="36581-139">Requirements</span></span>



| <span data-ttu-id="36581-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="36581-140">Requirement</span></span> | <span data-ttu-id="36581-141">Valore</span><span class="sxs-lookup"><span data-stu-id="36581-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36581-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="36581-142">Minimum supported client</span></span><br/> | <span data-ttu-id="36581-143">Solo app desktop Windows 10 versione 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="36581-143">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="36581-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="36581-144">Minimum supported server</span></span><br/> | <span data-ttu-id="36581-145">\[Solo app desktop Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="36581-145">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="36581-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="36581-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="36581-147"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="36581-147"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="36581-148">Libreria</span><span class="sxs-lookup"><span data-stu-id="36581-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="36581-149"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="36581-149"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="36581-150">DLL</span><span class="sxs-lookup"><span data-stu-id="36581-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36581-151"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36581-151"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="36581-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="36581-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36581-153">API per l'indicizzazione delle risorse del pacchetto e sistemi di compilazione personalizzati</span><span class="sxs-lookup"><span data-stu-id="36581-153">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

