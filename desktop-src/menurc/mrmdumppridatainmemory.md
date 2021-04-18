---
title: Funzione MrmDumpPriDataInMemory (MrmResourceIndexer. h)
description: Consente di eseguire il dump delle informazioni PRI (come BLOB in memoria, creato da una precedente chiamata a MrmCreateResourceFileInMemory) al relativo equivalente XML (come dati in memoria), in modo da renderlo più facilmente leggibile.
ms.assetid: 6E563B43-4E0A-465D-A8EA-7DE61738DE06
keywords:
- Menu della funzione MrmDumpPriDataInMemory e altre risorse
topic_type:
- apiref
api_name:
- MrmDumpPriDataInMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 072309dcf9ebda1ba4a5669034019582b99105f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302322"
---
# <a name="mrmdumppridatainmemory-function"></a><span data-ttu-id="c6230-104">MrmDumpPriDataInMemory (funzione)</span><span class="sxs-lookup"><span data-stu-id="c6230-104">MrmDumpPriDataInMemory function</span></span>

<span data-ttu-id="c6230-105">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="c6230-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c6230-106">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="c6230-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c6230-107">Consente di eseguire il dump delle informazioni PRI (come BLOB in memoria, creato da una precedente chiamata a [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md)) al relativo equivalente XML (come dati in memoria), in modo da renderlo più facilmente leggibile.</span><span class="sxs-lookup"><span data-stu-id="c6230-107">Dumps PRI info (as a blob in memory, created by a previous call to [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md)) to its XML equivalent (as in-memory data), in order to make it more easily readable.</span></span> <span data-ttu-id="c6230-108">La funzione alloca memoria e restituisce un puntatore a tale memoria in *outputXmlData*.</span><span class="sxs-lookup"><span data-stu-id="c6230-108">The function allocates memory and returns a pointer to that memory in *outputXmlData*.</span></span> <span data-ttu-id="c6230-109">Chiamare [**MrmFreeMemory**](mrmfreememory.md) con lo stesso puntatore per liberare la memoria.</span><span class="sxs-lookup"><span data-stu-id="c6230-109">Call [**MrmFreeMemory**](mrmfreememory.md) with the same pointer to free that memory.</span></span> <span data-ttu-id="c6230-110">Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere [API pri (Package Resource Indexing) e sistemi di compilazione personalizzati](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="c6230-110">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="c6230-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c6230-111">Syntax</span></span>


```C++
HRESULT HRESULT MrmDumpPriDataInMemory(
  _In_     BYTE        *inputPriData,
  _In_     ULONG       inputPriSize,
  _In_opt_ BYTE        *schemaPriData,
  _In_     ULONG       schemaPriSize,
  _In_     MrmDumpType dumpType,
  _Out_    BYTE        **outputXmlData,
  _Out_    ULONG       *outputXmlSize
);
```



## <a name="parameters"></a><span data-ttu-id="c6230-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="c6230-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6230-113">*inputPriData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c6230-113">*inputPriData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6230-114">Tipo: \**byte \** _</span><span class="sxs-lookup"><span data-stu-id="c6230-114">Type: \**BYTE\** _</span></span>

<span data-ttu-id="c6230-115">Puntatore ai dati PRI creati da una chiamata precedente a [_ *MrmCreateResourceFileInMemory* \*](mrmcreateresourcefileinmemory.md).</span><span class="sxs-lookup"><span data-stu-id="c6230-115">A pointer to PRI data created by a previous call to [_ *MrmCreateResourceFileInMemory*\*](mrmcreateresourcefileinmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="c6230-116">*inputPriSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c6230-116">*inputPriSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6230-117">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="c6230-117">Type: **ULONG**</span></span>

<span data-ttu-id="c6230-118">Dimensione dei dati a cui punta *inputPriData*.</span><span class="sxs-lookup"><span data-stu-id="c6230-118">The size of the data pointed to by *inputPriData*.</span></span>

</dd> <dt>

<span data-ttu-id="c6230-119">*schemaPriData* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="c6230-119">*schemaPriData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c6230-120">Tipo: \**byte \** _</span><span class="sxs-lookup"><span data-stu-id="c6230-120">Type: \**BYTE\** _</span></span>

<span data-ttu-id="c6230-121">Puntatore facoltativo a info PRI (come BLOB in memoria) che rappresenta i dati dello schema creati da una chiamata precedente a [_ *MrmCreateResourceFileInMemory* \*](mrmcreateresourcefileinmemory.md).</span><span class="sxs-lookup"><span data-stu-id="c6230-121">An optional pointer to PRI info (as a blob in memory) representing schema data created by a previous call to [_ *MrmCreateResourceFileInMemory*\*](mrmcreateresourcefileinmemory.md).</span></span> <span data-ttu-id="c6230-122">Non liberare *schemaPriData* fino al termine dell'uso dell'indicizzatore di risorse.</span><span class="sxs-lookup"><span data-stu-id="c6230-122">Don't free *schemaPriData* until after you've finished using the resource indexer.</span></span> <span data-ttu-id="c6230-123">Vedere anche la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="c6230-123">Also see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="c6230-124">*schemaPriSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c6230-124">*schemaPriSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6230-125">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="c6230-125">Type: **ULONG**</span></span>

<span data-ttu-id="c6230-126">Dimensione dei dati a cui punta *schemaPriData*.</span><span class="sxs-lookup"><span data-stu-id="c6230-126">The size of the data pointed to by *schemaPriData*.</span></span>

</dd> <dt>

<span data-ttu-id="c6230-127">*dumpType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c6230-127">*dumpType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6230-128">Tipo: **[ **MrmDumpType**](mrmdumptype.md)**</span><span class="sxs-lookup"><span data-stu-id="c6230-128">Type: **[**MrmDumpType**](mrmdumptype.md)**</span></span>

<span data-ttu-id="c6230-129">Specifica il modo in cui il dump XML deve essere dettagliato o se deve essere eseguito il dump di uno schema.</span><span class="sxs-lookup"><span data-stu-id="c6230-129">Specifies how detailed the XML dump should be, or whether a schema should be dumped.</span></span>

</dd> <dt>

<span data-ttu-id="c6230-130">*outputXmlData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c6230-130">*outputXmlData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c6230-131">Tipo: **byte \* \***</span><span class="sxs-lookup"><span data-stu-id="c6230-131">Type: **BYTE\*\***</span></span>

<span data-ttu-id="c6230-132">Indirizzo di un puntatore a BYTE.</span><span class="sxs-lookup"><span data-stu-id="c6230-132">The address of a pointer to BYTE.</span></span> <span data-ttu-id="c6230-133">La funzione alloca memoria e restituisce un puntatore a tale memoria in *outputXmlData*.</span><span class="sxs-lookup"><span data-stu-id="c6230-133">The function allocates memory and returns a pointer to that memory in *outputXmlData*.</span></span> <span data-ttu-id="c6230-134">Chiamare [**MrmFreeMemory**](mrmfreememory.md) con il puntatore a byte per liberare la memoria.</span><span class="sxs-lookup"><span data-stu-id="c6230-134">Call [**MrmFreeMemory**](mrmfreememory.md) with your pointer to BYTE to free that memory.</span></span>

</dd> <dt>

<span data-ttu-id="c6230-135">*outputXmlSize* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c6230-135">*outputXmlSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c6230-136">Tipo: \**ULONG \** _</span><span class="sxs-lookup"><span data-stu-id="c6230-136">Type: \**ULONG\** _</span></span>

<span data-ttu-id="c6230-137">Indirizzo di ULONG.</span><span class="sxs-lookup"><span data-stu-id="c6230-137">The address of a ULONG.</span></span> <span data-ttu-id="c6230-138">In _outputXmlSize \*, la funzione restituisce le dimensioni della memoria allocata a cui punta *outputXmlData*.</span><span class="sxs-lookup"><span data-stu-id="c6230-138">In _outputXmlSize\*, the function returns the size of the allocated memory pointed to by *outputXmlData*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6230-139">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c6230-139">Return value</span></span>

<span data-ttu-id="c6230-140">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c6230-140">Type: **HRESULT**</span></span>

<span data-ttu-id="c6230-141">S \_ OK se la funzione ha avuto esito positivo, in caso contrario un altro valore.</span><span class="sxs-lookup"><span data-stu-id="c6230-141">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="c6230-142">Utilizzare le macro SUCCEEDed () o FAILED () (definite in Winerror. h) per determinare l'esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="c6230-142">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6230-143">Commenti</span><span class="sxs-lookup"><span data-stu-id="c6230-143">Remarks</span></span>

<span data-ttu-id="c6230-144">Un pacchetto di risorse senza schema è uno creato con l'argomento [**MrmPackagingOptionsOmitSchemaFromResourcePacks**](mrmpackagingoptions.md) passato a [**MrmCreateResourceFile**](mrmcreateresourcefile.md) o [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) (oppure con l'opzione *omitSchemaFromResourcePacks* nel file di configurazione pri).</span><span class="sxs-lookup"><span data-stu-id="c6230-144">A schema-free resource pack is one that was created with the [**MrmPackagingOptionsOmitSchemaFromResourcePacks**](mrmpackagingoptions.md) argument passed to [**MrmCreateResourceFile**](mrmcreateresourcefile.md) or [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) (or with the *omitSchemaFromResourcePacks* switch in the PRI config file).</span></span> <span data-ttu-id="c6230-145">Per eseguire il dump di un pacchetto di risorse senza schema, passare il percorso ai dati PRI del pacchetto principale come argomento per il parametro *schemaPriData* .</span><span class="sxs-lookup"><span data-stu-id="c6230-145">To dump a schema-free resource pack, pass the path to your main package PRI data as the argument for the *schemaPriData* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6230-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c6230-146">Requirements</span></span>



| <span data-ttu-id="c6230-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6230-147">Requirement</span></span> | <span data-ttu-id="c6230-148">Valore</span><span class="sxs-lookup"><span data-stu-id="c6230-148">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6230-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c6230-149">Minimum supported client</span></span><br/> | <span data-ttu-id="c6230-150">Solo app desktop Windows 10 versione 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="c6230-150">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="c6230-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c6230-151">Minimum supported server</span></span><br/> | <span data-ttu-id="c6230-152">\[Solo app desktop Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="c6230-152">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c6230-153">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c6230-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6230-154"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6230-154"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="c6230-155">Libreria</span><span class="sxs-lookup"><span data-stu-id="c6230-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="c6230-156"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c6230-156"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="c6230-157">DLL</span><span class="sxs-lookup"><span data-stu-id="c6230-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6230-158"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6230-158"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="c6230-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c6230-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6230-160">API per l'indicizzazione delle risorse del pacchetto e sistemi di compilazione personalizzati</span><span class="sxs-lookup"><span data-stu-id="c6230-160">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

