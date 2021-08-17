---
title: Hosting del controllo Windows Media Player in un'Windows applicazione
description: Hosting del controllo Windows Media Player in un'Windows applicazione
ms.assetid: 8da04160-b9db-4082-aeff-b0107189e33e
keywords:
- Windows Media Player,incorporamento ActiveX controllo
- Windows Media Player a oggetti, incorporamento ActiveX controllo
- modello a oggetti, incorporamento ActiveX controllo
- Windows Media Player Dispositivi mobili, incorporamento ActiveX controllo
- Windows Media Player ActiveX, incorporamento
- Windows Media Player controllo ActiveX per dispositivi mobili, incorporamento
- ActiveX, incorporamento
- Windows Media Player,Windows basati su applicazioni
- Windows Media Player modello a oggetti, Windows basati su applicazioni
- modello a oggetti, Windows basati su applicazioni
- Windows Media Player Programmi basati Windows mobili
- Windows Media Player ActiveX controllo, Windows basati su applicazioni
- Windows Media Player Controllo ActiveX per dispositivi mobili, Windows basati su dispositivi mobili
- ActiveX controllo, Windows basati su applicazioni
- Windows incorporamento del programma basato su criteri
- incorporamento, Windows basati su applicazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f3c2b4d84194376bd16842f0a9567c83fce2aa616ed4bfef4f20f7255068e8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748278"
---
# <a name="hosting-the-windows-media-player-control-in-a-windows-application"></a>Hosting del controllo Windows Media Player in un'Windows applicazione

Per usare il controllo Windows Media Player ActiveX (inclusa l'interfaccia utente) in un programma basato su Windows, è necessario fornire un contenitore ActiveX controllo. ATL fornisce la **classe CAxWindow** per fornire ActiveX della finestra host.

Per ospitare il Windows Media Player usando la **classe CAxWindow,** seguire questa procedura:

1.  Includere le intestazioni seguenti:
    ```C++
    #include "wmp.h"
    #include <atlbase.h>
    #include <atlcom.h>
    #include <atlhost.h>
    #include <atlctl.h>
    ```

    

2.  Dichiarare le variabili membro, come indicato di seguito:
    ```C++
    CAxWindow  m_wndView;  // ActiveX host window class.
    CComPtr<IWMPPlayer>  m_spWMPPlayer;  // Smart pointer to IWMPPlayer interface.
    
    ```

    

3.  Quando viene creata la finestra dell'applicazione, chiamare **AtlAxWinInit,** che è necessario quando si usa la finestra host ActiveX ATL.
    ```C++
    AtlAxWinInit();
    
    ```

    

4.  Dichiarare le variabili locali per i codici restituiti e per contenere il puntatore all'interfaccia della finestra host:
    ```C++
    CComPtr<IAxWinHostWindow>  spHost;
    HRESULT  hr;
    
    ```

    

5.  Creare la finestra host:
    ```C++
    GetClientRect(&rcClient);
    m_wndView.Create(m_hWnd, rcClient, NULL, WS_CHILD | WS_VISIBLE | WS_CLIPCHILDREN, WS_EX_CLIENTEDGE);
    
    ```

    

6.  Recuperare il puntatore all'interfaccia della finestra host:
    ```C++
    hr = m_wndView.QueryHost(&spHost);
    
    ```

    

7.  Creare il Windows Media Player nella finestra host usando l'ID classe:
    ```C++
    hr = spHost->CreateControl(CComBSTR(_T("{6BF52A52-394A-11d3-B153-00C04F79FAA6}")), m_wndView, 0);
    
    ```

    

8.  Recuperare il **puntatore all'interfaccia IWMPPlayer:**
    ```C++
    hr = m_wndView.QueryControl(&m_spWMPPlayer);
    
    ```

    

Quando si scrive codice personalizzato, assicurarsi di controllare la presenza di errori in ogni **codice restituito HRESULT.**

Per un esempio completo che illustra come ospitare il controllo Windows Media Player ActiveX usando la classe **CAxWindow,** vedere l'esempio WMPHost.

## <a name="hosting-the-windows-media-player-10-mobile-control-in-windows-ce"></a>Hosting del controllo Windows Media Player 10 Mobile in Windows CE

Microsoft eMbedded Visual C++ 4.0 e Pocket PC 2003 SDK o Smartphone 2003 SDK devono essere installati durante lo sviluppo di applicazioni basate su Windows CE che ospitano un controllo Windows Media Player 10 Mobile. Inoltre, a differenza di ATL Windows, ATL per Windows CE non supporta il modello di threading apartment. Pertanto, è necessario trovare tutte le istanze del threading apartment nel progetto ATL e modificarle per usare il threading libero.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Esempi**](samples.md)
</dt> <dt>

[**Uso del Windows Media Player in un programma C++**](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




