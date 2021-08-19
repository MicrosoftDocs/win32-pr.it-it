---
title: Metodo OnCreate
description: Metodo OnCreate
ms.assetid: b23546b3-968f-41d8-ba07-3d694152c3ed
keywords:
- Windows Media Player plug-in, metodo OnCreate
- plug-in, metodo OnCreate
- plug-in dell'interfaccia utente, metodo OnCreate
- Plug-in dell'interfaccia utente, metodo OnCreate
- Metodo OnCreate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac52b1c58c6799f89d29fb1ee24c09767fee26729e760b2b454f1a359bd57596
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118118109"
---
# <a name="the-oncreate-method"></a>Metodo OnCreate

Il metodo OnCreate viene chiamato quando la finestra del plug-in viene creata per la prima volta.

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



Questo metodo crea **il pulsante** Cerca e lo associa all'ID del comando IDC SEARCH, definito \_ all'inizio del file:


```C++
#define IDC_SEARCH 2000

```



Questo ID di comando viene mappato al metodo OnSearch nella sezione della mappa messaggi descritta in precedenza.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Implementazione di CPluginWindow**](implementing-cpluginwindow.md)
</dt> </dl>

 

 




