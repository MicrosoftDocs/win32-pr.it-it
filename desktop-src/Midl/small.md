---
title: attributo Small
description: La parola chiave Small designa un numero intero a 8 bit.
ms.assetid: 368e8836-1baa-4547-a62b-f34ac38bbdb2
keywords:
- MIDL attributo Small
topic_type:
- apiref
api_name:
- small
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5a0f106f1be1ba6d0acabf877b5dbefab3eaff6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104397367"
---
# <a name="small-attribute"></a><span data-ttu-id="34c27-104">attributo Small</span><span class="sxs-lookup"><span data-stu-id="34c27-104">small attribute</span></span>

<span data-ttu-id="34c27-105">La parola chiave **small** designa un numero intero a 8 bit.</span><span class="sxs-lookup"><span data-stu-id="34c27-105">The **small** keyword designates an 8-bit integer number.</span></span>

``` syntax
small identifier-name;
```

## <a name="parameters"></a><span data-ttu-id="34c27-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="34c27-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34c27-107">*nome identificatore*</span><span class="sxs-lookup"><span data-stu-id="34c27-107">*identifier-name*</span></span> 
</dt> <dd>

<span data-ttu-id="34c27-108">Specifica un identificatore MIDL valido.</span><span class="sxs-lookup"><span data-stu-id="34c27-108">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="34c27-109">Gli identificatori MIDL validi sono costituiti da un massimo di 31 caratteri alfanumerici e/o di sottolineatura e devono iniziare con un carattere alfabetico o di sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="34c27-109">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="34c27-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="34c27-110">Remarks</span></span>

<span data-ttu-id="34c27-111">La parola chiave **small** può essere preceduta dalla parola chiave [**signed**](signed.md) o dalla parola chiave [**unsigned**](unsigned.md).</span><span class="sxs-lookup"><span data-stu-id="34c27-111">The **small** keyword can be preceded by either the keyword [**signed**](signed.md) or the keyword [**unsigned**](unsigned.md).</span></span> <span data-ttu-id="34c27-112">La parola chiave [**int**](int.md) è facoltativa e può essere omessa.</span><span class="sxs-lookup"><span data-stu-id="34c27-112">The [**int**](int.md) keyword is optional and can be omitted.</span></span> <span data-ttu-id="34c27-113">Per il compilatore MIDL, un numero intero piccolo è **firmato** per impostazione predefinita ed è sinonimo di **signed Small int**.</span><span class="sxs-lookup"><span data-stu-id="34c27-113">To the MIDL compiler, a small integer is **signed** by default and is synonymous with **signed small int**.</span></span>

<span data-ttu-id="34c27-114">Il tipo di valore integer **piccolo** è uno dei tipi di base del linguaggio IDL.</span><span class="sxs-lookup"><span data-stu-id="34c27-114">The **small** integer type is one of the base types of the IDL language.</span></span> <span data-ttu-id="34c27-115">Il tipo di valore integer **piccolo** può essere visualizzato come identificatore di tipo nelle dichiarazioni [**const**](const.md) , nelle dichiarazioni [**typedef**](typedef.md) , nelle dichiarazioni generali e nei dichiaratori di funzione (come identificatore del tipo restituito dalla funzione e come identificatore del tipo di parametro).</span><span class="sxs-lookup"><span data-stu-id="34c27-115">The **small** integer type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function return–type specifier and as a parameter-type specifier).</span></span> <span data-ttu-id="34c27-116">Per il contesto in cui vengono visualizzati gli identificatori di tipo, vedere [file di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="34c27-116">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

<span data-ttu-id="34c27-117">Il segno del tipo **piccolo** può essere modificato dall'opzione del compilatore MIDL [**/char**](-char.md).</span><span class="sxs-lookup"><span data-stu-id="34c27-117">The sign of the **small** type can be modified by the MIDL compiler switch [**/char**](-char.md).</span></span> <span data-ttu-id="34c27-118">Per evitare confusione, specificare il segno del tipo integer con le parole chiave [**signed**](signed.md) e [**unsigned**](unsigned.md).</span><span class="sxs-lookup"><span data-stu-id="34c27-118">To avoid confusion, specify the sign of the integer type with the keywords [**signed**](signed.md) and [**unsigned**](unsigned.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="34c27-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="34c27-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34c27-120">**/char**</span><span class="sxs-lookup"><span data-stu-id="34c27-120">**/char**</span></span>](-char.md)
</dt> <dt>

[<span data-ttu-id="34c27-121">**const**</span><span class="sxs-lookup"><span data-stu-id="34c27-121">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="34c27-122">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="34c27-122">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="34c27-123">**INT**</span><span class="sxs-lookup"><span data-stu-id="34c27-123">**int**</span></span>](int.md)
</dt> <dt>

[<span data-ttu-id="34c27-124">**long**</span><span class="sxs-lookup"><span data-stu-id="34c27-124">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="34c27-125">**short**</span><span class="sxs-lookup"><span data-stu-id="34c27-125">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="34c27-126">**con segno**</span><span class="sxs-lookup"><span data-stu-id="34c27-126">**signed**</span></span>](signed.md)
</dt> <dt>

[<span data-ttu-id="34c27-127">**unsigned**</span><span class="sxs-lookup"><span data-stu-id="34c27-127">**unsigned**</span></span>](unsigned.md)
</dt> <dt>

[<span data-ttu-id="34c27-128">**typedef**</span><span class="sxs-lookup"><span data-stu-id="34c27-128">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 




