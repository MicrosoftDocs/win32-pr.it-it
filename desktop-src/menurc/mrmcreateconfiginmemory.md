---
title: Funzione MrmCreateConfigInMemory (MrmResourceIndexer. h)
description: Crea le informazioni di configurazione PRI nuove inizializzate (come i dati in memoria, non come file) definendo le impostazioni predefinite del qualificatore specificate.
ms.assetid: D8822D6E-5F68-46A1-B99F-52575DB1D277
keywords:
- Menu della funzione MrmCreateConfigInMemory e altre risorse
topic_type:
- apiref
api_name:
- MrmCreateConfigInMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d809ac640061ecf8bd51b9e2016aefe537b1ee8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518694"
---
# <a name="mrmcreateconfiginmemory-function"></a><span data-ttu-id="eb659-104">MrmCreateConfigInMemory (funzione)</span><span class="sxs-lookup"><span data-stu-id="eb659-104">MrmCreateConfigInMemory function</span></span>

<span data-ttu-id="eb659-105">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="eb659-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="eb659-106">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="eb659-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="eb659-107">Crea le informazioni di configurazione PRI nuove inizializzate (come i dati in memoria, non come file) definendo le impostazioni predefinite del qualificatore specificate.</span><span class="sxs-lookup"><span data-stu-id="eb659-107">Creates new, initialized PRI configuration info (as in-memory data, not as a file) defining the qualifier defaults that you specify.</span></span> <span data-ttu-id="eb659-108">La funzione alloca memoria e restituisce un puntatore a tale memoria in *outputXmlData*.</span><span class="sxs-lookup"><span data-stu-id="eb659-108">The function allocates memory and returns a pointer to that memory in *outputXmlData*.</span></span> <span data-ttu-id="eb659-109">Chiamare [**MrmFreeMemory**](mrmfreememory.md) con lo stesso puntatore per liberare la memoria.</span><span class="sxs-lookup"><span data-stu-id="eb659-109">Call [**MrmFreeMemory**](mrmfreememory.md) with the same pointer to free that memory.</span></span> <span data-ttu-id="eb659-110">Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere [API pri (Package Resource Indexing) e sistemi di compilazione personalizzati](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="eb659-110">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="eb659-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eb659-111">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateConfigInMemory(
  _In_     MrmPlatformVersion platformVersion,
  _In_opt_ PCWSTR             defaultQualifiers,
  _Out_    BYTE               **outputXmlData,
  _Out_    ULONG              *outputXmlSize
);
```



## <a name="parameters"></a><span data-ttu-id="eb659-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="eb659-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb659-113">*platformVersion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eb659-113">*platformVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb659-114">Tipo: **[ **MrmPlatformVersion**](mrmplatformversion.md)**</span><span class="sxs-lookup"><span data-stu-id="eb659-114">Type: **[**MrmPlatformVersion**](mrmplatformversion.md)**</span></span>

<span data-ttu-id="eb659-115">Versione della piattaforma (*targetOsVersion*) da usare per le informazioni di configurazione generate.</span><span class="sxs-lookup"><span data-stu-id="eb659-115">The platform version (*targetOsVersion*) to use for the generated configuration info.</span></span>

</dd> <dt>

<span data-ttu-id="eb659-116">*defaultQualifiers* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="eb659-116">*defaultQualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eb659-117">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="eb659-117">Type: **PCWSTR**</span></span>

<span data-ttu-id="eb659-118">Elenco di qualificatori di risorse predefiniti.</span><span class="sxs-lookup"><span data-stu-id="eb659-118">A list of default resource qualifiers.</span></span> <span data-ttu-id="eb659-119">Ad esempio, L "lingua-en-US \_ scale-100 \_ contrasto-standard"</span><span class="sxs-lookup"><span data-stu-id="eb659-119">For example, L"language-en-US\_scale-100\_contrast-standard"</span></span>

</dd> <dt>

<span data-ttu-id="eb659-120">*outputXmlData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="eb659-120">*outputXmlData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eb659-121">Tipo: **byte \* \***</span><span class="sxs-lookup"><span data-stu-id="eb659-121">Type: **BYTE\*\***</span></span>

<span data-ttu-id="eb659-122">Indirizzo di un puntatore a BYTE.</span><span class="sxs-lookup"><span data-stu-id="eb659-122">The address of a pointer to BYTE.</span></span> <span data-ttu-id="eb659-123">La funzione alloca memoria e restituisce un puntatore a tale memoria in *outputXmlData*.</span><span class="sxs-lookup"><span data-stu-id="eb659-123">The function allocates memory and returns a pointer to that memory in *outputXmlData*.</span></span> <span data-ttu-id="eb659-124">Chiamare [**MrmFreeMemory**](mrmfreememory.md) con il puntatore a byte per liberare la memoria.</span><span class="sxs-lookup"><span data-stu-id="eb659-124">Call [**MrmFreeMemory**](mrmfreememory.md) with your pointer to BYTE to free that memory.</span></span>

</dd> <dt>

<span data-ttu-id="eb659-125">*outputXmlSize* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="eb659-125">*outputXmlSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eb659-126">Tipo: \**ULONG \** _</span><span class="sxs-lookup"><span data-stu-id="eb659-126">Type: \**ULONG\** _</span></span>

<span data-ttu-id="eb659-127">Indirizzo di ULONG.</span><span class="sxs-lookup"><span data-stu-id="eb659-127">The address of a ULONG.</span></span> <span data-ttu-id="eb659-128">In _outputXmlSize \*, la funzione restituisce le dimensioni della memoria allocata a cui punta *outputXmlData*.</span><span class="sxs-lookup"><span data-stu-id="eb659-128">In _outputXmlSize\*, the function returns the size of the allocated memory pointed to by *outputXmlData*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb659-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eb659-129">Return value</span></span>

<span data-ttu-id="eb659-130">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="eb659-130">Type: **HRESULT**</span></span>

<span data-ttu-id="eb659-131">S \_ OK se la funzione ha avuto esito positivo, in caso contrario un altro valore.</span><span class="sxs-lookup"><span data-stu-id="eb659-131">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="eb659-132">Utilizzare le macro SUCCEEDed () o FAILED () (definite in Winerror. h) per determinare l'esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="eb659-132">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb659-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eb659-133">Requirements</span></span>



| <span data-ttu-id="eb659-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb659-134">Requirement</span></span> | <span data-ttu-id="eb659-135">Valore</span><span class="sxs-lookup"><span data-stu-id="eb659-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb659-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eb659-136">Minimum supported client</span></span><br/> | <span data-ttu-id="eb659-137">Solo app desktop Windows 10 versione 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="eb659-137">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="eb659-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eb659-138">Minimum supported server</span></span><br/> | <span data-ttu-id="eb659-139">\[Solo app desktop Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="eb659-139">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="eb659-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eb659-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb659-141"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb659-141"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="eb659-142">Libreria</span><span class="sxs-lookup"><span data-stu-id="eb659-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="eb659-143"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eb659-143"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="eb659-144">DLL</span><span class="sxs-lookup"><span data-stu-id="eb659-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb659-145"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb659-145"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="eb659-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eb659-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb659-147">API per l'indicizzazione delle risorse del pacchetto e sistemi di compilazione personalizzati</span><span class="sxs-lookup"><span data-stu-id="eb659-147">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

