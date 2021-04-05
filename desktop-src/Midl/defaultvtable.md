---
title: defaultvtable (attributo)
description: L'attributo \ defaultvtable \ definisce un'interfaccia come interfaccia vtable predefinita.
ms.assetid: 05e50935-c630-4f9e-a7ec-3bb70a9834f1
keywords:
- attributo MIDL di defaultvtable
topic_type:
- apiref
api_name:
- defaultvtable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8086d60d0936dcf56738afadea4244a5fff758b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872461"
---
# <a name="defaultvtable-attribute"></a><span data-ttu-id="9defd-104">defaultvtable (attributo)</span><span class="sxs-lookup"><span data-stu-id="9defd-104">defaultvtable attribute</span></span>

<span data-ttu-id="9defd-105">L'attributo **\[ defaultvtable \]** definisce un'interfaccia come l'interfaccia vtable predefinita.</span><span class="sxs-lookup"><span data-stu-id="9defd-105">The **\[defaultvtable\]** attribute defines an interface as the default Vtable interface.</span></span>

``` syntax
[
    coclass-attribute-list, 
    defaultvtable
]
coclass coclass-name
{
    coclass-interface-list
}
```

## <a name="parameters"></a><span data-ttu-id="9defd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9defd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9defd-107">*coclass-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="9defd-107">*coclass-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="9defd-108">Altri attributi che si applicano alla classe.</span><span class="sxs-lookup"><span data-stu-id="9defd-108">Other attributes that apply to the class.</span></span> <span data-ttu-id="9defd-109">Gli **\[** attributi [**source**](source.md) **\]** e **\[** [**UUID**](uuid.md) **\]** sono obbligatori.</span><span class="sxs-lookup"><span data-stu-id="9defd-109">The **\[**[**source**](source.md)**\]** and **\[**[**uuid**](uuid.md)**\]** attributes are required.</span></span>

</dd> <dt>

<span data-ttu-id="9defd-110">*coclass-nome*</span><span class="sxs-lookup"><span data-stu-id="9defd-110">*coclass-name*</span></span> 
</dt> <dd>

<span data-ttu-id="9defd-111">Nome della classe.</span><span class="sxs-lookup"><span data-stu-id="9defd-111">The name of the class.</span></span>

</dd> <dt>

<span data-ttu-id="9defd-112">*coclass-interface-List*</span><span class="sxs-lookup"><span data-stu-id="9defd-112">*coclass-interface-list*</span></span> 
</dt> <dd>

<span data-ttu-id="9defd-113">Elenco di interfacce per la classe.</span><span class="sxs-lookup"><span data-stu-id="9defd-113">A list of interfaces for the class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9defd-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="9defd-114">Remarks</span></span>

<span data-ttu-id="9defd-115">Un'interfaccia vtable predefinita non può essere un'interfaccia dispatch, ma deve essere un'interfaccia dual o vtable o.</span><span class="sxs-lookup"><span data-stu-id="9defd-115">A default Vtable interface cannot be a dispinterface—it must be a dual or Vtable or interface.</span></span> <span data-ttu-id="9defd-116">Se l'interfaccia è un'interfaccia duale, i sink possono presumere che ricevano gli eventi tramite vtable.</span><span class="sxs-lookup"><span data-stu-id="9defd-116">If the interface is a dual interface, then sinks can assume that they will receive events through Vtable.</span></span>

<span data-ttu-id="9defd-117">Una classe può essere sia un'interfaccia di origine predefinita che un'interfaccia di origine vtable predefinita, come illustrato nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="9defd-117">A class can be both a default source interface and a default Vtable source interface as shown in the example.</span></span> <span data-ttu-id="9defd-118">In questo caso, un sink di notifica deve utilizzare \_ l'IID IDISPATCH per ricevere eventi di invio e utilizzare l'identificatore di interfaccia per ricevere eventi vtable.</span><span class="sxs-lookup"><span data-stu-id="9defd-118">In this case an advise sink should use IID\_IDISPATCH to receive dispatch events and use the interface identifier to receive Vtable events.</span></span>

### <a name="typeflag-representation"></a><span data-ttu-id="9defd-119">Rappresentazione TYPEFLAG</span><span class="sxs-lookup"><span data-stu-id="9defd-119">Typeflag Representation</span></span>

<span data-ttu-id="9defd-120">Presenza di IMPLTYPEFLAG \_ FDEFAULTVTABLE.</span><span class="sxs-lookup"><span data-stu-id="9defd-120">The presence of IMPLTYPEFLAG\_FDEFAULTVTABLE.</span></span>

## <a name="examples"></a><span data-ttu-id="9defd-121">Esempi</span><span class="sxs-lookup"><span data-stu-id="9defd-121">Examples</span></span>

``` syntax
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    restricted
]
interface IForm: IDispatch
{
    [propget] HRESULT Backcolor([out, retval] long *Value);
    [propput] HRESULT Backcolor([in] long Value);
    [propget] HRESULT Name([out, retval] BSTR *Value);
    [propput] HRESULT Name([in] BSTR Value);}

[
    dual,
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    restricted
]
interface IFormEvents: IDispatch
{
    HRESULT Click();
    HRESULT Resize();}

    [
        uuid(1e123456-1f3c-1069-996b-123456789ABC)
    ]
    coclass Form
    {
        [default] interface IForm;
        [default, defaultvtable, source] interface IFormEvents;
    }
}
```

## <a name="see-also"></a><span data-ttu-id="9defd-122">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="9defd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9defd-123">**coclass**</span><span class="sxs-lookup"><span data-stu-id="9defd-123">**coclass**</span></span>](coclass.md)
</dt> <dt>

[<span data-ttu-id="9defd-124">Sintassi del file di FAD</span><span class="sxs-lookup"><span data-stu-id="9defd-124">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="9defd-125">Esempio di file di FAD</span><span class="sxs-lookup"><span data-stu-id="9defd-125">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="9defd-126">Generazione di una libreria dei tipi con MIDL</span><span class="sxs-lookup"><span data-stu-id="9defd-126">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="9defd-127">**origine**</span><span class="sxs-lookup"><span data-stu-id="9defd-127">**source**</span></span>](source.md)
</dt> <dt>

[<span data-ttu-id="9defd-128">**uuid**</span><span class="sxs-lookup"><span data-stu-id="9defd-128">**uuid**</span></span>](uuid.md)
</dt> </dl>

 

 