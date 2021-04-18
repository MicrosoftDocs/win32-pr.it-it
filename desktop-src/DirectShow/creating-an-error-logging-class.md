---
description: Questo argomento descrive come implementare la registrazione degli errori nei servizi di modifica DirectShow.
ms.assetid: c0b3b25c-ed03-4f78-9c53-0c0bcff1c60c
title: Creazione di una classe di registrazione degli errori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db08971c7bf1a0024669935079b7a9403c429327
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304321"
---
# <a name="creating-an-error-logging-class"></a>Creazione di una classe di registrazione degli errori

\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]

Questo argomento descrive come implementare la registrazione degli errori nei [servizi di modifica DirectShow](directshow-editing-services.md).

Dichiarare prima di tutto una classe che implementerà la registrazione degli errori. La classe eredita l'interfaccia [**IAMErrorLog**](iamerrorlog.md) . Contiene le dichiarazioni per i tre metodi **IUnknown** e per il singolo metodo in [IAMErrorLog](implementing-iamerrorlog.md). La dichiarazione di classe è la seguente:


```C++
class CErrReporter : public IAMErrorLog
{
protected:
    long    m_lRef; // Reference count.

public:
    CErrReporter() { m_lRef = 0; }

    // IUnknown
    STDMETHOD(QueryInterface(REFIID, void**));
    STDMETHOD_(ULONG, AddRef());
    STDMETHOD_(ULONG, Release());

    // IAMErrorLog
    STDMETHOD(LogError(LONG, BSTR, LONG, HRESULT, VARIANT*));
};
```



L'unica variabile membro nella classe è m \_ lRef, che include il conteggio dei riferimenti dell'oggetto.

Definire quindi i metodi in **IUnknown**. Nell'esempio seguente viene illustrata un'implementazione standard per questi metodi:


```C++
STDMETHODIMP CErrReporter::QueryInterface(REFIID riid, void **ppv)
{
    if (ppv == NULL) return E_POINTER;

    *ppv = NULL;
    if (riid == IID_IUnknown)
        *ppv = static_cast<IUnknown*>(this);
    else if (riid == IID_IAMErrorLog)
        *ppv = static_cast<IAMErrorLog*>(this);
        
    else 
    return E_NOINTERFACE;

    AddRef();
    return S_OK;
}

STDMETHODIMP_(ULONG) CErrReporter::AddRef()
{
    return InterlockedIncrement(&m_lRef);
}

STDMETHODIMP_(ULONG) CErrReporter::Release()
{
    // Store the decremented count in a temporary
    // variable. 
    ULONG uCount = InterlockedDecrement(&m_lRef);
    if (uCount == 0)
    {
        delete this;
    }
    // Return the temporary variable, not the member
    // variable, for thread safety.
    return uCount;
}
```



Con il Framework COM sul posto, è ora possibile implementare l'interfaccia **IAMErrorLog** . La sezione successiva descrive come eseguire questa operazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Errori di registrazione](logging-errors.md)
</dt> </dl>

 

 



