---
title: attributo senza segno
description: La parola chiave unsigned indica che il bit più significativo di una variabile integer rappresenta un bit di dati anziché un bit con segno.
ms.assetid: bfcc6bec-895e-45e1-b162-b79651662aa6
keywords:
- attributo MIDL senza segno
topic_type:
- apiref
api_name:
- unsigned
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 329d638f1b5be97e5b441aa4e84825fe59a4a3f0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299167"
---
# <a name="unsigned-attribute"></a><span data-ttu-id="daa34-104">attributo senza segno</span><span class="sxs-lookup"><span data-stu-id="daa34-104">unsigned attribute</span></span>

<span data-ttu-id="daa34-105">La parola chiave **unsigned** indica che il bit più significativo di una variabile integer rappresenta un bit di dati anziché un bit con segno.</span><span class="sxs-lookup"><span data-stu-id="daa34-105">The **unsigned** keyword indicates that the most significant bit of an integer variable represents a data bit rather than a signed bit.</span></span>

``` syntax
[[ unsigned ]] type-qualifier [[ int ]]identifier-name;
```

## <a name="parameters"></a><span data-ttu-id="daa34-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="daa34-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="daa34-107">*type-qualifier*</span><span class="sxs-lookup"><span data-stu-id="daa34-107">*type-qualifier*</span></span> 
</dt> <dd>

<span data-ttu-id="daa34-108">Può essere qualsiasi tipo di [**carattere**](char-idl.md), [**WCHAR \_ t**](wchar-t.md), [**Long**](long.md), [**int**](int.md), [**short**](short.md)e [**small**](small.md).</span><span class="sxs-lookup"><span data-stu-id="daa34-108">Can be any of [**char**](char-idl.md), [**wchar\_t**](wchar-t.md), [**long**](long.md), [**int**](int.md), [**short**](short.md), and [**small**](small.md).</span></span>

</dd> <dt>

<span data-ttu-id="daa34-109">*nome identificatore*</span><span class="sxs-lookup"><span data-stu-id="daa34-109">*identifier-name*</span></span> 
</dt> <dd>

<span data-ttu-id="daa34-110">Specifica un identificatore MIDL valido.</span><span class="sxs-lookup"><span data-stu-id="daa34-110">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="daa34-111">Gli identificatori MIDL validi sono costituiti da un massimo di 31 caratteri alfanumerici e/o di sottolineatura e devono iniziare con un carattere alfabetico o di sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="daa34-111">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="daa34-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="daa34-112">Remarks</span></span>

<span data-ttu-id="daa34-113">Questa parola chiave è facoltativa e può essere utilizzata con qualsiasi tipo di carattere e integer [**char**](char-idl.md), [**WCHAR \_ t**](wchar-t.md), [**Long**](long.md), [**short**](short.md)e [**small**](small.md).</span><span class="sxs-lookup"><span data-stu-id="daa34-113">This keyword is optional and can be used with any of the character and integer types [**char**](char-idl.md), [**wchar\_t**](wchar-t.md), [**long**](long.md), [**short**](short.md), and [**small**](small.md).</span></span> <span data-ttu-id="daa34-114">Facoltativamente, è possibile includere la parola chiave [**int**](int.md) dopo i qualificatori di tipo **Long**, **short** e **small**.</span><span class="sxs-lookup"><span data-stu-id="daa34-114">You can optionally include the keyword [**int**](int.md) after the type qualifiers **long**, **short**, and **small**.</span></span>

<span data-ttu-id="daa34-115">Quando si usa l'opzione del compilatore MIDL [**/char**](-char.md), i tipi di carattere e Integer visualizzati nel file IDL senza parole chiave esplicite del segno possono apparire con la parola chiave [**signed**](signed.md) o **unsigned** nel file di intestazione generato.</span><span class="sxs-lookup"><span data-stu-id="daa34-115">When you use the MIDL compiler switch [**/char**](-char.md), character and integer types that appear in the IDL file without explicit sign keywords can appear with the [**signed**](signed.md) or **unsigned** keyword in the generated header file.</span></span> <span data-ttu-id="daa34-116">Per evitare confusione, specificare il segno dei tipi integer e character.</span><span class="sxs-lookup"><span data-stu-id="daa34-116">To avoid confusion, specify the sign of the integer and character types.</span></span>

## <a name="see-also"></a><span data-ttu-id="daa34-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="daa34-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="daa34-118">Tipi di base MIDL</span><span class="sxs-lookup"><span data-stu-id="daa34-118">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="daa34-119">**char**</span><span class="sxs-lookup"><span data-stu-id="daa34-119">**char**</span></span>](char-idl.md)
</dt> <dt>

[<span data-ttu-id="daa34-120">**/char**</span><span class="sxs-lookup"><span data-stu-id="daa34-120">**/char**</span></span>](-char.md)
</dt> <dt>

[<span data-ttu-id="daa34-121">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="daa34-121">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="daa34-122">**INT**</span><span class="sxs-lookup"><span data-stu-id="daa34-122">**int**</span></span>](int.md)
</dt> <dt>

[<span data-ttu-id="daa34-123">**long**</span><span class="sxs-lookup"><span data-stu-id="daa34-123">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="daa34-124">**short**</span><span class="sxs-lookup"><span data-stu-id="daa34-124">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="daa34-125">**con segno**</span><span class="sxs-lookup"><span data-stu-id="daa34-125">**signed**</span></span>](signed.md)
</dt> <dt>

[<span data-ttu-id="daa34-126">**piccolo**</span><span class="sxs-lookup"><span data-stu-id="daa34-126">**small**</span></span>](small.md)
</dt> <dt>

[<span data-ttu-id="daa34-127">**WCHAR \_ t**</span><span class="sxs-lookup"><span data-stu-id="daa34-127">**wchar\_t**</span></span>](wchar-t.md)
</dt> </dl>

 

 




