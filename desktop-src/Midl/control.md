---
title: attributo Control
description: L'attributo \ Control \ identifica una coclasse o una libreria come controllo COM, da cui un sito contenitore deriverà librerie dei tipi aggiuntive o classi di oggetti componente.
ms.assetid: c39dd4b6-743f-4888-8954-8b83584bdea5
keywords:
- attributo di controllo MIDL
topic_type:
- apiref
api_name:
- control
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 982327d581ddb606f733e9efbbcb89e2f9972cf4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103724954"
---
# <a name="control-attribute"></a><span data-ttu-id="d0abb-104">attributo Control</span><span class="sxs-lookup"><span data-stu-id="d0abb-104">control attribute</span></span>

<span data-ttu-id="d0abb-105">L'attributo **\[ Control \]** identifica una [**coclasse**](coclass.md) o una [**libreria**](library.md) come controllo com, da cui un sito contenitore deriverà librerie dei tipi aggiuntive o classi di oggetti componente.</span><span class="sxs-lookup"><span data-stu-id="d0abb-105">The **\[control\]** attribute identifies a [**coclass**](coclass.md) or [**library**](library.md) as a COM control, from which a container site will derive additional type libraries or component object classes.</span></span>

``` syntax
[
    uuid, 
    control 
    [, attribute-list]
] 
library | coclass lib-or-coclassname 
{ 
    definitions 
}
```

## <a name="parameters"></a><span data-ttu-id="d0abb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d0abb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0abb-107">*elenco attributi*</span><span class="sxs-lookup"><span data-stu-id="d0abb-107">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="d0abb-108">Specifica zero o più attributi che si applicano alla [**libreria**](library.md) o all'istruzione [**coclasse**](coclass.md) .</span><span class="sxs-lookup"><span data-stu-id="d0abb-108">Specifies zero or more attributes that apply to the [**library**](library.md) or [**coclass**](coclass.md) statement.</span></span> <span data-ttu-id="d0abb-109">Separare più attributi con virgole.</span><span class="sxs-lookup"><span data-stu-id="d0abb-109">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="d0abb-110">*lib-o-CoClassname*</span><span class="sxs-lookup"><span data-stu-id="d0abb-110">*lib-or-coclassname*</span></span> 
</dt> <dd>

<span data-ttu-id="d0abb-111">Specifica il nome della [**libreria**](library.md) o della [**coclasse**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="d0abb-111">Specifies the name of the [**library**](library.md) or [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0abb-112">*definizioni*</span><span class="sxs-lookup"><span data-stu-id="d0abb-112">*definitions*</span></span> 
</dt> <dd>

<span data-ttu-id="d0abb-113">Istruzioni MIDL che specificano i membri della [**libreria**](library.md) o della [**coclasse**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="d0abb-113">MIDL statements that specify the members of the [**library**](library.md) or [**coclass**](coclass.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d0abb-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="d0abb-114">Remarks</span></span>

<span data-ttu-id="d0abb-115">Questo attributo consente di contrassegnare le librerie dei tipi che descrivono i controlli in modo che non vengano visualizzate nei browser dei tipi destinati agli oggetti non visivi.</span><span class="sxs-lookup"><span data-stu-id="d0abb-115">This attribute allows you to mark type libraries that describe controls so they will not be displayed in type browsers intended for nonvisual objects.</span></span>

### <a name="flags"></a><span data-ttu-id="d0abb-116">Flags</span><span class="sxs-lookup"><span data-stu-id="d0abb-116">Flags</span></span>

<span data-ttu-id="d0abb-117">TYPEFLAG \_ FCONTROL, LIBFLAG \_ FCONTROL</span><span class="sxs-lookup"><span data-stu-id="d0abb-117">TYPEFLAG\_FCONTROL, LIBFLAG\_FCONTROL</span></span>

## <a name="examples"></a><span data-ttu-id="d0abb-118">Esempi</span><span class="sxs-lookup"><span data-stu-id="d0abb-118">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC),
    helpstring("Hello 2.1 COM Control Library"), 
    control,version(2.1)
] 
library Hello 
{ 
    /* library definitions */
}
```

## <a name="see-also"></a><span data-ttu-id="d0abb-119">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="d0abb-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0abb-120">Sintassi del file di FAD</span><span class="sxs-lookup"><span data-stu-id="d0abb-120">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="d0abb-121">Esempio di file di FAD</span><span class="sxs-lookup"><span data-stu-id="d0abb-121">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="d0abb-122">Generazione di una libreria dei tipi con MIDL</span><span class="sxs-lookup"><span data-stu-id="d0abb-122">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="d0abb-123">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="d0abb-123">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="d0abb-124">**coclass**</span><span class="sxs-lookup"><span data-stu-id="d0abb-124">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="d0abb-125">**libreria**</span><span class="sxs-lookup"><span data-stu-id="d0abb-125">**library**</span></span>](library.md)
</dt> </dl>

 

 