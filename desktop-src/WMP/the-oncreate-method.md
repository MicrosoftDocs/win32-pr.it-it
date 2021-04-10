---
title: Metodo OnCreate
description: Metodo OnCreate
ms.assetid: b23546b3-968f-41d8-ba07-3d694152c3ed
keywords:
- Plug-in di Windows Media Player, metodo OnCreate
- plug-in, metodo OnCreate
- plug-in dell'interfaccia utente, metodo OnCreate
- Plug-in dell'interfaccia utente, metodo OnCreate
- OnCreate (metodo)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d896ed9ebc6e9dc2bff9ff24ad23d50f7905c24
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855510"
---
# <a name="the-oncreate-method"></a>Metodo OnCreate

Il metodo OnCreate viene chiamato quando viene creata per la prima volta la finestra del plug-in.

Il codice seguente viene usato per implementare questo metodo:


```C++
LRESULT OnCreate(UINT uMsg, WPARAM wParam, LPARAM lParam, BOOL& bHandled)
{
    HWND hCtrl = ::CreateWindowEx(0L, _T("BUTTON"), _T("Search"),
        WS_CHILD | BS_PUSHBUTTON, 10, 10, 100, 30, m_hWnd, 
        (HMENU)IDC_SEARCH, _Module.GetResourceInstance(), NULL);
    ::ShowWindow(hCtrl, SW_SHOW );
    return 0;
}

```



Questo metodo crea il pulsante **Search** e lo associa all'ID del \_ comando di ricerca IDC, definito all'inizio del file:


```C++
#define IDC_SEARCH 2000

```



Questo ID comando è mappato al metodo OnSearch nella sezione della mappa messaggi descritta in precedenza.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Implementazione di CPluginWindow**](implementing-cpluginwindow.md)
</dt> </dl>

 

 




