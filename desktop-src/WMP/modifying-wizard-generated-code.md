---
title: Modifica del codice generato dalla procedura guidata
description: Modifica del codice generato dalla procedura guidata
ms.assetid: 391a7773-c3e2-499a-bb63-e5934537d963
keywords:
- Windows Media Player Mobile, plug-in
- Plug-in di Windows Media Player Mobile, interfaccia utente
- Plug-in di Windows Media Player Mobile
- plug-in, interfaccia utente
- plug-in, Windows Media Player Mobile
- plug-in dell'interfaccia utente, Windows Media Player Mobile
- Plug-in dell'interfaccia utente, Windows Media Player Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a83bda7cb265d0c2e039ada6d9d827c6da3faf63
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298603"
---
# <a name="modifying-wizard-generated-code"></a>Modifica del codice generato dalla procedura guidata

Esistono diverse posizioni nel codice del plug-in generato dalla procedura guidata che è necessario modificare prima che il plug-in funzioni con Windows Media Player 10 Mobile. Il codice che è necessario modificare è in grassetto negli esempi seguenti.

## <a name="changes-to-wmpplugh"></a>Modifiche a wmpplug. h

I metodi ANSI non sono supportati nei dispositivi che eseguono Windows CE, quindi è necessario modificare il metodo ANSI seguente generato dalla procedura guidata in wmpplug. h:


```C++
return( ::PostMessage( HWND_BROADCAST, ::RegisterWindowMessageA( "WMPlayer_PluginAddRemove" ), 0, 0 ) );
```



Modificarlo come illustrato di seguito in modo che diventi un metodo Unicode:


```C++
return( ::PostMessage( HWND_BROADCAST, ::RegisterWindowMessageW( L"WMPlayer_PluginAddRemove" ), 0, 0 ) );
```



## <a name="changes-to-networkpluginh"></a>Modifiche a NetworkPlugin. h

Trovare il codice seguente in NetworkPlugin. h:


```C++
BEGIN_COM_MAP(CNetworkPlugin)
    COM_INTERFACE(IWMPPluginUI)
END_COM_MAP()
```



Modificare il codice in modo che abbia un aspetto simile al seguente:


```C++
BEGIN_COM_MAP(CNetworkPlugin)
    
COM_INTERFACE_ENTRY_IID(__uuidof(IWMPPluginUI), IWMPPluginUI)
END_COM_MAP()
```



## <a name="changes-to-networkplugindllcpp"></a>Modifiche a NetworkPlugindll. cpp

Trovare la funzione **DllMain** in NetworkPlugindll. cpp:


```C++
extern "C" BOOL WINAPI DllMain(HINSTANCE hInstance, DWORD dwReason, LPVOID /*lpReserved*/)
{
    if (dwReason == DLL_PROCESS_ATTACH)
    {
        _Module.Init(ObjectMap, hInstance);
        DisableThreadLibraryCalls(hInstance);
    }
    else if (dwReason == DLL_PROCESS_DETACH)
        _Module.Term();
    return TRUE;    // ok
}
```



Modificare il codice in modo che abbia un aspetto simile al seguente:


```C++
extern "C" BOOL WINAPI DllMain(HANDLE hInstance, DWORD dwReason, LPVOID /*lpReserved*/)
{
    if (dwReason == DLL_PROCESS_ATTACH)
    {
        _Module.Init(ObjectMap, (HINSTANCE)hInstance);
#ifndef UNDER_CE
        DisableThreadLibraryCalls((HINSTANCE)hInstance);
#endif
    }
    else if (dwReason == DLL_PROCESS_DETACH)
        _Module.Term();
    return TRUE;    // ok
}
```



## <a name="changes-to-networkplugincpp"></a>Modifiche a NetworkPlugin. cpp

Trovare il codice seguente in NetworkPlugin. cpp:


```C++
hr = m_spCore->QueryInterface(&spConnectionContainer);
```



Modificare il codice in modo che abbia un aspetto simile al seguente:


```C++
hr = m_spCore->QueryInterface(__uuidof(IConnectionPointContainer), (void**)&spConnectionContainer);
```



## <a name="change-the-threading-model"></a>Modificare il modello di threading

Diversamente da ATL per Windows, ATL per Windows CE non supporta il modello di threading dell'Apartment perché il modello di Apartment richiede più risorse di memoria rispetto ai modelli a thread singolo e a thread libero. Pertanto, è necessario trovare tutte le istanze del threading Apartment in StdAfx. h e NetworkPlugin. RGS e modificarle per indicare il threading libero.

Inoltre, è possibile chiamare solo il controllo Windows Media Player 10 Mobile dal thread in cui è stato creato.

## <a name="build-and-test-the-project"></a>Compilare e testare il progetto

Dopo aver apportato queste modifiche, è possibile compilare il progetto per verificarne la compilazione prima di aggiungere qualsiasi codice personalizzato.

1.  Impostare la configurazione del progetto attivo sulla versione Win32 (WCE ARMV4) debug o Win32 (WCE ARMV4).
2.  Impostare la piattaforma attiva su Pocket PC 2003.
3.  Fare clic sulla voce di menu **Compila** , quindi selezionare **Compila NetworkPlugin.dll**. Deve compilare, scaricare e registrare se stesso nel dispositivo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione di un plug-in dell'interfaccia utente per Windows Media Player 10 Mobile**](creating-a-user-interface-plug-in-for-windows-media-player-10-mobile.md)
</dt> </dl>

 

 




