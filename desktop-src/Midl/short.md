---
title: attributo Short
description: La parola chiave short definisce un intero a 16 bit.
ms.assetid: 622464a3-0d79-421a-8742-8a3746fe1533
keywords:
- MIDL attributo breve
topic_type:
- apiref
api_name:
- short
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b993c830c631b5b95246a7a191388ce897dbaafb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104334284"
---
# <a name="short-attribute"></a><span data-ttu-id="fccea-104">attributo Short</span><span class="sxs-lookup"><span data-stu-id="fccea-104">short attribute</span></span>

<span data-ttu-id="fccea-105">La parola chiave **short** definisce un intero a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="fccea-105">The **short** keyword designates a 16-bit integer.</span></span>

``` syntax
[[ signed | unsigned ]] short [[ int ]] declarator-list;
```

## <a name="parameters"></a><span data-ttu-id="fccea-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fccea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fccea-107">*elenco di dichiaratori*</span><span class="sxs-lookup"><span data-stu-id="fccea-107">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="fccea-108">Specifica uno o più dichiaratori C standard, ad esempio identificatori, dichiaratori di puntatore e dichiaratori di matrici.</span><span class="sxs-lookup"><span data-stu-id="fccea-108">Specifies one or more standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="fccea-109">I dichiaratori di funzione e le dichiarazioni di campi di bit non sono consentiti nelle strutture trasmesse in chiamate a procedure remote.</span><span class="sxs-lookup"><span data-stu-id="fccea-109">(Function declarators and bit-field declarations are not allowed in structures that are transmitted in remote procedure calls.</span></span> <span data-ttu-id="fccea-110">Questi dichiaratori sono consentiti in strutture non trasmesse. Separare più dichiaratori con virgole.</span><span class="sxs-lookup"><span data-stu-id="fccea-110">These declarators are allowed in structures that are not transmitted.) Separate multiple declarators with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fccea-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="fccea-111">Remarks</span></span>

<span data-ttu-id="fccea-112">La parola chiave **short** può essere preceduta dalla parola chiave [**signed**](signed.md) o dalla parola chiave [**unsigned**](unsigned.md).</span><span class="sxs-lookup"><span data-stu-id="fccea-112">The **short** keyword can be preceded by either the keyword [**signed**](signed.md) or the keyword [**unsigned**](unsigned.md).</span></span> <span data-ttu-id="fccea-113">La parola chiave [**int**](int.md) è facoltativa e può essere omessa.</span><span class="sxs-lookup"><span data-stu-id="fccea-113">The [**int**](int.md) keyword is optional and can be omitted.</span></span> <span data-ttu-id="fccea-114">Per il compilatore MIDL, un valore short integer è firmato per impostazione predefinita ed è sinonimo di **signed short int**.</span><span class="sxs-lookup"><span data-stu-id="fccea-114">To the MIDL compiler, a short integer is signed by default and is synonymous with **signed short int**.</span></span>

<span data-ttu-id="fccea-115">Il tipo **short** Integer è uno dei tipi di base del linguaggio IDL.</span><span class="sxs-lookup"><span data-stu-id="fccea-115">The **short** integer type is one of the base types of the IDL language.</span></span> <span data-ttu-id="fccea-116">Il tipo **short** Integer può essere visualizzato come identificatore di tipo nelle dichiarazioni [**const**](const.md) , nelle dichiarazioni [**typedef**](typedef.md) , nelle dichiarazioni generali e nei dichiaratori di funzione (come identificatore del tipo restituito dalla funzione e come identificatore del tipo di parametro).</span><span class="sxs-lookup"><span data-stu-id="fccea-116">The **short** integer type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function-return-type specifier and a parameter-type specifier).</span></span> <span data-ttu-id="fccea-117">Per il contesto in cui vengono visualizzati gli identificatori di tipo, vedere [file di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="fccea-117">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="fccea-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fccea-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fccea-119">Tipi di base MIDL</span><span class="sxs-lookup"><span data-stu-id="fccea-119">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="fccea-120">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="fccea-120">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="fccea-121">**INT**</span><span class="sxs-lookup"><span data-stu-id="fccea-121">**int**</span></span>](int.md)
</dt> <dt>

[<span data-ttu-id="fccea-122">**long**</span><span class="sxs-lookup"><span data-stu-id="fccea-122">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="fccea-123">**con segno**</span><span class="sxs-lookup"><span data-stu-id="fccea-123">**signed**</span></span>](signed.md)
</dt> <dt>

[<span data-ttu-id="fccea-124">**piccolo**</span><span class="sxs-lookup"><span data-stu-id="fccea-124">**small**</span></span>](small.md)
</dt> <dt>

[<span data-ttu-id="fccea-125">**unsigned**</span><span class="sxs-lookup"><span data-stu-id="fccea-125">**unsigned**</span></span>](unsigned.md)
</dt> </dl>

 

 




