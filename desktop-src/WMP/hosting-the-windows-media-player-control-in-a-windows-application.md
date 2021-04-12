---
title: Hosting del controllo Media Player Windows in un'applicazione Windows
description: Hosting del controllo Media Player Windows in un'applicazione Windows
ms.assetid: 8da04160-b9db-4082-aeff-b0107189e33e
keywords:
- Windows Media Player, incorporamento del controllo ActiveX
- Modello a oggetti di Windows Media Player, incorporamento del controllo ActiveX
- modello a oggetti, incorporamento del controllo ActiveX
- Windows Media Player Mobile, incorporamento del controllo ActiveX
- Controllo ActiveX di Windows Media Player, incorporamento
- Controllo ActiveX Windows Media Player Mobile, incorporamento
- Controllo ActiveX, incorporamento
- Windows Media Player, programmi basati su Windows
- Modello a oggetti di Windows Media Player, programmi basati su Windows
- modello a oggetti, programmi basati su Windows
- Windows Media Player Mobile, programmi basati su Windows
- Controllo ActiveX di Windows Media Player, programmi basati su Windows
- Controllo ActiveX Windows Media Player Mobile, programmi basati su Windows
- Controllo ActiveX, programmi basati su Windows
- Incorporamento di programmi basati su Windows
- incorporamento, programmi basati su Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2190f0d0076fe3253c39f583ae7d2c197f8cb11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331452"
---
# <a name="hosting-the-windows-media-player-control-in-a-windows-application"></a>Hosting del controllo Media Player Windows in un'applicazione Windows

Per utilizzare il controllo ActiveX di Windows Media Player (inclusa l'interfaccia utente) in un programma basato su Windows, è necessario specificare un contenitore di controlli ActiveX. ATL fornisce la classe **CAxWindow** per fornire la funzionalità della finestra host ActiveX.

Per ospitare il controllo Media Player Windows utilizzando la classe **CAxWindow** , attenersi alla seguente procedura:

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

    

3.  Quando viene creata la finestra dell'applicazione, chiamare **AtlAxWinInit**, che è necessario quando si utilizza la finestra host ActiveX ATL.
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

    

7.  Creare il controllo Media Player Windows nella finestra host usando l'ID classe:
    ```C++
    hr = spHost->CreateControl(CComBSTR(_T("{6BF52A52-394A-11d3-B153-00C04F79FAA6}")), m_wndView, 0);
    
    ```

    

8.  Recuperare il puntatore all'interfaccia **IWMPPlayer** :
    ```C++
    hr = m_wndView.QueryControl(&m_spWMPPlayer);
    
    ```

    

Quando si scrive codice personalizzato, assicurarsi di controllare ogni codice restituito **HRESULT** per individuare eventuali errori.

Per un esempio completo in cui viene illustrato come ospitare il controllo ActiveX di Windows Media Player usando la classe **CAxWindow** , vedere l'esempio WMPHost.

## <a name="hosting-the-windows-media-player-10-mobile-control-in-windows-ce"></a>Hosting del controllo Windows Media Player 10 mobile in Windows CE

Microsoft eMbedded Visual C++ 4,0 e Pocket PC 2003 SDK o lo Smartphone 2003 SDK devono essere installati quando si sviluppano applicazioni basate su Windows CE che ospitano un controllo Windows Media Player 10 Mobile. Inoltre, a differenza di ATL per Windows, ATL per Windows CE non supporta il modello di threading dell'Apartment. Pertanto, è necessario trovare tutte le istanze del threading Apartment nel progetto ATL e modificarle in modo da utilizzare il threading libero.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Esempi**](samples.md)
</dt> <dt>

[**Uso del controllo Media Player di Windows in un programma C++**](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




