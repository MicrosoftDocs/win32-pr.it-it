---
title: Funzione MrmFreeMemory (MrmResourceIndexer. h)
description: Libera la memoria allocata da MrmCreateConfigInMemory, MrmCreateResourceFileInMemory, MrmDumpPriFileInMemory e MrmDumpPriDataInMemory.
ms.assetid: F8741379-CE1A-47BD-9B2C-721A5424CAD1
keywords:
- Menu della funzione MrmFreeMemory e altre risorse
topic_type:
- apiref
api_name:
- MrmFreeMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6c255cb4d1c73e40b5636914d2bc70ae4e1efe3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302321"
---
# <a name="mrmfreememory-function"></a><span data-ttu-id="149d9-104">MrmFreeMemory (funzione)</span><span class="sxs-lookup"><span data-stu-id="149d9-104">MrmFreeMemory function</span></span>

<span data-ttu-id="149d9-105">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="149d9-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="149d9-106">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="149d9-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="149d9-107">Libera la memoria allocata da [**MrmCreateConfigInMemory**](mrmcreateconfiginmemory.md), [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md), [**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md)e [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md).</span><span class="sxs-lookup"><span data-stu-id="149d9-107">Frees memory allocated by [**MrmCreateConfigInMemory**](mrmcreateconfiginmemory.md), [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md), [**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md), and [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md).</span></span> <span data-ttu-id="149d9-108">Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere [API pri (Package Resource Indexing) e sistemi di compilazione personalizzati](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="149d9-108">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="149d9-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="149d9-109">Syntax</span></span>


```C++
HRESULT HRESULT MrmFreeMemory(
  _In_ BYTE *data
);
```



## <a name="parameters"></a><span data-ttu-id="149d9-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="149d9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="149d9-111">*dati* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="149d9-111">*data* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="149d9-112">Tipo: \**byte \** _</span><span class="sxs-lookup"><span data-stu-id="149d9-112">Type: \**BYTE\** _</span></span>

<span data-ttu-id="149d9-113">Puntatore alla memoria allocata e restituita [da *_ MrmCreateConfigInMemory* \*](mrmcreateconfiginmemory.md), [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md), [**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md)o [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md).</span><span class="sxs-lookup"><span data-stu-id="149d9-113">A pointer to memory allocated and returned by [_ *MrmCreateConfigInMemory*\*](mrmcreateconfiginmemory.md), [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md), [**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md), or [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="149d9-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="149d9-114">Return value</span></span>

<span data-ttu-id="149d9-115">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="149d9-115">Type: **HRESULT**</span></span>

<span data-ttu-id="149d9-116">S \_ OK se la funzione ha avuto esito positivo, in caso contrario un altro valore.</span><span class="sxs-lookup"><span data-stu-id="149d9-116">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="149d9-117">Utilizzare le macro SUCCEEDed () o FAILED () (definite in Winerror. h) per determinare l'esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="149d9-117">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="149d9-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="149d9-118">Requirements</span></span>



| <span data-ttu-id="149d9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="149d9-119">Requirement</span></span> | <span data-ttu-id="149d9-120">Valore</span><span class="sxs-lookup"><span data-stu-id="149d9-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="149d9-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="149d9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="149d9-122">Solo app desktop Windows 10 versione 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="149d9-122">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="149d9-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="149d9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="149d9-124">\[Solo app desktop Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="149d9-124">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="149d9-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="149d9-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="149d9-126"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="149d9-126"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="149d9-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="149d9-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="149d9-128"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="149d9-128"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="149d9-129">DLL</span><span class="sxs-lookup"><span data-stu-id="149d9-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="149d9-130"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="149d9-130"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="149d9-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="149d9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="149d9-132">API per l'indicizzazione delle risorse del pacchetto e sistemi di compilazione personalizzati</span><span class="sxs-lookup"><span data-stu-id="149d9-132">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

