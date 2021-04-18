---
title: Funzione MrmCreateConfig (MrmResourceIndexer. h)
description: Crea un nuovo file di configurazione PRI inizializzato che definisce le impostazioni predefinite del qualificatore specificate. Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere API PRI (Package Resource Indexing) e sistemi di compilazione personalizzati.
ms.assetid: F8FB4E9C-1C04-460A-BFA1-FB663653DA3C
keywords:
- Menu della funzione MrmCreateConfig e altre risorse
topic_type:
- apiref
api_name:
- MrmCreateConfig
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3adb270d9bbd9194822181314a697fa1d267a127
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302326"
---
# <a name="mrmcreateconfig-function"></a><span data-ttu-id="e4c80-105">MrmCreateConfig (funzione)</span><span class="sxs-lookup"><span data-stu-id="e4c80-105">MrmCreateConfig function</span></span>

<span data-ttu-id="e4c80-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="e4c80-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e4c80-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="e4c80-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e4c80-108">Crea un nuovo file di configurazione PRI inizializzato che definisce le impostazioni predefinite del qualificatore specificate.</span><span class="sxs-lookup"><span data-stu-id="e4c80-108">Creates a new, initialized PRI config file defining the qualifier defaults that you specify.</span></span> <span data-ttu-id="e4c80-109">Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere [API pri (Package Resource Indexing) e sistemi di compilazione personalizzati](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="e4c80-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="e4c80-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e4c80-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmCreateConfig(
  _In_     MrmPlatformVersion platformVersion,
  _In_opt_ PCWSTR             defaultQualifiers,
  _In_     PCWSTR             outputXmlFile
);
```



## <a name="parameters"></a><span data-ttu-id="e4c80-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="e4c80-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4c80-112">*platformVersion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4c80-112">*platformVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4c80-113">Tipo: **[ **MrmPlatformVersion**](mrmplatformversion.md)**</span><span class="sxs-lookup"><span data-stu-id="e4c80-113">Type: **[**MrmPlatformVersion**](mrmplatformversion.md)**</span></span>

<span data-ttu-id="e4c80-114">Versione della piattaforma (*targetOsVersion*) da utilizzare per il file di configurazione generato.</span><span class="sxs-lookup"><span data-stu-id="e4c80-114">The platform version (*targetOsVersion*) to use for the generated configuration file.</span></span>

</dd> <dt>

<span data-ttu-id="e4c80-115">*defaultQualifiers* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="e4c80-115">*defaultQualifiers* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e4c80-116">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="e4c80-116">Type: **PCWSTR**</span></span>

<span data-ttu-id="e4c80-117">Elenco di qualificatori di risorse predefiniti.</span><span class="sxs-lookup"><span data-stu-id="e4c80-117">A list of default resource qualifiers.</span></span> <span data-ttu-id="e4c80-118">Ad esempio, L "lingua-en-US \_ scale-100 \_ contrasto-standard"</span><span class="sxs-lookup"><span data-stu-id="e4c80-118">For example, L"language-en-US\_scale-100\_contrast-standard"</span></span>

</dd> <dt>

<span data-ttu-id="e4c80-119">*outputXmlFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4c80-119">*outputXmlFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4c80-120">Tipo: **PCWSTR**</span><span class="sxs-lookup"><span data-stu-id="e4c80-120">Type: **PCWSTR**</span></span>

<span data-ttu-id="e4c80-121">Percorso del file di configurazione da creare.</span><span class="sxs-lookup"><span data-stu-id="e4c80-121">The path of the configuration file to create.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4c80-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e4c80-122">Return value</span></span>

<span data-ttu-id="e4c80-123">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e4c80-123">Type: **HRESULT**</span></span>

<span data-ttu-id="e4c80-124">S \_ OK se la funzione ha avuto esito positivo, in caso contrario un altro valore.</span><span class="sxs-lookup"><span data-stu-id="e4c80-124">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="e4c80-125">Utilizzare le macro SUCCEEDed () o FAILED () (definite in Winerror. h) per determinare l'esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="e4c80-125">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4c80-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e4c80-126">Requirements</span></span>



| <span data-ttu-id="e4c80-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4c80-127">Requirement</span></span> | <span data-ttu-id="e4c80-128">Valore</span><span class="sxs-lookup"><span data-stu-id="e4c80-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4c80-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e4c80-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e4c80-130">Solo app desktop Windows 10 versione 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="e4c80-130">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="e4c80-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e4c80-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e4c80-132">\[Solo app desktop Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="e4c80-132">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e4c80-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e4c80-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4c80-134"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4c80-134"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="e4c80-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="e4c80-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="e4c80-136"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e4c80-136"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="e4c80-137">DLL</span><span class="sxs-lookup"><span data-stu-id="e4c80-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4c80-138"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4c80-138"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="e4c80-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e4c80-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4c80-140">API per l'indicizzazione delle risorse del pacchetto e sistemi di compilazione personalizzati</span><span class="sxs-lookup"><span data-stu-id="e4c80-140">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

