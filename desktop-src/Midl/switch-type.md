---
title: switch_type (attributo)
description: L'attributo \ Switch \_ Type \ identifica il tipo della variabile utilizzata come unione discriminante. Il tipo di opzione può essere un Integer, un carattere, un valore booleano o un tipo di enumerazione.
ms.assetid: e4c6d33b-d4db-42b7-9d18-fd14bf1fb530
keywords:
- attributo switch_type MIDL
topic_type:
- apiref
api_name:
- switch_type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14184c5838d9f671f75536714d73c3f6ebf00a0a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857454"
---
# <a name="switch_type-attribute"></a><span data-ttu-id="0dc48-105">Switch \_ type-attributo</span><span class="sxs-lookup"><span data-stu-id="0dc48-105">switch\_type attribute</span></span>

<span data-ttu-id="0dc48-106">L'attributo **\[ Switch \_ Type \]** identifica il tipo della variabile utilizzata come unione discriminante.</span><span class="sxs-lookup"><span data-stu-id="0dc48-106">The **\[switch\_type\]** attribute identifies the type of the variable used as the union discriminant.</span></span> <span data-ttu-id="0dc48-107">Il tipo di opzione può essere un Integer, un carattere, un valore booleano o un tipo di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="0dc48-107">The switch type can be an integer, character, Boolean, or enumeration type.</span></span>

``` syntax
switch_type(switch-type-specifier)
```

## <a name="parameters"></a><span data-ttu-id="0dc48-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0dc48-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0dc48-109">*switch-type-specifier*</span><span class="sxs-lookup"><span data-stu-id="0dc48-109">*switch-type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="0dc48-110">Specifica un tipo [**int**](int.md), [**char**](char-idl.md), [**Boolean**](boolean.md)o [**enum**](enum.md) o un identificatore di tale tipo.</span><span class="sxs-lookup"><span data-stu-id="0dc48-110">Specifies an [**int**](int.md), [**char**](char-idl.md), [**Boolean**](boolean.md), or [**enum**](enum.md) type, or an identifier of such a type.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0dc48-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="0dc48-111">Remarks</span></span>

<span data-ttu-id="0dc48-112">Mentre l'attributo **\[ Switch \_ Type \]** identifica il tipo di variabile, l' **\[** [**opzione \_ is**](switch-is.md) **\]** attribute specifica il nome del parametro che rappresenta l'unione discriminante.</span><span class="sxs-lookup"><span data-stu-id="0dc48-112">While the **\[switch\_type\]** attribute identifies the variable type, the **\[**[**switch\_is**](switch-is.md)**\]** attribute specifies the name of the parameter that is the union discriminant.</span></span> <span data-ttu-id="0dc48-113">L'attributo **\[ Switch \_ Type \]** si applica ai parametri o ai membri di strutture o unioni.</span><span class="sxs-lookup"><span data-stu-id="0dc48-113">The **\[switch\_type\]** attribute applies to parameters or members of structures or unions.</span></span>

<span data-ttu-id="0dc48-114">L'Unione e il relativo discriminante devono essere specificati allo stesso livello logico.</span><span class="sxs-lookup"><span data-stu-id="0dc48-114">The union and its discriminant must be specified at the same logical level.</span></span> <span data-ttu-id="0dc48-115">Quando l'Unione è un parametro, il discriminante di Unione deve essere un altro parametro.</span><span class="sxs-lookup"><span data-stu-id="0dc48-115">When the union is a parameter, the union discriminant must be another parameter.</span></span> <span data-ttu-id="0dc48-116">Quando l'Unione è un campo di una struttura, discriminante deve essere un altro campo della struttura allo stesso livello del campo di Unione.</span><span class="sxs-lookup"><span data-stu-id="0dc48-116">When the union is a field of a structure, the discriminant must be another field of the structure at the same level as the union field.</span></span>

## <a name="examples"></a><span data-ttu-id="0dc48-117">Esempi</span><span class="sxs-lookup"><span data-stu-id="0dc48-117">Examples</span></span>

``` syntax
typedef [switch_type(short)] union _WILLIE_UNION_TYPE 
{ 
    [case(24)] 
        float fMays; 
    [case(25)] 
        double dMcCovey; 
    [default] 
        ; 
} WILLIE_UNION_TYPE; 
 
typedef struct _WINNER_TYPE 
{ 
    [switch_is(sUniformNumber)] WILLIE_UNION_TYPE w; 
    short sUniformNumber; 
} WINNER_TYPE;
```

## <a name="see-also"></a><span data-ttu-id="0dc48-118">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="0dc48-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0dc48-119">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="0dc48-119">**Boolean**</span></span>](boolean.md)
</dt> <dt>

[<span data-ttu-id="0dc48-120">**char**</span><span class="sxs-lookup"><span data-stu-id="0dc48-120">**char**</span></span>](char-idl.md)
</dt> <dt>

[<span data-ttu-id="0dc48-121">Unioni incapsulate</span><span class="sxs-lookup"><span data-stu-id="0dc48-121">Encapsulated Unions</span></span>](encapsulated-unions.md)
</dt> <dt>

[<span data-ttu-id="0dc48-122">**enum**</span><span class="sxs-lookup"><span data-stu-id="0dc48-122">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="0dc48-123">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="0dc48-123">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="0dc48-124">**INT**</span><span class="sxs-lookup"><span data-stu-id="0dc48-124">**int**</span></span>](int.md)
</dt> <dt>

[<span data-ttu-id="0dc48-125">Unioni non incapsulate</span><span class="sxs-lookup"><span data-stu-id="0dc48-125">Nonencapsulated Unions</span></span>](nonencapsulated-unions.md)
</dt> <dt>

[<span data-ttu-id="0dc48-126">**opzione \_**</span><span class="sxs-lookup"><span data-stu-id="0dc48-126">**switch\_is**</span></span>](switch-is.md)
</dt> <dt>

[<span data-ttu-id="0dc48-127">**Unione**</span><span class="sxs-lookup"><span data-stu-id="0dc48-127">**union**</span></span>](union.md)
</dt> </dl>

 

 




