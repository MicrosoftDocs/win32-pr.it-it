---
title: Enumerazione MrmResourceIndexerMessageSeverity (MrmResourceIndexer. h)
description: Definisce le costanti che specificano la gravità di un messaggio dell'indicizzatore di risorse. Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere API PRI (Package Resource Indexing) e sistemi di compilazione personalizzati.
ms.assetid: A4734256-94BD-43BE-B93C-55B98DF8A9BF
keywords:
- Menu di enumerazione MrmResourceIndexerMessageSeverity e altre risorse
topic_type:
- apiref
api_name:
- MrmResourceIndexerMessageSeverity
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fdcbb42291ab88e91eca6c16c0a6c95c3e89fd7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301199"
---
# <a name="mrmresourceindexermessageseverity-enumeration"></a><span data-ttu-id="99b1d-105">Enumerazione MrmResourceIndexerMessageSeverity</span><span class="sxs-lookup"><span data-stu-id="99b1d-105">MrmResourceIndexerMessageSeverity enumeration</span></span>

<span data-ttu-id="99b1d-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="99b1d-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="99b1d-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="99b1d-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="99b1d-108">Definisce le costanti che specificano la gravità di un messaggio dell'indicizzatore di risorse.</span><span class="sxs-lookup"><span data-stu-id="99b1d-108">Defines constants that specify the severity of an resource indexer message.</span></span> <span data-ttu-id="99b1d-109">Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere [API pri (Package Resource Indexing) e sistemi di compilazione personalizzati](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="99b1d-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="99b1d-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="99b1d-110">Syntax</span></span>


```C++
typedef enum _MrmResourceIndexerMessageSeverity { 
  MrmResourceIndexerMessageSeverityVerbose  = 1,
  MrmResourceIndexerMessageSeverityInfo     = 2,
  MrmResourceIndexerMessageSeverityWarning  = 3,
  MrmResourceIndexerMessageSeverityError    = 4
} MrmResourceIndexerMessageSeverity;
```



## <a name="constants"></a><span data-ttu-id="99b1d-111">Costanti</span><span class="sxs-lookup"><span data-stu-id="99b1d-111">Constants</span></span>

<dl> <dt>

<span data-ttu-id="99b1d-112"><span id="MrmResourceIndexerMessageSeverityVerbose"></span><span id="mrmresourceindexermessageseverityverbose"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYVERBOSE"></span>**MrmResourceIndexerMessageSeverityVerbose**</span><span class="sxs-lookup"><span data-stu-id="99b1d-112"><span id="MrmResourceIndexerMessageSeverityVerbose"></span><span id="mrmresourceindexermessageseverityverbose"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYVERBOSE"></span>**MrmResourceIndexerMessageSeverityVerbose**</span></span>
</dt> <dd>

<span data-ttu-id="99b1d-113">Indica che il messaggio è dettagliato.</span><span class="sxs-lookup"><span data-stu-id="99b1d-113">Indicates that the message is verbose.</span></span>

</dd> <dt>

<span data-ttu-id="99b1d-114"><span id="MrmResourceIndexerMessageSeverityInfo"></span><span id="mrmresourceindexermessageseverityinfo"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYINFO"></span>**MrmResourceIndexerMessageSeverityInfo**</span><span class="sxs-lookup"><span data-stu-id="99b1d-114"><span id="MrmResourceIndexerMessageSeverityInfo"></span><span id="mrmresourceindexermessageseverityinfo"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYINFO"></span>**MrmResourceIndexerMessageSeverityInfo**</span></span>
</dt> <dd>

<span data-ttu-id="99b1d-115">Indica che il messaggio è informativo.</span><span class="sxs-lookup"><span data-stu-id="99b1d-115">Indicates that the message is informational.</span></span>

</dd> <dt>

<span data-ttu-id="99b1d-116"><span id="MrmResourceIndexerMessageSeverityWarning"></span><span id="mrmresourceindexermessageseveritywarning"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYWARNING"></span>**MrmResourceIndexerMessageSeverityWarning**</span><span class="sxs-lookup"><span data-stu-id="99b1d-116"><span id="MrmResourceIndexerMessageSeverityWarning"></span><span id="mrmresourceindexermessageseveritywarning"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYWARNING"></span>**MrmResourceIndexerMessageSeverityWarning**</span></span>
</dt> <dd>

<span data-ttu-id="99b1d-117">Indica che il messaggio è un avviso.</span><span class="sxs-lookup"><span data-stu-id="99b1d-117">Indicates that the message is a warning.</span></span>

</dd> <dt>

<span data-ttu-id="99b1d-118"><span id="MrmResourceIndexerMessageSeverityError"></span><span id="mrmresourceindexermessageseverityerror"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYERROR"></span>**MrmResourceIndexerMessageSeverityError**</span><span class="sxs-lookup"><span data-stu-id="99b1d-118"><span id="MrmResourceIndexerMessageSeverityError"></span><span id="mrmresourceindexermessageseverityerror"></span><span id="MRMRESOURCEINDEXERMESSAGESEVERITYERROR"></span>**MrmResourceIndexerMessageSeverityError**</span></span>
</dt> <dd>

<span data-ttu-id="99b1d-119">Indica che il messaggio è un errore.</span><span class="sxs-lookup"><span data-stu-id="99b1d-119">Indicates that the message is an error.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="99b1d-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="99b1d-120">Requirements</span></span>



| <span data-ttu-id="99b1d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="99b1d-121">Requirement</span></span> | <span data-ttu-id="99b1d-122">Valore</span><span class="sxs-lookup"><span data-stu-id="99b1d-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99b1d-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="99b1d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="99b1d-124">Solo app desktop Windows 10 versione 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="99b1d-124">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="99b1d-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="99b1d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="99b1d-126">\[Solo app desktop Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="99b1d-126">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="99b1d-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="99b1d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="99b1d-128"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="99b1d-128"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99b1d-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="99b1d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99b1d-130">API per l'indicizzazione delle risorse del pacchetto e sistemi di compilazione personalizzati</span><span class="sxs-lookup"><span data-stu-id="99b1d-130">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

