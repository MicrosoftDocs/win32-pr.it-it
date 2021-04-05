---
title: retval (attributo)
description: L'attributo \ retval \ designa il parametro che riceve il valore restituito del membro.
ms.assetid: 3a5f1469-7828-4c38-b58f-195a47b2a66f
keywords:
- attributo retval MIDL
topic_type:
- apiref
api_name:
- retval
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04b53aa2b8ab66737bd4d97710fe942ee73bf0b8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872358"
---
# <a name="retval-attribute"></a><span data-ttu-id="f7757-104">retval (attributo)</span><span class="sxs-lookup"><span data-stu-id="f7757-104">retval attribute</span></span>

<span data-ttu-id="f7757-105">L'attributo **\[ retval \]** designa il parametro che riceve il valore restituito del membro.</span><span class="sxs-lookup"><span data-stu-id="f7757-105">The **\[retval\]** attribute designates the parameter that receives the return value of the member.</span></span>

``` syntax
return-type function-name(
    [out, retval [, optional-attributes]] data-type * param-name,
    ...);
```

## <a name="parameters"></a><span data-ttu-id="f7757-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f7757-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7757-107">*tipo restituito*</span><span class="sxs-lookup"><span data-stu-id="f7757-107">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="f7757-108">Tipo di dati del valore restituito della procedura remota.</span><span class="sxs-lookup"><span data-stu-id="f7757-108">The data type of the return value of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="f7757-109">*Nome funzione*</span><span class="sxs-lookup"><span data-stu-id="f7757-109">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="f7757-110">Nome utilizzato per richiamare la procedura remota.</span><span class="sxs-lookup"><span data-stu-id="f7757-110">The name used to invoke the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="f7757-111">*facoltativo-attributi*</span><span class="sxs-lookup"><span data-stu-id="f7757-111">*optional-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="f7757-112">Zero o più attributi MIDL.</span><span class="sxs-lookup"><span data-stu-id="f7757-112">Zero or more MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="f7757-113">*tipo di dati*</span><span class="sxs-lookup"><span data-stu-id="f7757-113">*data-type*</span></span> 
</dt> <dd>

<span data-ttu-id="f7757-114">Tipo di dati passati tramite il parametro.</span><span class="sxs-lookup"><span data-stu-id="f7757-114">The type of the data passed through the parameter.</span></span>

</dd> <dt>

<span data-ttu-id="f7757-115">*nome param*</span><span class="sxs-lookup"><span data-stu-id="f7757-115">*param-name*</span></span> 
</dt> <dd>

<span data-ttu-id="f7757-116">Nome dell'identificatore del parametro.</span><span class="sxs-lookup"><span data-stu-id="f7757-116">The identifier name of the parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f7757-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="f7757-117">Remarks</span></span>

<span data-ttu-id="f7757-118">È possibile usare l'attributo **\[ retval \]** sui parametri dei membri di interfaccia che descrivono metodi o ottengono proprietà.</span><span class="sxs-lookup"><span data-stu-id="f7757-118">You can use the **\[retval\]** attribute on parameters of interface members that describe methods or get properties.</span></span> <span data-ttu-id="f7757-119">L'attributo è obbligatorio per l'ultimo parametro di un metodo con il **\[** parametro [**propget**](propget.md) **\]** attributo). Il parametro deve avere l' **\[** attributo [**out**](out-idl.md) **\]** e deve essere un tipo di puntatore.</span><span class="sxs-lookup"><span data-stu-id="f7757-119">(The attribute is required on the last parameter of a method that has the **\[**[**propget**](propget.md)**\]** attribute.) The parameter must have the **\[**[**out**](out-idl.md)**\]** attribute and must be a pointer type.</span></span>

<span data-ttu-id="f7757-120">Non è possibile applicare l' **\[** attributo [**facoltativo**](optional.md) **\]** a un parametro **\[ \] retval** .</span><span class="sxs-lookup"><span data-stu-id="f7757-120">You cannot apply the **\[**[**optional**](optional.md)**\]** attribute to a **\[retval\]** parameter.</span></span>

<span data-ttu-id="f7757-121">Il compilatore MIDL accetta l'ordinamento dei parametri seguente (da sinistra a destra):</span><span class="sxs-lookup"><span data-stu-id="f7757-121">The MIDL compiler accepts the following parameter ordering (from left-to-right):</span></span>

1.  <span data-ttu-id="f7757-122">Parametri obbligatori (parametri senza **\[** [](defaultvalue.md) **\]** attributi DefaultValue o **\[** [**facoltativi**](optional.md) **\]** ).</span><span class="sxs-lookup"><span data-stu-id="f7757-122">Required parameters (parameters that do not have the **\[**[**defaultvalue**](defaultvalue.md)**\]** or **\[**[**optional**](optional.md)**\]** attributes).</span></span>
2.  <span data-ttu-id="f7757-123">Parametri facoltativi con o senza l' **\[** [](defaultvalue.md) **\]** attributo DefaultValue.</span><span class="sxs-lookup"><span data-stu-id="f7757-123">Optional parameters with or without the **\[**[**defaultvalue**](defaultvalue.md)**\]** attribute.</span></span>
3.  <span data-ttu-id="f7757-124">Parametri con l' **\[** attributo [**facoltativo**](optional.md) **\]** e senza l' **\[** attributo [**DefaultValue**](defaultvalue.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="f7757-124">Parameters with the **\[**[**optional**](optional.md)**\]** attribute and without the **\[**[**defaultvalue**](defaultvalue.md)**\]** attribute.</span></span>
4.  <span data-ttu-id="f7757-125">**\[** parametro [**LCID**](lcid.md) **\]** , se disponibile.</span><span class="sxs-lookup"><span data-stu-id="f7757-125">**\[**[**lcid**](lcid.md)**\]** parameter, if any.</span></span>
5.  <span data-ttu-id="f7757-126">parametro **\[ retval \]** .</span><span class="sxs-lookup"><span data-stu-id="f7757-126">**\[retval\]** parameter.</span></span>

<span data-ttu-id="f7757-127">I parametri con l'attributo **\[ retval \]** non vengono visualizzati nei browser orientati agli utenti.</span><span class="sxs-lookup"><span data-stu-id="f7757-127">Parameters with the **\[retval\]** attribute are not displayed in user-oriented browsers.</span></span>

### <a name="flags"></a><span data-ttu-id="f7757-128">Flags</span><span class="sxs-lookup"><span data-stu-id="f7757-128">Flags</span></span>

<span data-ttu-id="f7757-129">\_FRETVAL IDLFLAG</span><span class="sxs-lookup"><span data-stu-id="f7757-129">IDLFLAG\_FRETVAL</span></span>

## <a name="examples"></a><span data-ttu-id="f7757-130">Esempi</span><span class="sxs-lookup"><span data-stu-id="f7757-130">Examples</span></span>

``` syntax
HRESULT MyMethod([out, retval] InMyFace** ReturnVal);
HRESULT MyOtherMethod([out, retval] VARIANT_BOOL* ReturnVal);
```

## <a name="see-also"></a><span data-ttu-id="f7757-131">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="f7757-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7757-132">**DefaultValue**</span><span class="sxs-lookup"><span data-stu-id="f7757-132">**defaultvalue**</span></span>](defaultvalue.md)
</dt> <dt>

[<span data-ttu-id="f7757-133">Generazione di una libreria dei tipi con MIDL</span><span class="sxs-lookup"><span data-stu-id="f7757-133">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="f7757-134">**LCID**</span><span class="sxs-lookup"><span data-stu-id="f7757-134">**lcid**</span></span>](lcid.md)
</dt> <dt>

[<span data-ttu-id="f7757-135">Esempio di file di FAD</span><span class="sxs-lookup"><span data-stu-id="f7757-135">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="f7757-136">Sintassi del file di FAD</span><span class="sxs-lookup"><span data-stu-id="f7757-136">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="f7757-137">**opzionale**</span><span class="sxs-lookup"><span data-stu-id="f7757-137">**optional**</span></span>](optional.md)
</dt> <dt>

[<span data-ttu-id="f7757-138">**out**</span><span class="sxs-lookup"><span data-stu-id="f7757-138">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="f7757-139">**propget**</span><span class="sxs-lookup"><span data-stu-id="f7757-139">**propget**</span></span>](propget.md)
</dt> <dt>

[<span data-ttu-id="f7757-140">**TYPEFLAGS**</span><span class="sxs-lookup"><span data-stu-id="f7757-140">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 