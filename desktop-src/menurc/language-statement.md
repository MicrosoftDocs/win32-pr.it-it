---
title: LANGUAGE (istruzione)
description: Definisce la lingua per tutte le risorse fino alla successiva istruzione del linguaggio o alla fine del file.
ms.assetid: 175e27e2-903a-4aaf-89ef-532166b167e8
keywords:
- Menu di istruzioni della lingua e altre risorse
topic_type:
- apiref
api_name:
- LANGUAGE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9563ba2ec00362a3b9caa3911a701919a81cae1e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104516780"
---
# <a name="language-statement"></a><span data-ttu-id="6322f-104">LANGUAGE (istruzione)</span><span class="sxs-lookup"><span data-stu-id="6322f-104">LANGUAGE statement</span></span>

<span data-ttu-id="6322f-105">Definisce la lingua per tutte le risorse fino alla successiva istruzione del **linguaggio** o alla fine del file.</span><span class="sxs-lookup"><span data-stu-id="6322f-105">Defines the language for all resources up to the next **LANGUAGE** statement or to the end of the file.</span></span>

<span data-ttu-id="6322f-106">Quando l'istruzione **Language** viene visualizzata prima dell'inizio del corpo di un [**acceleratore**](accelerators-resource.md), [**DIALOGEX**](dialogex-resource.md), [**menu**](menu-resource.md), [**RCDATA**](rcdata-resource.md)o [**un'STRINGTABLE**](stringtable-resource.md) , la lingua specificata si applica solo a tale risorsa.</span><span class="sxs-lookup"><span data-stu-id="6322f-106">When the **LANGUAGE** statement appears before the beginning of the body of an [**ACCELERATORS**](accelerators-resource.md), [**DIALOGEX**](dialogex-resource.md), [**MENU**](menu-resource.md), [**RCDATA**](rcdata-resource.md), or [**STRINGTABLE**](stringtable-resource.md) resource definition, the specified language applies only to that resource.</span></span>

``` syntax
LANGUAGE language, sublanguage
```

<dl> <dt>

<span data-ttu-id="6322f-107"><span id="language"></span><span id="LANGUAGE"></span>*linguaggio*</span><span class="sxs-lookup"><span data-stu-id="6322f-107"><span id="language"></span><span id="LANGUAGE"></span>*language*</span></span>
</dt> <dd>

<span data-ttu-id="6322f-108">Identificatore della lingua.</span><span class="sxs-lookup"><span data-stu-id="6322f-108">Language identifier.</span></span>

</dd> <dt>

<span data-ttu-id="6322f-109"><span id="sublanguage"></span><span id="SUBLANGUAGE"></span>*sottolingua*</span><span class="sxs-lookup"><span data-stu-id="6322f-109"><span id="sublanguage"></span><span id="SUBLANGUAGE"></span>*sublanguage*</span></span>
</dt> <dd>

<span data-ttu-id="6322f-110">Identificatore del linguaggio di sottolinguaggio.</span><span class="sxs-lookup"><span data-stu-id="6322f-110">Sublanguage identifier.</span></span>

</dd> </dl>

<span data-ttu-id="6322f-111">Per altre informazioni, vedere [costanti e stringhe degli identificatori di lingua](/windows/desktop/Intl/language-identifier-constants-and-strings).</span><span class="sxs-lookup"><span data-stu-id="6322f-111">For more information, see [Language Identifier Constants and Strings](/windows/desktop/Intl/language-identifier-constants-and-strings).</span></span>

## <a name="see-also"></a><span data-ttu-id="6322f-112">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6322f-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6322f-113">**ACCELERATORI**</span><span class="sxs-lookup"><span data-stu-id="6322f-113">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="6322f-114">**CARATTERISTICHE**</span><span class="sxs-lookup"><span data-stu-id="6322f-114">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="6322f-115">**MENU**</span><span class="sxs-lookup"><span data-stu-id="6322f-115">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="6322f-116">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="6322f-116">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="6322f-117">**UN'STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="6322f-117">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> <dt>

[<span data-ttu-id="6322f-118">**Versione**</span><span class="sxs-lookup"><span data-stu-id="6322f-118">**VERSION**</span></span>](version-statement.md)
</dt> </dl>

 

 