---
title: Enumerazione MrmPackagingMode (MrmResourceIndexer. h)
description: Definisce le costanti che specificano il tipo di file PRI che devono essere creati da MrmCreateResourceFile e MrmCreateResourceFileInMemory.
ms.assetid: 5695B67E-5446-4538-83D2-F8FF91A5080E
keywords:
- Menu di enumerazione MrmPackagingMode e altre risorse
topic_type:
- apiref
api_name:
- MrmPackagingMode
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eaca681dbcf9d171e279083abbb730895ff99333
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340742"
---
# <a name="mrmpackagingmode-enumeration"></a><span data-ttu-id="9f226-104">Enumerazione MrmPackagingMode</span><span class="sxs-lookup"><span data-stu-id="9f226-104">MrmPackagingMode enumeration</span></span>

<span data-ttu-id="9f226-105">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="9f226-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="9f226-106">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="9f226-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="9f226-107">Definisce le costanti che specificano il tipo di file PRI che devono essere creati da [**MrmCreateResourceFile**](mrmcreateresourcefile.md) e [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md).</span><span class="sxs-lookup"><span data-stu-id="9f226-107">Defines constants that specify what kind of PRI file(s) should be created by [**MrmCreateResourceFile**](mrmcreateresourcefile.md) and [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md).</span></span> <span data-ttu-id="9f226-108">Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere [API pri (Package Resource Indexing) e sistemi di compilazione personalizzati](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="9f226-108">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="9f226-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9f226-109">Syntax</span></span>


```C++
typedef enum _MrmPackagingMode { 
  MrmPackagingModeStandaloneFile  = 0,
  MrmPackagingModeAutoSplit       = 1,
  MrmPackagingModeResourcePack    = 2
} MrmPackagingMode;
```



## <a name="constants"></a><span data-ttu-id="9f226-110">Costanti</span><span class="sxs-lookup"><span data-stu-id="9f226-110">Constants</span></span>

<dl> <dt>

<span data-ttu-id="9f226-111"><span id="MrmPackagingModeStandaloneFile"></span><span id="mrmpackagingmodestandalonefile"></span><span id="MRMPACKAGINGMODESTANDALONEFILE"></span>**MrmPackagingModeStandaloneFile**</span><span class="sxs-lookup"><span data-stu-id="9f226-111"><span id="MrmPackagingModeStandaloneFile"></span><span id="mrmpackagingmodestandalonefile"></span><span id="MRMPACKAGINGMODESTANDALONEFILE"></span>**MrmPackagingModeStandaloneFile**</span></span>
</dt> <dd>

<span data-ttu-id="9f226-112">Specifica che deve essere creato un singolo file PRI.</span><span class="sxs-lookup"><span data-stu-id="9f226-112">Specifies that a single PRI file should be created.</span></span>

</dd> <dt>

<span data-ttu-id="9f226-113"><span id="MrmPackagingModeAutoSplit"></span><span id="mrmpackagingmodeautosplit"></span><span id="MRMPACKAGINGMODEAUTOSPLIT"></span>**MrmPackagingModeAutoSplit**</span><span class="sxs-lookup"><span data-stu-id="9f226-113"><span id="MrmPackagingModeAutoSplit"></span><span id="mrmpackagingmodeautosplit"></span><span id="MRMPACKAGINGMODEAUTOSPLIT"></span>**MrmPackagingModeAutoSplit**</span></span>
</dt> <dd>

<span data-ttu-id="9f226-114">Specifica che devono essere creati più file PRI. Dividi automaticamente da tutti i qualificatori supportati (in particolare, lingua e scala).</span><span class="sxs-lookup"><span data-stu-id="9f226-114">Specifies that multiple PRI files should be created; split automatically by all supported qualifiers (specifically, language and scale).</span></span>

</dd> <dt>

<span data-ttu-id="9f226-115"><span id="MrmPackagingModeResourcePack"></span><span id="mrmpackagingmoderesourcepack"></span><span id="MRMPACKAGINGMODERESOURCEPACK"></span>**MrmPackagingModeResourcePack**</span><span class="sxs-lookup"><span data-stu-id="9f226-115"><span id="MrmPackagingModeResourcePack"></span><span id="mrmpackagingmoderesourcepack"></span><span id="MRMPACKAGINGMODERESOURCEPACK"></span>**MrmPackagingModeResourcePack**</span></span>
</dt> <dd>

<span data-ttu-id="9f226-116">Specifica che deve essere creato un file PRI satellite del componente aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="9f226-116">Specifies that an add-on satellite PRI file should be created.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9f226-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9f226-117">Requirements</span></span>



| <span data-ttu-id="9f226-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f226-118">Requirement</span></span> | <span data-ttu-id="9f226-119">Valore</span><span class="sxs-lookup"><span data-stu-id="9f226-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f226-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f226-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9f226-121">Solo app desktop Windows 10 versione 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="9f226-121">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="9f226-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f226-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9f226-123">\[Solo app desktop Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="9f226-123">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9f226-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9f226-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f226-125"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f226-125"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f226-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9f226-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f226-127">API per l'indicizzazione delle risorse del pacchetto e sistemi di compilazione personalizzati</span><span class="sxs-lookup"><span data-stu-id="9f226-127">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

