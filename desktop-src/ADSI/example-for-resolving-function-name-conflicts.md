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
# <a name="example-for-resolving-function-name-conflicts"></a>Esempio per la risoluzione dei conflitti di nomi di funzione

Considerare quanto segue:

-   IADs0 non supporta Func0.
-   IADs1 supporta func1 e Func0.
-   IADs2 supporta Func2 e Func0.

Tutte e tre le interfacce sono interfacce duali.


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



Tenere presente che anche se IADs1 non supporta Func2, un client ADSI riconosce un [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) che supporta tutte le interfacce dual e dispatch nel modello. Pertanto, il client ADSI può chiamare direttamente Func2 usando myInf1. Func2 senza risolvere l'interfaccia che supporta Func2.


```VB
myInf1.Func2
```



Sia IADs1 che IADs2 hanno una funzione denominata Func0, ma IADs1:: Func0 viene richiamata direttamente usando l'accesso vtable, perché entrambe le condizioni seguenti si applicano al client:

-   Il client dispone di un puntatore a un oggetto IADs1 a doppia interfaccia con una funzione denominata Func0.
-   Visual Basic supporta l'accesso diretto a vtable, supponendo che il tipo di dati sia disponibile tramite la libreria dei tipi.

Nell'esempio di codice successivo il client dispone di un puntatore a interfaccia duale a IADs2 anziché IADs1. Pertanto, IADs2:: Func0 viene richiamato utilizzando l'accesso diretto a vtable.


```VB
Dim myInf2 as IADs2
Set myInf2 = myInf1 ' Query for pointer to IADs2 
myInf2.Func0
```



Anche in questo caso, nell'esempio di codice successivo, IADs1 e IADs2 hanno una funzione denominata Func0, ma in questo caso il client dispone di un puntatore a una doppia interfaccia, IADs0, che non dispone di una funzione denominata Func0. Non è pertanto possibile eseguire alcun accesso diretto a vtable. Al contrario, [**IDispatch:: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) e [**Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) vengono chiamati per richiamare Func0.


```VB
Dim myInfNone as IADs0
Set myInfNone = myInf1    ' The aggregated object that 
   ' supports IADs1 and IADs2.
myInfNone.Func0
```



Si considerino i due casi seguenti:

-   IADs1 e IADs2 sono implementati rispettivamente da due componenti COM, EXT1 e ext2. Se EXT1 precede ext2 nel registro di sistema, viene richiamato IADs1:: Func0. Tuttavia, se ext2 viene visualizzato per primo nel registro di sistema, viene richiamato IADs2:: Func0.
-   Se IADs1 e ADs2 sono implementati dallo stesso oggetto di estensione, Func0 viene sempre richiamato dai metodi [**IADsExtension::P rivategetidsofnames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) e [**PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) dell'estensione.

Lo sviluppatore dell'estensione deve determinare come risolvere i conflitti di funzioni, o proprietà, di interfacce dual [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) diverse con lo stesso nome in un'estensione. L'implementazione dei metodi [**IADsExtension::P rivategetidsofnames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) e [**PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) deve risolvere questo conflitto. Ad esempio, se si usa IMyInterface1:: func1 e IMyInterface2:: func1, dove IMyInterface1 e IMyInterface2 sono interfacce dual **IDispatch** supportate dallo stesso oggetto di estensione. I metodi **PrivateGetIDsOfNames** e **PrivateInvoke** devono determinare quale func1 deve essere sempre chiamato.

Lo stesso vale per i DISPID in conflitto in interfacce duali o [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) differenti.

Il DISPID di IMyInterface1:: Y, ad esempio, è 2 nel file IMyInterface1. FAD o IMyInterface1. idl. Il DISPID di IMyInterface2:: X è anche 2 in iMyInterface2. FAD. [**IADsExtension::P rivategetidsofnames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) deve restituire un DISPID univoco, all'interno dell'estensione, per ogni, anziché restituire lo stesso DISPID per entrambi.

ADSI risolve il primo problema non supportando più interfacce con nomi di funzione o di proprietà in conflitto. Risolve il secondo problema aggiungendo un univoco, che si trova all'interno dello stesso oggetto di estensione, numero di interfaccia ai bit inutilizzati del DISPID.

 

 