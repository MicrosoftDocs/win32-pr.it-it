---
description: L'interfaccia IHWEventHandler può essere registrata nella tabella degli oggetti in esecuzione (ROT, Running Object Table) in modo che le applicazioni in esecuzione possano accedere agli eventi AutoPlay.
ms.assetid: 6FEFFB5D-DD8B-4FEA-B273-D32FC30CAFEA
title: Come usare gli eventi AutoPlay nelle applicazioni in esecuzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab30fa020b5501f8832a5b350ad409934ecbb4258d75adf147e908c699516474
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714817"
---
# <a name="how-to-use-autoplay-events-in-running-applications"></a>Come usare gli eventi AutoPlay nelle applicazioni in esecuzione

[**L'interfaccia IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) può essere registrata nella tabella degli oggetti in esecuzione (ROT, Running Object Table) in modo che le applicazioni in esecuzione possano accedere agli eventi AutoPlay.

Le istruzioni seguenti descrivono come usare gli eventi AutoPlay nelle applicazioni in esecuzione.

## <a name="instructions"></a>Istruzioni

### <a name="step-1"></a>Passaggio 1:

Creare un nuovo componente che implementa [**l'interfaccia IHWEventHandler.**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler)

### <a name="step-2"></a>Passaggio 2:

Inizializzare il nuovo componente con il valore InitCmdLine della voce del gestore specifico sotto la **chiave Handlers.**

Questo passaggio è obbligatorio perché Autoplay non chiama il metodo Initialize.

### <a name="step-3"></a>Passaggio 3:

Chiamare la [**funzione CreateHardwareEventMoniker**](createhardwareeventmoniker.md) per ottenere un moniker che rappresenta il componente e il gestore eventi da chiamare.

### <a name="step-4"></a>Passaggio 4:

Usare il *parametro ppmoniker* per registrare il componente nella rot.

## <a name="remarks"></a>Commenti

> [!Note]  
> [**LoadLibrary può**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) comportare rischi per la sicurezza. Fare riferimento alla **documentazione di LoadLibrary** per informazioni su come caricare correttamente le DLL con versioni diverse Windows.

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

La chiamata a [**IRunningObjectTable::Register**](/windows/win32/api/objidl/nf-objidl-irunningobjecttable-register) richiede che il componente abbia le informazioni **AppID** seguenti nel Registro di sistema.

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
