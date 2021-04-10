---
title: nonbrowsable (attributo)
description: Usare l'attributo \ nonbrowsable \ per contrassegnare un'interfaccia o un membro dispatch che non deve essere visualizzato in un browser delle proprietà.
ms.assetid: 94e868cc-8d9c-4b8a-ac18-1ea513a103da
keywords:
- attributo MIDL non esplorabile
topic_type:
- apiref
api_name:
- nonbrowsable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e24c39511df9637c352245b98b237fe8fd451eb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103956395"
---
# <a name="nonbrowsable-attribute"></a><span data-ttu-id="932f1-104">nonbrowsable (attributo)</span><span class="sxs-lookup"><span data-stu-id="932f1-104">nonbrowsable attribute</span></span>

<span data-ttu-id="932f1-105">Usare l'attributo **\[ nonbrowsable \]** per contrassegnare un'interfaccia o un membro dispatch che non deve essere visualizzato in un browser delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="932f1-105">Use the **\[nonbrowsable\]** attribute to tag an interface or dispinterface member that should not be displayed in a properties browser.</span></span>

``` syntax
[property-attribute-list, nonbrowsable]return-type property-name(prop-param-list)
```

## <a name="parameters"></a><span data-ttu-id="932f1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="932f1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="932f1-107">*Property-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="932f1-107">*property-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="932f1-108">Altri attributi che si applicano alla proprietà.</span><span class="sxs-lookup"><span data-stu-id="932f1-108">Other attributes that apply to the property.</span></span>

</dd> <dt>

<span data-ttu-id="932f1-109">*tipo restituito*</span><span class="sxs-lookup"><span data-stu-id="932f1-109">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="932f1-110">Tipo dei dati restituiti dal metodo.</span><span class="sxs-lookup"><span data-stu-id="932f1-110">The type of the data returned by the method.</span></span>

</dd> <dt>

<span data-ttu-id="932f1-111">*nome proprietà*</span><span class="sxs-lookup"><span data-stu-id="932f1-111">*property-name*</span></span> 
</dt> <dd>

<span data-ttu-id="932f1-112">Nome della proprietà o del metodo.</span><span class="sxs-lookup"><span data-stu-id="932f1-112">The name of the property or method.</span></span>

</dd> <dt>

<span data-ttu-id="932f1-113">*prop-param-list*</span><span class="sxs-lookup"><span data-stu-id="932f1-113">*prop-param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="932f1-114">Zero o più parametri da passare al metodo.</span><span class="sxs-lookup"><span data-stu-id="932f1-114">Zero or more parameters to be passed to the method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="932f1-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="932f1-115">Remarks</span></span>

<span data-ttu-id="932f1-116">Alcune proprietà non devono essere visualizzate in un browser delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="932f1-116">Certain properties should not be displayed in a properties browser.</span></span> <span data-ttu-id="932f1-117">Questo può essere dovuto al fatto che il recupero del valore richiede molto tempo.</span><span class="sxs-lookup"><span data-stu-id="932f1-117">This may be because retrieving the value would take a very long time.</span></span> <span data-ttu-id="932f1-118">Nell'esempio viene impedito all'utente di tentare di recuperare la proprietà *count* , che restituisce il numero di righe nel dynaset. Questo numero può rappresentare i risultati di una query di dimensioni molto grandi.</span><span class="sxs-lookup"><span data-stu-id="932f1-118">The example prevents the user from attempting to retrieve the *Count* property, which returns the number of rows in the dynaset.This number may represent the results of a very large query.</span></span>

<span data-ttu-id="932f1-119">Altre proprietà possono avere effetti imprevisti sul browser.</span><span class="sxs-lookup"><span data-stu-id="932f1-119">Other properties may have unexpected effects on the browser.</span></span> <span data-ttu-id="932f1-120">Si consideri, ad esempio, un controllo con la proprietà "IsSelected" per indicare se il controllo è selezionato.</span><span class="sxs-lookup"><span data-stu-id="932f1-120">For example, consider a control with the property "IsSelected" to tell whether the control is selected.</span></span> <span data-ttu-id="932f1-121">Se "IsSelected" è impostato su false, un visualizzatore di proprietà basate sulla selezione esplorerà un oggetto diverso.</span><span class="sxs-lookup"><span data-stu-id="932f1-121">If "IsSelected" is set to false, a selection-based properties browser will browse a different object.</span></span>

<span data-ttu-id="932f1-122">Si noti che una proprietà contrassegnata come non **\[ esplorabile \]** verrà comunque visualizzata in un Visualizzatore oggetti, che non Mostra i valori delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="932f1-122">Note that a property tagged as **\[nonbrowsable\]** will still appear in an object browser, which does not show property values.</span></span>

### <a name="typeflag-representation"></a><span data-ttu-id="932f1-123">Rappresentazione TYPEFLAG</span><span class="sxs-lookup"><span data-stu-id="932f1-123">Typeflag Representation</span></span>

<span data-ttu-id="932f1-124">Presenza di FUNCFLAG \_ FNONBROWSABLE o VARFLAG \_ FNONBROWSABLE.</span><span class="sxs-lookup"><span data-stu-id="932f1-124">The presence of FUNCFLAG\_FNONBROWSABLE or VARFLAG\_FNONBROWSABLE.</span></span>

## <a name="examples"></a><span data-ttu-id="932f1-125">Esempi</span><span class="sxs-lookup"><span data-stu-id="932f1-125">Examples</span></span>

``` syntax
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    restricted
]
interface IDynaset:IDispatch
{
    [propget, nonbrowsable]HRESULT Count([out, retval] long *Value);
}
```

## <a name="see-also"></a><span data-ttu-id="932f1-126">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="932f1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="932f1-127">Sintassi del file di FAD</span><span class="sxs-lookup"><span data-stu-id="932f1-127">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="932f1-128">Esempio di file di FAD</span><span class="sxs-lookup"><span data-stu-id="932f1-128">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="932f1-129">Generazione di una libreria dei tipi con MIDL</span><span class="sxs-lookup"><span data-stu-id="932f1-129">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 