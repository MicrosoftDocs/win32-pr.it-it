---
title: Esempio per la risoluzione dei conflitti di nomi di funzione
description: In questo argomento viene descritto come risolvere i conflitti di nomi di funzione quando si crea un'estensione per ADSI.
ms.assetid: 8121f037-3845-44ba-a2cd-8d7f15e0beb2
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, esempio di codice Visual Basic, risoluzione dei conflitti di nomi di funzione
- risoluzione dei conflitti di nomi di funzione ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 049f9ce6447bf6d6ead783db3e34f74374333f10
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104339247"
---
# <a name="example-for-resolving-function-name-conflicts"></a><span data-ttu-id="1ac85-105">Esempio per la risoluzione dei conflitti di nomi di funzione</span><span class="sxs-lookup"><span data-stu-id="1ac85-105">Example for Resolving Function Name Conflicts</span></span>

<span data-ttu-id="1ac85-106">Considerare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="1ac85-106">Consider the following:</span></span>

-   <span data-ttu-id="1ac85-107">IADs0 non supporta Func0.</span><span class="sxs-lookup"><span data-stu-id="1ac85-107">IADs0 does not support Func0.</span></span>
-   <span data-ttu-id="1ac85-108">IADs1 supporta func1 e Func0.</span><span class="sxs-lookup"><span data-stu-id="1ac85-108">IADs1 supports Func1 and Func0.</span></span>
-   <span data-ttu-id="1ac85-109">IADs2 supporta Func2 e Func0.</span><span class="sxs-lookup"><span data-stu-id="1ac85-109">IADs2 supports Func2 and Func0.</span></span>

<span data-ttu-id="1ac85-110">Tutte e tre le interfacce sono interfacce duali.</span><span class="sxs-lookup"><span data-stu-id="1ac85-110">All three interfaces are dual interfaces.</span></span>


```C++
IADs0 : IDispatch
{
    OtherFunc();
}

IADs1 : IDispatch
{
    Func0() 
    Func1();
}

IADs2 : IDispatch
{
    Func0()
    Func2();
}
```




```VB
Dim myInf1 as IADs1
 
myInf1.Func1  ' IADs1::Func1 is invoked using direct vtable access 
 
myInf1.Func2  ' IADs2::Func2 is invoked using GetIDsOfNames/Invoke
```



<span data-ttu-id="1ac85-111">Tenere presente che anche se IADs1 non supporta Func2, un client ADSI riconosce un [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) che supporta tutte le interfacce dual e dispatch nel modello.</span><span class="sxs-lookup"><span data-stu-id="1ac85-111">Be aware that even though IADs1 does not support Func2, an ADSI client recognizes one [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that supports all the dual and dispatch interfaces in the model.</span></span> <span data-ttu-id="1ac85-112">Pertanto, il client ADSI può chiamare direttamente Func2 usando myInf1. Func2 senza risolvere l'interfaccia che supporta Func2.</span><span class="sxs-lookup"><span data-stu-id="1ac85-112">Thus, the ADSI client can directly call Func2 using myInf1.Func2 without resolving which interface supports Func2.</span></span>


```VB
myInf1.Func2
```



<span data-ttu-id="1ac85-113">Sia IADs1 che IADs2 hanno una funzione denominata Func0, ma IADs1:: Func0 viene richiamata direttamente usando l'accesso vtable, perché entrambe le condizioni seguenti si applicano al client:</span><span class="sxs-lookup"><span data-stu-id="1ac85-113">Both IADs1 and IADs2 have a function called Func0, but IADs1::Func0 is invoked directly using vtable access, because both of following apply to the client:</span></span>

-   <span data-ttu-id="1ac85-114">Il client dispone di un puntatore a un oggetto IADs1 a doppia interfaccia con una funzione denominata Func0.</span><span class="sxs-lookup"><span data-stu-id="1ac85-114">The client has a pointer to dual interface IADs1 object, which has a function called Func0.</span></span>
-   <span data-ttu-id="1ac85-115">Visual Basic supporta l'accesso diretto a vtable, supponendo che il tipo di dati sia disponibile tramite la libreria dei tipi.</span><span class="sxs-lookup"><span data-stu-id="1ac85-115">Visual Basic supports direct vtable access, assuming that type of data is available through the type library.</span></span>

<span data-ttu-id="1ac85-116">Nell'esempio di codice successivo il client dispone di un puntatore a interfaccia duale a IADs2 anziché IADs1.</span><span class="sxs-lookup"><span data-stu-id="1ac85-116">In the next code example, the client has a dual interface pointer to IADs2 instead of IADs1.</span></span> <span data-ttu-id="1ac85-117">Pertanto, IADs2:: Func0 viene richiamato utilizzando l'accesso diretto a vtable.</span><span class="sxs-lookup"><span data-stu-id="1ac85-117">Therefore, IADs2::Func0 is invoked using direct vtable access.</span></span>


```VB
Dim myInf2 as IADs2
Set myInf2 = myInf1 ' Query for pointer to IADs2 
myInf2.Func0
```



<span data-ttu-id="1ac85-118">Anche in questo caso, nell'esempio di codice successivo, IADs1 e IADs2 hanno una funzione denominata Func0, ma in questo caso il client dispone di un puntatore a una doppia interfaccia, IADs0, che non dispone di una funzione denominata Func0.</span><span class="sxs-lookup"><span data-stu-id="1ac85-118">Again, in the next code example, both IADs1 and IADs2 have a function called Func0, but, here, the client has a pointer to a dual interface, IADs0, which does not have a function called Func0.</span></span> <span data-ttu-id="1ac85-119">Non è pertanto possibile eseguire alcun accesso diretto a vtable.</span><span class="sxs-lookup"><span data-stu-id="1ac85-119">Therefore, no direct vtable access can be performed.</span></span> <span data-ttu-id="1ac85-120">Al contrario, [**IDispatch:: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) e [**Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) vengono chiamati per richiamare Func0.</span><span class="sxs-lookup"><span data-stu-id="1ac85-120">Instead, [**IDispatch::GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) and [**Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) are called to invoke Func0.</span></span>


```VB
Dim myInfNone as IADs0
Set myInfNone = myInf1    ' The aggregated object that 
   ' supports IADs1 and IADs2.
myInfNone.Func0
```



<span data-ttu-id="1ac85-121">Si considerino i due casi seguenti:</span><span class="sxs-lookup"><span data-stu-id="1ac85-121">Consider these two cases:</span></span>

-   <span data-ttu-id="1ac85-122">IADs1 e IADs2 sono implementati rispettivamente da due componenti COM, EXT1 e ext2.</span><span class="sxs-lookup"><span data-stu-id="1ac85-122">IADs1 and IADs2 are implemented by two COM components, Ext1 and Ext2, respectively.</span></span> <span data-ttu-id="1ac85-123">Se EXT1 precede ext2 nel registro di sistema, viene richiamato IADs1:: Func0.</span><span class="sxs-lookup"><span data-stu-id="1ac85-123">If Ext1 comes before Ext2 in the registry, IADs1::Func0 is invoked.</span></span> <span data-ttu-id="1ac85-124">Tuttavia, se ext2 viene visualizzato per primo nel registro di sistema, viene richiamato IADs2:: Func0.</span><span class="sxs-lookup"><span data-stu-id="1ac85-124">However, if Ext2 comes first in the registry, IADs2::Func0 is invoked.</span></span>
-   <span data-ttu-id="1ac85-125">Se IADs1 e ADs2 sono implementati dallo stesso oggetto di estensione, Func0 viene sempre richiamato dai metodi [**IADsExtension::P rivategetidsofnames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) e [**PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="1ac85-125">If IADs1 and ADs2 are implemented by the same extension object, Func0 is always invoked by the extension's [**IADsExtension::PrivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) and [**PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) methods.</span></span>

<span data-ttu-id="1ac85-126">Lo sviluppatore dell'estensione deve determinare come risolvere i conflitti di funzioni, o proprietà, di interfacce dual [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) diverse con lo stesso nome in un'estensione.</span><span class="sxs-lookup"><span data-stu-id="1ac85-126">The extension developer must determine how to resolve conflicts of functions, or properties, of different dual [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interfaces that have the same name in an extension.</span></span> <span data-ttu-id="1ac85-127">L'implementazione dei metodi [**IADsExtension::P rivategetidsofnames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) e [**PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) deve risolvere questo conflitto.</span><span class="sxs-lookup"><span data-stu-id="1ac85-127">The implementation of [**IADsExtension::PrivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) and [**PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) methods should resolve this conflict.</span></span> <span data-ttu-id="1ac85-128">Ad esempio, se si usa IMyInterface1:: func1 e IMyInterface2:: func1, dove IMyInterface1 e IMyInterface2 sono interfacce dual **IDispatch** supportate dallo stesso oggetto di estensione.</span><span class="sxs-lookup"><span data-stu-id="1ac85-128">For example, if you use IMyInterface1::Func1 and IMyInterface2::Func1, where IMyInterface1 and IMyInterface2 are dual **IDispatch** interfaces supported by the same extension object.</span></span> <span data-ttu-id="1ac85-129">I metodi **PrivateGetIDsOfNames** e **PrivateInvoke** devono determinare quale func1 deve essere sempre chiamato.</span><span class="sxs-lookup"><span data-stu-id="1ac85-129">The **PrivateGetIDsOfNames** and **PrivateInvoke** methods must determine which Func1 should always be called.</span></span>

<span data-ttu-id="1ac85-130">Lo stesso vale per i DISPID in conflitto in interfacce duali o [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) differenti.</span><span class="sxs-lookup"><span data-stu-id="1ac85-130">The same applies to conflicting DISPIDs in different dual or [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interfaces.</span></span>

<span data-ttu-id="1ac85-131">Il DISPID di IMyInterface1:: Y, ad esempio, è 2 nel file IMyInterface1. FAD o IMyInterface1. idl.</span><span class="sxs-lookup"><span data-stu-id="1ac85-131">For example, the DISPID of IMyInterface1::Y is 2 in the file imyinterface1.odl, or imyinterface1.idl.</span></span> <span data-ttu-id="1ac85-132">Il DISPID di IMyInterface2:: X è anche 2 in iMyInterface2. FAD.</span><span class="sxs-lookup"><span data-stu-id="1ac85-132">The DISPID of IMyInterface2::X is also 2 in iMyInterface2.odl.</span></span> <span data-ttu-id="1ac85-133">[**IADsExtension::P rivategetidsofnames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) deve restituire un DISPID univoco, all'interno dell'estensione, per ogni, anziché restituire lo stesso DISPID per entrambi.</span><span class="sxs-lookup"><span data-stu-id="1ac85-133">[**IADsExtension::PrivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) must return a unique DISPID, within the extension itself, for each, instead of returning the same DISPID for both.</span></span>

<span data-ttu-id="1ac85-134">ADSI risolve il primo problema non supportando più interfacce con nomi di funzione o di proprietà in conflitto.</span><span class="sxs-lookup"><span data-stu-id="1ac85-134">ADSI resolves the first problem by not supporting multiple interfaces with conflicting function or property names.</span></span> <span data-ttu-id="1ac85-135">Risolve il secondo problema aggiungendo un univoco, che si trova all'interno dello stesso oggetto di estensione, numero di interfaccia ai bit inutilizzati del DISPID.</span><span class="sxs-lookup"><span data-stu-id="1ac85-135">It resolves the second problem by adding a unique, that is within the same extension object, interface number to the unused bits of the DISPID.</span></span>

 

 