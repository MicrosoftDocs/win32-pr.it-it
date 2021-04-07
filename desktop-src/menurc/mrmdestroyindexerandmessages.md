---
title: Funzione MrmDestroyIndexerAndMessages (MrmResourceIndexer. h)
description: Rilascia le risorse del computer associate a un indicizzatore di risorse.
ms.assetid: AD770F40-BEDB-46C3-9527-DC46169C6193
keywords:
- Menu della funzione MrmDestroyIndexerAndMessages e altre risorse
topic_type:
- apiref
api_name:
- MrmDestroyIndexerAndMessages
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e351c4d9e43bbb094d9738a6fef1b90c657b01e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048737"
---
# <a name="mrmdestroyindexerandmessages-function"></a><span data-ttu-id="2cc3e-104">MrmDestroyIndexerAndMessages (funzione)</span><span class="sxs-lookup"><span data-stu-id="2cc3e-104">MrmDestroyIndexerAndMessages function</span></span>

<span data-ttu-id="2cc3e-105">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="2cc3e-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2cc3e-106">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="2cc3e-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2cc3e-107">Rilascia le risorse del computer associate a un indicizzatore di risorse.</span><span class="sxs-lookup"><span data-stu-id="2cc3e-107">Releases machine resources associated with a resource indexer.</span></span> <span data-ttu-id="2cc3e-108">Elimina l'handle, libera l'indicizzatore ed Elimina tutti i messaggi.</span><span class="sxs-lookup"><span data-stu-id="2cc3e-108">Destroys the handle, frees the indexer, and deletes any messages.</span></span> <span data-ttu-id="2cc3e-109">Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere [API pri (Package Resource Indexing) e sistemi di compilazione personalizzati](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="2cc3e-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="2cc3e-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2cc3e-110">Syntax</span></span>


```C++
HRESULT HRESULT MrmDestroyIndexerAndMessages(
  _In_ MrmResourceIndexerHandle indexer
);
```



## <a name="parameters"></a><span data-ttu-id="2cc3e-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="2cc3e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cc3e-112">*indicizzatore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2cc3e-112">*indexer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cc3e-113">Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span><span class="sxs-lookup"><span data-stu-id="2cc3e-113">Type: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**</span></span>

<span data-ttu-id="2cc3e-114">Handle che identifica l'indicizzatore di risorse da eliminare.</span><span class="sxs-lookup"><span data-stu-id="2cc3e-114">A handle identifying the resource indexer to destroy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cc3e-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2cc3e-115">Return value</span></span>

<span data-ttu-id="2cc3e-116">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="2cc3e-116">Type: **HRESULT**</span></span>

<span data-ttu-id="2cc3e-117">S \_ OK se la funzione ha avuto esito positivo, in caso contrario un altro valore.</span><span class="sxs-lookup"><span data-stu-id="2cc3e-117">S\_OK if the function succeeded, otherwise some other value.</span></span> <span data-ttu-id="2cc3e-118">Utilizzare le macro SUCCEEDed () o FAILED () (definite in Winerror. h) per determinare l'esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="2cc3e-118">Use the SUCCEEDED() or FAILED() macros (defined in winerror.h) to determine success or failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="2cc3e-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2cc3e-119">Requirements</span></span>



| <span data-ttu-id="2cc3e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2cc3e-120">Requirement</span></span> | <span data-ttu-id="2cc3e-121">Valore</span><span class="sxs-lookup"><span data-stu-id="2cc3e-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cc3e-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2cc3e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2cc3e-123">Solo app desktop Windows 10 versione 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="2cc3e-123">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="2cc3e-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2cc3e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2cc3e-125">\[Solo app desktop Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="2cc3e-125">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2cc3e-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2cc3e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2cc3e-127"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="2cc3e-127"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |
| <span data-ttu-id="2cc3e-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="2cc3e-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="2cc3e-129"><dt>Mrmsupport. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2cc3e-129"><dt>Mrmsupport.lib</dt></span></span> </dl>       |
| <span data-ttu-id="2cc3e-130">DLL</span><span class="sxs-lookup"><span data-stu-id="2cc3e-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2cc3e-131"><dt>Mrmsupport.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2cc3e-131"><dt>Mrmsupport.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="2cc3e-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2cc3e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cc3e-133">API per l'indicizzazione delle risorse del pacchetto e sistemi di compilazione personalizzati</span><span class="sxs-lookup"><span data-stu-id="2cc3e-133">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

