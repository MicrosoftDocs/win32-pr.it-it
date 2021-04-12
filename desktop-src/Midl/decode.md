---
title: Decode (attributo)
description: L'attributo \ Decode \ ACF specifica che una routine o un tipo necessita del supporto di deserializzazione.
ms.assetid: 78cd855f-6731-4ef8-9097-e8da5a9b3bdc
keywords:
- Decode attribute MIDL
topic_type:
- apiref
api_name:
- decode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dca24b3a601b9fcafd8d78a0194b6b986813f38c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337167"
---
# <a name="decode-attribute"></a><span data-ttu-id="ba4c1-104">Decode (attributo)</span><span class="sxs-lookup"><span data-stu-id="ba4c1-104">decode attribute</span></span>

<span data-ttu-id="ba4c1-105">L'attributo **\[ Decode \]** ACF specifica che una routine o un tipo necessita del supporto di deserializzazione.</span><span class="sxs-lookup"><span data-stu-id="ba4c1-105">The **\[decode\]** ACF attribute specifies that a procedure or a type needs de-serialization support.</span></span>

``` syntax
[ 
    decode 
    [ , interface-attribute-list] 
] 
interface interface-name
{
    interface-definition
}

[ decode [ , op-attribute-list] ] proc-name(...);

typedef [decode [ , type-attribute-list] ] type-name;
```

## <a name="parameters"></a><span data-ttu-id="ba4c1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ba4c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba4c1-107">*Interface-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="ba4c1-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="ba4c1-108">Specifica altri attributi che si applicano all'interfaccia nel suo complesso.</span><span class="sxs-lookup"><span data-stu-id="ba4c1-108">Specifies other attributes that apply to the interface as a whole.</span></span>

</dd> <dt>

<span data-ttu-id="ba4c1-109">*Nome interfaccia*</span><span class="sxs-lookup"><span data-stu-id="ba4c1-109">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="ba4c1-110">Specifica il nome dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="ba4c1-110">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="ba4c1-111">*interfaccia-definizione*</span><span class="sxs-lookup"><span data-stu-id="ba4c1-111">*interface-definition*</span></span> 
</dt> <dd>

<span data-ttu-id="ba4c1-112">Specifica le istruzioni IDL che formano la definizione dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="ba4c1-112">Specifies IDL statements which form the definition of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="ba4c1-113">*op-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="ba4c1-113">*op-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="ba4c1-114">Specifica altri attributi operativi che si applicano alla procedura, ad esempio **\[** [**Encode**](encode.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="ba4c1-114">Specifies other operational attributes that apply to the procedure such as **\[**[**encode**](encode.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="ba4c1-115">*proc-name*</span><span class="sxs-lookup"><span data-stu-id="ba4c1-115">*proc-name*</span></span> 
</dt> <dd>

<span data-ttu-id="ba4c1-116">Specifica il nome della stored procedure.</span><span class="sxs-lookup"><span data-stu-id="ba4c1-116">Specifies the name of the procedure.</span></span>

</dd> <dt>

<span data-ttu-id="ba4c1-117">*tipo-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="ba4c1-117">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="ba4c1-118">Specifica altri attributi, ad esempio **\[** [**Encode**](encode.md) **\]** e **\[** [**allocate**](allocate.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="ba4c1-118">Specifies other attributes such as **\[**[**encode**](encode.md)**\]** and **\[**[**allocate**](allocate.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="ba4c1-119">*Nome-tipo*</span><span class="sxs-lookup"><span data-stu-id="ba4c1-119">*type-name*</span></span> 
</dt> <dd>

<span data-ttu-id="ba4c1-120">Specifica un tipo definito nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="ba4c1-120">Specifies a type defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ba4c1-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="ba4c1-121">Remarks</span></span>

<span data-ttu-id="ba4c1-122">L'attributo **\[ Decode \]** induce il compilatore MIDL a generare codice che può essere utilizzato da un'applicazione per recuperare dati serializzati da un buffer.</span><span class="sxs-lookup"><span data-stu-id="ba4c1-122">The **\[decode\]** attribute causes the MIDL compiler to generate code that an application can use to retrieve serialized data from a buffer.</span></span> <span data-ttu-id="ba4c1-123">L' **\[** [](encode.md) **\]** attributo Encode fornisce supporto per la serializzazione, che genera il codice per serializzare i dati in un buffer.</span><span class="sxs-lookup"><span data-stu-id="ba4c1-123">The **\[**[**encode**](encode.md)**\]** attribute provides serialization support, generating the code to serialize data into a buffer.</span></span>

<span data-ttu-id="ba4c1-124">Utilizzare gli **\[** attributi [**Encode**](encode.md) **\]** e **\[ Decode \]** in un oggetto ACF per generare il codice di serializzazione per le procedure o i tipi definiti nel file IDL di un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="ba4c1-124">Use the **\[**[**encode**](encode.md)**\]** and **\[decode\]** attributes in an ACF to generate serialization code for procedures or types defined in the IDL file of an interface.</span></span> <span data-ttu-id="ba4c1-125">Quando viene usato come attributo di interfaccia, **\[ Decode \]** si applica a tutti i tipi e le procedure definiti nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="ba4c1-125">When used as an interface attribute, **\[decode\]** applies to all types and procedures defined in the IDL file.</span></span> <span data-ttu-id="ba4c1-126">Quando viene usato come attributo di tipo, **\[ Decode \]** si applica solo al tipo specificato.</span><span class="sxs-lookup"><span data-stu-id="ba4c1-126">When used as a type attribute, **\[decode\]** applies only to the specified type.</span></span> <span data-ttu-id="ba4c1-127">Quando viene usato come attributo operativo, **\[ Decode \]** si applica solo a tale procedura.</span><span class="sxs-lookup"><span data-stu-id="ba4c1-127">When used as an operational attribute, **\[decode\]** applies only to that procedure.</span></span>

<span data-ttu-id="ba4c1-128">Per ulteriori informazioni sull'utilizzo di questo supporto della serializzazione, vedere [serializzazione di servizi](/windows/desktop/Rpc/serialization-services) e **\[** [**codifica**](encode.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="ba4c1-128">For more information about using this serialization support, see [Serialization Services](/windows/desktop/Rpc/serialization-services) and **\[**[**encode**](encode.md)**\]**.</span></span>

## <a name="see-also"></a><span data-ttu-id="ba4c1-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ba4c1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba4c1-130">File di configurazione dell'applicazione (ACF)</span><span class="sxs-lookup"><span data-stu-id="ba4c1-130">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="ba4c1-131">**allocare**</span><span class="sxs-lookup"><span data-stu-id="ba4c1-131">**allocate**</span></span>](allocate.md)
</dt> <dt>

[<span data-ttu-id="ba4c1-132">**codificare**</span><span class="sxs-lookup"><span data-stu-id="ba4c1-132">**encode**</span></span>](encode.md)
</dt> </dl>

 

 