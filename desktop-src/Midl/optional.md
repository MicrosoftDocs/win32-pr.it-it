---
title: optional (attributo)
description: L'attributo \ optional \ specifica un parametro facoltativo per una funzione membro.
ms.assetid: 683e5c9e-5b25-4beb-99ce-cfae4fee4ea6
keywords:
- attributo MIDL facoltativo
topic_type:
- apiref
api_name:
- optional
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b446cf2a7a14e5909d2c99d41fd918147d23c6f1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872490"
---
# <a name="optional-attribute"></a><span data-ttu-id="5034e-104">optional (attributo)</span><span class="sxs-lookup"><span data-stu-id="5034e-104">optional attribute</span></span>

<span data-ttu-id="5034e-105">L'attributo **\[ facoltativo \]** specifica un parametro facoltativo per una funzione membro.</span><span class="sxs-lookup"><span data-stu-id="5034e-105">The **\[optional\]** attribute specifies an optional parameter for a member function.</span></span>

``` syntax
return-type function-name([optional [, other-attributes]] parameter-type parameter-name)
```

## <a name="parameters"></a><span data-ttu-id="5034e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5034e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5034e-107">*tipo restituito*</span><span class="sxs-lookup"><span data-stu-id="5034e-107">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="5034e-108">Specifica il tipo restituito della funzione.</span><span class="sxs-lookup"><span data-stu-id="5034e-108">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="5034e-109">*Nome funzione*</span><span class="sxs-lookup"><span data-stu-id="5034e-109">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="5034e-110">Specifica il nome della funzione come definito nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="5034e-110">Specifies the name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="5034e-111">*altri attributi*</span><span class="sxs-lookup"><span data-stu-id="5034e-111">*other-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="5034e-112">Zero o più attributi MIDL facoltativi.</span><span class="sxs-lookup"><span data-stu-id="5034e-112">Zero or more optional MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="5034e-113">*tipo di parametro*</span><span class="sxs-lookup"><span data-stu-id="5034e-113">*parameter-type*</span></span> 
</dt> <dd>

<span data-ttu-id="5034e-114">Tipo di dati del parametro facoltativo.</span><span class="sxs-lookup"><span data-stu-id="5034e-114">The data type of the optional parameter.</span></span>

</dd> <dt>

<span data-ttu-id="5034e-115">*Nome parametro*</span><span class="sxs-lookup"><span data-stu-id="5034e-115">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="5034e-116">Specifica il nome del parametro facoltativo.</span><span class="sxs-lookup"><span data-stu-id="5034e-116">Specifies the name of the optional parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5034e-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="5034e-117">Remarks</span></span>

<span data-ttu-id="5034e-118">L'attributo **\[ facoltativo \]** è valido solo se il parametro è di tipo **Variant** o **Variant** \* .</span><span class="sxs-lookup"><span data-stu-id="5034e-118">The **\[optional\]** attribute is valid only if the parameter is of type **VARIANT** or **VARIANT** Â \*.</span></span>

<span data-ttu-id="5034e-119">Il compilatore MIDL accetta l'ordinamento dei parametri seguente (da sinistra a destra):</span><span class="sxs-lookup"><span data-stu-id="5034e-119">The MIDL compiler accepts the following parameter ordering (from left-to-right):</span></span>

1.  <span data-ttu-id="5034e-120">Parametri obbligatori (parametri che non dispongono degli **\[** attributi [**DefaultValue**](defaultvalue.md) **\]** o **\[ Optional \]** ),</span><span class="sxs-lookup"><span data-stu-id="5034e-120">Required parameters (parameters that do not have the **\[**[**defaultvalue**](defaultvalue.md)**\]** or **\[optional\]** attributes),</span></span>
2.  <span data-ttu-id="5034e-121">Parametri facoltativi con o senza l' **\[** [](defaultvalue.md) **\]** attributo DefaultValue,</span><span class="sxs-lookup"><span data-stu-id="5034e-121">Optional parameters with or without the **\[**[**defaultvalue**](defaultvalue.md)**\]** attribute,</span></span>
3.  <span data-ttu-id="5034e-122">Parametri con l'attributo **\[ facoltativo \]** e senza l' **\[** attributo [**DefaultValue**](defaultvalue.md) **\]** ,</span><span class="sxs-lookup"><span data-stu-id="5034e-122">Parameters with the **\[optional\]** attribute and without the **\[**[**defaultvalue**](defaultvalue.md)**\]** attribute,</span></span>
4.  <span data-ttu-id="5034e-123">**\[** parametro [**LCID**](lcid.md) **\]** , se presente,</span><span class="sxs-lookup"><span data-stu-id="5034e-123">**\[**[**lcid**](lcid.md)**\]** parameter, if any,</span></span>
5.  <span data-ttu-id="5034e-124">**\[**[**retval**](retval.md) **\]** parametro</span><span class="sxs-lookup"><span data-stu-id="5034e-124">**\[**[**retval**](retval.md)**\]** parameter</span></span>

<span data-ttu-id="5034e-125">Non è possibile applicare l'attributo **\[ facoltativo \]** a un parametro che include anche gli **\[** attributi [**LCID**](lcid.md) **\]** o **\[** [**retval**](retval.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="5034e-125">You cannot apply the **\[optional\]** attribute to a parameter that also has the **\[**[**lcid**](lcid.md)**\]** or **\[**[**retval**](retval.md)**\]** attributes.</span></span>

## <a name="examples"></a><span data-ttu-id="5034e-126">Esempi</span><span class="sxs-lookup"><span data-stu-id="5034e-126">Examples</span></span>

``` syntax
HRESULT MyFunc([in, optional] VARIANT Param1, 
               [out, optional] VARIANT Param2)
```

## <a name="see-also"></a><span data-ttu-id="5034e-127">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="5034e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5034e-128">**DefaultValue**</span><span class="sxs-lookup"><span data-stu-id="5034e-128">**defaultvalue**</span></span>](defaultvalue.md)
</dt> <dt>

[<span data-ttu-id="5034e-129">Generazione di una libreria dei tipi con MIDL</span><span class="sxs-lookup"><span data-stu-id="5034e-129">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="5034e-130">**LCID**</span><span class="sxs-lookup"><span data-stu-id="5034e-130">**lcid**</span></span>](lcid.md)
</dt> <dt>

[<span data-ttu-id="5034e-131">Esempio di file di FAD</span><span class="sxs-lookup"><span data-stu-id="5034e-131">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="5034e-132">Sintassi del file di FAD</span><span class="sxs-lookup"><span data-stu-id="5034e-132">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="5034e-133">**retval**</span><span class="sxs-lookup"><span data-stu-id="5034e-133">**retval**</span></span>](retval.md)
</dt> </dl>

 

 