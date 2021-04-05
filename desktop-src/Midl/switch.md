---
title: attributo switch
description: La parola chiave switch seleziona discriminante per un'Unione incapsulata \_ .
ms.assetid: 66179b68-852f-4943-9105-e9fb310f3c2e
keywords:
- cambia attributo MIDL
topic_type:
- apiref
api_name:
- switch
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cdf9342789d5603a3b64d778bd60364eebde50e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103955975"
---
# <a name="switch-attribute"></a><span data-ttu-id="c99a0-104">attributo switch</span><span class="sxs-lookup"><span data-stu-id="c99a0-104">switch attribute</span></span>

<span data-ttu-id="c99a0-105">La parola chiave **Switch** seleziona discriminante per un' [**\_ Unione incapsulata**](encapsulated-unions.md).</span><span class="sxs-lookup"><span data-stu-id="c99a0-105">The **switch** keyword selects the discriminant for an [**encapsulated\_union**](encapsulated-unions.md).</span></span>

``` syntax
switch (switch-type switch-name)
```

## <a name="parameters"></a><span data-ttu-id="c99a0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c99a0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c99a0-107">*switch-type*</span><span class="sxs-lookup"><span data-stu-id="c99a0-107">*switch-type*</span></span> 
</dt> <dd>

<span data-ttu-id="c99a0-108">Specifica un tipo [**int**](int.md), [**char**](-char.md), [**enum**](enum.md) o un identificatore che viene risolto in uno di questi tipi.</span><span class="sxs-lookup"><span data-stu-id="c99a0-108">Specifies an [**int**](int.md), [**char**](-char.md), [**enum**](enum.md) type, or an identifier that resolves to one of these types.</span></span>

</dd> <dt>

<span data-ttu-id="c99a0-109">*Switch-name*</span><span class="sxs-lookup"><span data-stu-id="c99a0-109">*switch-name*</span></span> 
</dt> <dd>

<span data-ttu-id="c99a0-110">Specifica il nome della variabile di tipo *switch-type* che funge da discriminante di Unione.</span><span class="sxs-lookup"><span data-stu-id="c99a0-110">Specifies the name of the variable of type *switch-type* that acts as the union discriminant.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="c99a0-111">Esempi</span><span class="sxs-lookup"><span data-stu-id="c99a0-111">Examples</span></span>

``` syntax
typedef union _S1_TYPE switch (long l1) U1_TYPE 
{ 
    case 1024: 
        float f1; 
    case 2048: 
        double d2; 
} S1_TYPE; 
 
/* in generated header file */ 
typedef struct _S1_TYPE 
{ 
    long l1; 
    union 
    { 
        float f1; 
        double d2; 
    } U1_TYPE; 
} S1_TYPE;
```

## <a name="see-also"></a><span data-ttu-id="c99a0-112">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="c99a0-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c99a0-113">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="c99a0-113">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="c99a0-114">Unioni non incapsulate</span><span class="sxs-lookup"><span data-stu-id="c99a0-114">Nonencapsulated Unions</span></span>](nonencapsulated-unions.md)
</dt> <dt>

[<span data-ttu-id="c99a0-115">**opzione \_**</span><span class="sxs-lookup"><span data-stu-id="c99a0-115">**switch\_is**</span></span>](switch-is.md)
</dt> <dt>

[<span data-ttu-id="c99a0-116">**tipo di opzione \_**</span><span class="sxs-lookup"><span data-stu-id="c99a0-116">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="c99a0-117">**Unione**</span><span class="sxs-lookup"><span data-stu-id="c99a0-117">**union**</span></span>](union.md)
</dt> </dl>

 

 




