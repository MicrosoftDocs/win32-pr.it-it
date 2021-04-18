---
title: Enumerazione MrmPackagingOptions (MrmResourceIndexer. h)
description: Definisce le costanti che specificano le opzioni per il file PRI creato da MrmCreateResourceFile e MrmCreateResourceFileInMemory.
ms.assetid: 11FADCB2-CE6F-449E-8A85-DA50B52B26D0
keywords:
- Menu di enumerazione MrmPackagingOptions e altre risorse
topic_type:
- apiref
api_name:
- MrmPackagingOptions
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9a8b2bee733fe17e91501fe295e5f80be159ec5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301022"
---
# <a name="mrmpackagingoptions-enumeration"></a><span data-ttu-id="491a9-104">Enumerazione MrmPackagingOptions</span><span class="sxs-lookup"><span data-stu-id="491a9-104">MrmPackagingOptions enumeration</span></span>

<span data-ttu-id="491a9-105">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="491a9-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="491a9-106">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="491a9-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="491a9-107">Definisce le costanti che specificano le opzioni per il file PRI creato da [**MrmCreateResourceFile**](mrmcreateresourcefile.md) e [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md).</span><span class="sxs-lookup"><span data-stu-id="491a9-107">Defines constants that specify options for the PRI file created by [**MrmCreateResourceFile**](mrmcreateresourcefile.md) and [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md).</span></span> <span data-ttu-id="491a9-108">Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere [API pri (Package Resource Indexing) e sistemi di compilazione personalizzati](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="491a9-108">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="491a9-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="491a9-109">Syntax</span></span>


```C++
typedef enum _MrmPackagingOptions { 
  MrmPackagingOptionsNone                         = 0x00,
  MrmPackagingOptionsOmitSchemaFromResourcePacks  = 0x01,
  MrmPackagingOptionsSplitLanguageVariants        = 0x02
} MrmPackagingOptions;
```



## <a name="constants"></a><span data-ttu-id="491a9-110">Costanti</span><span class="sxs-lookup"><span data-stu-id="491a9-110">Constants</span></span>

<dl> <dt>

<span data-ttu-id="491a9-111"><span id="MrmPackagingOptionsNone"></span><span id="mrmpackagingoptionsnone"></span><span id="MRMPACKAGINGOPTIONSNONE"></span>**MrmPackagingOptionsNone**</span><span class="sxs-lookup"><span data-stu-id="491a9-111"><span id="MrmPackagingOptionsNone"></span><span id="mrmpackagingoptionsnone"></span><span id="MRMPACKAGINGOPTIONSNONE"></span>**MrmPackagingOptionsNone**</span></span>
</dt> <dd>

<span data-ttu-id="491a9-112">Non specifica alcuna opzione per la creazione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="491a9-112">Specifies no packaging options.</span></span>

</dd> <dt>

<span data-ttu-id="491a9-113"><span id="MrmPackagingOptionsOmitSchemaFromResourcePacks"></span><span id="mrmpackagingoptionsomitschemafromresourcepacks"></span><span id="MRMPACKAGINGOPTIONSOMITSCHEMAFROMRESOURCEPACKS"></span>**MrmPackagingOptionsOmitSchemaFromResourcePacks**</span><span class="sxs-lookup"><span data-stu-id="491a9-113"><span id="MrmPackagingOptionsOmitSchemaFromResourcePacks"></span><span id="mrmpackagingoptionsomitschemafromresourcepacks"></span><span id="MRMPACKAGINGOPTIONSOMITSCHEMAFROMRESOURCEPACKS"></span>**MrmPackagingOptionsOmitSchemaFromResourcePacks**</span></span>
</dt> <dd>

<span data-ttu-id="491a9-114">Specifica che deve essere creato un pacchetto di risorse senza schema.</span><span class="sxs-lookup"><span data-stu-id="491a9-114">Specifies that a schema-free resource pack should be created.</span></span>

</dd> <dt>

<span data-ttu-id="491a9-115"><span id="MrmPackagingOptionsSplitLanguageVariants"></span><span id="mrmpackagingoptionssplitlanguagevariants"></span><span id="MRMPACKAGINGOPTIONSSPLITLANGUAGEVARIANTS"></span>**MrmPackagingOptionsSplitLanguageVariants**</span><span class="sxs-lookup"><span data-stu-id="491a9-115"><span id="MrmPackagingOptionsSplitLanguageVariants"></span><span id="mrmpackagingoptionssplitlanguagevariants"></span><span id="MRMPACKAGINGOPTIONSSPLITLANGUAGEVARIANTS"></span>**MrmPackagingOptionsSplitLanguageVariants**</span></span>
</dt> <dd>

<span data-ttu-id="491a9-116">Specifica che il file PRI deve essere suddiviso automaticamente da tutti i qualificatori supportati (in particolare, lingua e scala).</span><span class="sxs-lookup"><span data-stu-id="491a9-116">Specifies that the PRI file should be automatically split by all supported qualifiers (specifically, language and scale).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="491a9-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="491a9-117">Requirements</span></span>



| <span data-ttu-id="491a9-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="491a9-118">Requirement</span></span> | <span data-ttu-id="491a9-119">Valore</span><span class="sxs-lookup"><span data-stu-id="491a9-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="491a9-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="491a9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="491a9-121">Solo app desktop Windows 10 versione 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="491a9-121">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="491a9-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="491a9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="491a9-123">\[Solo app desktop Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="491a9-123">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="491a9-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="491a9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="491a9-125"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="491a9-125"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="491a9-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="491a9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="491a9-127">API per l'indicizzazione delle risorse del pacchetto e sistemi di compilazione personalizzati</span><span class="sxs-lookup"><span data-stu-id="491a9-127">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

