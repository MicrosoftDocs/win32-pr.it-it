---
title: Uso del controllo Media Player Windows in un'applicazione console
description: Uso del controllo Media Player Windows in un'applicazione console
ms.assetid: e5162aad-69d5-4253-83d1-46735336e6da
keywords:
- Windows Media Player, incorporamento del controllo ActiveX
- Modello a oggetti di Windows Media Player, incorporamento del controllo ActiveX
- modello a oggetti, incorporamento del controllo ActiveX
- Windows Media Player Mobile, incorporamento del controllo ActiveX
- Controllo ActiveX di Windows Media Player, incorporamento
- Controllo ActiveX Windows Media Player Mobile, incorporamento
- Controllo ActiveX, incorporamento
- Windows Media Player, applicazioni console
- Modello a oggetti di Windows Media Player, applicazioni console
- modello a oggetti, applicazioni console
- Windows Media Player Mobile, applicazioni console
- Controllo ActiveX Windows Media Player, applicazioni console
- Controllo ActiveX Windows Media Player Mobile, applicazioni console
- Controllo ActiveX, applicazioni console
- incorporamento di applicazioni console
- incorporamento, applicazioni console
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53cc7701fc10848ca246d9cf100d0716e1955b5e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330703"
---
# <a name="using-the-windows-media-player-control-in-a-console-application"></a>Uso del controllo Media Player Windows in un'applicazione console

È possibile creare un'istanza dell'oggetto COM Media Player Windows direttamente tramite **CoCreateInstance**. Quando si esegue questa operazione, l'oggetto **Player** non visualizza alcuna interfaccia utente. Tuttavia, l'oggetto è ancora utile per le attività che non richiedono l'interfaccia utente, ad esempio l'uso della libreria, la riproduzione di file audio digitali o l'accesso alle proprietà del lettore.

Nell'esempio di codice seguente viene illustrato un semplice programma console che visualizza la versione di Windows Media Player in una finestra di messaggio. Il codice di esempio USA ATL per sfruttare i puntatori intelligenti e la classe String **CComBSTR** .


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

[**Uso del controllo Media Player di Windows in un programma C++**](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




