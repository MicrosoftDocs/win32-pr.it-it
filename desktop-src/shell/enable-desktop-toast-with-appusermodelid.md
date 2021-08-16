---
description: Questo argomento illustra come creare un collegamento per l'app, assegnarle un AppUserModelID e installarlo nel schermata Start.
title: Come abilitare le notifiche di tipo avviso popup sul desktop tramite un AppUserModelID
ms.topic: article
ms.date: 05/31/2018
ms.assetid: BB32CD0A-99E6-47dc-A913-39A7B3027314
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbSyntax
ms.openlocfilehash: 517c2b72e830c00b105048adc63923291f896cd5d0d77569c91b1aa12e034e60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459793"
---
# <a name="how-to-enable-desktop-toast-notifications-through-an-appusermodelid"></a>Come abilitare le notifiche di tipo avviso popup sul desktop tramite un AppUserModelID

Questo argomento illustra come creare un collegamento per l'app, assegnarle un [AppUserModelID](appids.md)e installarlo nel schermata Start. È consigliabile eseguire questa operazione nel programma di installazione Windows anziché nel codice dell'app. Senza un collegamento valido installato nel schermata Start o **in** Tutti i programmi, non è possibile generare una notifica di tipo avviso popup da un'app desktop.

> [!Note]  
> I metodi di esempio usati in questo argomento sono tratto [dall'esempio di](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DesktopToasts)avviso popup desktop .

 

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   COM

### <a name="prerequisites"></a>Prerequisiti

-   Librerie
    -   C++: Runtime.object.lib
    -   C: \# Windows. Winmd
-   C: \# Windows Code Pack dell'API per Microsoft .NET Framework
-   Una versione di Microsoft Visual Studio che supporta almeno Windows 8

## <a name="instructions"></a>Istruzioni

### <a name="step-1-prepare-the-shortcut-to-be-created"></a>Passaggio 1: Preparare il collegamento da creare

Questo esempio determina innanzitutto il percorso della cartella dei dati dell'app dell'utente tramite la [**funzione GetEnvironmentVariable.**](/windows/win32/api/processenv/nf-processenv-getenvironmentvariablea) Compone quindi il percorso completo del collegamento, determina che un collegamento con tale nome non esiste già in tale percorso e passa le informazioni a un altro metodo che crea e installa il collegamento.

Si noti che il collegamento può essere distribuito per utente o per app.


```C++
HRESULT DesktopToastsApp::TryCreateShortcut()
{
    wchar_t shortcutPath[MAX_PATH];
    DWORD charWritten = GetEnvironmentVariable(L"APPDATA", shortcutPath, MAX_PATH);
    HRESULT hr = charWritten > 0 ? S_OK : E_INVALIDARG;

    if (SUCCEEDED(hr))
    {
        errno_t concatError = wcscat_s(shortcutPath, ARRAYSIZE(shortcutPath), L"\\Microsoft\\Windows\\Start Menu\\Programs\\Desktop Toasts App.lnk");
 
        hr = concatError == 0 ? S_OK : E_INVALIDARG;
        if (SUCCEEDED(hr))
        {
            DWORD attributes = GetFileAttributes(shortcutPath);
            bool fileExists = attributes < 0xFFFFFFF;

            if (!fileExists)
            {
                hr = InstallShortcut(shortcutPath);  // See step 2.
            }
            else
            {
                hr = S_FALSE;
            }
        }
    }
    return hr;
}
```



### <a name="step-2-create-the-shortcut-and-install-it-in-the-start-screen"></a>Passaggio 2: Creare il collegamento e installarlo nel schermata Start

Questo esempio recupera anche l'archivio delle proprietà del collegamento e imposta la [proprietà](../properties/props-system-appusermodel-id.md) System.AppUserModel.ID richiesta da una variabile definita in precedenza, `AppID` .


```C++
HRESULT DesktopToastsApp::InstallShortcut(_In_z_ wchar_t *shortcutPath)
{
    wchar_t exePath[MAX_PATH];
    
    DWORD charWritten = GetModuleFileNameEx(GetCurrentProcess(), nullptr, exePath, ARRAYSIZE(exePath));

    HRESULT hr = charWritten > 0 ? S_OK : E_FAIL;
    
    if (SUCCEEDED(hr))
    {
        ComPtr<IShellLink> shellLink;
        hr = CoCreateInstance(CLSID_ShellLink, nullptr, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&shellLink));

        if (SUCCEEDED(hr))
        {
            hr = shellLink->SetPath(exePath);
            if (SUCCEEDED(hr))
            {
                hr = shellLink->SetArguments(L"");
                if (SUCCEEDED(hr))
                {
                    ComPtr<IPropertyStore> propertyStore;

                    hr = shellLink.As(&propertyStore);
                    if (SUCCEEDED(hr))
                    {
                        PROPVARIANT appIdPropVar;
                        hr = InitPropVariantFromString(AppId, &appIdPropVar);
                        if (SUCCEEDED(hr))
                        {
                            hr = propertyStore->SetValue(PKEY_AppUserModel_ID, appIdPropVar);
                            if (SUCCEEDED(hr))
                            {
                                hr = propertyStore->Commit();
                                if (SUCCEEDED(hr))
                                {
                                    ComPtr<IPersistFile> persistFile;
                                    hr = shellLink.As(&persistFile);
                                    if (SUCCEEDED(hr))
                                    {
                                        hr = persistFile->Save(shortcutPath, TRUE);
                                    }
                                }
                            }
                            PropVariantClear(&appIdPropVar);
                        }
                    }
                }
            }
        }
    }
    return hr;
}
```



## <a name="remarks"></a>Commenti

In alternativa all'approccio illustrato in questo argomento, è possibile usare un framework come Windows Installer XML (WiX) per generare il collegamento e distribuirlo come parte del programma di installazione Windows. In tal caso, questo codice deve essere incluso nell'msi anziché nel codice dell'app. Per altre informazioni, vedere il file di configurazione WiX di esempio incluso nell'esempio Invio di [notifiche di tipo avviso popup da app desktop.](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Toast%20notifications%20sample%20(Windows%208))

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Avvio rapido: Invio di una notifica di tipo avviso popup dal desktop](quickstart-sending-desktop-toast.md)
</dt> <dt>

[Esempio di invio notifiche di tipo avviso popup da app desktop](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Toast%20notifications%20sample%20(Windows%208))
</dt> <dt>

[ID modello utente applicazione (AppUserModelID)](appids.md)
</dt> <dt>

[Procedura: Installare gli strumenti Windows Installer XML (WiX)](/previous-versions/windows/server-essentials/gg513936(v=msdn.10))
</dt> <dt>

[Schema XML di tipo avviso popup](/uwp/schemas/tiles/toastschema/schema-root)
</dt> <dt>

[Panoramica delle notifiche di tipo avviso popup](/previous-versions/windows/apps/hh779727(v=win.10))
</dt> <dt>

[Avvio rapido: Invio di una notifica di tipo avviso popup](/previous-versions/windows/apps/hh465448(v=win.10))
</dt> <dt>

[Avvio rapido: Invio di una notifica push di tipo avviso popup](/previous-versions/windows/hh761487(v=win.10))
</dt> <dt>

[Linee guida ed elenco di controllo per le notifiche di tipo avviso popup](/windows/uwp/design/shell/tiles-and-notifications/)
</dt> <dt>

[Come aggiungere immagini a un modello di avviso popup](/previous-versions/windows/)
</dt> <dt>

[Come controllare le impostazioni di notifica di tipo avviso popup](/previous-versions/windows/)
</dt> <dt>

[Come scegliere e usare un modello di avviso popup](/previous-versions/windows/apps/hh465448(v=win.10))
</dt> <dt>

[Come gestire l'attivazione da una notifica di tipo avviso popup](/previous-versions/windows/apps/hh761468(v=win.10))
</dt> <dt>

[Come acconsentire esplicitamente alle notifiche di tipo avviso popup](/previous-versions/windows/apps/hh781238(v=win.10))
</dt> <dt>

[Scelta di un modello di avviso popup](/previous-versions/windows/apps/hh761494(v=win.10))
</dt> <dt>

[Opzioni audio di tipo Avviso popup](/previous-versions/windows/apps/hh761492(v=win.10))
</dt> </dl>

 

 
