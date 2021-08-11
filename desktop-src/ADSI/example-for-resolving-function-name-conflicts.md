---
title: Esempio per la risoluzione dei conflitti di nomi di funzione
description: Questo argomento descrive come risolvere i conflitti di nomi di funzione durante la creazione di un'estensione per ADSI.
ms.assetid: 8121f037-3845-44ba-a2cd-8d7f15e0beb2
ms.tgt_platform: multiple
keywords:
- CODICE ADSI ADSI , codice di esempio Visual Basic , risoluzione dei conflitti tra nomi di funzione
- risoluzione dei conflitti di nomi di funzione ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e6ce09251ba61b31768d973e258c568694067aff0420f0512a13913bb6fce90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118179981"
---
# <a name="example-for-resolving-function-name-conflicts"></a>Esempio per la risoluzione dei conflitti di nomi di funzione

Considerare quanto segue:

-   IADs0 non supporta Func0.
-   IADs1 supporta Func1 e Func0.
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



Tenere presente che anche se IADs1 non supporta Func2, un client ADSI riconosce un [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) che supporta tutte le interfacce duali e dispatch nel modello. Il client ADSI può quindi chiamare direttamente Func2 usando myInf1.Func2 senza risolvere l'interfaccia che supporta Func2.


```VB
myInf1.Func2
```



Sia IADs1 che IADs2 hanno una funzione denominata Func0, ma IADs1::Func0 viene richiamato direttamente usando l'accesso vtable, perché entrambi gli elementi seguenti si applicano al client:

-   Il client ha un puntatore all'oggetto IADs1 a interfaccia duale, che ha una funzione denominata Func0.
-   Visual Basic supporta l'accesso vtable diretto, presupponendo che il tipo di dati sia disponibile tramite la libreria dei tipi.

Nell'esempio di codice successivo il client ha un puntatore a interfaccia duale a IADs2 invece di IADs1. Pertanto, IADs2::Func0 viene richiamato usando l'accesso vtable diretto.


```VB
Dim myInf2 as IADs2
Set myInf2 = myInf1 ' Query for pointer to IADs2 
myInf2.Func0
```



Anche in questo caso, nell'esempio di codice successivo, sia IADs1 che IADs2 hanno una funzione denominata Func0, ma in questo caso il client ha un puntatore a un'interfaccia duale, IADs0, che non dispone di una funzione denominata Func0. Pertanto, non è possibile eseguire l'accesso vtable diretto. Vengono invece [**chiamati IDispatch::GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) e [**Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) per richiamare Func0.


```VB
Dim myInfNone as IADs0
Set myInfNone = myInf1    ' The aggregated object that 
   ' supports IADs1 and IADs2.
myInfNone.Func0
```



Si considerino questi due casi:

-   IADs1 e IADs2 vengono implementati rispettivamente da due componenti COM, Ext1 ed Ext2. Se Ext1 viene prima di Ext2 nel Registro di sistema, viene richiamato IADs1::Func0. Tuttavia, se Ext2 viene fornito per primo nel Registro di sistema, viene richiamato IADs2::Func0.
-   Se IADs1 e ADs2 vengono implementati dallo stesso oggetto di estensione, Func0 viene sempre richiamato dai metodi [**IADsExtension::P rivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) e [**PrivateInvoke dell'estensione.**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke)

Lo sviluppatore di estensioni deve determinare come risolvere i conflitti di funzioni o proprietà di interfacce [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) duali diverse con lo stesso nome in un'estensione. L'implementazione dei metodi [**IADsExtension::P rivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) e [**PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) deve risolvere questo conflitto. Ad esempio, se si usano IMyInterface1::Func1 e IMyInterface2::Func1, dove IMyInterface1 e IMyInterface2 sono interfacce **IDispatch** doppie supportate dallo stesso oggetto di estensione. I **metodi PrivateGetIDsOfNames** e **PrivateInvoke** devono determinare quale Func1 deve sempre essere chiamato.

Lo stesso vale per i DISPID in conflitto in interfacce duali [**o IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) diverse.

Ad esempio, il DISPID di IMyInterface1::Y è 2 nel file imyinterface1.odl o imyinterface1.idl. Anche il DISPID di IMyInterface2::X è 2 in iMyInterface2.odl. [**IADsExtension::P rivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) deve restituire un DISPID univoco, all'interno dell'estensione stessa, per ognuno, anziché restituire lo stesso DISPID per entrambi.

ADSI risolve il primo problema non supportando più interfacce con nomi di funzioni o proprietà in conflitto. Risolve il secondo problema aggiungendo un valore univoco, che si trova all'interno dello stesso oggetto di estensione, numero di interfaccia ai bit inutilizzati del DISPID.

 

 