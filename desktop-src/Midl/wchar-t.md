---
title: attributo wchar_t
description: La \_ parola chiave wchar t designa un tipo di carattere wide.
ms.assetid: e21b2587-909a-4e2b-8c6d-6cc570bf509f
keywords:
- attributo wchar_t MIDL
topic_type:
- apiref
api_name:
- wchar_t
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0be9af276a8f87fe5ee7a4dfeb499b864de92f4
ms.sourcegitcommit: 686cb805bed0e89573fc68d145809f50c6b0e6d5
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/13/2020
ms.locfileid: "104046400"
---
# <a name="wchar_t-attribute"></a><span data-ttu-id="a2515-104">WCHAR \_ t (attributo)</span><span class="sxs-lookup"><span data-stu-id="a2515-104">wchar\_t attribute</span></span>

<span data-ttu-id="a2515-105">La parola chiave **WCHAR \_ t** designa un tipo di carattere wide.</span><span class="sxs-lookup"><span data-stu-id="a2515-105">The **wchar\_t** keyword designates a wide-character type.</span></span>

``` syntax
wchar_t identifier-name;
```

## <a name="parameters"></a><span data-ttu-id="a2515-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a2515-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2515-107">*nome identificatore*</span><span class="sxs-lookup"><span data-stu-id="a2515-107">*identifier-name*</span></span> 
</dt> <dd>

<span data-ttu-id="a2515-108">Specifica un identificatore MIDL valido.</span><span class="sxs-lookup"><span data-stu-id="a2515-108">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="a2515-109">Gli identificatori MIDL validi sono costituiti da un massimo di 31 caratteri alfanumerici e/o di sottolineatura e devono iniziare con un carattere alfabetico o di sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="a2515-109">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a2515-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="a2515-110">Remarks</span></span>

<span data-ttu-id="a2515-111">Il tipo **WCHAR \_ t** viene definito da MIDL come oggetto dati [**short**](short.md) [**senza segno**](unsigned.md) (a 16 bit).</span><span class="sxs-lookup"><span data-stu-id="a2515-111">The **wchar\_t** type is defined by MIDL as an [**unsigned**](unsigned.md) [**short**](short.md) (16-bit) data object.</span></span>

<span data-ttu-id="a2515-112">Il compilatore MIDL consente la ridefinizione di **WCHAR \_ t**, ma solo se è coerente con la definizione precedente.</span><span class="sxs-lookup"><span data-stu-id="a2515-112">The MIDL compiler allows redefinition of **wchar\_t**, but only if it is consistent with the preceding definition.</span></span>

<span data-ttu-id="a2515-113">Il tipo di carattere wide è uno dei tipi predefiniti di MIDL.</span><span class="sxs-lookup"><span data-stu-id="a2515-113">The wide-character type is one of the predefined types of MIDL.</span></span> <span data-ttu-id="a2515-114">Il tipo di carattere wide può essere visualizzato come identificatore di tipo nelle dichiarazioni [**const**](const.md) , nelle dichiarazioni [**typedef**](typedef.md) , nelle dichiarazioni generali e nei dichiaratori di funzione (come identificatore del tipo restituito della funzione e come identificatore del tipo di parametro).</span><span class="sxs-lookup"><span data-stu-id="a2515-114">The wide-character type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function return type specifier and as a parameter-type specifier).</span></span> <span data-ttu-id="a2515-115">Per il contesto in cui vengono visualizzati gli identificatori di tipo, vedere [file di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="a2515-115">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

<span data-ttu-id="a2515-116">L'attributo **\[ stringa \]** può essere applicato a un puntatore o a una matrice di tipo **WCHAR \_ t**.</span><span class="sxs-lookup"><span data-stu-id="a2515-116">The **\[string\]** attribute can be applied to a pointer or array of type **wchar\_t**.</span></span>

<span data-ttu-id="a2515-117">Usare il carattere **L** prima di un carattere o una costante di stringa per definire la costante del tipo di carattere wide.</span><span class="sxs-lookup"><span data-stu-id="a2515-117">Use the **L** character before a character or a string constant to designate the wide character type constant.</span></span>

## <a name="see-also"></a><span data-ttu-id="a2515-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a2515-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2515-119">Tipi di base MIDL</span><span class="sxs-lookup"><span data-stu-id="a2515-119">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="a2515-120">**char**</span><span class="sxs-lookup"><span data-stu-id="a2515-120">**char**</span></span>](char-idl.md)
</dt> <dt>

[<span data-ttu-id="a2515-121">**const**</span><span class="sxs-lookup"><span data-stu-id="a2515-121">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="a2515-122">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="a2515-122">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="a2515-123">**short**</span><span class="sxs-lookup"><span data-stu-id="a2515-123">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="a2515-124">**typedef**</span><span class="sxs-lookup"><span data-stu-id="a2515-124">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="a2515-125">**unsigned**</span><span class="sxs-lookup"><span data-stu-id="a2515-125">**unsigned**</span></span>](unsigned.md)
</dt> </dl>

 

 




