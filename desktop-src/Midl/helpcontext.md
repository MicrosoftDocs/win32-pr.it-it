---
title: helpcontext (attributo)
description: L'attributo \ HelpContext \ specifica un identificatore di contesto che consente all'utente di visualizzare informazioni sull'elemento nel file della guida.
ms.assetid: 44a60c75-be69-4cd9-afb0-5eb988830e6c
keywords:
- attributo MIDL di HelpContext
topic_type:
- apiref
api_name:
- helpcontext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75a8811a73515528981a8214caba3fe2778e2ea9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103956399"
---
# <a name="helpcontext-attribute"></a><span data-ttu-id="b8f5f-104">helpcontext (attributo)</span><span class="sxs-lookup"><span data-stu-id="b8f5f-104">helpcontext attribute</span></span>

<span data-ttu-id="b8f5f-105">L' \[ attributo **HelpContext** \] specifica un identificatore di contesto che consente all'utente di visualizzare informazioni sull'elemento nel file della guida.</span><span class="sxs-lookup"><span data-stu-id="b8f5f-105">The \[**helpcontext**\] attribute specifies a context identifier that lets the user view information about this element in the Help file.</span></span>

``` syntax
[
    uuid(uuid-number), 
    helpcontext(helpcontext-value)
    [, attribute-list]
] 
element element-name
{
    definitions
}
```

## <a name="parameters"></a><span data-ttu-id="b8f5f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b8f5f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8f5f-107">*UUID-numero*</span><span class="sxs-lookup"><span data-stu-id="b8f5f-107">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="b8f5f-108">Specifica un numero di identificazione univoco universale per la [**libreria**](library.md), \[ [**importlib**](importlib.md) \] , [**Interface**](interface.md), [**Dispatch**](dispinterface.md), [**Module**](module.md), [**typedef**](typedef.md), **Methods**, **\[ Property \]** o [**coclass**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="b8f5f-108">Specifies a universally unique identification number for the [**library**](library.md), \[[**importlib**](importlib.md)\], [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**module**](module.md), [**typedef**](typedef.md), **methods**, **\[property\]**, or [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8f5f-109">*HelpContext-valore*</span><span class="sxs-lookup"><span data-stu-id="b8f5f-109">*helpcontext-value*</span></span> 
</dt> <dd>

<span data-ttu-id="b8f5f-110">Intero univoco che identifica il testo della Guida associato all'elemento MIDL corrente.</span><span class="sxs-lookup"><span data-stu-id="b8f5f-110">A unique integer that identifies the help text associated with the current MIDL element.</span></span>

</dd> <dt>

<span data-ttu-id="b8f5f-111">*elenco attributi*</span><span class="sxs-lookup"><span data-stu-id="b8f5f-111">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="b8f5f-112">Specifica un elenco di uno o più attributi applicabili all'elemento MIDL nel suo complesso.</span><span class="sxs-lookup"><span data-stu-id="b8f5f-112">Specifies a list of one or more attributes that apply to the MIDL element as a whole.</span></span>

</dd> <dt>

<span data-ttu-id="b8f5f-113">*elemento*</span><span class="sxs-lookup"><span data-stu-id="b8f5f-113">*element*</span></span> 
</dt> <dd>

<span data-ttu-id="b8f5f-114">Una delle direttive seguenti: [**Library**](library.md), \[ [**importlib**](importlib.md) \] , [**Interface**](interface.md), [**Dispatch**](dispinterface.md), [**Module**](module.md), [**typedef**](typedef.md), **Method**, **Property** o [**coclass**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="b8f5f-114">One of the following directives: [**library**](library.md), \[[**importlib**](importlib.md)\], [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**module**](module.md), [**typedef**](typedef.md), **method**, **property**, or [**coclass**](coclass.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8f5f-115">*Nome elemento*</span><span class="sxs-lookup"><span data-stu-id="b8f5f-115">*element-name*</span></span> 
</dt> <dd>

<span data-ttu-id="b8f5f-116">Nome che altri componenti software possono utilizzare per delineare l'elemento corrente.</span><span class="sxs-lookup"><span data-stu-id="b8f5f-116">The name that other software components can use to delineate the current element.</span></span>

</dd> <dt>

<span data-ttu-id="b8f5f-117">*definizioni*</span><span class="sxs-lookup"><span data-stu-id="b8f5f-117">*definitions*</span></span> 
</dt> <dd>

<span data-ttu-id="b8f5f-118">Specifica le istruzioni che compongono la definizione dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="b8f5f-118">Specifies statements that make up the element definition.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b8f5f-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="b8f5f-119">Remarks</span></span>

<span data-ttu-id="b8f5f-120">L' \[ **attributo HelpContext** \] può essere applicato agli elementi seguenti: [**Library**](library.md), \[ [**importlib**](importlib.md) \] , [**Interface**](interface.md), [**Dispatch**](dispinterface.md), [**Module**](module.md), [**typedef**](typedef.md), **Method**, **Property** o [**coclass**](coclass.md).</span><span class="sxs-lookup"><span data-stu-id="b8f5f-120">The \[**helpcontext**\] attribute can be applied to the following elements: [**library**](library.md), \[[**importlib**](importlib.md)\], [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**module**](module.md), [**typedef**](typedef.md), **method**, **property**, or [**coclass**](coclass.md).</span></span>

<span data-ttu-id="b8f5f-121">*HelpContext-value* è un identificatore di contesto a 32 bit all'interno del file della guida che può essere recuperato con le funzioni [**GetDocumentation**](/windows/win32/api/oaidl/nf-oaidl-itypelib-getdocumentation) nelle interfacce [**ITypeLib**](/windows/win32/api/oaidl/nn-oaidl-itypelib) e [**ITypeInfo**](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) .</span><span class="sxs-lookup"><span data-stu-id="b8f5f-121">The *helpcontext-value* is a 32-bit context identifier within the Help file that can be retrieved with the [**GetDocumentation**](/windows/win32/api/oaidl/nf-oaidl-itypelib-getdocumentation) functions in the [**ITypeLib**](/windows/win32/api/oaidl/nn-oaidl-itypelib) and [**ITypeInfo**](/windows/win32/api/oaidl/nn-oaidl-itypeinfo) interfaces.</span></span>

## <a name="examples"></a><span data-ttu-id="b8f5f-122">Esempi</span><span class="sxs-lookup"><span data-stu-id="b8f5f-122">Examples</span></span>

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpcontext(7035943),
    helpstring("Hello Class"),
    appobject
] 
coclass Hello
{
    [default, helpcontext(3914972)] interface IHello : IUnknown;
    interface IDispatch;
}
```

## <a name="see-also"></a><span data-ttu-id="b8f5f-123">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="b8f5f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8f5f-124">**coclass**</span><span class="sxs-lookup"><span data-stu-id="b8f5f-124">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="b8f5f-125">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="b8f5f-125">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="b8f5f-126">Generazione di una libreria dei tipi con MIDL</span><span class="sxs-lookup"><span data-stu-id="b8f5f-126">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="b8f5f-127">**importlib**</span><span class="sxs-lookup"><span data-stu-id="b8f5f-127">**importlib**</span></span>](importlib.md)
</dt> <dt>

[<span data-ttu-id="b8f5f-128">**interfaccia**</span><span class="sxs-lookup"><span data-stu-id="b8f5f-128">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="b8f5f-129">**libreria**</span><span class="sxs-lookup"><span data-stu-id="b8f5f-129">**library**</span></span>](library.md)
</dt> <dt>

[<span data-ttu-id="b8f5f-130">**modulo**</span><span class="sxs-lookup"><span data-stu-id="b8f5f-130">**module**</span></span>](module.md)
</dt> <dt>

[<span data-ttu-id="b8f5f-131">Sintassi del file di FAD</span><span class="sxs-lookup"><span data-stu-id="b8f5f-131">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="b8f5f-132">Esempio di file di FAD</span><span class="sxs-lookup"><span data-stu-id="b8f5f-132">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="b8f5f-133">**typedef**</span><span class="sxs-lookup"><span data-stu-id="b8f5f-133">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 