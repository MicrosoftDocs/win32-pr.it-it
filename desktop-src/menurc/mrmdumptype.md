---
title: Enumerazione MrmDumpType (MrmResourceIndexer. h)
description: Definisce le costanti che specificano il tipo di dump del file PRI da produrre. Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere API PRI (Package Resource Indexing) e sistemi di compilazione personalizzati.
ms.assetid: 71E49F35-4B79-478A-A26A-C0D9A9FC2D11
keywords:
- Menu di enumerazione MrmDumpType e altre risorse
topic_type:
- apiref
api_name:
- MrmDumpType
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ff693f933af299d042b97de319fb221ac133a5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477152"
---
# <a name="mrmdumptype-enumeration"></a><span data-ttu-id="654cb-105">Enumerazione MrmDumpType</span><span class="sxs-lookup"><span data-stu-id="654cb-105">MrmDumpType enumeration</span></span>

<span data-ttu-id="654cb-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="654cb-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="654cb-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="654cb-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="654cb-108">Definisce le costanti che specificano il tipo di dump del file PRI da produrre.</span><span class="sxs-lookup"><span data-stu-id="654cb-108">Defines constants that specify the type of PRI file dump to produce.</span></span> <span data-ttu-id="654cb-109">Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere [API pri (Package Resource Indexing) e sistemi di compilazione personalizzati](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="654cb-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="654cb-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="654cb-110">Syntax</span></span>


```C++
typedef enum _MrmDumpType { 
  MrmDumpType_Basic     = 0,
  MrmDumpType_Detailed  = 1,
  MrmDumpType_Schema    = 2
} MrmDumpType;
```



## <a name="constants"></a><span data-ttu-id="654cb-111">Costanti</span><span class="sxs-lookup"><span data-stu-id="654cb-111">Constants</span></span>

<dl> <dt>

<span data-ttu-id="654cb-112"><span id="MrmDumpType_Basic"></span><span id="mrmdumptype_basic"></span><span id="MRMDUMPTYPE_BASIC"></span>**MrmDumpType \_ Basic**</span><span class="sxs-lookup"><span data-stu-id="654cb-112"><span id="MrmDumpType_Basic"></span><span id="mrmdumptype_basic"></span><span id="MRMDUMPTYPE_BASIC"></span>**MrmDumpType\_Basic**</span></span>
</dt> <dd>

<span data-ttu-id="654cb-113">Specifica che il dump deve essere di base.</span><span class="sxs-lookup"><span data-stu-id="654cb-113">Specifies that the dump should be basic.</span></span>

</dd> <dt>

<span data-ttu-id="654cb-114"><span id="MrmDumpType_Detailed"></span><span id="mrmdumptype_detailed"></span><span id="MRMDUMPTYPE_DETAILED"></span>**MrmDumpType \_ dettagliata**</span><span class="sxs-lookup"><span data-stu-id="654cb-114"><span id="MrmDumpType_Detailed"></span><span id="mrmdumptype_detailed"></span><span id="MRMDUMPTYPE_DETAILED"></span>**MrmDumpType\_Detailed**</span></span>
</dt> <dd>

<span data-ttu-id="654cb-115">Specifica che il dump deve essere dettagliato.</span><span class="sxs-lookup"><span data-stu-id="654cb-115">Specifies that the dump should be detailed.</span></span>

</dd> <dt>

<span data-ttu-id="654cb-116"><span id="MrmDumpType_Schema"></span><span id="mrmdumptype_schema"></span><span id="MRMDUMPTYPE_SCHEMA"></span>**\_Schema MrmDumpType**</span><span class="sxs-lookup"><span data-stu-id="654cb-116"><span id="MrmDumpType_Schema"></span><span id="mrmdumptype_schema"></span><span id="MRMDUMPTYPE_SCHEMA"></span>**MrmDumpType\_Schema**</span></span>
</dt> <dd>

<span data-ttu-id="654cb-117">Specifica che il dump deve essere uno schema.</span><span class="sxs-lookup"><span data-stu-id="654cb-117">Specifies that the dump should be a schema.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="654cb-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="654cb-118">Requirements</span></span>



| <span data-ttu-id="654cb-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="654cb-119">Requirement</span></span> | <span data-ttu-id="654cb-120">Valore</span><span class="sxs-lookup"><span data-stu-id="654cb-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="654cb-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="654cb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="654cb-122">Solo app desktop Windows 10 versione 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="654cb-122">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="654cb-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="654cb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="654cb-124">\[Solo app desktop Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="654cb-124">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="654cb-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="654cb-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="654cb-126"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="654cb-126"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="654cb-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="654cb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="654cb-128">API per l'indicizzazione delle risorse del pacchetto e sistemi di compilazione personalizzati</span><span class="sxs-lookup"><span data-stu-id="654cb-128">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

