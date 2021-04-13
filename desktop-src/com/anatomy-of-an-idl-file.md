---
title: Anatomia di un file IDL
description: In questi file IDL di esempio vengono illustrati i costrutti fondamentali della definizione dell'interfaccia.
ms.assetid: 9c276b8a-5342-4c09-91a7-c9a9f0f83c73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acbcfbf5c145a1fb389cc26543cf75d8cc75a107
ms.sourcegitcommit: 5ebaf3a456bc68cd0c6bd46c8135b67b1bf6fa54
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "104351011"
---
# <a name="anatomy-of-an-idl-file"></a><span data-ttu-id="49137-103">Anatomia di un file IDL</span><span class="sxs-lookup"><span data-stu-id="49137-103">Anatomy of an IDL File</span></span>

<span data-ttu-id="49137-104">In questi file IDL di esempio vengono illustrati i costrutti fondamentali della definizione dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="49137-104">These example IDL files demonstrate the fundamental constructs of interface definition.</span></span> <span data-ttu-id="49137-105">L'allocazione di memoria, il marshalling personalizzato e la messaggistica asincrona sono solo alcune delle funzionalità che è possibile implementare in un'interfaccia COM personalizzata.</span><span class="sxs-lookup"><span data-stu-id="49137-105">Memory allocation, custom marshaling, and asynchronous messaging are just a few of the features you can implement in a custom COM interface.</span></span> <span data-ttu-id="49137-106">Gli attributi MIDL vengono utilizzati per definire le interfacce COM.</span><span class="sxs-lookup"><span data-stu-id="49137-106">MIDL attributes are used to define COM interfaces.</span></span> <span data-ttu-id="49137-107">Per ulteriori informazioni sull'implementazione di interfacce e librerie dei tipi, incluso un riepilogo degli attributi MIDL, vedere [definizioni di interfaccia e librerie dei tipi](/windows/desktop/Midl/interface-definitions-and-type-libraries) nella guida e guida di riferimento per programmatori MIDL.</span><span class="sxs-lookup"><span data-stu-id="49137-107">For more information about implementing interfaces and type libraries, including a summary of MIDL attributes, see [Interface Definitions and Type Libraries](/windows/desktop/Midl/interface-definitions-and-type-libraries) in the MIDL Programmer's Guide and Reference.</span></span> <span data-ttu-id="49137-108">Per un riferimento completo di tutti gli attributi, le parole chiave e le direttive MIDL, vedere le informazioni di [riferimento sul linguaggio MIDL](/windows/desktop/Midl/midl-language-reference).</span><span class="sxs-lookup"><span data-stu-id="49137-108">For a complete reference of all MIDL attributes, keywords, and directives, see the [MIDL Language Reference](/windows/desktop/Midl/midl-language-reference).</span></span>

## <a name="exampleidl"></a><span data-ttu-id="49137-109">Esempio di IDL</span><span class="sxs-lookup"><span data-stu-id="49137-109">Example.idl</span></span>

<span data-ttu-id="49137-110">Il file IDL di esempio seguente definisce due interfacce COM.</span><span class="sxs-lookup"><span data-stu-id="49137-110">The following example IDL file defines two COM interfaces.</span></span> <span data-ttu-id="49137-111">Da questo file IDL Midl.exe genererà i file di intestazione e il codice di marshalling e di marshalling.</span><span class="sxs-lookup"><span data-stu-id="49137-111">From this IDL file, Midl.exe will generate proxy/stub and marshaling code and header files.</span></span> <span data-ttu-id="49137-112">Una dissezione riga per riga segue l'esempio.</span><span class="sxs-lookup"><span data-stu-id="49137-112">A line-by-line dissection follows the example.</span></span>

``` syntax
//
// Example.idl 
//
import "mydefs.h","unknwn.idl"; 
[
object,
uuid(a03d1420-b1ec-11d0-8c3a-00c04fc31d2f),
] interface IFace1 : IUnknown
{
HRESULT MethodA([in] short Bread, [out] BKFST * pBToast);
HRESULT MethodB([in, out] BKFST * pBPoptart);
};
 
[
object,
uuid(a03d1421-b1ec-11d0-8c3a-00c04fc31d2f),
pointer_default(unique)
] interface IFace2 : IUnknown
{
HRESULT MethodC([in] long Max,
                [in, max_is(Max)] BkfstStuff[ ],
                [out] long * pSize,
                [out, size_is( , *pSize)] BKFST ** ppBKFST);
}; 
 
```

<span data-ttu-id="49137-113">L'istruzione di [**importazione**](/windows/desktop/Midl/import) IDL viene utilizzata qui per inserire un file di intestazione, Mydefs. h, che contiene i tipi definiti dall'utente e Unknwn. idl, che contiene la definizione di [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), da cui derivano IFace1 e IFace2.</span><span class="sxs-lookup"><span data-stu-id="49137-113">The IDL [**import**](/windows/desktop/Midl/import) statement is used here to bring in a header file, Mydefs.h, which contains user-defined types, and Unknwn.idl, which contains the definition of [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), from which IFace1 and IFace2 derive.</span></span>

<span data-ttu-id="49137-114">L'attributo [**Object**](/windows/desktop/Midl/object) identifica l'interfaccia come un'interfaccia oggetto e indica al compilatore MIDL di generare codice proxy/stub anziché stub client e server RPC.</span><span class="sxs-lookup"><span data-stu-id="49137-114">The [**object**](/windows/desktop/Midl/object) attribute identifies the interface as an object interface and tells the MIDL compiler to generate proxy/stub code instead of RPC client and server stubs.</span></span> <span data-ttu-id="49137-115">I metodi dell'interfaccia oggetto devono avere un tipo restituito [**HRESULT**](/openspecs/windows_protocols/ms-erref/0642cb2f-2075-4469-918c-4441e69c548a), per consentire al meccanismo RPC sottostante di segnalare gli errori per le chiamate che non vengono completate a causa di problemi di rete.</span><span class="sxs-lookup"><span data-stu-id="49137-115">Object interface methods must have a return type of [**HRESULT**](/openspecs/windows_protocols/ms-erref/0642cb2f-2075-4469-918c-4441e69c548a), to allow the underlying RPC mechanism to report errors for calls that fail to complete due to network problems.</span></span>

<span data-ttu-id="49137-116">L'attributo [**UUID**](/windows/desktop/Midl/uuid) specifica l'identificatore di interfaccia (IID).</span><span class="sxs-lookup"><span data-stu-id="49137-116">The [**uuid**](/windows/desktop/Midl/uuid) attribute specifies the interface identifier (IID).</span></span> <span data-ttu-id="49137-117">Ogni interfaccia, classe e libreria dei tipi deve essere identificata con il relativo identificatore univoco.</span><span class="sxs-lookup"><span data-stu-id="49137-117">Each interface, class, and type library must be identified with its own unique identifier.</span></span> <span data-ttu-id="49137-118">Utilizzare l'utilità Uuidgen.exe per generare un set di ID univoci per le interfacce e altri componenti.</span><span class="sxs-lookup"><span data-stu-id="49137-118">Use the utility Uuidgen.exe to generate a set of unique IDs for your interfaces and other components.</span></span>

<span data-ttu-id="49137-119">La parola chiave [**Interface**](/windows/desktop/Midl/interface) definisce il nome dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="49137-119">The [**interface**](/windows/desktop/Midl/interface) keyword defines the interface name.</span></span> <span data-ttu-id="49137-120">Tutte le interfacce oggetto devono derivare, direttamente o indirettamente, da [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown).</span><span class="sxs-lookup"><span data-stu-id="49137-120">All object interfaces must derive, directly or indirectly, from [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown).</span></span>

<span data-ttu-id="49137-121">Il parametro [**in**](/windows/desktop/Midl/in) direzionale specifica un parametro che viene impostato solo dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="49137-121">The [**in**](/windows/desktop/Midl/in) directional parameter specifies a parameter that is set only by the caller.</span></span> <span data-ttu-id="49137-122">Il parametro [**out**](/windows/desktop/Midl/out-idl) specifica i dati che vengono passati di nuovo al chiamante.</span><span class="sxs-lookup"><span data-stu-id="49137-122">The [**out**](/windows/desktop/Midl/out-idl) parameter specifies data that is passed back to the caller.</span></span> <span data-ttu-id="49137-123">L'uso di entrambi gli attributi direzionali in un parametro specifica che il parametro viene usato sia per inviare dati al metodo che per passare i dati al chiamante.</span><span class="sxs-lookup"><span data-stu-id="49137-123">Using both directional attributes on one parameter specifies that the parameter is used both to send data to the method and to pass data back to the caller.</span></span>

<span data-ttu-id="49137-124">L' [**attributo \_ default del puntatore**](/windows/desktop/Midl/pointer-default) specifica il tipo di puntatore predefinito ([**Unique**](/windows/desktop/Midl/unique), [**ref**](/windows/desktop/Midl/ref)o [**ptr**](/windows/desktop/Midl/ptr)) per tutti i puntatori tranne quelli inclusi negli elenchi di parametri.</span><span class="sxs-lookup"><span data-stu-id="49137-124">The [**pointer\_default**](/windows/desktop/Midl/pointer-default) attribute specifies the default pointer type ([**unique**](/windows/desktop/Midl/unique), [**ref**](/windows/desktop/Midl/ref), or [**ptr**](/windows/desktop/Midl/ptr)) for all pointers except for those included in parameter lists.</span></span> <span data-ttu-id="49137-125">Se non viene specificato alcun tipo predefinito, MIDL presuppone che i puntatori singoli siano **univoci**.</span><span class="sxs-lookup"><span data-stu-id="49137-125">If no default type is specified, MIDL assumes that single pointers are **unique**.</span></span> <span data-ttu-id="49137-126">Tuttavia, quando si dispone di più livelli di puntatori, è necessario specificare in modo esplicito un tipo di puntatore predefinito, anche se si desidera che il tipo predefinito sia **univoco**.</span><span class="sxs-lookup"><span data-stu-id="49137-126">However, when you have multiple levels of pointers, you must explicitly specify a default pointer type, even if you want the default type to be **unique**.</span></span>

<span data-ttu-id="49137-127">Nell'esempio precedente, la matrice BkfstStuff \[ \] è una *matrice conforme*, la cui dimensione è determinata in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="49137-127">In the preceding example, the array BkfstStuff\[ \] is a *conformant array*, the size of which is determined at run time.</span></span> <span data-ttu-id="49137-128">L'attributo [**Max \_ is**](/windows/desktop/Midl/max-is) specifica la variabile che contiene il valore massimo per l'indice della matrice.</span><span class="sxs-lookup"><span data-stu-id="49137-128">The [**max\_is**](/windows/desktop/Midl/max-is) attribute specifies the variable that contains the maximum value for the array index.</span></span>

<span data-ttu-id="49137-129">L'attributo [**size \_ è**](/windows/desktop/Midl/size-is) usato anche per specificare la dimensione di una matrice o, come nell'esempio precedente, più livelli di puntatori.</span><span class="sxs-lookup"><span data-stu-id="49137-129">The [**size\_is**](/windows/desktop/Midl/size-is) attribute is also used to specify the size of an array or, as in the preceding example, multiple levels of pointers.</span></span> <span data-ttu-id="49137-130">Nell'esempio, la chiamata può essere effettuata senza conoscere in anticipo la quantità di dati che verranno restituiti.</span><span class="sxs-lookup"><span data-stu-id="49137-130">In the example, the call can be made without knowing in advance how much data will be returned.</span></span>

## <a name="example2idl"></a><span data-ttu-id="49137-131">Example2. idl</span><span class="sxs-lookup"><span data-stu-id="49137-131">Example2.idl</span></span>

<span data-ttu-id="49137-132">Nell'esempio IDL seguente, che riutilizza le interfacce descritte nell'esempio IDL precedente, vengono illustrati i vari modi per generare informazioni sulla libreria dei tipi per le interfacce.</span><span class="sxs-lookup"><span data-stu-id="49137-132">The following IDL example (which reuses the interfaces described in the previous IDL example) shows the various ways to generate type library information for interfaces.</span></span>

``` syntax
//
// Example2.idl
//

import "example.idl","oaidl.idl"; 

[
uuid(a03d1422-b1ec-11d0-8c3a-00c04fc31d2f),
helpstring("IFace3 interface"),
pointer_default(unique);
dual,
oleautomation
] 
interface IFace3 : IDispatch
{
   HRESULT MethodD([in] BSTR OrderIn,
                   [out, retval] * pTakeOut);
}; //end IFace3 def

[
uuid(a03d1423-b1ec-11d0-8c3a-00c04fc31d2f),
version(1.0),
helpstring("Example Type Library"),
] library ExampleLib
{
  importlib("stdole32.tlb");
  interface IFace3;
  [
  uuid(a03d1424-b1ec-11d0-8c3a-00c04fc31d2f),
  helpstring("Breakfast Component Class")
  ] coclass BkfstComponent
    {
    [default]interface IFace1;
    interfaceIFace2
    }; //end coclass def

[
uuid(a03d1424-b1ec-11d0-8c3a-00c04fc31d2f),
helpstring("IFace4 interface"),
pointer_default(unique);
dual,
oleautomation
] 
interface IFace4 : IDispatch
{
[propput] HRESULT MethodD([in] BSTR OrderIn);
[propget] HRESULT MethodE([out, retval] * pTakeOut);
}; //end IFace4 def
 
}; //end library def
 
```

<span data-ttu-id="49137-133">L'attributo [**helpstring**](/windows/desktop/Midl/helpstring) è facoltativo. viene usato per descrivere brevemente l'oggetto o per fornire una riga di stato.</span><span class="sxs-lookup"><span data-stu-id="49137-133">The [**helpstring**](/windows/desktop/Midl/helpstring) attribute is optional; you use it to briefly describe the object or to provide a status line.</span></span> <span data-ttu-id="49137-134">Queste stringhe della guida sono leggibili con un Visualizzatore oggetti, ad esempio quello fornito con Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="49137-134">These help strings are readable with an object browser such as the one provided with Microsoft Visual Basic.</span></span>

<span data-ttu-id="49137-135">L'attributo [**duale**](/windows/desktop/Midl/dual) in IFace3 crea un'interfaccia che è sia un'interfaccia dispatch che un'interfaccia com.</span><span class="sxs-lookup"><span data-stu-id="49137-135">The [**dual**](/windows/desktop/Midl/dual) attribute on IFace3 creates an interface that is both a dispatch interface and a COM interface.</span></span> <span data-ttu-id="49137-136">Poiché è derivato da **IDispatch**, un'interfaccia duale supporta l'automazione, che è l'elemento specificato dall'attributo [**oleautomation**](/windows/desktop/Midl/oleautomation) .</span><span class="sxs-lookup"><span data-stu-id="49137-136">Because it is derived from **IDispatch**, a dual interface supports Automation, which is what the [**oleautomation**](/windows/desktop/Midl/oleautomation) attribute specifies.</span></span> <span data-ttu-id="49137-137">IFace3 importa OAIDL. idl per ottenere la definizione di **IDispatch**.</span><span class="sxs-lookup"><span data-stu-id="49137-137">IFace3 imports Oaidl.idl to get the definition of **IDispatch**.</span></span>

<span data-ttu-id="49137-138">L'istruzione [**Library**](/windows/desktop/Midl/library) definisce la libreria dei tipi ExampleLib, che ha gli attributi [**UUID**](/windows/desktop/Midl/uuid), [**helpstring**](/windows/desktop/Midl/helpstring)e [**Version**](/windows/desktop/Midl/version) .</span><span class="sxs-lookup"><span data-stu-id="49137-138">The [**library**](/windows/desktop/Midl/library) statement defines the ExampleLib type library, which has its own [**uuid**](/windows/desktop/Midl/uuid), [**helpstring**](/windows/desktop/Midl/helpstring), and [**version**](/windows/desktop/Midl/version) attributes.</span></span>

<span data-ttu-id="49137-139">All'interno della definizione della libreria dei tipi, la direttiva [**importlib**](/windows/desktop/Midl/importlib) porta in una libreria dei tipi compilata.</span><span class="sxs-lookup"><span data-stu-id="49137-139">Within the type library definition, the [**importlib**](/windows/desktop/Midl/importlib) directive brings in a compiled type library.</span></span> <span data-ttu-id="49137-140">Tutte le definizioni di librerie dei tipi devono inserire la libreria dei tipi di base definita in Stdole32. tlb.</span><span class="sxs-lookup"><span data-stu-id="49137-140">All type library definitions should bring in the base type library defined in Stdole32.tlb.</span></span>

<span data-ttu-id="49137-141">Questa definizione della libreria dei tipi illustra tre modi diversi per includere le interfacce nella libreria dei tipi.</span><span class="sxs-lookup"><span data-stu-id="49137-141">This type library definition demonstrates three different ways to include interfaces in the type library.</span></span> <span data-ttu-id="49137-142">IFace3 è incluso semplicemente facendo riferimento all'interno dell'istruzione Library.</span><span class="sxs-lookup"><span data-stu-id="49137-142">IFace3 is included merely by referencing it within the library statement.</span></span>

<span data-ttu-id="49137-143">L'istruzione [**coclass**](/windows/desktop/Midl/coclass) definisce una classe di componenti completamente nuova, BkfstComponent, che include due interfacce definite in precedenza, IFace1 e IFace2.</span><span class="sxs-lookup"><span data-stu-id="49137-143">The [**coclass**](/windows/desktop/Midl/coclass) statement defines an entirely new component class, BkfstComponent, that includes two previously defined interfaces, IFace1 and IFace2.</span></span> <span data-ttu-id="49137-144">L'attributo default designa IFace1 come interfaccia predefinita.</span><span class="sxs-lookup"><span data-stu-id="49137-144">The default attribute designates IFace1 as the default interface.</span></span>

<span data-ttu-id="49137-145">IFace4 è descritto nell'istruzione Library.</span><span class="sxs-lookup"><span data-stu-id="49137-145">IFace4 is described within the library statement.</span></span> <span data-ttu-id="49137-146">L'attributo [**propput**](/windows/desktop/Midl/propput) su methodd indica che il metodo esegue un'azione set su una proprietà con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="49137-146">The [**propput**](/windows/desktop/Midl/propput) attribute on MethodD indicates that the method performs a set action on a property of the same name.</span></span> <span data-ttu-id="49137-147">L'attributo [**propget**](/windows/desktop/Midl/propget) indica che il metodo recupera informazioni da una proprietà con lo stesso nome del metodo.</span><span class="sxs-lookup"><span data-stu-id="49137-147">The [**propget**](/windows/desktop/Midl/propget) attribute indicates that the method retrieves information from a property of the same name as the method.</span></span> <span data-ttu-id="49137-148">L'attributo [**retval**](/windows/desktop/Midl/retval) in methodd definisce un parametro di output che contiene il valore restituito della funzione.</span><span class="sxs-lookup"><span data-stu-id="49137-148">The [**retval**](/windows/desktop/Midl/retval) attribute in MethodD designates an output parameter that contains the return value of the function.</span></span>

 

 
