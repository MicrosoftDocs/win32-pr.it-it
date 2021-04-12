---
title: aggregatable (attributo)
description: L'attributo \ aggregable \ indica che la classe supporta l'aggregazione.
ms.assetid: 3b680692-fbf7-4aeb-b11a-c3a87ddaea67
keywords:
- MIDL attributo aggregabile
topic_type:
- apiref
api_name:
- aggregatable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5091815cf38060c30b82aa33fd05ad6be9d6c390
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337086"
---
# <a name="aggregatable-attribute"></a><span data-ttu-id="c760f-104">aggregatable (attributo)</span><span class="sxs-lookup"><span data-stu-id="c760f-104">aggregatable attribute</span></span>

<span data-ttu-id="c760f-105">L'attributo **\[ aggregable \]** indica che la classe supporta l'aggregazione.</span><span class="sxs-lookup"><span data-stu-id="c760f-105">The **\[aggregatable\]** attribute indicates that the class supports aggregation.</span></span>

``` syntax
[
   coclass-attribute-list,
   aggregatable
]
coclass coclass-name
{
   coclass-interface-list
}
```

## <a name="parameters"></a><span data-ttu-id="c760f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c760f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c760f-107">*coclass-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="c760f-107">*coclass-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="c760f-108">Altri attributi che si applicano alla classe.</span><span class="sxs-lookup"><span data-stu-id="c760f-108">Other attributes that apply to the class.</span></span>

</dd> <dt>

<span data-ttu-id="c760f-109">*coclass-nome*</span><span class="sxs-lookup"><span data-stu-id="c760f-109">*coclass-name*</span></span> 
</dt> <dd>

<span data-ttu-id="c760f-110">Nome della classe.</span><span class="sxs-lookup"><span data-stu-id="c760f-110">The name of the class.</span></span>

</dd> <dt>

<span data-ttu-id="c760f-111">*coclass-interface-List*</span><span class="sxs-lookup"><span data-stu-id="c760f-111">*coclass-interface-list*</span></span> 
</dt> <dd>

<span data-ttu-id="c760f-112">Elenco di interfacce per la classe.</span><span class="sxs-lookup"><span data-stu-id="c760f-112">A list of interfaces for the class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c760f-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="c760f-113">Remarks</span></span>

<span data-ttu-id="c760f-114">Usare l'attributo **\[ aggregable \]** in un'istruzione [**coclass**](coclass.md) per informare gli utenti che la classe supporta le aggregazioni.</span><span class="sxs-lookup"><span data-stu-id="c760f-114">Use the **\[aggregatable\]** attribute on a [**coclass**](coclass.md) statement to let users know that the class supports aggregations.</span></span> <span data-ttu-id="c760f-115">Ovvero la classe consente l'esposizione delle interfacce da parte di una classe contenitore come se queste interfacce fossero interfacce del contenitore.</span><span class="sxs-lookup"><span data-stu-id="c760f-115">That is, the class allows its interfaces to be exposed by a container class as if these interfaces were the container's own interfaces.</span></span>

<span data-ttu-id="c760f-116">La rappresentazione TypeFlag per questo attributo è TYPEFLAG \_ FAGGREGATABLE.</span><span class="sxs-lookup"><span data-stu-id="c760f-116">The typeflag representation for this attribute is TYPEFLAG\_FAGGREGATABLE.</span></span>

## <a name="examples"></a><span data-ttu-id="c760f-117">Esempi</span><span class="sxs-lookup"><span data-stu-id="c760f-117">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    aggregatable
]
coclass Form
{
    [default] interface IForm;
    [default, source] interface IFormEvents;
}
```

## <a name="see-also"></a><span data-ttu-id="c760f-118">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="c760f-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c760f-119">**coclass**</span><span class="sxs-lookup"><span data-stu-id="c760f-119">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="c760f-120">Generazione di una libreria dei tipi con MIDL</span><span class="sxs-lookup"><span data-stu-id="c760f-120">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="c760f-121">Esempio di file di FAD</span><span class="sxs-lookup"><span data-stu-id="c760f-121">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="c760f-122">Sintassi del file di FAD</span><span class="sxs-lookup"><span data-stu-id="c760f-122">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> </dl>

 

 