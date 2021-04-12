---
title: defaultvalue (attributo)
description: L'attributo \ DefaultValue \ consente di specificare un valore predefinito per un parametro facoltativo tipizzato.
ms.assetid: a974a0f7-7b08-4f17-bb28-0e23e6aa97db
keywords:
- attributo DefaultValue MIDL
topic_type:
- apiref
api_name:
- defaultvalue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04f4efaac16325ec77721665a4dee14c9514a192
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337270"
---
# <a name="defaultvalue-attribute"></a><span data-ttu-id="18566-104">defaultvalue (attributo)</span><span class="sxs-lookup"><span data-stu-id="18566-104">defaultvalue attribute</span></span>

<span data-ttu-id="18566-105">L'attributo **\[ DefaultValue \]** consente di specificare un valore predefinito per un parametro facoltativo tipizzato.</span><span class="sxs-lookup"><span data-stu-id="18566-105">The **\[defaultvalue\]** attribute allows you to specify a default value for a typed optional parameter.</span></span>

``` syntax
interface interface-name
{
  return-type function-name(
        mandatory-param-list, 
        [[attribute-list,] defaultvalue(value)] param-type param-name
        [ , optional-param-list]);
}
```

## <a name="parameters"></a><span data-ttu-id="18566-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="18566-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18566-107">*Nome interfaccia*</span><span class="sxs-lookup"><span data-stu-id="18566-107">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="18566-108">Specifica il nome dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="18566-108">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="18566-109">*tipo restituito*</span><span class="sxs-lookup"><span data-stu-id="18566-109">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="18566-110">Specifica il tipo restituito della funzione.</span><span class="sxs-lookup"><span data-stu-id="18566-110">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="18566-111">*Nome funzione*</span><span class="sxs-lookup"><span data-stu-id="18566-111">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="18566-112">Specifica il nome della funzione a cui verrà applicato l'attributo **\[ DefaultValue \]** .</span><span class="sxs-lookup"><span data-stu-id="18566-112">Specifies the name of the function to which the **\[defaultvalue\]** attribute will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="18566-113">*elenco di parametri obbligatori*</span><span class="sxs-lookup"><span data-stu-id="18566-113">*mandatory-param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="18566-114">Specifica o più parametri obbligatori.</span><span class="sxs-lookup"><span data-stu-id="18566-114">Specifies on or more required parameters.</span></span>

</dd> <dt>

<span data-ttu-id="18566-115">*elenco attributi*</span><span class="sxs-lookup"><span data-stu-id="18566-115">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="18566-116">Specifica un elenco di uno o più attributi, separati da virgole, che si applicano al parametro.</span><span class="sxs-lookup"><span data-stu-id="18566-116">Specifies a list of one or more attributes, separated by commas, that apply to the parameter.</span></span>

</dd> <dt>

<span data-ttu-id="18566-117">*param-Type*</span><span class="sxs-lookup"><span data-stu-id="18566-117">*param-type*</span></span> 
</dt> <dd>

<span data-ttu-id="18566-118">Indica il tipo del parametro facoltativo.</span><span class="sxs-lookup"><span data-stu-id="18566-118">Indicates the type of the optional parameter.</span></span>

</dd> <dt>

<span data-ttu-id="18566-119">*nome param*</span><span class="sxs-lookup"><span data-stu-id="18566-119">*param-name*</span></span> 
</dt> <dd>

<span data-ttu-id="18566-120">Specifica il nome del parametro facoltativo.</span><span class="sxs-lookup"><span data-stu-id="18566-120">Specifies the name of the optional parameter.</span></span>

</dd> <dt>

<span data-ttu-id="18566-121">*facoltativo-param-list*</span><span class="sxs-lookup"><span data-stu-id="18566-121">*optional-param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="18566-122">Specifica zero o più parametri aggiuntivi, ognuno dei quali deve avere un valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="18566-122">Specifies zero or more additional parameters, each of which must have a default value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="18566-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="18566-123">Remarks</span></span>

<span data-ttu-id="18566-124">Il valore predefinito specificato per il parametro può essere qualsiasi costante oppure un'espressione che viene risolta in una costante, che può essere rappresentata da un **Variant**.</span><span class="sxs-lookup"><span data-stu-id="18566-124">The default value you specify for the parameter can be any constant, or an expression that resolves to a constant, that can be represented by a **VARIANT**.</span></span> <span data-ttu-id="18566-125">In particolare, non è possibile applicare l'attributo **\[ \] DefaultValue** a un parametro che è una struttura, una matrice o un tipo **SAFEARRAY** .</span><span class="sxs-lookup"><span data-stu-id="18566-125">Specifically, you cannot apply the **\[defaultvalue\]** attribute to a parameter that is a structure, an array, or a **SAFEARRAY** type.</span></span>

<span data-ttu-id="18566-126">Il compilatore MIDL accetta l'ordinamento dei parametri seguente (da sinistra a destra):</span><span class="sxs-lookup"><span data-stu-id="18566-126">The MIDL compiler accepts the following parameter ordering (from left-to-right):</span></span>

1.  <span data-ttu-id="18566-127">Parametri obbligatori (parametri che non dispongono degli attributi **\[ DefaultValue \]** o **\[** [**Optional**](optional.md) **\]** ),</span><span class="sxs-lookup"><span data-stu-id="18566-127">Required parameters (parameters that do not have the **\[defaultvalue\]** or **\[**[**optional**](optional.md)**\]** attributes),</span></span>
2.  <span data-ttu-id="18566-128">parametri facoltativi con o senza l'attributo **\[ DefaultValue \]** ,</span><span class="sxs-lookup"><span data-stu-id="18566-128">optional parameters with or without the **\[defaultvalue\]** attribute,</span></span>
3.  <span data-ttu-id="18566-129">parametri con l'attributo **\[ facoltativo \]** e senza l'attributo **\[ DefaultValue \]** ,</span><span class="sxs-lookup"><span data-stu-id="18566-129">parameters with the **\[optional\]** attribute and without the **\[defaultvalue\]** attribute,</span></span>
4.  <span data-ttu-id="18566-130">**\[** parametro [**LCID**](lcid.md) **\]** , se presente,</span><span class="sxs-lookup"><span data-stu-id="18566-130">**\[**[**lcid**](lcid.md)**\]** parameter, if any,</span></span>
5.  <span data-ttu-id="18566-131">**\[**[**retval**](retval.md) **\]** parametro</span><span class="sxs-lookup"><span data-stu-id="18566-131">**\[**[**retval**](retval.md)**\]** parameter</span></span>

## <a name="examples"></a><span data-ttu-id="18566-132">Esempi</span><span class="sxs-lookup"><span data-stu-id="18566-132">Examples</span></span>

``` syntax
interface IFace : IUnknown
{
    HRESULT Ex1([defaultvalue(44)] LONG i);
    HRESULT Ex2([defaultvalue(44)] SHORT i);
...
};

interface QueryDef : IUnknown
{
    HRESULT OpenRecordset( [in, defaultvalue(DBOPENTABLE)]
    LONG Type,
    [out,retval] Recordset **pprst);
}
//  Type is now known to be a LONG type (good for browser in VBA and
//  good for a C/C++ programmer) and has a default value of
//  DBOPENTABLE
```

## <a name="see-also"></a><span data-ttu-id="18566-133">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="18566-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18566-134">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="18566-134">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="18566-135">Generazione di una libreria dei tipi con MIDL</span><span class="sxs-lookup"><span data-stu-id="18566-135">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="18566-136">**interfaccia**</span><span class="sxs-lookup"><span data-stu-id="18566-136">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="18566-137">**LCID**</span><span class="sxs-lookup"><span data-stu-id="18566-137">**lcid**</span></span>](lcid.md)
</dt> <dt>

[<span data-ttu-id="18566-138">**opzionale**</span><span class="sxs-lookup"><span data-stu-id="18566-138">**optional**</span></span>](optional.md)
</dt> <dt>

[<span data-ttu-id="18566-139">Esempio di file di FAD</span><span class="sxs-lookup"><span data-stu-id="18566-139">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="18566-140">Sintassi del file di FAD</span><span class="sxs-lookup"><span data-stu-id="18566-140">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="18566-141">**retval**</span><span class="sxs-lookup"><span data-stu-id="18566-141">**retval**</span></span>](retval.md)
</dt> <dt>

[<span data-ttu-id="18566-142">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="18566-142">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 