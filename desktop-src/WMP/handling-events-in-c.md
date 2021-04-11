---
title: Gestione degli eventi in C++
description: Gestione degli eventi in C++
ms.assetid: 5d9eb1c7-7022-4442-b67a-6a96fe5ce97f
keywords:
- Windows Media Player, C++
- Modello a oggetti di Windows Media Player, C++
- modello a oggetti, C++
- Windows Media Player Mobile, C++
- Controllo ActiveX di Windows Media Player, C++
- Controllo ActiveX Windows Media Player Mobile, C++
- Controllo ActiveX, C++
- Incorporamento del programma C++
- incorporamento, programmi C++
- Controllo ActiveX Windows Media Player, gestione eventi
- Controllo ActiveX Windows Media Player Mobile, gestione eventi
- Controllo ActiveX, gestione eventi
- eventi, C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16cbef547ab2604244c5c204707a08eb87a6b70a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116861"
---
# <a name="handling-events-in-c"></a>Gestione degli eventi in C++

È possibile ricevere eventi da Windows Media Player in due modi.

-   Tramite **IDispatch** usando l'interfaccia **\_ WMPOCXEvents** . Si tratta dell'interfaccia da utilizzare per la maggior parte degli scenari di incorporamento.
-   Tramite l'interfaccia **IWMPEvents** . Questa interfaccia è disponibile quando il codice è connesso al lettore in modalità completa, ad esempio quando si esegue la comunicazione remota del controllo Media Player Windows o in un plug-in dell'interfaccia utente.

In ogni scenario si inizia ad ascoltare gli eventi usando i punti di connessione COM.

Il codice di esempio seguente usa tre variabili membro:


```C++
CComPtr<IWMPPlayer>         m_spWMPPlayer;
CComPtr<IConnectionPoint>   m_spConnectionPoint;
DWORD                       m_dwAdviseCookie;

```



Per recuperare un punto di connessione, è necessario innanzitutto **QueryInterface** per il contenitore del punto di connessione.


```C++
HRESULT  hr = S_OK;
// Smart pointer to IConnectionPointContainer
CComPtr<IConnectionPointContainer>  spConnectionContainer;

hr = m_spWMPPlayer->QueryInterface(&spConnectionContainer);

```



Successivamente, richiedere il punto di connessione per l'interfaccia evento che si vuole usare. Il codice di esempio seguente tenta prima di usare **IWMPEvents**. Se l'interfaccia non è disponibile, viene usato **\_ WMPOCXEvents**.


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



Infine, chiamare **IConnectionPoint:: Advise** per richiedere gli eventi.


```C++
if(SUCCEEDED(hr))
{
    hr = m_spConnectionPoint->Advise(this, &m_dwAdviseCookie);
}

```



Nell'esempio precedente, il primo parametro presuppone che la classe chiamante implementi sia **IWMPEvents** che **\_ WMPOCXEvents**. Il secondo parametro è un valore restituito che viene usato per arrestare l'ascolto degli eventi, ad esempio quando il programma viene chiuso, usando un codice simile al seguente:


```C++
// Stop listening to events
if (m_spConnectionPoint)
{
    if (0 != m_dwAdviseCookie)
        m_spConnectionPoint->Unadvise(m_dwAdviseCookie);
        m_spConnectionPoint.Release();
}

```



L'implementazione dei gestori eventi per **IWMPEvents** e **\_ WMPOCXEvents** è diversa. Per **IWMPEvents**, è necessario implementare una funzione per gestire ogni evento definito dall'interfaccia, anche se non si intende usare l'evento.


```C++
// IWMPEvents methods
void STDMETHODCALLTYPE OpenStateChange( long NewState ){ return; }
void STDMETHODCALLTYPE PlayStateChange( long NewState ){ return; }
void STDMETHODCALLTYPE AudioLanguageChange( long LangID ){ return; }
// And so on...

```



Per implementare i gestori **\_ WMPOCXEvents** , è necessario usare **IDispatch:: Invoke**, ovvero un'unica implementazione del gestore eventi per tutti gli eventi che si verificano nell'interfaccia **IDispatch** . Ciò significa che è possibile scegliere di gestire solo determinati eventi e ignorarne altri. Il codice di esempio seguente mostra un gestore **\_ WMPOCXEvents** , che usa **Invoke**, che gestisce solo gli eventi **OpenStateChange** e **PlayStateChange** :


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



Nel codice di esempio precedente, ogni case esegue semplicemente chiamate al gestore **IWMPEvents** per l'evento corrispondente. Se il codice gestisce solo **\_ WMPOCXEvents**, è possibile chiamare semplicemente una funzione personalizzata o gestire l'evento inline dopo l'istruzione **case** .

## <a name="receiving-events-from-windows-media-player-10-mobile"></a>Ricezione di eventi da Windows Media Player 10 Mobile

Il controllo Windows Media Player 10 Mobile supporta solo la ricezione di determinati eventi tramite **\_ WMPOCXEvents** e **IWMPEvents**. Per ulteriori informazioni, vedere la documentazione relativa a **IWMPEvents**.

## <a name="samples"></a>Esempi

Il pacchetto di installazione di Windows Media Player installa un esempio che illustra la gestione degli eventi. Per ulteriori informazioni, vedere l'esempio WMPHost.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Esempi**](samples.md)
</dt> <dt>

[**Uso del controllo Media Player di Windows in un programma C++**](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




