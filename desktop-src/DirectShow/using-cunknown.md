---
description: DirectShow implementa IUnknown in una classe di base denominata CUnknown.
ms.assetid: 1fc74db6-c23a-464f-b9fa-b19d7e8672b7
title: Uso di CUnknown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c1758065e8d618bf6ca74b37d98b0a8b5425919
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314399"
---
# <a name="using-cunknown"></a>Uso di CUnknown

DirectShow implementa [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) in una classe di base denominata [**CUnknown**](cunknown.md). È possibile utilizzare **CUnknown** per derivare altre classi, eseguendo l'override solo dei metodi che cambiano tra i componenti. La maggior parte delle altre classi di base in DirectShow derivano da **CUnknown**, quindi il componente può ereditare direttamente da **CUnknown** o da un'altra classe di base.

## <a name="inondelegatingunknown"></a>INonDelegatingUnknown

[**CUnknown**](cunknown.md) implementa [**INonDelegatingUnknown**](inondelegatingunknown.md). Gestisce i conteggi dei riferimenti internamente e nella maggior parte dei casi la classe derivata può ereditare i due metodi di conteggio dei riferimenti senza alcuna modifica. Tenere presente che **CUnknown** si elimina quando il conteggio dei riferimenti scende a zero. D'altra parte, è necessario eseguire l'override di [**CUnknown:: NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md), perché il metodo nella classe di base restituisce E \_ nointerface se riceve un IID diverso da IID \_ IUnknown. Nella classe derivata testare il IID di interfacce supportate, come illustrato nell'esempio seguente:


```C++
STDMETHODIMP NonDelegatingQueryInterface(REFIID riid, void **ppv)
{
    if (riid == IID_ISomeInterface)
    {
        return GetInterface((ISomeInterface*)this, ppv);
    }
    // Default: Call parent class method. 
    // The CUnknown class must be in the inheritance chain.
    return CParentClass::NonDelegatingQueryInterface(riid, ppv);
}
```



La funzione di utilità [**GetInterface**](getinterface.md) (vedere [**funzioni helper com**](com-helper-functions.md)) imposta il puntatore, incrementa il conteggio dei riferimenti in modo thread-safe e restituisce S \_ OK. Nel caso predefinito, chiamare il metodo della classe base e restituire il risultato. Se si deriva da un'altra classe di base, chiamare invece il relativo metodo [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) . In questo modo è possibile supportare tutte le interfacce supportate dalla classe padre.

## <a name="iunknown"></a>IUnknown

Come indicato in precedenza, la versione delegante di [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) è la stessa per ogni componente, poiché non esegue alcuna operazione oltre a richiamare l'istanza corretta della versione non delegata. Per praticità, il file di intestazione ComBase. h contiene una macro, [**Declare \_ IUnknown**](declare-iunknown.md), che dichiara i tre metodi delegati come metodi inline. Espande il codice seguente:


```C++
STDMETHODIMP QueryInterface(REFIID riid, void **ppv) {      
    return GetOwner()->QueryInterface(riid,ppv);            
};                                                          
STDMETHODIMP_(ULONG) AddRef() {                             
    return GetOwner()->AddRef();                            
};                                                          
STDMETHODIMP_(ULONG) Release() {                            
    return GetOwner()->Release();                           
};
```



La funzione di utilità [**CUnknown:: GetOwner**](cunknown-getowner.md) recupera un puntatore all'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) del componente proprietario di questo componente. Per un componente aggregato, il proprietario è il componente esterno. In caso contrario, il componente è proprietario. Includere la \_ macro DECLARE IUnknown nella sezione public della definizione della classe.

## <a name="class-constructor"></a>Costruttore di classe

Il costruttore della classe deve richiamare il metodo del costruttore per la classe padre, oltre a qualsiasi elemento che è specifico della classe. Nell'esempio seguente viene riportato un tipico metodo del costruttore:


```C++
CMyComponent(TCHAR *tszName, LPUNKNOWN pUnk, HRESULT *phr) 
    : CUnknown(tszName, pUnk, phr)
{ 
    /* Other initializations */ 
};
```



Il metodo accetta i parametri seguenti, che passano direttamente al metodo del costruttore [**CUnknown**](cunknown.md) .

-   *tszName* specifica un nome per il componente.
-   il *punk* è un puntatore all' [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)di aggregazione.
-   *pHr* è un puntatore a un valore HRESULT che indica l'esito positivo o negativo del metodo.

## <a name="summary"></a>Riepilogo

Nell'esempio seguente viene illustrata una classe derivata che supporta [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) e un'interfaccia ipotetica denominata ISomeInterface:


```C++
class CMyComponent : public CUnknown, public ISomeInterface
{
public:

    DECLARE_IUNKNOWN;

    STDMETHODIMP NonDelegatingQueryInterface(REFIID riid, void **ppv)
    {
        if( riid == IID_ISomeInterface )
        {
            return GetInterface((ISomeInterface*)this, ppv);
        }
        return CUnknown::NonDelegatingQueryInterface(riid, ppv);
    }

    CMyComponent(TCHAR *tszName, LPUNKNOWN pUnk, HRESULT *phr) 
        : CUnknown(tszName, pUnk, phr)
    { 
        /* Other initializations */ 
    };

    // More declarations will be added later.
};
```



Questo esempio illustra i punti seguenti:

-   La classe [**CUnknown**](cunknown.md) implementa l'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . Il nuovo componente eredita da **CUnknown** e da tutte le interfacce supportate dal componente. Il componente può derivare invece da un'altra classe di base che eredita da **CUnknown**.
-   La macro [**Declare \_ IUnknown**](declare-iunknown.md) dichiara i metodi [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) deleganti come metodi inline.
-   La classe [**CUnknown**](cunknown.md) fornisce l'implementazione di per [**INonDelegatingUnknown**](inondelegatingunknown.md).
-   Per supportare un'interfaccia diversa da [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), la classe derivata deve eseguire l'override del metodo [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) e verificare l'IID della nuova interfaccia.
-   Il costruttore della classe richiama il metodo del costruttore per [**CUnknown**](cunknown.md).

Il passaggio successivo per la scrittura di un filtro consiste nel consentire a un'applicazione di creare nuove istanze del componente. Questa operazione richiede una conoscenza delle dll e della relativa relazione con le class factory e i metodi del costruttore di classe. Per ulteriori informazioni, vedere [How to create an DirectShow Filter DLL](how-to-create-a-dll.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come implementare IUnknown](how-to-implement-iunknown.md)
</dt> </dl>

 

 
