---
title: pointer_default (attributo)
description: L'attributo \ Pointer \_ default \ specifica l'attributo puntatore predefinito per tutti i puntatori eccetto i puntatori di primo livello visualizzati negli elenchi di parametri.
ms.assetid: a6e83034-8adb-483d-8d1e-432a1aed22c6
keywords:
- attributo pointer_default MIDL
topic_type:
- apiref
api_name:
- pointer_default
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08555358eb0abd42957d60527e18a4fd4f49165a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046598"
---
# <a name="pointer_default-attribute"></a><span data-ttu-id="c2da3-104">\_attributo predefinito puntatore</span><span class="sxs-lookup"><span data-stu-id="c2da3-104">pointer\_default attribute</span></span>

<span data-ttu-id="c2da3-105">L'attributo **\[ \_ default \] del puntatore** specifica l'attributo del puntatore predefinito per tutti i puntatori ad eccezione dei puntatori di primo livello visualizzati negli elenchi di parametri.</span><span class="sxs-lookup"><span data-stu-id="c2da3-105">The **\[pointer\_default\]** attribute specifies the default pointer attribute for all pointers except top-level pointers that appear in parameter lists.</span></span>

``` syntax
pointer_default ( ptr | ref | unique )
```

## <a name="parameters"></a><span data-ttu-id="c2da3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c2da3-106">Parameters</span></span>

<span data-ttu-id="c2da3-107">Questo attributo non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="c2da3-107">This attribute has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="c2da3-108">Esempi</span><span class="sxs-lookup"><span data-stu-id="c2da3-108">Examples</span></span>

``` syntax
[
    uuid(6B29FC40-CA47-1067-B31D-00DD010662DA), 
    version(3.3), 
    pointer_default(unique)
] 
interface dictionary 
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="c2da3-109">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="c2da3-109">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2da3-110">**interfaccia**</span><span class="sxs-lookup"><span data-stu-id="c2da3-110">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="c2da3-111">Attributi array e Sized-Pointer</span><span class="sxs-lookup"><span data-stu-id="c2da3-111">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="c2da3-112">**matrici**</span><span class="sxs-lookup"><span data-stu-id="c2da3-112">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="c2da3-113">Matrici e puntatori</span><span class="sxs-lookup"><span data-stu-id="c2da3-113">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="c2da3-114">**ptr**</span><span class="sxs-lookup"><span data-stu-id="c2da3-114">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="c2da3-115">**ref**</span><span class="sxs-lookup"><span data-stu-id="c2da3-115">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="c2da3-116">**unico**</span><span class="sxs-lookup"><span data-stu-id="c2da3-116">**unique**</span></span>](unique.md)
</dt> <dt>

[<span data-ttu-id="c2da3-117">Tipi di puntatore predefiniti</span><span class="sxs-lookup"><span data-stu-id="c2da3-117">Default Pointer Types</span></span>](/windows/desktop/Rpc/default-pointer-types)
</dt> </dl>

 

 