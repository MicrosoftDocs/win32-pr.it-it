---
title: attributo Long
description: La parola chiave Long designa un intero a 32 bit.
ms.assetid: 5619e482-e3c3-4898-a70b-afd337d2749a
keywords:
- MIDL attributo Long
topic_type:
- apiref
api_name:
- long
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47ea9af3bfac85ff375f6d5433b4e9f3ed37d8f7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103955919"
---
# <a name="long-attribute"></a><span data-ttu-id="c8ad8-104">attributo Long</span><span class="sxs-lookup"><span data-stu-id="c8ad8-104">long attribute</span></span>

<span data-ttu-id="c8ad8-105">La parola chiave **Long** designa un intero a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="c8ad8-105">The **long** keyword designates a 32-bit integer.</span></span>

``` syntax
[ signed | unsigned ] long [ int ] declarator-list;
```

## <a name="parameters"></a><span data-ttu-id="c8ad8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c8ad8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8ad8-107">*elenco di dichiaratori*</span><span class="sxs-lookup"><span data-stu-id="c8ad8-107">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="c8ad8-108">Specifica uno o più dichiaratori C standard, ad esempio identificatori, dichiaratori di puntatore e dichiaratori di matrici.</span><span class="sxs-lookup"><span data-stu-id="c8ad8-108">Specifies one or more standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="c8ad8-109">I dichiaratori di funzione e le dichiarazioni di campi di bit non sono consentiti nelle strutture trasmesse in chiamate a procedure remote.</span><span class="sxs-lookup"><span data-stu-id="c8ad8-109">(Function declarators and bit-field declarations are not allowed in structures that are transmitted in remote procedure calls.</span></span> <span data-ttu-id="c8ad8-110">Questi dichiaratori sono consentiti in strutture non trasmesse. Separare più dichiaratori con virgole.</span><span class="sxs-lookup"><span data-stu-id="c8ad8-110">These declarators are allowed in structures that are not transmitted.) Separate multiple declarators with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c8ad8-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="c8ad8-111">Remarks</span></span>

<span data-ttu-id="c8ad8-112">La parola chiave **Long** può essere preceduta dalla parola chiave [**signed**](signed.md) o dalla parola chiave [**unsigned**](unsigned.md).</span><span class="sxs-lookup"><span data-stu-id="c8ad8-112">The **long** keyword can be preceded by either the keyword [**signed**](signed.md) or the keyword [**unsigned**](unsigned.md).</span></span> <span data-ttu-id="c8ad8-113">La parola chiave [**int**](int.md) è facoltativa e può essere omessa.</span><span class="sxs-lookup"><span data-stu-id="c8ad8-113">The [**int**](int.md) keyword is optional and can be omitted.</span></span> <span data-ttu-id="c8ad8-114">Per il compilatore MIDL, un valore long integer è firmato per impostazione predefinita ed è sinonimo di **signed long int**. Sulle piattaforme a 32 bit, **Long** è sinonimo di **int**.</span><span class="sxs-lookup"><span data-stu-id="c8ad8-114">To the MIDL compiler, a long integer is signed by default and is synonymous with **signed long int**. On 32-bit platforms, **long** is synonymous with **int**.</span></span>

<span data-ttu-id="c8ad8-115">Il tipo **Long** Integer è uno dei tipi di base del linguaggio IDL.</span><span class="sxs-lookup"><span data-stu-id="c8ad8-115">The **long** integer type is one of the base types of the IDL language.</span></span> <span data-ttu-id="c8ad8-116">Il tipo **Long** Integer può essere visualizzato come identificatore di tipo nelle dichiarazioni [**const**](const.md) , nelle dichiarazioni [**typedef**](typedef.md) , nelle dichiarazioni generali e nei dichiaratori di funzione (come identificatore del tipo restituito dalla funzione e come identificatore del tipo di parametro).</span><span class="sxs-lookup"><span data-stu-id="c8ad8-116">The **long** integer type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function return–type specifier and as a parameter-type specifier).</span></span> <span data-ttu-id="c8ad8-117">Per il contesto in cui vengono visualizzati gli identificatori di tipo, vedere [file di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="c8ad8-117">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="c8ad8-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c8ad8-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8ad8-119">**const**</span><span class="sxs-lookup"><span data-stu-id="c8ad8-119">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="c8ad8-120">Tipi di base MIDL</span><span class="sxs-lookup"><span data-stu-id="c8ad8-120">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="c8ad8-121">**Hyper**</span><span class="sxs-lookup"><span data-stu-id="c8ad8-121">**hyper**</span></span>](hyper.md)
</dt> <dt>

[<span data-ttu-id="c8ad8-122">**INT**</span><span class="sxs-lookup"><span data-stu-id="c8ad8-122">**int**</span></span>](int.md)
</dt> <dt>

[<span data-ttu-id="c8ad8-123">**short**</span><span class="sxs-lookup"><span data-stu-id="c8ad8-123">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="c8ad8-124">**con segno**</span><span class="sxs-lookup"><span data-stu-id="c8ad8-124">**signed**</span></span>](signed.md)
</dt> <dt>

[<span data-ttu-id="c8ad8-125">**piccolo**</span><span class="sxs-lookup"><span data-stu-id="c8ad8-125">**small**</span></span>](small.md)
</dt> <dt>

[<span data-ttu-id="c8ad8-126">**typedef**</span><span class="sxs-lookup"><span data-stu-id="c8ad8-126">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="c8ad8-127">**unsigned**</span><span class="sxs-lookup"><span data-stu-id="c8ad8-127">**unsigned**</span></span>](unsigned.md)
</dt> </dl>

 

 




