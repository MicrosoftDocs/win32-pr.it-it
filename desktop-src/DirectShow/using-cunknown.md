---
description: DirectShow implementa IUnknown in una classe di base denominata CUnknown.
ms.assetid: 1fc74db6-c23a-464f-b9fa-b19d7e8672b7
title: Uso di CUnknown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e211ebf8c581502665c5f07b3720759efc7afab75a05a49a68f9945029dd6cce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051381"
---
# <a name="using-cunknown"></a>Uso di CUnknown

DirectShow implementa [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) in una classe di base [**denominata CUnknown.**](cunknown.md) È possibile usare **CUnknown per** derivare altre classi, eseguendo l'override solo dei metodi che cambiano tra i componenti. La maggior parte delle altre classi di base in DirectShow deriva da **CUnknown,** quindi il componente può ereditare direttamente da **CUnknown** o da un'altra classe di base.

## <a name="inondelegatingunknown"></a>INonDelegatingUnknown

[**CUnknown implementa**](cunknown.md) [**INonDelegatingUnknown.**](inondelegatingunknown.md) Gestisce internamente i conteggi dei riferimenti e nella maggior parte dei casi la classe derivata può ereditare i due metodi di conteggio dei riferimenti senza alcuna modifica. Tenere presente che **CUnknown** elimina se stesso quando il conteggio dei riferimenti scende a zero. D'altra parte, è necessario eseguire l'override di [**CUnknown::NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md), perché il metodo nella classe di base restituisce E NOINTERFACE se riceve qualsiasi IID diverso da \_ IID \_ IUnknown. Nella classe derivata testare gli ID delle interfacce supportate, come illustrato nell'esempio seguente:


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



La funzione di utilità [**GetInterface**](getinterface.md) (vedere [**Funzioni helper COM**](com-helper-functions.md)) imposta il puntatore, incrementa il conteggio dei riferimenti in modo thread-safe e restituisce S \_ OK. Nel caso predefinito, chiamare il metodo della classe base e restituire il risultato. Se si deriva da un'altra classe di base, chiamare invece il relativo [**metodo NonDelegatingQueryInterface.**](cunknown-nondelegatingqueryinterface.md) In questo modo è possibile supportare tutte le interfacce supportate dalla classe padre.

## <a name="iunknown"></a>IUnknown

Come accennato in precedenza, la versione delegante di [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) è la stessa per ogni componente, perché non esegue altro che richiamare l'istanza corretta della versione non delegante. Per praticità, il file di intestazione Combase.h contiene una macro, [**DECLARE \_ IUNKNOWN,**](declare-iunknown.md)che dichiara i tre metodi deleganti come metodi inline. Si espande fino al codice seguente:


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



La funzione di [**utilità CUnknown::GetOwner**](cunknown-getowner.md) recupera un puntatore all'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) del componente proprietario di questo componente. Per un componente aggregato, il proprietario è il componente esterno. In caso contrario, il componente è proprietario di se stesso. Includere la macro DECLARE \_ IUNKNOWN nella sezione pubblica della definizione di classe.

## <a name="class-constructor"></a>Costruttore di classe

Il costruttore della classe deve richiamare il metodo del costruttore per la classe padre, oltre a qualsiasi operazione che sia specifica della classe. L'esempio seguente è un metodo costruttore tipico:


```C++
CMyComponent(TCHAR *tszName, LPUNKNOWN pUnk, HRESULT *phr) 
    : CUnknown(tszName, pUnk, phr)
{ 
    /* Other initializations */ 
};
```



Il metodo accetta i parametri seguenti, che passa direttamente al [**metodo costruttore CUnknown.**](cunknown.md)

-   *tszName* specifica un nome per il componente.
-   *pUnk* è un puntatore all'oggetto [**IUnknown aggregato.**](/windows/win32/api/unknwn/nn-unknwn-iunknown)
-   *pHr* è un puntatore a un valore HRESULT, che indica l'esito positivo o negativo del metodo.

## <a name="summary"></a>Riepilogo

L'esempio seguente illustra una classe derivata che supporta [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) e un'interfaccia ipotetica denominata ISomeInterface:


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

-   La [**classe CUnknown**](cunknown.md) implementa [**l'interfaccia IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) Il nuovo componente eredita da **CUnknown** e da tutte le interfacce supportate dal componente. Il componente potrebbe invece derivare da un'altra classe di base che eredita da **CUnknown.**
-   La macro [**DECLARE \_ IUNKNOWN**](declare-iunknown.md) dichiara i metodi [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) delegati come metodi inline.
-   La [**classe CUnknown fornisce**](cunknown.md) l'implementazione per [**INonDelegatingUnknown.**](inondelegatingunknown.md)
-   Per supportare un'interfaccia diversa da [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), la classe derivata deve eseguire l'override del metodo [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) e verificare l'IID della nuova interfaccia.
-   Il costruttore della classe richiama il metodo del costruttore [**per CUnknown.**](cunknown.md)

Il passaggio successivo per la scrittura di un filtro consiste nell'abilitare un'applicazione alla creazione di nuove istanze del componente. A questo scopo è necessario conoscere le DLL e la relativa relazione con le class factory e i metodi del costruttore di classi. Per altre informazioni, vedere [How to Create a DirectShow Filter DLL](how-to-create-a-dll.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come implementare IUnknown](how-to-implement-iunknown.md)
</dt> </dl>

 

 
