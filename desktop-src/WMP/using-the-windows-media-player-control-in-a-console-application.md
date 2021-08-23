---
title: Uso del controllo Windows Media Player in un'applicazione console
description: Uso del controllo Windows Media Player in un'applicazione console
ms.assetid: e5162aad-69d5-4253-83d1-46735336e6da
keywords:
- Windows Media Player,incorporamento ActiveX controllo
- Windows Media Player a oggetti, incorporamento ActiveX controllo
- modello a oggetti, incorporamento ActiveX controllo
- Windows Media Player Mobile, incorporamento ActiveX controllo
- Windows Media Player ActiveX, incorporamento
- Windows Media Player Controllo ActiveX per dispositivi mobili, incorporamento
- ActiveX, incorporamento
- Windows Media Player,applicazioni console
- Windows Media Player a oggetti, applicazioni console
- modello a oggetti, applicazioni console
- Windows Media Player Applicazioni per dispositivi mobili e console
- Windows Media Player ActiveX, applicazioni console
- Windows Media Player Controllo ActiveX per dispositivi mobili, applicazioni console
- ActiveX, applicazioni console
- incorporamento di applicazioni console
- incorporamento, applicazioni console
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eef4bab6457314546f8953980678c672dad82984a4badc548a5c9d868da2839
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118830470"
---
# <a name="using-the-windows-media-player-control-in-a-console-application"></a>Uso del controllo Windows Media Player in un'applicazione console

È possibile creare un'istanza dell'Windows Media Player COM direttamente usando **CoCreateInstance**. In questo caso, **l'oggetto Player** non visualizza alcuna interfaccia utente. Tuttavia, l'oggetto è ancora utile per le attività che non richiedono l'interfaccia utente, ad esempio l'uso della libreria, la riproduzione di file audio digitali o l'accesso alle proprietà del lettore.

Il codice di esempio seguente illustra un semplice programma console che visualizza la Windows Media Player in una finestra di messaggio. Il codice di esempio usa ATL per sfruttare i puntatori intelligenti e la **classe stringa CComBSTR.**


```C++
#include "atlbase.h"
#include "atlwin.h"
#include "wmp.h"

int _tmain(int argc, _TCHAR* argv[])
{
    CoInitialize(NULL);

    HRESULT hr = S_OK;
    CComBSTR bstrVersionInfo; // Contains the version string.
    CComPtr<IWMPPlayer> spPlayer;  // Smart pointer to IWMPPlayer interface.

    hr = spPlayer.CoCreateInstance( __uuidof(WindowsMediaPlayer), 0, CLSCTX_INPROC_SERVER );

    if(SUCCEEDED(hr))
    {
        hr = spPlayer->get_versionInfo(&bstrVersionInfo);
    }

    if(SUCCEEDED(hr))
    {
        // Show the version in a message box.
        COLE2T pStr(bstrVersionInfo);
        MessageBox( NULL, (LPCSTR)pStr, _T("Windows Media Player Version"), MB_OK );
    }

    // Clean up.
    spPlayer.Release();
    CoUninitialize();

    return 0;
}

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso del Windows Media Player controllo in un programma C++**](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




