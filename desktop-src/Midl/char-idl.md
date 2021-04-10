---
title: attributo char
description: La parola chiave char specifica un elemento di dati a 8 bit.
ms.assetid: 3c9ba8bb-5aea-4166-acf6-b251377e5384
keywords:
- attributo char MIDL
topic_type:
- apiref
api_name:
- char
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1eab719f6f8ea6e21ccc5b389b12a66b617d5773
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857593"
---
# <a name="char-attribute"></a><span data-ttu-id="56134-104">attributo char</span><span class="sxs-lookup"><span data-stu-id="56134-104">char attribute</span></span>

<span data-ttu-id="56134-105">La parola chiave **char** specifica un elemento di dati a 8 bit.</span><span class="sxs-lookup"><span data-stu-id="56134-105">The **char** keyword specifies an 8-bit data item.</span></span>

``` syntax
char identifier-name;
```

## <a name="parameters"></a><span data-ttu-id="56134-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="56134-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56134-107">*nome identificatore*</span><span class="sxs-lookup"><span data-stu-id="56134-107">*identifier-name*</span></span> 
</dt> <dd>

<span data-ttu-id="56134-108">Specifica un identificatore MIDL valido.</span><span class="sxs-lookup"><span data-stu-id="56134-108">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="56134-109">Gli identificatori MIDL validi sono costituiti da un massimo di 31 caratteri alfanumerici e/o di sottolineatura e devono iniziare con un carattere alfabetico o di sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="56134-109">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="56134-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="56134-110">Remarks</span></span>

<span data-ttu-id="56134-111">La parola chiave **char** identifica un elemento di dati con 8 bit.</span><span class="sxs-lookup"><span data-stu-id="56134-111">The keyword **char** identifies a data item that has 8 bits.</span></span> <span data-ttu-id="56134-112">Al compilatore MIDL, un **carattere** è senza segno per impostazione predefinita ed è sinonimo di [](unsigned.md) **carattere** senza segno.</span><span class="sxs-lookup"><span data-stu-id="56134-112">To the MIDL compiler, a **char** is unsigned by default and is synonymous with [**unsigned**](unsigned.md) **char**.</span></span>

<span data-ttu-id="56134-113">In questa versione di Microsoft RPC, le tabelle di conversione dei caratteri che eseguono la conversione tra ASCII e EBCDIC sono compilate nelle librerie di runtime e non possono essere modificate dall'utente.</span><span class="sxs-lookup"><span data-stu-id="56134-113">In this version of Microsoft RPC, the character translation tables that convert between ASCII and EBCDIC are built into the run-time libraries and cannot be changed by the user.</span></span>

<span data-ttu-id="56134-114">Il tipo **char** è uno dei tipi di base del linguaggio di definizione dell'interfaccia (IDL).</span><span class="sxs-lookup"><span data-stu-id="56134-114">The **char** type is one of the base types of the interface definition language (IDL).</span></span> <span data-ttu-id="56134-115">Il tipo **char** può essere visualizzato come identificatore di tipo nelle dichiarazioni [**const**](const.md) , nelle dichiarazioni [**typedef**](typedef.md) , nelle dichiarazioni generali e nei dichiaratori di funzione (come identificatore del tipo restituito dalla funzione e come identificatore del tipo di parametro).</span><span class="sxs-lookup"><span data-stu-id="56134-115">The **char** type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function-return-type specifier and a parameter-type specifier).</span></span> <span data-ttu-id="56134-116">Per il contesto in cui vengono visualizzati gli identificatori di tipo, vedere [file di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="56134-116">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

<span data-ttu-id="56134-117">I compilatori IDL DCE non accettano la parola chiave [**signed**](signed.md) applicata ai tipi **char** .</span><span class="sxs-lookup"><span data-stu-id="56134-117">DCE IDL compilers do not accept the keyword [**signed**](signed.md) applied to **char** types.</span></span> <span data-ttu-id="56134-118">Questa funzionalità non è pertanto disponibile quando si usa l'opzione [**/OSF**](-osf.md) del compilatore MIDL.</span><span class="sxs-lookup"><span data-stu-id="56134-118">Therefore, this feature is not available when you use the MIDL compiler [**/osf**](-osf.md) switch.</span></span>

## <a name="see-also"></a><span data-ttu-id="56134-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="56134-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56134-120">Tipi di base MIDL</span><span class="sxs-lookup"><span data-stu-id="56134-120">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="56134-121">**byte**</span><span class="sxs-lookup"><span data-stu-id="56134-121">**byte**</span></span>](byte.md)
</dt> <dt>

[<span data-ttu-id="56134-122">**/char**</span><span class="sxs-lookup"><span data-stu-id="56134-122">**/char**</span></span>](-char.md)
</dt> <dt>

[<span data-ttu-id="56134-123">**const**</span><span class="sxs-lookup"><span data-stu-id="56134-123">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="56134-124">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="56134-124">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="56134-125">**/osf**</span><span class="sxs-lookup"><span data-stu-id="56134-125">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="56134-126">**con segno**</span><span class="sxs-lookup"><span data-stu-id="56134-126">**signed**</span></span>](signed.md)
</dt> <dt>

[<span data-ttu-id="56134-127">**string**</span><span class="sxs-lookup"><span data-stu-id="56134-127">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="56134-128">**typedef**</span><span class="sxs-lookup"><span data-stu-id="56134-128">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="56134-129">**unsigned**</span><span class="sxs-lookup"><span data-stu-id="56134-129">**unsigned**</span></span>](unsigned.md)
</dt> <dt>

[<span data-ttu-id="56134-130">**WCHAR \_ t**</span><span class="sxs-lookup"><span data-stu-id="56134-130">**wchar\_t**</span></span>](wchar-t.md)
</dt> </dl>

 

 




