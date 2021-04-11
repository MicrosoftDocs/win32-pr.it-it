---
title: propputref (attributo)
description: L'attributo \ propputref \ specifica una funzione di impostazione di proprietà che usa un riferimento invece di un valore.
ms.assetid: 84f1cd08-3c42-4a6d-bb1d-0bfd3f4c33f2
keywords:
- attributo MIDL di propputref
topic_type:
- apiref
api_name:
- propputref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ead5ccf7f9dc6a59580b7c3e3576f3c7503ccafc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103956373"
---
# <a name="propputref-attribute"></a><span data-ttu-id="3d008-104">propputref (attributo)</span><span class="sxs-lookup"><span data-stu-id="3d008-104">propputref attribute</span></span>

<span data-ttu-id="3d008-105">L'attributo **\[ propputref \]** specifica una funzione di impostazione di proprietà che usa un riferimento invece di un valore.</span><span class="sxs-lookup"><span data-stu-id="3d008-105">The **\[propputref\]** attribute specifies a property-setting function that uses a reference instead of a value.</span></span>

``` syntax
[propputref [,optional-property-attributes]] return-type function-name( parameters);
```

## <a name="parameters"></a><span data-ttu-id="3d008-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3d008-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d008-107">*facoltativo-Property-Attributes*</span><span class="sxs-lookup"><span data-stu-id="3d008-107">*optional-property-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="3d008-108">Zero o più attributi della proprietà.</span><span class="sxs-lookup"><span data-stu-id="3d008-108">Zero or more property attributes.</span></span>

</dd> <dt>

<span data-ttu-id="3d008-109">*tipo restituito*</span><span class="sxs-lookup"><span data-stu-id="3d008-109">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="3d008-110">Tipo di dati restituiti dalla procedura remota.</span><span class="sxs-lookup"><span data-stu-id="3d008-110">The type of the data returned by the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="3d008-111">*Nome funzione*</span><span class="sxs-lookup"><span data-stu-id="3d008-111">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="3d008-112">Nome della procedura remota.</span><span class="sxs-lookup"><span data-stu-id="3d008-112">The name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="3d008-113">*parameters*</span><span class="sxs-lookup"><span data-stu-id="3d008-113">*parameters*</span></span> 
</dt> <dd>

<span data-ttu-id="3d008-114">Zero o più parametri per la procedura remota.</span><span class="sxs-lookup"><span data-stu-id="3d008-114">Zero or more parameters to the remote procedure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3d008-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="3d008-115">Remarks</span></span>

<span data-ttu-id="3d008-116">Una funzione con l'attributo **\[ propputref \]** deve avere anche l'ultimo parametro, ovvero un puntatore **\[** [**con l'attributo in**](in.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="3d008-116">A function that has the **\[propputref\]** attribute must also have, as its last parameter, a pointer that has the **\[**[**in**](in.md)**\]** attribute.</span></span>

<span data-ttu-id="3d008-117">La proprietà deve avere lo stesso nome della funzione.</span><span class="sxs-lookup"><span data-stu-id="3d008-117">The property must have the same name as the function.</span></span> <span data-ttu-id="3d008-118">**\[** [](propget.md) **\]** **\[** [](propput.md) **\]** Per una funzione è possibile specificare al massimo uno degli attributi propget, propput e **\[ propputref \]** .</span><span class="sxs-lookup"><span data-stu-id="3d008-118">At most, one of **\[**[**propget**](propget.md)**\]**, **\[**[**propput**](propput.md)**\]** and **\[propputref\]** attributes can be specified for a function.</span></span>

### <a name="flags"></a><span data-ttu-id="3d008-119">Flags</span><span class="sxs-lookup"><span data-stu-id="3d008-119">Flags</span></span>

<span data-ttu-id="3d008-120">RICHIAMA \_ PROPERTYPUTREF</span><span class="sxs-lookup"><span data-stu-id="3d008-120">INVOKE\_PROPERTYPUTREF</span></span>

## <a name="examples"></a><span data-ttu-id="3d008-121">Esempi</span><span class="sxs-lookup"><span data-stu-id="3d008-121">Examples</span></span>

``` syntax
interface InMyFace : IDispatch 
{
    [propget, 
     helpstring("A meaningful comment."), 
     id(1)] HRESULT Method2([out, retval] YourInterface** ReturnVal); 
    [propputref, 
     helpstring("Another meaningful comment."), 
     id(1)] HRESULT Method2([in] YourPoint* Point);
}
```

## <a name="see-also"></a><span data-ttu-id="3d008-122">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="3d008-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d008-123">Generazione di una libreria dei tipi con MIDL</span><span class="sxs-lookup"><span data-stu-id="3d008-123">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="3d008-124">**in**</span><span class="sxs-lookup"><span data-stu-id="3d008-124">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="3d008-125">Esempio di file di FAD</span><span class="sxs-lookup"><span data-stu-id="3d008-125">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="3d008-126">Sintassi del file di FAD</span><span class="sxs-lookup"><span data-stu-id="3d008-126">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="3d008-127">**propget**</span><span class="sxs-lookup"><span data-stu-id="3d008-127">**propget**</span></span>](propget.md)
</dt> <dt>

[<span data-ttu-id="3d008-128">**propput**</span><span class="sxs-lookup"><span data-stu-id="3d008-128">**propput**</span></span>](propput.md)
</dt> <dt>

[<span data-ttu-id="3d008-129">**TYPEFLAGS**</span><span class="sxs-lookup"><span data-stu-id="3d008-129">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 