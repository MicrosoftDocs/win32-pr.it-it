---
title: attributo helpstring
description: L'attributo \ helpstring \ specifica una stringa di caratteri utilizzata per descrivere l'elemento a cui si applica.
ms.assetid: f05d3fdd-d975-4f0e-8181-07e16288ff48
keywords:
- attributo MIDL di helpstring
topic_type:
- apiref
api_name:
- helpstring
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c58bbe61b10e2f223cf9f662f10d95ca72819b02
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103956386"
---
# <a name="helpstring-attribute"></a><span data-ttu-id="f8eae-104">attributo helpstring</span><span class="sxs-lookup"><span data-stu-id="f8eae-104">helpstring attribute</span></span>

<span data-ttu-id="f8eae-105">L'attributo **\[ helpstring \]** specifica una stringa di caratteri utilizzata per descrivere l'elemento a cui si applica.</span><span class="sxs-lookup"><span data-stu-id="f8eae-105">The **\[helpstring\]** attribute specifies a character string that is used to describe the element to which it applies.</span></span> <span data-ttu-id="f8eae-106">È possibile applicare l'attributo **\[ helpstring \]** alle istruzioni Library, importlib, Interface, dispatch, Module o coclass, i typedef, le proprietà e i metodi.</span><span class="sxs-lookup"><span data-stu-id="f8eae-106">You can apply the **\[helpstring\]** attribute to library, importlib, interface, dispinterface, module, or coclass statements, typedefs, properties, and methods.</span></span>

``` syntax
[
    helpstring(help-text-string)
    [, optional-attribute-list]
] 
element element-name
{
    definition
}

[idl-statement, helpstring(help-text-string)]
```

## <a name="parameters"></a><span data-ttu-id="f8eae-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="f8eae-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8eae-108">*Guida-testo-stringa*</span><span class="sxs-lookup"><span data-stu-id="f8eae-108">*help-text-string*</span></span> 
</dt> <dd>

<span data-ttu-id="f8eae-109">Stringa di caratteri con terminazione zero contenente il testo della guida.</span><span class="sxs-lookup"><span data-stu-id="f8eae-109">A zero-terminated string of characters containing help text.</span></span>

</dd> <dt>

<span data-ttu-id="f8eae-110">*facoltativo-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="f8eae-110">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="f8eae-111">Zero o più istruzioni di attributo MIDL.</span><span class="sxs-lookup"><span data-stu-id="f8eae-111">Zero or more MIDL attribute statements.</span></span>

</dd> <dt>

<span data-ttu-id="f8eae-112">*elemento*</span><span class="sxs-lookup"><span data-stu-id="f8eae-112">*element*</span></span> 
</dt> <dd>

<span data-ttu-id="f8eae-113">Una delle direttive seguenti: [**Library**](library.md), **\[** [**importlib**](importlib.md) **\]** , [**Interface**](interface.md), [**Dispatch**](dispinterface.md), [**Module**](module.md), [**typedef**](typedef.md), **Method**, **Property** o [**coclass**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="f8eae-113">One of the following directives: [**library**](library.md), **\[**[**importlib**](importlib.md)**\]**, [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**module**](module.md), [**typedef**](typedef.md), **method**, **property**, or [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8eae-114">*Nome elemento*</span><span class="sxs-lookup"><span data-stu-id="f8eae-114">*element-name*</span></span> 
</dt> <dd>

<span data-ttu-id="f8eae-115">Nome che altri componenti software possono usare per delineare l'elemento corrente</span><span class="sxs-lookup"><span data-stu-id="f8eae-115">The name that other software components can use to delineate the current element</span></span>

</dd> <dt>

<span data-ttu-id="f8eae-116">*definizione*</span><span class="sxs-lookup"><span data-stu-id="f8eae-116">*definition*</span></span> 
</dt> <dd>

<span data-ttu-id="f8eae-117">Specifica le istruzioni che compongono la definizione dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="f8eae-117">Specifies statements that make up the element definition.</span></span>

</dd> <dt>

<span data-ttu-id="f8eae-118">*IDL-Statement*</span><span class="sxs-lookup"><span data-stu-id="f8eae-118">*idl-statement*</span></span> 
</dt> <dd>

<span data-ttu-id="f8eae-119">Un'istruzione di definizione dell'interfaccia MIDL, ad esempio [**propget**](propget.md) o [**propput**](propput.md).</span><span class="sxs-lookup"><span data-stu-id="f8eae-119">A MIDL interface definition statement such as [**propget**](propget.md) or [**propput**](propput.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f8eae-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="f8eae-120">Remarks</span></span>

<span data-ttu-id="f8eae-121">Usare le funzioni [**GetDocumentation**](/windows/win32/api/oaidl/nf-oaidl-itypelib-getdocumentation) nelle interfacce [**ITypeLib**](/windows/win32/api/oaidl/nn-oaidl-itypelib) e [**ITypeInfo**](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) per recuperare la stringa della guida.</span><span class="sxs-lookup"><span data-stu-id="f8eae-121">Use the [**GetDocumentation**](/windows/win32/api/oaidl/nf-oaidl-itypelib-getdocumentation) functions in the [**ITypeLib**](/windows/win32/api/oaidl/nn-oaidl-itypelib) and [**ITypeInfo**](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) interfaces to retrieve the help string.</span></span>

## <a name="examples"></a><span data-ttu-id="f8eae-122">Esempi</span><span class="sxs-lookup"><span data-stu-id="f8eae-122">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpstring("Lines 1.0 Type Library"),
    version(1.0)
]
library Lines
{
     [
         uuid(1e123456-1f3c-1069-996b-00dd010fe676), 
         helpstring("Line object."),
         oleautomation,
         dual
     ]
     interface ILine : IDispatch                         
     {
         [propget, helpstring("Returns and sets RGB color.")]
         HRESULT Color([out, retval] long* ReturnVal); 
         [propput, helpstring("Returns and sets RGB color.")]
         HRESULT Color([in] long rgb);
     }
};
```

## <a name="see-also"></a><span data-ttu-id="f8eae-123">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="f8eae-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8eae-124">**libreria**</span><span class="sxs-lookup"><span data-stu-id="f8eae-124">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="f8eae-125">**importlib**</span><span class="sxs-lookup"><span data-stu-id="f8eae-125">**importlib**</span></span>](importlib.md)
</dt> <dt>

[<span data-ttu-id="f8eae-126">**interfaccia**</span><span class="sxs-lookup"><span data-stu-id="f8eae-126">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="f8eae-127">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="f8eae-127">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="f8eae-128">**modulo**</span><span class="sxs-lookup"><span data-stu-id="f8eae-128">**module**</span></span>](module.md)
</dt> <dt>

[<span data-ttu-id="f8eae-129">**coclass**</span><span class="sxs-lookup"><span data-stu-id="f8eae-129">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="f8eae-130">**typedef**</span><span class="sxs-lookup"><span data-stu-id="f8eae-130">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="f8eae-131">Sintassi del file di FAD</span><span class="sxs-lookup"><span data-stu-id="f8eae-131">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="f8eae-132">Esempio di file di FAD</span><span class="sxs-lookup"><span data-stu-id="f8eae-132">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="f8eae-133">Generazione di una libreria dei tipi con MIDL</span><span class="sxs-lookup"><span data-stu-id="f8eae-133">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 