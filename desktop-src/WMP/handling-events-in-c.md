---
title: Gestione di eventi in C++
description: Gestione di eventi in C++
ms.assetid: 5d9eb1c7-7022-4442-b67a-6a96fe5ce97f
keywords:
- Windows Media Player,C++
- Windows Media Player a oggetti, C++
- modello a oggetti,C++
- Windows Media Player Mobile,C++
- Windows Media Player ActiveX, C++
- Windows Media Player Controllo ActiveX per dispositivi mobili,C++
- ActiveX, C++
- Incorporamento di programmi C++
- incorporamento, programmi C++
- Windows Media Player ActiveX, gestione degli eventi
- Windows Media Player Controllo ActiveX per dispositivi mobili, gestione degli eventi
- ActiveX, gestione degli eventi
- eventi,C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf5d50be4622cee9ee455710f8b9d2e4cafc63d6560e08faf5c3deaddcdaccc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748406"
---
# <a name="handling-events-in-c"></a>Gestione di eventi in C++

È possibile ricevere eventi da Windows Media Player in due modi.

-   Tramite **IDispatch** usando **\_ l'interfaccia WMPOCXEvents.** Questa è l'interfaccia da usare per la maggior parte degli scenari di incorporamento.
-   Tramite **l'interfaccia IWMPEvents.** Questa interfaccia è disponibile quando il codice è connesso al lettore in modalità completa, ad esempio quando si esegue la comunicazione remota del controllo Windows Media Player o in un plug-in dell'interfaccia utente.

In ogni scenario si inizia ad ascoltare gli eventi usando i punti di connessione COM.

Il codice di esempio seguente usa tre variabili membro:


```C++
CComPtr<IWMPPlayer>         m_spWMPPlayer;
CComPtr<IConnectionPoint>   m_spConnectionPoint;
DWORD                       m_dwAdviseCookie;

```



Per recuperare un punto di connessione, è necessario prima **QueryInterface** per il contenitore del punto di connessione.


```C++
HRESULT  hr = S_OK;
// Smart pointer to IConnectionPointContainer
CComPtr<IConnectionPointContainer>  spConnectionContainer;

hr = m_spWMPPlayer->QueryInterface(&spConnectionContainer);

```



Richiedere quindi il punto di connessione per l'interfaccia eventi che si vuole usare. Il codice di esempio seguente tenta prima di tutto di usare **IWMPEvents**. Se tale interfaccia non è disponibile, usa **\_ WMPOCXEvents**.


```C++
// Test whether the control supports the IWMPEvents interface.
if(SUCCEEDED(hr))
{
    hr = spConnectionContainer->FindConnectionPoint(__uuidof(IWMPEvents), &m_spConnectionPoint);
    if (FAILED(hr))
    {
        // If not, try the _WMPOCXEvents interface, which uses IDispatch.
        hr = spConnectionContainer->FindConnectionPoint(__uuidof(_WMPOCXEvents), &m_spConnectionPoint);
    }
}

```



Chiamare infine **IConnectionPoint::Advise per** richiedere eventi.


```C++
if(SUCCEEDED(hr))
{
    hr = m_spConnectionPoint->Advise(this, &m_dwAdviseCookie);
}

```



Nell'esempio precedente il primo parametro presuppone che la classe chiamante implementi sia **IWMPEvents** che **\_ WMPOCXEvents**. Il secondo parametro è un valore restituito che viene utilizzato per interrompere l'ascolto di eventi, ad esempio quando il programma viene chiuso, usando codice simile al seguente:


```C++
// Stop listening to events
if (m_spConnectionPoint)
{
    if (0 != m_dwAdviseCookie)
        m_spConnectionPoint->Unadvise(m_dwAdviseCookie);
        m_spConnectionPoint.Release();
}

```



L'implementazione dei gestori eventi **per IWMPEvents** **\_ e WMPOCXEvents** è diversa. Per **IWMPEvents**, è necessario implementare una funzione per gestire ogni evento definito dall'interfaccia, anche se non si intende usare l'evento .


```C++
// IWMPEvents methods
void STDMETHODCALLTYPE OpenStateChange( long NewState ){ return; }
void STDMETHODCALLTYPE PlayStateChange( long NewState ){ return; }
void STDMETHODCALLTYPE AudioLanguageChange( long LangID ){ return; }
// And so on...

```



Per implementare i gestori **\_ WMPOCXEvents,** è necessario usare **IDispatch::Invoke**, che è una singola implementazione del gestore eventi per tutti gli eventi che si verificano **nell'interfaccia IDispatch.** Ciò significa che è possibile scegliere di gestire solo determinati eventi e ignorarli. Il codice di esempio seguente illustra un gestore **\_ WMPOCXEvents,** usando **Invoke,** che gestisce solo gli **eventi OpenStateChange** **e PlayStateChange:**


```C++
HRESULT CMyClass::Invoke(
    DISPID  dispIdMember,      
    REFIID  riid,              
    LCID  lcid,                
    WORD  wFlags,              
    DISPPARAMS FAR*  pDispParams,  
    VARIANT FAR*  pVarResult,  
    EXCEPINFO FAR*  pExcepInfo,  
    unsigned int FAR*  puArgErr )
{
    if (!pDispParams)
        return E_POINTER;

    if (pDispParams->cNamedArgs != 0)
        return DISP_E_NONAMEDARGS;

    HRESULT hr = DISP_E_MEMBERNOTFOUND;

    switch (dispIdMember)
    {
        case DISPID_WMPCOREEVENT_OPENSTATECHANGE:
            OpenStateChange(pDispParams->rgvarg[0].lVal /* NewState */ );
            break;

        case DISPID_WMPCOREEVENT_PLAYSTATECHANGE:
            PlayStateChange(pDispParams->rgvarg[0].lVal /* NewState */);
            break;

        // Other cases can handle additional events by using DISPIDs.
    }

    return( hr );
}

```



Nel codice di esempio precedente, ogni caso chiama semplicemente il gestore **IWMPEvents** per l'evento corrispondente. Se il codice gestisce **\_ solo WMPOCXEvents,** è sufficiente chiamare una funzione personalizzata o gestire l'evento inline dopo l'istruzione **case.**

## <a name="receiving-events-from-windows-media-player-10-mobile"></a>Ricezione di eventi da Windows Media Player 10 Mobile

Il Windows Media Player 10 Mobile supporta solo la ricezione di determinati eventi **\_ tramite WMPOCXEvents** e **IWMPEvents**. Per altre informazioni, vedere la documentazione di **IWMPEvents.**

## <a name="samples"></a>Esempi

Il Windows Media Player di installazione installa un esempio che illustra la gestione degli eventi. Per altre informazioni, vedere l'esempio WMPHost.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Esempi**](samples.md)
</dt> <dt>

[**Uso del Windows Media Player controllo in un programma C++**](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




