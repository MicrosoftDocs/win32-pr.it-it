---
title: Enumerazione MrmPlatformVersion (MrmResourceIndexer. h)
description: Definisce le costanti che specificano una versione della piattaforma. Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere API PRI (Package Resource Indexing) e sistemi di compilazione personalizzati.
ms.assetid: 7BA30B8F-FB23-4DCA-930D-099C7F8476E9
keywords:
- Menu di enumerazione MrmPlatformVersion e altre risorse
topic_type:
- apiref
api_name:
- MrmPlatformVersion
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8127d3e6e99d974315327cf89ae9e82add7bc628
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964863"
---
# <a name="mrmplatformversion-enumeration"></a><span data-ttu-id="8e98f-105">Enumerazione MrmPlatformVersion</span><span class="sxs-lookup"><span data-stu-id="8e98f-105">MrmPlatformVersion enumeration</span></span>

<span data-ttu-id="8e98f-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="8e98f-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="8e98f-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="8e98f-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="8e98f-108">Definisce le costanti che specificano una versione della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="8e98f-108">Defines constants that specify a platform version.</span></span> <span data-ttu-id="8e98f-109">Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere [API pri (Package Resource Indexing) e sistemi di compilazione personalizzati](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="8e98f-109">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="syntax"></a><span data-ttu-id="8e98f-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8e98f-110">Syntax</span></span>


```C++
typedef enum _MrmPlatformVersion { 
  MrmPlatformVersion_Default          = 0,
  MrmPlatformVersion_Windows10_0_0_0  = 0x010A0000,
  MrmPlatformVersion_Windows10_0_0_5  = 0x010A0005
} MrmPlatformVersion;
```



## <a name="constants"></a><span data-ttu-id="8e98f-111">Costanti</span><span class="sxs-lookup"><span data-stu-id="8e98f-111">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8e98f-112"><span id="MrmPlatformVersion_Default"></span><span id="mrmplatformversion_default"></span><span id="MRMPLATFORMVERSION_DEFAULT"></span>**\_Impostazione predefinita MrmPlatformVersion**</span><span class="sxs-lookup"><span data-stu-id="8e98f-112"><span id="MrmPlatformVersion_Default"></span><span id="mrmplatformversion_default"></span><span id="MRMPLATFORMVERSION_DEFAULT"></span>**MrmPlatformVersion\_Default**</span></span>
</dt> <dd>

<span data-ttu-id="8e98f-113">Specifica che la versione della piattaforma è quella predefinita.</span><span class="sxs-lookup"><span data-stu-id="8e98f-113">Specifies that the platform version is the default.</span></span>

</dd> <dt>

<span data-ttu-id="8e98f-114"><span id="MrmPlatformVersion_Windows10_0_0_0"></span><span id="mrmplatformversion_windows10_0_0_0"></span><span id="MRMPLATFORMVERSION_WINDOWS10_0_0_0"></span>**MrmPlatformVersion \_ Windows10 \_ 0 \_ 0 \_ 0**</span><span class="sxs-lookup"><span data-stu-id="8e98f-114"><span id="MrmPlatformVersion_Windows10_0_0_0"></span><span id="mrmplatformversion_windows10_0_0_0"></span><span id="MRMPLATFORMVERSION_WINDOWS10_0_0_0"></span>**MrmPlatformVersion\_Windows10\_0\_0\_0**</span></span>
</dt> <dd>

<span data-ttu-id="8e98f-115">Specifica una versione della piattaforma di Windows 10.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="8e98f-115">Specifies a platform version of Windows 10.0.0.0.</span></span>

</dd> <dt>

<span data-ttu-id="8e98f-116"><span id="MrmPlatformVersion_Windows10_0_0_5"></span><span id="mrmplatformversion_windows10_0_0_5"></span><span id="MRMPLATFORMVERSION_WINDOWS10_0_0_5"></span>**MrmPlatformVersion \_ Windows10 \_ 0 \_ 0 \_ 5**</span><span class="sxs-lookup"><span data-stu-id="8e98f-116"><span id="MrmPlatformVersion_Windows10_0_0_5"></span><span id="mrmplatformversion_windows10_0_0_5"></span><span id="MRMPLATFORMVERSION_WINDOWS10_0_0_5"></span>**MrmPlatformVersion\_Windows10\_0\_0\_5**</span></span>
</dt> <dd>

<span data-ttu-id="8e98f-117">Specifica una versione della piattaforma di Windows 10.0.0.5.</span><span class="sxs-lookup"><span data-stu-id="8e98f-117">Specifies a platform version of Windows 10.0.0.5.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8e98f-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8e98f-118">Requirements</span></span>



| <span data-ttu-id="8e98f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e98f-119">Requirement</span></span> | <span data-ttu-id="8e98f-120">Valore</span><span class="sxs-lookup"><span data-stu-id="8e98f-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e98f-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8e98f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8e98f-122">Solo app desktop Windows 10 versione 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="8e98f-122">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="8e98f-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8e98f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8e98f-124">\[Solo app desktop Windows Server\]</span><span class="sxs-lookup"><span data-stu-id="8e98f-124">Windows Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8e98f-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8e98f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e98f-126"><dt>MrmResourceIndexer. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e98f-126"><dt>MrmResourceIndexer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e98f-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8e98f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e98f-128">API per l'indicizzazione delle risorse del pacchetto e sistemi di compilazione personalizzati</span><span class="sxs-lookup"><span data-stu-id="8e98f-128">Package resource indexing (PRI) APIs and custom build systems</span></span>](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

