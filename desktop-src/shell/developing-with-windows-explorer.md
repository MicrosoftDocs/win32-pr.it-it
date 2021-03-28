---
description: Esplora risorse è una potente applicazione di esplorazione e gestione delle risorse.
ms.assetid: 879CE652-EDC0-4a14-925E-C83763133BE5
title: Sviluppo con Esplora risorse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b7b68d48f2d1becea23311847a5ce41b3776321
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484388"
---
# <a name="developing-with-windows-explorer"></a>Sviluppo con Esplora risorse

Esplora risorse è una potente applicazione di esplorazione e gestione delle risorse. È possibile accedere a Esplora risorse come un intero integrato tramite Explorer.exe o l'interfaccia [**IExplorerBrowser**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser) . Esplora risorse (Explorer.exe) può essere generato come processo separato utilizzando [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) o una funzione simile.

> [!Note]  
> Le opzioni della riga di comando per Explorer.exe sono documentate nel sito di supporto di Microsoft Windows nell'articolo [Opzioni di Esplora risorse Command-Line](https://support.microsoft.com/kb/152457).

 

Le finestre aperte di Esplora risorse possono essere individuate e programmate tramite [**ishellwindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows) (CLSID \_ ShellWindows) e le nuove istanze di Esplora risorse possono essere create tramite [**IWebBrowser2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752127(v=vs.85)) (CLSID \_ ShellBrowserWindow).

Nell'esempio di codice riportato di seguito viene illustrato come utilizzare il modello di automazione di Esplora risorse per creare e individuare le finestre di esplorazione in esecuzione.


```
#define _WIN32_WINNT 0x0600
#define _WIN32_IE 0x0700
#define _UNICODE

#include <windows.h>
#include <shobjidl.h>
#include <shlobj.h>
#include <shlwapi.h>
#include <strsafe.h>
#include <propvarutil.h>
 
#pragma comment(lib, "shlwapi.lib")
#pragma comment(lib, "ole32.lib")
#pragma comment(lib, "shell32.lib")
#pragma comment(lib, "propsys.lib")
 
// Use the Shell Windows object to find all of the explorer and IExplorer 
// windows and close them.
 
void CloseExplorerWindows()
{
    IShellWindows* psw;
    
    if (SUCCEEDED(CoCreateInstance(CLSID_ShellWindows, 
                                   NULL,  
                                   CLSCTX_LOCAL_SERVER, 
                                   IID_PPV_ARGS(&psw))))
    {
        VARIANT v = { VT_I4 };
        if (SUCCEEDED(psw->get_Count(&v.lVal)))
        {
            // Walk backward to make sure that the windows that close
            // do not cause the array to be reordered.
            while (--v.lVal >= 0)
            {
                IDispatch *pdisp;
                
                if (S_OK == psw->Item(v, &pdisp))
                {
                    IWebBrowser2 *pwb;
                    if (SUCCEEDED(pdisp->QueryInterface(IID_PPV_ARGS(&pwb))))
                    {
                        pwb->Quit();
                        pwb->Release();
                    }
                    pdisp->Release();
                }
            }
        }
        psw->Release();
    }
}
 
// Convert an IShellItem or IDataObject into a VARIANT that holds an IDList
// suitable for use with IWebBrowser2::Navigate2.
 
HRESULT InitVariantFromObject(IUnknown *punk, VARIANT *pvar)
{
    VariantInit(pvar);
 
    PIDLIST_ABSOLUTE pidl;
    HRESULT hr = SHGetIDListFromObject(punk, &pidl);
    if (SUCCEEDED(hr))
    {
        hr = InitVariantFromBuffer(pidl, ILGetSize(pidl), pvar);
        CoTaskMemFree(pidl);
    }
    return hr;
}
 
HRESULT ParseItemAsVariant(PCWSTR pszItem, IBindCtx *pbc, VARIANT *pvar)
{
    VariantInit(pvar);
 
    IShellItem *psi;
    HRESULT hr = SHCreateItemFromParsingName(pszItem, NULL, IID_PPV_ARGS(&psi));
    if (SUCCEEDED(hr))
    {
        hr = InitVariantFromObject(psi, pvar);
        psi->Release();
    }
    return hr;
}

HRESULT GetKnownFolderAsVariant(REFKNOWNFOLDERID kfid, VARIANT *pvar)
{
    VariantInit(pvar);
 
    PIDLIST_ABSOLUTE pidl;
    HRESULT hr = SHGetKnownFolderIDList(kfid, 0, NULL, &pidl);
    if (SUCCEEDED(hr))
    {
        hr = InitVariantFromBuffer(pidl, ILGetSize(pidl), pvar);
        CoTaskMemFree(pidl);
    }
    return hr;
}

HRESULT GetShellItemFromCommandLine(REFIID riid, void **ppv)
{
    *ppv = NULL;
    HRESULT hr = E_FAIL;

    int cArgs;
    PWSTR *ppszCmd = CommandLineToArgvW(GetCommandLineW(), &cArgs);
    if (ppszCmd && cArgs > 1)
    {
        WCHAR szSpec[MAX_PATH];
        StringCchCopyW(szSpec, ARRAYSIZE(szSpec), ppszCmd[1]);
        PathUnquoteSpacesW(szSpec);

        hr = szSpec[0] ? S_OK : E_FAIL;   // Protect against empty data
        if (SUCCEEDED(hr))
        {
            hr = SHCreateItemFromParsingName(szSpec, NULL, riid, ppv);
            if (FAILED(hr))
            {
                WCHAR szFolder[MAX_PATH];
                GetCurrentDirectoryW(ARRAYSIZE(szFolder), szFolder);

                hr = PathAppendW(szFolder, szSpec) ? S_OK : E_FAIL;
                if (SUCCEEDED(hr))
                {
                    hr = SHCreateItemFromParsingName(szFolder, NULL, riid, ppv);
                }
            }
        }
    }
    return hr;
}

HRESULT GetShellItemFromCommandLineAsVariant(VARIANT *pvar)
{
    VariantInit(pvar);

    IShellItem *psi;
    HRESULT hr = GetShellItemFromCommandLine(IID_PPV_ARGS(&psi));
    if (SUCCEEDED(hr))
    {
        hr = InitVariantFromObject(psi, pvar);
        psi->Release();
    }
    return hr;
}

void OpenWindow()
{
    IWebBrowser2 *pwb;
    HRESULT hr = CoCreateInstance(CLSID_ShellBrowserWindow, 
                                  NULL,
                                  CLSCTX_LOCAL_SERVER, 
                                  IID_PPV_ARGS(&pwb));
    if (SUCCEEDED(hr))
    {
        CoAllowSetForegroundWindow(pwb, 0);

        pwb->put_Left(100);
        pwb->put_Top(100);
        pwb->put_Height(600);
        pwb->put_Width(800);
 
        VARIANT varTarget = {0};
        hr = GetShellItemFromCommandLineAsVariant(&varTarget);
        if (FAILED(hr))
        {
            hr = GetKnownFolderAsVariant(FOLDERID_UsersFiles, &varTarget);
        }

        if (SUCCEEDED(hr))
        {
            VARIANT vEmpty = {0};
            hr = pwb->Navigate2(&varTarget, &vEmpty, &vEmpty, &vEmpty, &vEmpty);
            if (SUCCEEDED(hr))
            {
                pwb->put_Visible(VARIANT_TRUE);
            }
            VariantClear(&varTarget);
        }
        pwb->Release();
    }
}

int WINAPI WinMain(HINSTANCE, HINSTANCE, LPSTR, int)
{
    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED |  COINIT_DISABLE_OLE1DDE);
    if (SUCCEEDED(hr))
    {
        CloseExplorerWindows();

        OpenWindow();

        CoUninitialize();
    }
    return 0;
}
```



L'area client di Esplora risorse può essere ospitata tramite l'interfaccia [IExplorerBrowser](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser) . Il client di Esplora risorse e i controlli struttura ad albero dello spazio dei nomi sono componenti standard di Windows Vista e versioni successive. Gli sviluppatori possono riutilizzare le interfacce come componenti di compilazione. Un uso comune di questi controlli consiste nel creare esplorazioni personalizzate appropriate per il dominio del problema.

I controlli in Esplora risorse sono suddivisi nelle seguenti categorie funzionali:

-   [Controlli di navigazione](#navigation-controls)
-   [Controlli Command](#command-controls)
-   [Controlli di proprietà e di anteprima](#property-and-preview-controls)
-   [Filtro e visualizzazione di controlli](#filtering-and-view-controls)
-   [ListView (controllo)](#listview-control)

## <a name="navigation-controls"></a>Controlli di navigazione

I controlli di spostamento aiutano gli utenti a determinare il contesto e a spostarsi nello spazio del dominio logico associato, denominato pagespace. Ad esempio, pagespace per Esplora risorse è lo spazio dei nomi della shell. Pagespaces sono costituiti da zero o più pagine.

Nella tabella seguente sono elencati e descritti i controlli di navigazione disponibili in Esplora risorse in Windows Vista e nei sistemi operativi successivi.



| Controllo di navigazione               | Descrizione                                                                                                                                                                                |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Barra degli indirizzi (controllo di navigazione) | Consente di visualizzare l'indirizzo della pagina corrente in pagespace. È possibile fare clic sui pulsanti di navigazione per spostarsi tra i predecessori in pagespace. Gli utenti possono anche digitare URL e percorsi da esplorare. |
| Albero delle cartelle                      | Fornisce una nuova versione di un controllo struttura ad albero, ottimizzata per pagespaces di grandi dimensioni.                                                                                                                  |
| Viaggi                           | Abilita la navigazione relativa attraverso pulsanti di tipo Web, ad esempio **indietro** e **in** secondo piano.                                                                                                    |
| Titolo                            | Visualizza il nome e il contesto della finestra di esplorazione corrente.                                                                                                                                            |
| Pagespace                        | Visualizza il ramo corrente di pagespace. Le pagine possono essere ordinate in base a criteri diversi. Gli utenti possono fare clic su una pagina per passare a questa pagina.                                                        |



 

## <a name="command-controls"></a>Controlli Command

I controlli comando annunciano le funzionalità e le funzionalità di Esplora risorse agli utenti. Questi controlli eseguono azioni generali o azioni specifiche per uno o più elementi selezionati.



| Controllo Command | Descrizione                                                                                                                                                                                        |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Barra degli strumenti         | Visualizza i pulsanti per i comandi di uso comune, ovvero una nuova versione di una barra degli strumenti dei comandi. Le opzioni di personalizzazione includono i pulsanti a discesa, i pulsanti di divisione, il testo descrittivo facoltativo e un'area di overflow. |
| Banner            | Viene visualizzato come singolo controllo personalizzato, facoltativo al centro della barra degli strumenti. Rappresenta il comando primario per il contesto corrente.                                                             |
| Barra dei menu        | Visualizza i comandi attraverso i menu.                                                                                                                                                                   |
| Menu di scelta rapida    | Elenca un subset di comandi disponibili in modo contestuale pertinente che vengono visualizzati in seguito al clic con il pulsante destro del mouse su un elemento.                                                                               |



 

## <a name="property-and-preview-controls"></a>Controlli di proprietà e di anteprima

I controlli proprietà e anteprima vengono usati per visualizzare in anteprima gli elementi e per visualizzare e modificare le proprietà degli elementi.



| Controllo    | Descrizione                                                                                                                                                                                                                                        |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Anteprima    | Visualizza un'anteprima dell'elemento selezionato, ad esempio un'anteprima o un'icona in tempo reale.                                                                                                                                                                       |
| Proprietà | Consente di visualizzare le proprietà dell'elemento selezionato. Per le selezioni multiple, viene visualizzato un riepilogo delle proprietà per il gruppo selezionato di elementi. Per una selezione null, viene visualizzato un riepilogo delle proprietà della pagina corrente (contenuto del controllo ListView). |



 

## <a name="filtering-and-view-controls"></a>Filtro e visualizzazione di controlli

I controlli Filtering e View vengono usati per modificare il set di elementi nel controllo ListView e per modificare la presentazione degli elementi nel controllo ListView.



| Controllo   | Descrizione                                                                                                                 |
|-----------|-----------------------------------------------------------------------------------------------------------------------------|
| Filtro    | Filtra o dispone gli elementi in un controllo ListView in base alle proprietà elencate come colonne. Facendo clic su una colonna viene ordinata in base a tale proprietà. |
| Wordwheel | Filtra dinamicamente e in modo incrementale gli elementi visualizzati in un controllo ListView in base a una stringa di testo di input.                      |
| Visualizzazione      | Consente all'utente di modificare la modalità di visualizzazione di un controllo ListView. Un dispositivo di scorrimento può essere utilizzato per determinare le dimensioni dell'icona.                |



 

## <a name="listview-control"></a>ListView (controllo)

Il controllo ListView viene usato per visualizzare un set di elementi in una delle quattro modalità di visualizzazione: dettagli, riquadri, icone o panorama. Il controllo ListView consente inoltre all'utente di selezionare e attivare uno o più elementi.

> [!Caution]  
> Anche se alcuni di questi controlli hanno nomi e/o funzionalità simili ai controlli Windows Presentation Foundation standard (WPF) trovati nello spazio dei nomi System. Windows. Controls, sono classi distinte.

 

Questi controlli separati interagiscono in gran parte tramite gli eventi generati dall'interazione dell'utente o dai controlli stessi. Nella tabella seguente vengono illustrate le tre categorie di eventi principali.



| Categoria evento | Esempio                                                       |
|----------------|---------------------------------------------------------------|
| Spostamento     | Passa da una pagina all'altra.                               |
| Selezione      | Modifica della selezione corrente nel controllo ListView.               |
| Visualizza modifica    | Modifica dell'ordine di presentazione o della modalità di visualizzazione in ListView. |



 

 

 
