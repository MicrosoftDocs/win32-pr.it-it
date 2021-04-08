---
title: dispinterface (attributo)
description: L'istruzione dispatch definisce un set di proprietà e metodi sui quali è possibile chiamare IDispatch Invoke.
ms.assetid: d85a8e2b-0155-4d68-bb38-e86f4807e7de
keywords:
- attributo dispatch MIDL
topic_type:
- apiref
api_name:
- dispinterface
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f7cc2b6087b53ff81aa7270a209266dd8248884
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872494"
---
# <a name="dispinterface-attribute"></a><span data-ttu-id="dcd15-104">dispinterface (attributo)</span><span class="sxs-lookup"><span data-stu-id="dcd15-104">dispinterface attribute</span></span>

<span data-ttu-id="dcd15-105">L'istruzione **Dispatch** definisce un set di proprietà e metodi su cui è possibile chiamare **IDispatch:: Invoke**.</span><span class="sxs-lookup"><span data-stu-id="dcd15-105">The **dispinterface** statement defines a set of properties and methods on which you can call **IDispatch::Invoke**.</span></span> <span data-ttu-id="dcd15-106">Un'interfaccia dispatch può essere definita elencando in modo esplicito il set di metodi e proprietà supportati (sintassi 1) o elencando una singola interfaccia (sintassi 2).</span><span class="sxs-lookup"><span data-stu-id="dcd15-106">A dispinterface may be defined by explicitly listing the set of supported methods and properties (Syntax 1), or by listing a single interface (Syntax 2).</span></span>

``` syntax
[
    [attributes]
]
dispinterface dispinterface-name
{
    properties:
        property-list
    methods:
        method-list
};

[
  [attributes]
]
dispinterface dispinterface-name
{
    interface interface-name
};
```

## <a name="parameters"></a><span data-ttu-id="dcd15-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="dcd15-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcd15-108">*attributes*</span><span class="sxs-lookup"><span data-stu-id="dcd15-108">*attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="dcd15-109">Specifica gli attributi che si applicano all'intera **interfaccia dispatch**.</span><span class="sxs-lookup"><span data-stu-id="dcd15-109">Specifies attributes that apply to the entire **dispinterface**.</span></span> <span data-ttu-id="dcd15-110">Sono accettati gli attributi seguenti: **\[** [**helpstring**](helpstring.md) **\]** , **\[** [**HelpContext**](helpcontext.md) **\]** , fileguida **\[** [](helpfile.md) **\]** , **\[** [**Hidden**](hidden.md) **\]** , non **\[** [**estensibile**](nonextensible.md) **\]** , **\[** [**oleautomation**](oleautomation.md) **\]** , **\[** [**Restricted**](restricted.md) **\]** , **\[** [**UUID**](uuid.md) **\]** e **\[** [**Version**](version.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="dcd15-110">The following attributes are accepted: **\[**[**helpstring**](helpstring.md)**\]**, **\[**[**helpcontext**](helpcontext.md)**\]**, **\[**[**helpfile**](helpfile.md)**\]**, **\[**[**hidden**](hidden.md)**\]**, **\[**[**nonextensible**](nonextensible.md)**\]**, **\[**[**oleautomation**](oleautomation.md)**\]**, **\[**[**restricted**](restricted.md)**\]**, **\[**[**uuid**](uuid.md)**\]**, and **\[**[**version**](version.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="dcd15-111">*dispatch-nome*</span><span class="sxs-lookup"><span data-stu-id="dcd15-111">*dispinterface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="dcd15-112">Nome con cui l' **interfaccia dispatch** è nota nella libreria dei tipi.</span><span class="sxs-lookup"><span data-stu-id="dcd15-112">The name by which the **dispinterface** is known in the type library.</span></span> <span data-ttu-id="dcd15-113">Questo nome deve essere univoco all'interno della libreria dei tipi.</span><span class="sxs-lookup"><span data-stu-id="dcd15-113">This name must be unique within the type library.</span></span>

</dd> <dt>

<span data-ttu-id="dcd15-114">*elenco proprietà*</span><span class="sxs-lookup"><span data-stu-id="dcd15-114">*property-list*</span></span> 
</dt> <dd>

<span data-ttu-id="dcd15-115">(Sintassi 1) Elenco facoltativo di proprietà supportate dall'oggetto, dichiarate sotto forma di variabili.</span><span class="sxs-lookup"><span data-stu-id="dcd15-115">(Syntax 1) An optional list of properties supported by the object, declared in the form of variables.</span></span> <span data-ttu-id="dcd15-116">Si tratta della forma abbreviata per dichiarare le funzioni di proprietà nell'elenco dei metodi.</span><span class="sxs-lookup"><span data-stu-id="dcd15-116">This is the short form for declaring the property functions in the methods list.</span></span> <span data-ttu-id="dcd15-117">Per informazioni dettagliate, vedere la sezione commenti.</span><span class="sxs-lookup"><span data-stu-id="dcd15-117">See the comments section for details.</span></span>

</dd> <dt>

<span data-ttu-id="dcd15-118">*elenco di metodi*</span><span class="sxs-lookup"><span data-stu-id="dcd15-118">*method-list*</span></span> 
</dt> <dd>

<span data-ttu-id="dcd15-119">(Sintassi 1) Elenco che comprende un prototipo di funzione per ogni metodo e proprietà nell' **interfaccia dispatch**.</span><span class="sxs-lookup"><span data-stu-id="dcd15-119">(Syntax 1) A list comprising a function prototype for each method and property in the **dispinterface**.</span></span> <span data-ttu-id="dcd15-120">In *meth* è possibile visualizzare un numero qualsiasi di definizioni di funzione.</span><span class="sxs-lookup"><span data-stu-id="dcd15-120">Any number of function definitions can appear in *methlist*.</span></span> <span data-ttu-id="dcd15-121">Una funzione in *meth* è il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="dcd15-121">A function in *methlist* has the following form:</span></span>

<span data-ttu-id="dcd15-122">**\[  attributi \]** *returnType MethName tipo paramName ***(*** params \* \* *);**</span><span class="sxs-lookup"><span data-stu-id="dcd15-122">**\[***attributes***\]** *returntype methname type paramname ***(*** params\*\*\*);*\*</span></span>

<span data-ttu-id="dcd15-123">Gli attributi seguenti sono accettati in un metodo in un' **interfaccia dispatch**: **\[ helpstring \]**, **\[ HelpContext \]**, **\[** [**propget**](propget.md) **\]** , **\[** [**propput**](propput.md) **\]** , **\[** [**propputref**](propputref.md) **\]** , **\[** [**String**](string.md) **\]** e **\[** [**vararg**](vararg.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="dcd15-123">The following attributes are accepted on a method in a **dispinterface**: **\[helpstring\]**, **\[helpcontext\]**, **\[**[**propget**](propget.md)**\]**, **\[**[**propput**](propput.md)**\]**, **\[**[**propputref**](propputref.md)**\]**, **\[**[**string**](string.md)**\]**, and **\[**[**vararg**](vararg.md)**\]**.</span></span> <span data-ttu-id="dcd15-124">Se viene specificato **\[ \] vararg** , l'ultimo parametro deve essere una matrice sicura di tipo **Variant** .</span><span class="sxs-lookup"><span data-stu-id="dcd15-124">If **\[vararg\]** is specified, the last parameter must be a safe array of **VARIANT** type.</span></span>

<span data-ttu-id="dcd15-125">L'elenco di parametri è un elenco delimitato da virgole, in cui ogni elemento ha il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="dcd15-125">The parameter list is a comma-delimited list, each element of which has the following form:</span></span>

<span data-ttu-id="dcd15-126">**\[***attributi***\]**</span><span class="sxs-lookup"><span data-stu-id="dcd15-126">**\[***attributes***\]**</span></span>

<span data-ttu-id="dcd15-127">Il *tipo* può essere qualsiasi tipo dichiarato o incorporato o un puntatore a qualsiasi tipo.</span><span class="sxs-lookup"><span data-stu-id="dcd15-127">The *type* can be any declared or built-in type, or a pointer to any type.</span></span> <span data-ttu-id="dcd15-128">Gli attributi nei parametri sono:</span><span class="sxs-lookup"><span data-stu-id="dcd15-128">Attributes on parameters are:</span></span>

<span data-ttu-id="dcd15-129">**\[**[**in**](in.md) **\]** , **\[** [**out**](out-idl.md) **\]** , **\[** [**Optional**](optional.md) **\]** , **\[ stringa \]**</span><span class="sxs-lookup"><span data-stu-id="dcd15-129">**\[**[**in**](in.md)**\]**, **\[**[**out**](out-idl.md)**\]**, **\[**[**optional**](optional.md)**\]**, **\[string\]**</span></span>

</dd> <dt>

<span data-ttu-id="dcd15-130">*Nome interfaccia*</span><span class="sxs-lookup"><span data-stu-id="dcd15-130">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="dcd15-131">(Sintassi 2) Nome dell'interfaccia da dichiarare come interfaccia IDispatch.</span><span class="sxs-lookup"><span data-stu-id="dcd15-131">(Syntax 2) The name of the interface to declare as an IDispatch interface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dcd15-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="dcd15-132">Remarks</span></span>

<span data-ttu-id="dcd15-133">Il compilatore MIDL accetta l'ordinamento dei parametri seguente (da sinistra a destra):</span><span class="sxs-lookup"><span data-stu-id="dcd15-133">The MIDL compiler accepts the following parameter ordering (from left-to-right):</span></span>

1.  <span data-ttu-id="dcd15-134">Parametri obbligatori (parametri che non dispongono degli \[ \] attributi DefaultValue o \[ Optional \] ),</span><span class="sxs-lookup"><span data-stu-id="dcd15-134">Required parameters (parameters that do not have the \[defaultvalue\] or \[optional\] attributes),</span></span>
2.  <span data-ttu-id="dcd15-135">parametri facoltativi con o senza \[ l' \] attributo DefaultValue,</span><span class="sxs-lookup"><span data-stu-id="dcd15-135">optional parameters with or without the \[defaultvalue\] attribute,</span></span>
3.  <span data-ttu-id="dcd15-136">parametri con l' \[ \] attributo facoltativo e senza l' \[ \] attributo DefaultValue,</span><span class="sxs-lookup"><span data-stu-id="dcd15-136">parameters with the \[optional\] attribute and without the \[defaultvalue\] attribute,</span></span>
4.  <span data-ttu-id="dcd15-137">\[parametro [**LCID**](lcid.md) \] , se presente,</span><span class="sxs-lookup"><span data-stu-id="dcd15-137">\[ [**lcid**](lcid.md)\] parameter, if any,</span></span>
5.  <span data-ttu-id="dcd15-138">\[[**retval**](retval.md) \] parametro</span><span class="sxs-lookup"><span data-stu-id="dcd15-138">\[ [**retval**](retval.md)\] parameter</span></span>

<span data-ttu-id="dcd15-139">Le funzioni di metodo vengono specificate esattamente come descritto nella pagina di riferimento per il [**modulo**](module.md) , ad eccezione del fatto che l' \[ attributo [**entry**](entry.md) \] non è consentito.</span><span class="sxs-lookup"><span data-stu-id="dcd15-139">Method functions are specified exactly as described in the reference page for [**module**](module.md) except that the \[ [**entry**](entry.md)\] attribute is not allowed.</span></span> <span data-ttu-id="dcd15-140">Si noti che STDOLE32. TLB (STDOLE. È necessario importare TLB nei sistemi a 16 bit perché un' **interfaccia dispatch** eredita da IDispatch.</span><span class="sxs-lookup"><span data-stu-id="dcd15-140">Note that STDOLE32.TLB (STDOLE.TLB on 16-bit systems) must be imported, because a **dispinterface** inherits from IDispatch.</span></span>

<span data-ttu-id="dcd15-141">È possibile dichiarare le proprietà negli elenchi delle proprietà o dei metodi.</span><span class="sxs-lookup"><span data-stu-id="dcd15-141">You can declare properties in either the properties or methods lists.</span></span> <span data-ttu-id="dcd15-142">La dichiarazione delle proprietà nell'elenco delle proprietà non indica il tipo di accesso supportato dalla proprietà (ovvero Get, put o putref).</span><span class="sxs-lookup"><span data-stu-id="dcd15-142">Declaring properties in the properties list does not indicate the type of access the property supports (that is, get, put, or putref).</span></span> <span data-ttu-id="dcd15-143">Specificare l' \[ [](readonly.md) \] attributo ReadOnly per le proprietà che non supportano put o putref.</span><span class="sxs-lookup"><span data-stu-id="dcd15-143">Specify the \[ [**readonly**](readonly.md)\] attribute for properties that don't support put or putref.</span></span> <span data-ttu-id="dcd15-144">Se si dichiarano le funzioni di proprietà nell'elenco dei metodi, le funzioni per una proprietà hanno tutti lo stesso identificatore.</span><span class="sxs-lookup"><span data-stu-id="dcd15-144">If you declare the property functions in the methods list, functions for one property all have the same identifier.</span></span>

<span data-ttu-id="dcd15-145">Con la prima sintassi sono necessari i tag Properties: e:.</span><span class="sxs-lookup"><span data-stu-id="dcd15-145">Using the first syntax, the properties: and methods: tags are required.</span></span> <span data-ttu-id="dcd15-146">L' \[ attributo [**ID**](id.md) \] è obbligatorio anche per ogni membro.</span><span class="sxs-lookup"><span data-stu-id="dcd15-146">The \[ [**id**](id.md)\] attribute is also required on each member.</span></span> <span data-ttu-id="dcd15-147">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="dcd15-147">For example:</span></span>

``` syntax
properties: 
    [id(0)] int Value;    // Default property. 
methods: 
    [id(1)] HRESULT Show();
```

<span data-ttu-id="dcd15-148">A differenza dei membri di interfaccia, i membri dell'interfaccia dispatch non possono usare l'attributo [**retval**](retval.md) per restituire un valore oltre a un codice di errore HRESULT.</span><span class="sxs-lookup"><span data-stu-id="dcd15-148">Unlike interface members, dispinterface members cannot use the [**retval**](retval.md) attribute to return a value in addition to an HRESULT error code.</span></span> <span data-ttu-id="dcd15-149">L' \[ [](lcid.md) \] attributo LCID è altrettanto non valido per dispinterfaces, perché IDispatch:: Invoke passa un LCID.</span><span class="sxs-lookup"><span data-stu-id="dcd15-149">The \[ [**lcid**](lcid.md)\] attribute is likewise invalid for dispinterfaces, because IDispatch::Invoke passes an LCID.</span></span> <span data-ttu-id="dcd15-150">Tuttavia, è possibile dichiarare nuovamente un'interfaccia che utilizza questi attributi.</span><span class="sxs-lookup"><span data-stu-id="dcd15-150">However, it is possible to redeclare an interface that uses these attributes.</span></span>

<span data-ttu-id="dcd15-151">Utilizzando la seconda sintassi, le interfacce che supportano IDispatch e vengono dichiarate in precedenza in uno script FAD possono essere ridichiarate come interfacce IDispatch come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="dcd15-151">Using the second syntax, interfaces that support IDispatch and are declared earlier in an ODL script can be redeclared as IDispatch interfaces as follows:</span></span>

``` syntax
dispinterface helloPro 
{ 
    interface hello; 
};
```

<span data-ttu-id="dcd15-152">Nell'esempio precedente vengono dichiarati tutti i membri di Hello e tutti i membri che Hello eredita come supporto IDispatch.</span><span class="sxs-lookup"><span data-stu-id="dcd15-152">The preceding example declares all the members of hello and all the members that hello inherits as supporting IDispatch.</span></span> <span data-ttu-id="dcd15-153">In questo caso, se Hello venisse dichiarato in precedenza con \[ \] \[ i membri LCID e retval \] che restituivano HRESULT, MkTypLib rimuoverebbe ogni \[ \] parametro LCID e il tipo restituito HRESULT e invece contrassegnerà il tipo restituito come quello del \[ \] parametro retval.</span><span class="sxs-lookup"><span data-stu-id="dcd15-153">In this case, if hello were declared earlier with \[lcid\] and \[retval\] members that returned HRESULTs, MkTypLib would remove each \[lcid\] parameter and HRESULT return type, and instead mark the return type as that of the \[retval\] parameter.</span></span>

> [!Note]  
> <span data-ttu-id="dcd15-154">Lo strumento Mktyplib.exe è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="dcd15-154">The Mktyplib.exe tool is obsolete.</span></span> <span data-ttu-id="dcd15-155">Usare invece il compilatore MIDL.</span><span class="sxs-lookup"><span data-stu-id="dcd15-155">Use the MIDL compiler instead.</span></span>

 

<span data-ttu-id="dcd15-156">Le proprietà e i metodi di un'interfaccia dispatch non fanno parte di VTBL dell'interfaccia dispatch.</span><span class="sxs-lookup"><span data-stu-id="dcd15-156">The properties and methods of a dispinterface are not part of the VTBL of the dispinterface.</span></span> <span data-ttu-id="dcd15-157">Di conseguenza, non è possibile usare [CreateStdDispatch](/windows/win32/api/oleauto/nf-oleauto-createstddispatch) e [DispInvoke](/windows/win32/api/oleauto/nf-oleauto-dispinvoke) per implementare IDispatch:: Invoke.</span><span class="sxs-lookup"><span data-stu-id="dcd15-157">Consequently, [CreateStdDispatch](/windows/win32/api/oleauto/nf-oleauto-createstddispatch) and [DispInvoke](/windows/win32/api/oleauto/nf-oleauto-dispinvoke) cannot be used to implement IDispatch::Invoke.</span></span> <span data-ttu-id="dcd15-158">L'interfaccia dispatch viene usata quando un'applicazione deve esporre le funzioni non VTBL esistenti tramite l'automazione.</span><span class="sxs-lookup"><span data-stu-id="dcd15-158">The dispinterface is used when an application needs to expose existing non-VTBL functions through Automation.</span></span> <span data-ttu-id="dcd15-159">Queste applicazioni possono implementare IDispatch:: Invoke esaminando il parametro dispidMember e chiamando direttamente la funzione corrispondente.</span><span class="sxs-lookup"><span data-stu-id="dcd15-159">These applications can implement IDispatch::Invoke by examining the dispidMember parameter and directly calling the corresponding function.</span></span>

## <a name="examples"></a><span data-ttu-id="dcd15-160">Esempi</span><span class="sxs-lookup"><span data-stu-id="dcd15-160">Examples</span></span>

``` syntax
[ 
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676), 
    version(1.0), 
    helpstring("Useful help string."), 
    helpcontext(2480)
] 
dispinterface MyDispatchObject 
{ 
    properties: 
        [id(1)] int x;    //An integer property named x 
        [id(2)] BSTR y;   //A string property named y 
    methods: 
        [id(3)] HRESULT show();    //No arguments, no result 
        [id(11)] int computeit(int inarg, double *outarg); 
}; 
 
[
    uuid(1e123456-1f3c-1069-996b-00dd010fe676)
] 
dispinterface MyObject 
{ 
    properties: 
    methods: 
        [id(1), propget, bindable, defaultbind, displaybind] long x(); 
 
        [id(1), propput, bindable, defaultbind, 
         displaybind] HRESULT x(long rhs); 
}
```

## <a name="see-also"></a><span data-ttu-id="dcd15-161">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="dcd15-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcd15-162">**bindable**</span><span class="sxs-lookup"><span data-stu-id="dcd15-162">**bindable**</span></span>](bindable.md)
</dt> <dt>

[<span data-ttu-id="dcd15-163">**defaultbind**</span><span class="sxs-lookup"><span data-stu-id="dcd15-163">**defaultbind**</span></span>](defaultbind.md)
</dt> <dt>

[<span data-ttu-id="dcd15-164">**displaybind**</span><span class="sxs-lookup"><span data-stu-id="dcd15-164">**displaybind**</span></span>](displaybind.md)
</dt> <dt>

[<span data-ttu-id="dcd15-165">**helpcontext**</span><span class="sxs-lookup"><span data-stu-id="dcd15-165">**helpcontext**</span></span>](helpcontext.md)
</dt> <dt>

[<span data-ttu-id="dcd15-166">**helpfile**</span><span class="sxs-lookup"><span data-stu-id="dcd15-166">**helpfile**</span></span>](helpfile.md)
</dt> <dt>

[<span data-ttu-id="dcd15-167">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="dcd15-167">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="dcd15-168">**nascosto**</span><span class="sxs-lookup"><span data-stu-id="dcd15-168">**hidden**</span></span>](hidden.md)
</dt> <dt>

[<span data-ttu-id="dcd15-169">**in**</span><span class="sxs-lookup"><span data-stu-id="dcd15-169">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="dcd15-170">**interfaccia**</span><span class="sxs-lookup"><span data-stu-id="dcd15-170">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="dcd15-171">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="dcd15-171">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="dcd15-172">Sintassi del file di FAD</span><span class="sxs-lookup"><span data-stu-id="dcd15-172">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="dcd15-173">Esempio di file di FAD</span><span class="sxs-lookup"><span data-stu-id="dcd15-173">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="dcd15-174">Generazione di una libreria dei tipi con MIDL</span><span class="sxs-lookup"><span data-stu-id="dcd15-174">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="dcd15-175">**opzionale**</span><span class="sxs-lookup"><span data-stu-id="dcd15-175">**optional**</span></span>](optional.md)
</dt> <dt>

[<span data-ttu-id="dcd15-176">**out**</span><span class="sxs-lookup"><span data-stu-id="dcd15-176">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="dcd15-177">**nonextensible**</span><span class="sxs-lookup"><span data-stu-id="dcd15-177">**nonextensible**</span></span>](nonextensible.md)
</dt> <dt>

[<span data-ttu-id="dcd15-178">**propget**</span><span class="sxs-lookup"><span data-stu-id="dcd15-178">**propget**</span></span>](propget.md)
</dt> <dt>

[<span data-ttu-id="dcd15-179">**propput**</span><span class="sxs-lookup"><span data-stu-id="dcd15-179">**propput**</span></span>](propput.md)
</dt> <dt>

[<span data-ttu-id="dcd15-180">**propputref**</span><span class="sxs-lookup"><span data-stu-id="dcd15-180">**propputref**</span></span>](propputref.md)
</dt> <dt>

[<span data-ttu-id="dcd15-181">**oleautomation**</span><span class="sxs-lookup"><span data-stu-id="dcd15-181">**oleautomation**</span></span>](oleautomation.md)
</dt> <dt>

[<span data-ttu-id="dcd15-182">**limitato**</span><span class="sxs-lookup"><span data-stu-id="dcd15-182">**restricted**</span></span>](restricted.md)
</dt> <dt>

[<span data-ttu-id="dcd15-183">**string**</span><span class="sxs-lookup"><span data-stu-id="dcd15-183">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="dcd15-184">**uuid**</span><span class="sxs-lookup"><span data-stu-id="dcd15-184">**uuid**</span></span>](uuid.md)
</dt> <dt>

[<span data-ttu-id="dcd15-185">**vararg**</span><span class="sxs-lookup"><span data-stu-id="dcd15-185">**vararg**</span></span>](vararg.md)
</dt> <dt>

[<span data-ttu-id="dcd15-186">**Versione**</span><span class="sxs-lookup"><span data-stu-id="dcd15-186">**version**</span></span>](version.md)
</dt> </dl>

 

 