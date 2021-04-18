---
title: attributo byte
description: La parola chiave byte specifica un elemento di dati a 8 bit.
ms.assetid: d6401e05-5498-4d66-8f70-2c794ed26527
keywords:
- attributo byte MIDL
topic_type:
- apiref
api_name:
- byte
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 347b1f22f06431c5490d4fdac15cdb22b25da69e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299212"
---
# <a name="byte-attribute"></a><span data-ttu-id="13c48-104">attributo byte</span><span class="sxs-lookup"><span data-stu-id="13c48-104">byte attribute</span></span>

<span data-ttu-id="13c48-105">La parola chiave **byte** specifica un elemento di dati a 8 bit.</span><span class="sxs-lookup"><span data-stu-id="13c48-105">The **byte** keyword specifies an 8-bit data item.</span></span>

``` syntax
byte identifier-name;
```

## <a name="parameters"></a><span data-ttu-id="13c48-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="13c48-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13c48-107">*nome identificatore*</span><span class="sxs-lookup"><span data-stu-id="13c48-107">*identifier-name*</span></span> 
</dt> <dd>

<span data-ttu-id="13c48-108">Specifica un identificatore MIDL valido.</span><span class="sxs-lookup"><span data-stu-id="13c48-108">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="13c48-109">Gli identificatori MIDL validi sono costituiti da un massimo di 31 caratteri alfanumerici e/o di sottolineatura e devono iniziare con un carattere alfabetico o di sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="13c48-109">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="13c48-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="13c48-110">Remarks</span></span>

<span data-ttu-id="13c48-111">Un elemento dati **byte** non subisce alcuna conversione per la trasmissione in rete come tipo [**char**](char-idl.md) .</span><span class="sxs-lookup"><span data-stu-id="13c48-111">A **byte** data item does not undergo any conversion for transmission on the network as a [**char**](char-idl.md) type might.</span></span>

<span data-ttu-id="13c48-112">Il tipo di **byte** è uno dei tipi di base del linguaggio di definizione dell'interfaccia (IDL).</span><span class="sxs-lookup"><span data-stu-id="13c48-112">The **byte** type is one of the base types of the interface definition language (IDL).</span></span> <span data-ttu-id="13c48-113">Il tipo di **byte** può essere visualizzato come identificatore di tipo nelle dichiarazioni [**const**](const.md) , nelle dichiarazioni [**typedef**](typedef.md) , nelle dichiarazioni generali e nei dichiaratori di funzione (come identificatore del tipo restituito dalla funzione e come identificatore del tipo di parametro).</span><span class="sxs-lookup"><span data-stu-id="13c48-113">The **byte** type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function-return-type specifier and as a parameter-type specifier).</span></span> <span data-ttu-id="13c48-114">Per il contesto in cui vengono visualizzati gli identificatori di tipo, vedere [file di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="13c48-114">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="13c48-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="13c48-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13c48-116">Tipi di base MIDL</span><span class="sxs-lookup"><span data-stu-id="13c48-116">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="13c48-117">**char**</span><span class="sxs-lookup"><span data-stu-id="13c48-117">**char**</span></span>](char-idl.md)
</dt> <dt>

[<span data-ttu-id="13c48-118">**const**</span><span class="sxs-lookup"><span data-stu-id="13c48-118">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="13c48-119">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="13c48-119">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="13c48-120">**typedef**</span><span class="sxs-lookup"><span data-stu-id="13c48-120">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 




