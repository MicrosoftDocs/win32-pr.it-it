---
title: uidefault (attributo)
description: L'attributo \ uidefault \ indica che il membro delle informazioni sul tipo è il membro predefinito per la visualizzazione nell'interfaccia utente.
ms.assetid: e789be38-a509-437d-89c9-ebbc830e5ae2
keywords:
- attributo MIDL di uidefault
topic_type:
- apiref
api_name:
- uidefault
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcef39f36abad7c7cb5562b2d892761bd1bb7b5b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398879"
---
# <a name="uidefault-attribute"></a><span data-ttu-id="02112-104">uidefault (attributo)</span><span class="sxs-lookup"><span data-stu-id="02112-104">uidefault attribute</span></span>

<span data-ttu-id="02112-105">L'attributo **\[ uidefault \]** indica che il membro Information del tipo è il membro predefinito per la visualizzazione nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="02112-105">The **\[uidefault\]** attribute indicates that the type information member is the default member for display in the user interface.</span></span>

``` syntax
[method-attribute-list, uidefault]return-type method-name(method-parameter-list)
```

## <a name="parameters"></a><span data-ttu-id="02112-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="02112-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02112-107">*Method-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="02112-107">*method-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="02112-108">Altri attributi che si applicano al metodo.</span><span class="sxs-lookup"><span data-stu-id="02112-108">Other attributes that apply to the method.</span></span>

</dd> <dt>

<span data-ttu-id="02112-109">*tipo restituito*</span><span class="sxs-lookup"><span data-stu-id="02112-109">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="02112-110">Tipo di dati che il metodo restituirà al termine dell'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="02112-110">The type of the data that the method will return when it finishes execution.</span></span>

</dd> <dt>

<span data-ttu-id="02112-111">*Nome metodo*</span><span class="sxs-lookup"><span data-stu-id="02112-111">*method-name*</span></span> 
</dt> <dd>

<span data-ttu-id="02112-112">Nome del metodo.</span><span class="sxs-lookup"><span data-stu-id="02112-112">The name of the method.</span></span>

</dd> <dt>

<span data-ttu-id="02112-113">*elenco di parametri di metodo*</span><span class="sxs-lookup"><span data-stu-id="02112-113">*method-parameter-list*</span></span> 
</dt> <dd>

<span data-ttu-id="02112-114">Zero o più parametri per il metodo.</span><span class="sxs-lookup"><span data-stu-id="02112-114">Zero or more parameters for the method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="02112-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="02112-115">Remarks</span></span>

<span data-ttu-id="02112-116">L'applicazione dell'attributo **\[ uidefault \]** a un membro di un'interfaccia o di un'interfaccia dispatch indica Visual Basic, in fase di progettazione, di visualizzare automaticamente questo evento o proprietà all'utente.</span><span class="sxs-lookup"><span data-stu-id="02112-116">Applying the **\[uidefault\]** attribute to a member of an interface or a dispinterface tells Visual Basic, at design-time, to automatically display this event or property to the user.</span></span> <span data-ttu-id="02112-117">Ciò significa che quando l'utente fa doppio clic su un oggetto, Visual Basic passa all'evento nell'interfaccia di origine predefinita con l'attributo **\[ uidefault \]** .</span><span class="sxs-lookup"><span data-stu-id="02112-117">This means that when the user double-clicks an object, Visual Basic jumps to the event in the default source interface that has the **\[uidefault\]** attribute.</span></span> <span data-ttu-id="02112-118">Quando l'utente seleziona un oggetto, il Visualizzatore proprietà di Visual Basic Visualizza la proprietà nell'interfaccia di origine predefinita con questo attributo.</span><span class="sxs-lookup"><span data-stu-id="02112-118">When the user selects an object, Visual Basic's Properties browser displays the property in the default source interface that has this attribute.</span></span> <span data-ttu-id="02112-119">Se nessun evento o proprietà ha l'attributo **\[ uidefault \]** , Visual Basic Visualizza il primo evento o proprietà elencato nell'interfaccia predefinita.</span><span class="sxs-lookup"><span data-stu-id="02112-119">If no event or property has the **\[uidefault\]** attribute, Visual Basic displays the first event or property listed in the default interface.</span></span>

### <a name="typeflag-representation"></a><span data-ttu-id="02112-120">Rappresentazione TYPEFLAG</span><span class="sxs-lookup"><span data-stu-id="02112-120">Typeflag Representation</span></span>

<span data-ttu-id="02112-121">Presenza di FUNCFLAG \_ FUIDEFAULT o VARFLAG \_ FUIDEFAULT</span><span class="sxs-lookup"><span data-stu-id="02112-121">The presence of FUNCFLAG\_FUIDEFAULT or VARFLAG\_FUIDEFAULT</span></span>

## <a name="examples"></a><span data-ttu-id="02112-122">Esempi</span><span class="sxs-lookup"><span data-stu-id="02112-122">Examples</span></span>

``` syntax
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    restricted
]
interface IForm: IDispatch
{
    [propget]HRESULT Backcolor([out, retval] long *Value);
    [propput]HRESULT Backcolor([in] long Value);
    [propget, uidefault]HRESULT Name([out, retval] BSTR *Value);
    [propput, uidefault]HRESULT Name([in] BSTR Value);
}
[
    odl,
    dual,
    uuid(87654321-1234-1234-1234-123456789ABC),
    restricted
] 
interface IFormEvents: IDispatch
{
    [uidefault]HRESULT Click();
    HRESULT Resize();
}

[
    uuid(12345678-1234-1234-1234-987654321ABC)
]
coclass Form
{
    [default] interface IForm;
    [default, source] interface IFormEvents;
}
```

## <a name="see-also"></a><span data-ttu-id="02112-123">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="02112-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02112-124">Generazione di una libreria dei tipi con MIDL</span><span class="sxs-lookup"><span data-stu-id="02112-124">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="02112-125">Esempio di file di FAD</span><span class="sxs-lookup"><span data-stu-id="02112-125">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="02112-126">Sintassi del file di FAD</span><span class="sxs-lookup"><span data-stu-id="02112-126">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> </dl>

 

 