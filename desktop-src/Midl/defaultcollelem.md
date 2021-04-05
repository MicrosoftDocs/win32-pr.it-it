---
title: defaultcollelem (attributo)
description: L'attributo \ defaultcollelem \ contrassegna una proprietà come funzione di accesso per un elemento della raccolta predefinita.
ms.assetid: e409f845-3f26-4551-abda-86c4776160aa
keywords:
- attributo MIDL di defaultcollelem
topic_type:
- apiref
api_name:
- defaultcollelem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45fdbd59ca954d955fc5598b2bc2dc7a39ee14b2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046690"
---
# <a name="defaultcollelem-attribute"></a><span data-ttu-id="63657-104">defaultcollelem (attributo)</span><span class="sxs-lookup"><span data-stu-id="63657-104">defaultcollelem attribute</span></span>

<span data-ttu-id="63657-105">L'attributo **\[ defaultcollelem \]** contrassegna una proprietà come funzione di accesso per un elemento della raccolta predefinita.</span><span class="sxs-lookup"><span data-stu-id="63657-105">The **\[defaultcollelem\]** attribute flags a property as an accessor function for an element of the default collection.</span></span>

``` syntax
[property-attribute-list, defaultcollelem] return-type property-name(prop-param-list)
```

## <a name="parameters"></a><span data-ttu-id="63657-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="63657-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63657-107">*Property-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="63657-107">*property-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="63657-108">Altri attributi che si applicano alla proprietà.</span><span class="sxs-lookup"><span data-stu-id="63657-108">Other attributes that apply to the property.</span></span>

</dd> <dt>

<span data-ttu-id="63657-109">*tipo restituito*</span><span class="sxs-lookup"><span data-stu-id="63657-109">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="63657-110">Specifica il tipo restituito della funzione.</span><span class="sxs-lookup"><span data-stu-id="63657-110">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="63657-111">*nome proprietà*</span><span class="sxs-lookup"><span data-stu-id="63657-111">*property-name*</span></span> 
</dt> <dd>

<span data-ttu-id="63657-112">Nome della proprietà.</span><span class="sxs-lookup"><span data-stu-id="63657-112">The name of the property.</span></span>

</dd> <dt>

<span data-ttu-id="63657-113">*prop-param-list*</span><span class="sxs-lookup"><span data-stu-id="63657-113">*prop-param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="63657-114">Elenco di zero o più parametri associati alla proprietà.</span><span class="sxs-lookup"><span data-stu-id="63657-114">A list of zero or more parameters associated with the property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="63657-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="63657-115">Remarks</span></span>

<span data-ttu-id="63657-116">L'attributo **\[ defaultcollelem \]** viene usato per l'ottimizzazione del codice® Visual BasicÂ.</span><span class="sxs-lookup"><span data-stu-id="63657-116">The **\[defaultcollelem\]** attribute is used for Visual BasicÂ® code optimization.</span></span> <span data-ttu-id="63657-117">Se un membro di un'interfaccia o di un'interfaccia dispatch viene contrassegnato come funzione di accesso, la chiamata passerà direttamente a tale membro.</span><span class="sxs-lookup"><span data-stu-id="63657-117">If a member of an interface or dispinterface is flagged as an accessor function, then the call will go directly to that member.</span></span>

<span data-ttu-id="63657-118">L'uso di **\[ defaultcollelem \]** deve essere coerente per una proprietà.</span><span class="sxs-lookup"><span data-stu-id="63657-118">Use of **\[defaultcollelem\]** must be consistent for a property.</span></span> <span data-ttu-id="63657-119">Se ad esempio si usa l'attributo in una proprietà *Get* , deve essere presente anche in una proprietà *Let* .</span><span class="sxs-lookup"><span data-stu-id="63657-119">For example, if you use the attribute on a *Get* property, it must also be present on a *Let* property.</span></span>

### <a name="typeflags-representation"></a><span data-ttu-id="63657-120">Rappresentazione TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="63657-120">Typeflags Representation</span></span>

<span data-ttu-id="63657-121">Presenza di FUNCFLAG \_ FDEFAULTCOLLELEM o VARFLAG \_ FDEFAULTCOLLELEM.</span><span class="sxs-lookup"><span data-stu-id="63657-121">The presence of FUNCFLAG\_FDEFAULTCOLLELEM or VARFLAG\_FDEFAULTCOLLELEM.</span></span>

## <a name="examples"></a><span data-ttu-id="63657-122">Esempi</span><span class="sxs-lookup"><span data-stu-id="63657-122">Examples</span></span>

``` syntax
//A form has a button on it named Button1. 
//To enable use of the property syntax and efficient use of the !
//syntax, the form describes itself in type info this way.
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    helpstring("This is IForm"),
    restricted
]
interface IForm1: IForm
{
    [propget, defaultcollelem] HRESULT Button1(
        [out, retval] Button *Value);
}

//User code may access the button using property syntax or ! syntax.

Sub Test()
Dim f as Form1
Dim b1 As Button
Dim b2 As Button

Set f = Form1

Set b1 = f.Button1        ' Property syntax
Set b = f!Button1        ' ! syntax
End Sub
```

## <a name="see-also"></a><span data-ttu-id="63657-123">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="63657-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63657-124">Sintassi del file di FAD</span><span class="sxs-lookup"><span data-stu-id="63657-124">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="63657-125">Esempio di file di FAD</span><span class="sxs-lookup"><span data-stu-id="63657-125">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="63657-126">Generazione di una libreria dei tipi con MIDL</span><span class="sxs-lookup"><span data-stu-id="63657-126">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 