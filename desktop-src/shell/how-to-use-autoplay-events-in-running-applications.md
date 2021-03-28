---
description: L'interfaccia IHWEventHandler può essere registrata nella tabella degli oggetti in esecuzione (ROT), in modo che le applicazioni in esecuzione abbiano accesso agli eventi AutoPlay.
ms.assetid: 6FEFFB5D-DD8B-4FEA-B273-D32FC30CAFEA
title: Come usare gli eventi AutoPlay nelle applicazioni in esecuzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51795a3992bdb40dde833bb3e352905efaa2be63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967438"
---
# <a name="how-to-use-autoplay-events-in-running-applications"></a>Come usare gli eventi AutoPlay nelle applicazioni in esecuzione

L'interfaccia [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) può essere registrata nella tabella degli oggetti in esecuzione (ROT), in modo che le applicazioni in esecuzione abbiano accesso agli eventi AutoPlay.

Nelle istruzioni seguenti viene descritto come utilizzare gli eventi AutoPlay nelle applicazioni in esecuzione.

## <a name="instructions"></a>Istruzioni

### <a name="step-1"></a>Passaggio 1:

Creare un nuovo componente che implementi l'interfaccia [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) .

### <a name="step-2"></a>Passaggio 2:

Inizializzare il nuovo componente con il valore InitCmdLine dalla voce specifica del gestore sotto la chiave dei **gestori** .

Questo passaggio è necessario perché AutoPlay non chiama il metodo Initialize.

### <a name="step-3"></a>Passaggio 3:

Chiamare la funzione [**CreateHardwareEventMoniker**](createhardwareeventmoniker.md) per ottenere un moniker che rappresenta il componente e il gestore eventi che si desidera chiamare.

### <a name="step-4"></a>Passaggio 4:

Usare il parametro *ppmoniker* per registrare il componente nella tabella ROT.

## <a name="remarks"></a>Commenti

> [!Note]  
> [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) può rappresentare rischi per la sicurezza. Per informazioni su come caricare correttamente le dll con versioni diverse di Windows, vedere la documentazione di **LoadLibrary** .

```cpp
typedef HRESULT (*CREATEHARDWAREEVENTMONIKER)(REFCLSID clsid, LPCWSTR pszEventHandler, IMoniker **ppmoniker);

HRESULT RegisterComponent(IUnknown* punk, DWORD* dpwToken)
{
    HRESULT hr = E_FAIL;
    HINSTANCE hinstShSvcs = LoadLibrary(TEXT("shsvcs.dll"));
    
    if (hinstShSvcs)
    {   
        CREATEHARDWAREEVENTMONIKER fct = (CREATEHARDWAREEVENTMONIKER)GetProcAddress(hinstShSvcs, "CreateHardwareEventMoniker");
        if (fct)
        {
            IMoniker* pmoniker;
            
            hr = fct(CLSID_App, TEXT("VideoCameraArrival"), &pmoniker);

            if (SUCCEEDED(hr))
            {
                IRunningObjectTable *prot;
                    
                if (SUCCEEDED(GetRunningObjectTable(0, &prot)))
                {
                    hr = prot->Register(ROTFLAGS_ALLOWANYCLIENT | ROTFLAGS_REGISTRATIONKEEPSALIVE, punk, pmoniker, &_dwRegisterROT);
                    prot->Release();
                }
                pmoniker->Release();
            }
            CoRegisterClassObject(CLSID_App, static_cast<IClassFactory *>(this), CLSCTX_LOCAL_SERVER, REGCLS_MULTIPLEUSE, &_dwRegisterClass;
        }
        FreeLibrary(hinstShSvcs);
    }
    return hr;
}
```

Per la chiamata a [**IRunningObjectTable:: Register**](/windows/win32/api/objidl/nf-objidl-irunningobjecttable-register) è necessario che il componente includa le seguenti informazioni **AppID** nel registro di sistema.

```
HKEY_CLASSES_ROOT
   AppID
      MyApp.exe
         (Default) = MyApplication
         AppID [REG_SZ] = {Your GUID here}
```

```
HKEY_CLASSES_ROOT
   AppID
      {The same GUID here}
         (Default) = MyApplication
         RunAs = Interactive User
```

## <a name="related-topics"></a>Argomenti correlati

[**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler)

[**CreateHardwareEventMoniker**](createhardwareeventmoniker.md)
