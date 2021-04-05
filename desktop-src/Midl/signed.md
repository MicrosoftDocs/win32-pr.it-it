---
title: attributo firmato
description: La parola chiave signed indica il bit più significativo di una variabile integer che rappresenta un bit di segno anziché un bit di dati.
ms.assetid: 6116089a-647e-485b-8f79-9c9267aa4810
keywords:
- attributo MIDL firmato
topic_type:
- apiref
api_name:
- signed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 500b87c849f31082a036d605db0947650e914bed
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857085"
---
# <a name="signed-attribute"></a><span data-ttu-id="97516-104">attributo firmato</span><span class="sxs-lookup"><span data-stu-id="97516-104">signed attribute</span></span>

<span data-ttu-id="97516-105">La parola chiave **signed** indica il bit più significativo di una variabile integer che rappresenta un bit di segno anziché un bit di dati.</span><span class="sxs-lookup"><span data-stu-id="97516-105">The **signed** keyword indicates the most significant bit of an integer variable represents a sign bit rather than a data bit.</span></span>

``` syntax
[[ signed ]] type-qualifier [[ int ]]identifier-name;
```

## <a name="parameters"></a><span data-ttu-id="97516-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="97516-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97516-107">*type-qualifier*</span><span class="sxs-lookup"><span data-stu-id="97516-107">*type-qualifier*</span></span> 
</dt> <dd>

<span data-ttu-id="97516-108">Può essere qualsiasi di [**char**](char-idl.md), [**WCHAR \_ t**](wchar-t.md), [**Long**](long.md), [**short**](short.md)e [**small**](small.md).</span><span class="sxs-lookup"><span data-stu-id="97516-108">Can be any of [**char**](char-idl.md), [**wchar\_t**](wchar-t.md), [**long**](long.md), [**short**](short.md), and [**small**](small.md).</span></span>

</dd> <dt>

<span data-ttu-id="97516-109">*nome identificatore*</span><span class="sxs-lookup"><span data-stu-id="97516-109">*identifier-name*</span></span> 
</dt> <dd>

<span data-ttu-id="97516-110">Specifica un identificatore MIDL valido.</span><span class="sxs-lookup"><span data-stu-id="97516-110">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="97516-111">Gli identificatori MIDL validi sono costituiti da un massimo di 31 caratteri alfanumerici e/o di sottolineatura e devono iniziare con un carattere alfabetico o di sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="97516-111">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="97516-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="97516-112">Remarks</span></span>

<span data-ttu-id="97516-113">Questa parola chiave è facoltativa e può essere utilizzata con qualsiasi tipo di carattere e integer [**char**](char-idl.md), [**WCHAR \_ t**](wchar-t.md), [**Long**](long.md), [**short**](short.md)e [**small**](small.md).</span><span class="sxs-lookup"><span data-stu-id="97516-113">This keyword is optional and can be used with any of the character and integer types [**char**](char-idl.md), [**wchar\_t**](wchar-t.md), [**long**](long.md), [**short**](short.md), and [**small**](small.md).</span></span> <span data-ttu-id="97516-114">Facoltativamente, è possibile includere la parola chiave [**int**](int.md) dopo i qualificatori di tipo **Long**, **short** e **small**.</span><span class="sxs-lookup"><span data-stu-id="97516-114">You can optionally include the keyword [**int**](int.md) after the type qualifiers **long**, **short**, and **small**.</span></span>

<span data-ttu-id="97516-115">Quando si usa l'opzione del compilatore MIDL [**char**](char-idl.md), i tipi di carattere e Integer visualizzati nel file IDL senza parole chiave esplicite del segno possono apparire con le parole chiave **signed** o [**unsigned**](unsigned.md) nel file di intestazione generato.</span><span class="sxs-lookup"><span data-stu-id="97516-115">When you use the MIDL compiler switch [**char**](char-idl.md), character and integer types that appear in the IDL file without explicit sign keywords can appear with the **signed** or [**unsigned**](unsigned.md) keywords in the generated header file.</span></span> <span data-ttu-id="97516-116">Per evitare confusione, specificare il segno dei tipi integer e character.</span><span class="sxs-lookup"><span data-stu-id="97516-116">To avoid confusion, specify the sign of the integer and character types.</span></span>

## <a name="see-also"></a><span data-ttu-id="97516-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="97516-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97516-118">Tipi di base MIDL</span><span class="sxs-lookup"><span data-stu-id="97516-118">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="97516-119">**/char**</span><span class="sxs-lookup"><span data-stu-id="97516-119">**/char**</span></span>](-char.md)
</dt> <dt>

[<span data-ttu-id="97516-120">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="97516-120">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="97516-121">**INT**</span><span class="sxs-lookup"><span data-stu-id="97516-121">**int**</span></span>](int.md)
</dt> <dt>

[<span data-ttu-id="97516-122">**long**</span><span class="sxs-lookup"><span data-stu-id="97516-122">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="97516-123">**short**</span><span class="sxs-lookup"><span data-stu-id="97516-123">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="97516-124">**piccolo**</span><span class="sxs-lookup"><span data-stu-id="97516-124">**small**</span></span>](small.md)
</dt> <dt>

[<span data-ttu-id="97516-125">**unsigned**</span><span class="sxs-lookup"><span data-stu-id="97516-125">**unsigned**</span></span>](unsigned.md)
</dt> <dt>

[<span data-ttu-id="97516-126">**WCHAR \_ t**</span><span class="sxs-lookup"><span data-stu-id="97516-126">**wchar\_t**</span></span>](wchar-t.md)
</dt> </dl>

 

 




