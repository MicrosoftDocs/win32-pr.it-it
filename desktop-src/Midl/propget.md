---
title: propget (attributo)
description: L'attributo \ propget \ specifica una funzione di accesso alla proprietà. La proprietà deve avere lo stesso nome della funzione.
ms.assetid: 0b76ece3-e19b-4c80-883c-ff414bc2e435
keywords:
- attributo MIDL di propget
topic_type:
- apiref
api_name:
- propget
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6337409e021670c282400d38b97543687fa81c2a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046588"
---
# <a name="propget-attribute"></a><span data-ttu-id="f6cb2-105">propget (attributo)</span><span class="sxs-lookup"><span data-stu-id="f6cb2-105">propget attribute</span></span>

<span data-ttu-id="f6cb2-106">L'attributo **\[ propget \]** specifica una funzione di accesso alla proprietà.</span><span class="sxs-lookup"><span data-stu-id="f6cb2-106">The **\[propget\]** attribute specifies a property accessor function.</span></span> <span data-ttu-id="f6cb2-107">La proprietà deve avere lo stesso nome della funzione.</span><span class="sxs-lookup"><span data-stu-id="f6cb2-107">The property must have the same name as the function.</span></span>

``` syntax
[propget [,optional-property-attributes]] return-type function-name( parameters);
```

## <a name="parameters"></a><span data-ttu-id="f6cb2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f6cb2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6cb2-109">*facoltativo-Property-Attributes*</span><span class="sxs-lookup"><span data-stu-id="f6cb2-109">*optional-property-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="f6cb2-110">Zero o più attributi della proprietà.</span><span class="sxs-lookup"><span data-stu-id="f6cb2-110">Zero or more property attributes.</span></span>

</dd> <dt>

<span data-ttu-id="f6cb2-111">*tipo restituito*</span><span class="sxs-lookup"><span data-stu-id="f6cb2-111">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="f6cb2-112">Tipo di dati restituiti dalla procedura remota.</span><span class="sxs-lookup"><span data-stu-id="f6cb2-112">The type of the data returned by the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="f6cb2-113">*Nome funzione*</span><span class="sxs-lookup"><span data-stu-id="f6cb2-113">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="f6cb2-114">Nome della procedura remota.</span><span class="sxs-lookup"><span data-stu-id="f6cb2-114">The name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="f6cb2-115">*parameters*</span><span class="sxs-lookup"><span data-stu-id="f6cb2-115">*parameters*</span></span> 
</dt> <dd>

<span data-ttu-id="f6cb2-116">Zero o più parametri per la procedura remota.</span><span class="sxs-lookup"><span data-stu-id="f6cb2-116">Zero or more parameters to the remote procedure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f6cb2-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="f6cb2-117">Remarks</span></span>

<span data-ttu-id="f6cb2-118">Una funzione con l'attributo propget deve avere anche l'ultimo parametro, un tipo di puntatore con gli **\[** attributi [**out**](out-idl.md) **\]** e **\[** [**retval**](retval.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="f6cb2-118">A function that has the propget attribute should also have, as its last parameter, a pointer type with the **\[**[**out**](out-idl.md)**\]** and **\[**[**retval**](retval.md)**\]** attributes.</span></span> <span data-ttu-id="f6cb2-119">Se l'ultimo parametro non dispone degli \[ attributi out, retval \] , il valore restituito della funzione viene considerato come un \[ parametro out, retval \] .</span><span class="sxs-lookup"><span data-stu-id="f6cb2-119">If the last parameter does not have the \[out, retval\] attributes, the return value of the function is treated as an \[out, retval\] parameter.</span></span> <span data-ttu-id="f6cb2-120">Ad esempio, una funzione con il prototipo</span><span class="sxs-lookup"><span data-stu-id="f6cb2-120">For example, a function with the prototype</span></span>

``` syntax
[propget] short MyFunction([in] long aLongValue);
```

<span data-ttu-id="f6cb2-121">viene considerato come</span><span class="sxs-lookup"><span data-stu-id="f6cb2-121">is treated as</span></span>

``` syntax
[propget] HRESULT MyFunction([in] long aLongValue, [out,retval] short *outValue);
```

<span data-ttu-id="f6cb2-122">**\[ \]** **\[** [](propput.md) **\]** **\[** [](propputref.md) **\]** Per una funzione è possibile specificare al massimo uno dei propget, propput e propputref.</span><span class="sxs-lookup"><span data-stu-id="f6cb2-122">At most, one of **\[propget\]**, **\[**[**propput**](propput.md)**\]**, and **\[**[**propputref**](propputref.md)**\]** can be specified for a function.</span></span>

<span data-ttu-id="f6cb2-123">Se l' **\[** attributo [**LCID**](lcid.md) **\]** viene usato nell'elenco di parametri di una funzione che contiene un parametro con l' **\[** [](propput.md) **\]** attributo propput, il parametro **\[ LCID \]** deve essere il secondo all'ultimo.</span><span class="sxs-lookup"><span data-stu-id="f6cb2-123">If the **\[**[**lcid**](lcid.md)**\]** attribute is used in the parameter list of a function that contains a parameter with the **\[**[**propput**](propput.md)**\]** attribute, the **\[lcid\]** parameter must be second to the last.</span></span>

### <a name="flags"></a><span data-ttu-id="f6cb2-124">Flags</span><span class="sxs-lookup"><span data-stu-id="f6cb2-124">Flags</span></span>

<span data-ttu-id="f6cb2-125">RICHIAMA \_ PropertyGet (</span><span class="sxs-lookup"><span data-stu-id="f6cb2-125">INVOKE\_PROPERTYGET</span></span>

## <a name="examples"></a><span data-ttu-id="f6cb2-126">Esempi</span><span class="sxs-lookup"><span data-stu-id="f6cb2-126">Examples</span></span>

``` syntax
interface MyInterface : IDispatch                         
{                
    [propget, 
     helpstring("A meaningful comment.")] HRESULT Method1(
         [out, retval] int* ReturnVal); 

    [propput, 
     helpstring("Another meaningful comment.")] HRESULT Method1(
         [in] int Value);
        
    [propget, 
     helpstring("A meaningful comment."), id(1)] HRESULT Method2(
         [out, retval] YourInterface** ReturnVal); 

    [propputref, 
     helpstring("Another meaningful comment."), 
     id(1)] HRESULT Method2([in] YourPoint* Point);
}                 
```

## <a name="see-also"></a><span data-ttu-id="f6cb2-127">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="f6cb2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6cb2-128">Generazione di una libreria dei tipi con MIDL</span><span class="sxs-lookup"><span data-stu-id="f6cb2-128">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="f6cb2-129">Esempio di file di FAD</span><span class="sxs-lookup"><span data-stu-id="f6cb2-129">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="f6cb2-130">Sintassi del file di FAD</span><span class="sxs-lookup"><span data-stu-id="f6cb2-130">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="f6cb2-131">**out**</span><span class="sxs-lookup"><span data-stu-id="f6cb2-131">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="f6cb2-132">**retval**</span><span class="sxs-lookup"><span data-stu-id="f6cb2-132">**retval**</span></span>](retval.md)
</dt> <dt>

[<span data-ttu-id="f6cb2-133">**propput**</span><span class="sxs-lookup"><span data-stu-id="f6cb2-133">**propput**</span></span>](propput.md)
</dt> <dt>

[<span data-ttu-id="f6cb2-134">**propputref**</span><span class="sxs-lookup"><span data-stu-id="f6cb2-134">**propputref**</span></span>](propputref.md)
</dt> <dt>

[<span data-ttu-id="f6cb2-135">**TYPEFLAGS**</span><span class="sxs-lookup"><span data-stu-id="f6cb2-135">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 