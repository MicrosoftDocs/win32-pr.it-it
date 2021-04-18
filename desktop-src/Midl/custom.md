---
title: attributo personalizzato
description: L'attributo \ custom \ crea un attributo definito dall'utente.
ms.assetid: 63c93eca-c9c1-4c14-9f46-aa78b01d9ff8
keywords:
- MIDL attributo personalizzato
topic_type:
- apiref
api_name:
- custom
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef7c4210091cc028d7724cb40724f22a91eb7d74
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299602"
---
# <a name="custom-attribute"></a><span data-ttu-id="c79bc-104">attributo personalizzato</span><span class="sxs-lookup"><span data-stu-id="c79bc-104">custom attribute</span></span>

<span data-ttu-id="c79bc-105">L'attributo **\[ Custom \]** crea un attributo definito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="c79bc-105">The **\[custom\]** attribute creates a user-defined attribute.</span></span>

``` syntax
[custom(attribute-id, attribute-value),attribute-list] element-type element-name
```

## <a name="parameters"></a><span data-ttu-id="c79bc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c79bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c79bc-107">*ID attributo*</span><span class="sxs-lookup"><span data-stu-id="c79bc-107">*attribute-id*</span></span> 
</dt> <dd>

<span data-ttu-id="c79bc-108">GUID per l'attributo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="c79bc-108">The GUID for the custom attribute.</span></span>

</dd> <dt>

<span data-ttu-id="c79bc-109">*valore attributo*</span><span class="sxs-lookup"><span data-stu-id="c79bc-109">*attribute-value*</span></span> 
</dt> <dd>

<span data-ttu-id="c79bc-110">Valore che l'attributo include.</span><span class="sxs-lookup"><span data-stu-id="c79bc-110">The value that the attribute holds.</span></span> <span data-ttu-id="c79bc-111">Il valore deve essere un valore che può essere inserito in un tipo VARIANT.</span><span class="sxs-lookup"><span data-stu-id="c79bc-111">The value must be one that can be put into a VARIANT type.</span></span>

</dd> <dt>

<span data-ttu-id="c79bc-112">*elenco attributi*</span><span class="sxs-lookup"><span data-stu-id="c79bc-112">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="c79bc-113">Altri attributi, ad esempio **\[** [**UUID**](uuid.md) **\]** e **\[** [**helpstring**](helpstring.md) **\]** , che si applicano a questo elemento.</span><span class="sxs-lookup"><span data-stu-id="c79bc-113">Other attributes, such as **\[**[**uuid**](uuid.md)**\]** and **\[**[**helpstring**](helpstring.md)**\]**, that apply to this element.</span></span>

</dd> <dt>

<span data-ttu-id="c79bc-114">*tipo di elemento*</span><span class="sxs-lookup"><span data-stu-id="c79bc-114">*element-type*</span></span> 
</dt> <dd>

<span data-ttu-id="c79bc-115">Tipo di elemento a cui viene applicato l'attributo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="c79bc-115">The type of element to which the custom attribute applies.</span></span> <span data-ttu-id="c79bc-116">Può trattarsi di un'istruzione di libreria, informazioni sul tipo, una variabile, una funzione o un parametro.</span><span class="sxs-lookup"><span data-stu-id="c79bc-116">This can be a library statement, type information, a variable, a function, or a parameter.</span></span> <span data-ttu-id="c79bc-117">Non è possibile usare un attributo personalizzato per un membro di una coclasse.</span><span class="sxs-lookup"><span data-stu-id="c79bc-117">You cannot use a custom attribute on a member of a coclass.</span></span>

</dd> <dt>

<span data-ttu-id="c79bc-118">*Nome elemento*</span><span class="sxs-lookup"><span data-stu-id="c79bc-118">*element-name*</span></span> 
</dt> <dd>

<span data-ttu-id="c79bc-119">Nome dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="c79bc-119">The name of the element.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c79bc-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="c79bc-120">Remarks</span></span>

<span data-ttu-id="c79bc-121">Usare l'attributo personalizzato per definire un attributo **\[ personalizzato \]** .</span><span class="sxs-lookup"><span data-stu-id="c79bc-121">Use the **\[custom\]** attribute to define your own attribute.</span></span> <span data-ttu-id="c79bc-122">Ad esempio, è possibile creare un attributo con valori di stringa che fornisce il ProgID per una classe.</span><span class="sxs-lookup"><span data-stu-id="c79bc-122">For example, you might create a string-valued attribute that gives the ProgID for a class.</span></span>

<span data-ttu-id="c79bc-123">Per recuperare un valore di attributo personalizzato, chiamare uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="c79bc-123">To retrieve a custom attribute value call one of the following:</span></span>

-   <span data-ttu-id="c79bc-124">ITypeLib2:: GetCustData (rguid, pvarVal)</span><span class="sxs-lookup"><span data-stu-id="c79bc-124">ITypeLib2::GetCustData(rguid, pvarVal)</span></span>
-   <span data-ttu-id="c79bc-125">ITypeInfo2:: GetCustData (rguid, pvarVal)</span><span class="sxs-lookup"><span data-stu-id="c79bc-125">ITypeInfo2::GetCustData(rguid, pvarVal)</span></span>
-   <span data-ttu-id="c79bc-126">ITypeInfo2:: GetFuncCustData (index, rguid, pvarVal)</span><span class="sxs-lookup"><span data-stu-id="c79bc-126">ITypeInfo2::GetFuncCustData(index, rguid, pvarVal)</span></span>
-   <span data-ttu-id="c79bc-127">ITypeInfo2:: GetVarCustData (index, rguid, pVarVal)</span><span class="sxs-lookup"><span data-stu-id="c79bc-127">ITypeInfo2::GetVarCustData(index, rguid, pvarval)</span></span>
-   <span data-ttu-id="c79bc-128">ITypeInfo2:: GetParamCustData (indexFunc, indexParam, rguid, pvarVal)</span><span class="sxs-lookup"><span data-stu-id="c79bc-128">ITypeInfo2::GetParamCustData(indexFunc, indexParam, rguid, pvarVal)</span></span>

## <a name="see-also"></a><span data-ttu-id="c79bc-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c79bc-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c79bc-130">Generazione di una libreria dei tipi con MIDL</span><span class="sxs-lookup"><span data-stu-id="c79bc-130">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="c79bc-131">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="c79bc-131">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="c79bc-132">**libreria**</span><span class="sxs-lookup"><span data-stu-id="c79bc-132">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="c79bc-133">Esempio di file di FAD</span><span class="sxs-lookup"><span data-stu-id="c79bc-133">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="c79bc-134">Sintassi del file di FAD</span><span class="sxs-lookup"><span data-stu-id="c79bc-134">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="c79bc-135">**uuid**</span><span class="sxs-lookup"><span data-stu-id="c79bc-135">**uuid**</span></span>](uuid.md)
</dt> </dl>

 

 