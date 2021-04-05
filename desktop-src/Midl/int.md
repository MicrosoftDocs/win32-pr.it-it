---
title: attributo int
description: La parola chiave int specifica un intero con segno a 32 bit sulle piattaforme a 32 bit. Nelle piattaforme a 16 bit la parola chiave int è una parola chiave facoltativa che può accompagnare le parole chiave Small, short e Long.
ms.assetid: ad6ce0ff-e87b-4701-b9d2-a69c34e0339b
keywords:
- attributo int MIDL
topic_type:
- apiref
api_name:
- int
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f916c4f03023c756b71a2e3cbb38acd9f41f1e8
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718064"
---
# <a name="int-attribute"></a><span data-ttu-id="b4e7c-105">attributo int</span><span class="sxs-lookup"><span data-stu-id="b4e7c-105">int attribute</span></span>

<span data-ttu-id="b4e7c-106">La parola chiave **int** specifica un intero con segno a 32 bit sulle piattaforme a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="b4e7c-106">The keyword **int** specifies a 32-bit signed integer on 32-bit platforms.</span></span> <span data-ttu-id="b4e7c-107">Nelle piattaforme a 16 bit la parola chiave **int** è una parola chiave facoltativa che può accompagnare le parole chiave [**small**](small.md), [**short**](short.md)e [**Long**](long.md).</span><span class="sxs-lookup"><span data-stu-id="b4e7c-107">On 16-bit platforms, the keyword **int** is an optional keyword that can accompany the keywords [**small**](small.md), [**short**](short.md), and [**long**](long.md).</span></span>

``` syntax
[ signed | unsigned ] integer-modifier [ int ] declarator-list;
```

## <a name="parameters"></a><span data-ttu-id="b4e7c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b4e7c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4e7c-109">*modificatore Integer*</span><span class="sxs-lookup"><span data-stu-id="b4e7c-109">*integer-modifier*</span></span> 
</dt> <dd>

<span data-ttu-id="b4e7c-110">Specifica la parola chiave [**small**](small.md), [**short**](short.md), [**Long**](long.md), [**Hyper**](hyper.md), [**\_ \_ int3264**](--int3264.md)o [**\_ \_ Int64**](--int64.md), che consente di selezionare le dimensioni dei dati Integer.</span><span class="sxs-lookup"><span data-stu-id="b4e7c-110">Specifies the keyword [**small**](small.md), [**short**](short.md), [**long**](long.md), [**hyper**](hyper.md), [**\_\_int3264**](--int3264.md), or [**\_\_int64**](--int64.md),which selects the size of the integer data.</span></span> <span data-ttu-id="b4e7c-111">Nelle piattaforme a 16 bit è necessario che il qualificatore delle dimensioni sia presente.</span><span class="sxs-lookup"><span data-stu-id="b4e7c-111">On 16-bit platforms, the size qualifier must be present.</span></span>

</dd> <dt>

<span data-ttu-id="b4e7c-112">*elenco di dichiaratori*</span><span class="sxs-lookup"><span data-stu-id="b4e7c-112">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="b4e7c-113">Specifica uno o più dichiaratori C standard, ad esempio identificatori, dichiaratori di puntatore e dichiaratori di matrici.</span><span class="sxs-lookup"><span data-stu-id="b4e7c-113">Specifies one or more standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="b4e7c-114">I dichiaratori di funzione e le dichiarazioni di campi di bit non sono consentiti nelle strutture trasmesse in chiamate a procedure remote.</span><span class="sxs-lookup"><span data-stu-id="b4e7c-114">(Function declarators and bit-field declarations are not allowed in structures that are transmitted in remote procedure calls.</span></span> <span data-ttu-id="b4e7c-115">Questi dichiaratori sono consentiti in strutture non trasmesse. Separare più dichiaratori con virgole.</span><span class="sxs-lookup"><span data-stu-id="b4e7c-115">These declarators are allowed in structures that are not transmitted.) Separate multiple declarators with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b4e7c-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="b4e7c-116">Remarks</span></span>

<span data-ttu-id="b4e7c-117">I tipi integer sono tra i tipi di base del linguaggio di definizione dell'interfaccia (IDL).</span><span class="sxs-lookup"><span data-stu-id="b4e7c-117">Integer types are among the base types of the interface definition language (IDL).</span></span> <span data-ttu-id="b4e7c-118">Possono apparire come identificatori di tipo nelle dichiarazioni [**typedef**](typedef.md) , nelle dichiarazioni generali e nei dichiaratori di funzione (come identificatore del tipo restituito dalla funzione e come identificatore del tipo di parametro).</span><span class="sxs-lookup"><span data-stu-id="b4e7c-118">They can appear as type specifiers in [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function-return-type specifier and as a parameter-type specifier).</span></span> <span data-ttu-id="b4e7c-119">Per il contesto in cui vengono visualizzati gli identificatori di tipo, vedere [file di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="b4e7c-119">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

<span data-ttu-id="b4e7c-120">Se non viene specificata alcuna specifica del segno integer, l'impostazione predefinita del tipo Integer è [**signed**](signed.md).</span><span class="sxs-lookup"><span data-stu-id="b4e7c-120">If no integer sign specification is provided, the integer type defaults to [**signed**](signed.md).</span></span>

<span data-ttu-id="b4e7c-121">I compilatori IDL DCE non consentono alla parola chiave [**signed**](signed.md) di specificare il segno dei tipi Integer.</span><span class="sxs-lookup"><span data-stu-id="b4e7c-121">DCE IDL compilers do not allow the keyword [**signed**](signed.md) to specify the sign of integer types.</span></span> <span data-ttu-id="b4e7c-122">Questa funzionalità non è pertanto disponibile quando si usa l'opzione [**/OSF**](-osf.md) del compilatore MIDL.</span><span class="sxs-lookup"><span data-stu-id="b4e7c-122">Therefore, this feature is not available when you use the MIDL compiler [**/osf**](-osf.md) switch.</span></span>

<span data-ttu-id="b4e7c-123">\_ \_ Se può essere evitato, Microsoft non consiglia l'uso di int3264 per la comunicazione remota.</span><span class="sxs-lookup"><span data-stu-id="b4e7c-123">Microsoft does not recommend the use of \_\_int3264 for remoting if it can be avoided.</span></span> <span data-ttu-id="b4e7c-124">Per ulteriori informazioni sull'utilizzo e sulle limitazioni, vedere l'argomento relativo a [**\_ \_ int3264**](--int3264.md) .</span><span class="sxs-lookup"><span data-stu-id="b4e7c-124">Please see the topic on [**\_\_int3264**](--int3264.md) for more information regarding it's use and limitations.</span></span>

## <a name="examples"></a><span data-ttu-id="b4e7c-125">Esempi</span><span class="sxs-lookup"><span data-stu-id="b4e7c-125">Examples</span></span>

``` syntax
signed short int i = 0; 
int j = i; 
typedef struct 
{ 
    small int         i1; 
    short             i2; 
    unsigned long int i3; 
} INTSIZETYPE; 
 
HRESULT MyFunc([in] long int lCount);
```

## <a name="see-also"></a><span data-ttu-id="b4e7c-126">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="b4e7c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4e7c-127">Tipi di base MIDL</span><span class="sxs-lookup"><span data-stu-id="b4e7c-127">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="b4e7c-128">**enum**</span><span class="sxs-lookup"><span data-stu-id="b4e7c-128">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="b4e7c-129">**Hyper**</span><span class="sxs-lookup"><span data-stu-id="b4e7c-129">**hyper**</span></span>](hyper.md)
</dt> <dt>

[<span data-ttu-id="b4e7c-130">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="b4e7c-130">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="b4e7c-131">**long**</span><span class="sxs-lookup"><span data-stu-id="b4e7c-131">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="b4e7c-132">**/osf**</span><span class="sxs-lookup"><span data-stu-id="b4e7c-132">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="b4e7c-133">**short**</span><span class="sxs-lookup"><span data-stu-id="b4e7c-133">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="b4e7c-134">**con segno**</span><span class="sxs-lookup"><span data-stu-id="b4e7c-134">**signed**</span></span>](signed.md)
</dt> <dt>

[<span data-ttu-id="b4e7c-135">**piccolo**</span><span class="sxs-lookup"><span data-stu-id="b4e7c-135">**small**</span></span>](small.md)
</dt> <dt>

[<span data-ttu-id="b4e7c-136">**struct**</span><span class="sxs-lookup"><span data-stu-id="b4e7c-136">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="b4e7c-137">**typedef**</span><span class="sxs-lookup"><span data-stu-id="b4e7c-137">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="b4e7c-138">**Unione**</span><span class="sxs-lookup"><span data-stu-id="b4e7c-138">**union**</span></span>](union.md)
</dt> </dl>

 

 




