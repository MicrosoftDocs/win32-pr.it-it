---
description: Questo argomento descrive come implementare la registrazione degli errori nei DirectShow di modifica.
ms.assetid: c0b3b25c-ed03-4f78-9c53-0c0bcff1c60c
title: Creazione di una classe di registrazione degli errori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 194d927b2e4eae73f75a326ed03363d96f6121634e46b606ba87409e3bf07f9f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108201"
---
# <a name="creating-an-error-logging-class"></a>Creazione di una classe di registrazione degli errori

\[Questa API non è supportata e potrebbe essere modificata o non disponibile in futuro.\]

In questo argomento viene descritto come implementare la registrazione degli errori in [DirectShow Servizi di modifica](directshow-editing-services.md).

Dichiarare prima di tutto una classe che implementerà la registrazione degli errori. La classe eredita [**l'interfaccia IAMErrorLog.**](iamerrorlog.md) Contiene dichiarazioni per i tre **metodi IUnknown** e per il singolo metodo in [IAMErrorLog](implementing-iamerrorlog.md). La dichiarazione di classe è la seguente:


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



L'unica variabile membro nella classe è m \_ lRef, che contiene il conteggio dei riferimenti dell'oggetto.

Definire quindi i metodi in **IUnknown**. L'esempio seguente illustra un'implementazione standard per questi metodi:


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



Dopo aver implementato il framework COM, è ora possibile implementare **l'interfaccia IAMErrorLog.** La sezione successiva descrive come eseguire questa operazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Errori di registrazione](logging-errors.md)
</dt> </dl>

 

 



