---
description: Windows Explorer è una potente applicazione di esplorazione e gestione delle risorse.
ms.assetid: 879CE652-EDC0-4a14-925E-C83763133BE5
title: Sviluppo con Windows Explorer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22d00b513b3ee73c30b100cb4236d2c9fb327e1f9557d12ba86738ee9e910ca2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118460185"
---
# <a name="developing-with-windows-explorer"></a>Sviluppo con Windows Explorer

Windows Explorer è una potente applicazione di esplorazione e gestione delle risorse. Windows Explorer è accessibile come intero integrato tramite Explorer.exe o [**l'interfaccia IExplorerBrowser.**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser) Windows Explorer (Explorer.exe) può essere generato come processo separato usando [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) o una funzione simile.

> [!Note]  
> Le opzioni della riga di comando Explorer.exe sono documentate nel sito del supporto tecnico microsoft Windows nell'articolo Windows [Explorer Command-Line Opzioni](https://support.microsoft.com/kb/152457).

 

Le finestre di Esplora risorse aperte possono essere individuate e programmate usando [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows) (CLSID ShellWindows) e le nuove istanze di Windows Explorer possono essere create usando \_ [**IWebBrowser2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752127(v=vs.85)) (CLSID \_ ShellBrowserWindow).

L'esempio di codice seguente illustra come usare Windows di automazione di Esplora risorse per creare e individuare le finestre di esplorazione in esecuzione.


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



L Windows area client di Esplora risorse può essere ospitata tramite [l'interfaccia IExplorerBrowser.](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser) Il client Windows Explorer e i controlli albero dello spazio dei nomi sono componenti standard Windows Vista e versioni successive. Gli sviluppatori possono riutilizzare le interfacce come componenti di compilazione. Un uso comune di questi controlli è la creazione di esplorazioni personalizzate appropriate al dominio del problema.

I controlli in Windows Explorer sono classificati nelle categorie funzionali seguenti:

-   [Controlli di spostamento](#navigation-controls)
-   [Controlli dei comandi](#command-controls)
-   [Controlli delle proprietà e dell'anteprima](#property-and-preview-controls)
-   [Applicazione di filtri e controlli di visualizzazione](#filtering-and-view-controls)
-   [Controllo Listview](#listview-control)

## <a name="navigation-controls"></a>Controlli di spostamento

I controlli di spostamento consentono agli utenti di determinare il contesto e di spostarsi nello spazio di dominio logico associato, denominato spazio di pagina. Ad esempio, lo spazio di pagina per Windows Explorer è lo spazio dei nomi Shell. Gli spazi di pagina sono costituiti da zero o più pagine.

Nella tabella seguente sono elencati e descritti i controlli di navigazione disponibili in Windows Explorer nel Windows Vista e nei sistemi operativi successivi.



| Controllo di spostamento               | Descrizione                                                                                                                                                                                |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Barra degli indirizzi (controllo Breadcrumb) | Visualizza l'indirizzo della pagina corrente nello spazio pagine. È possibile fare clic sui pulsanti di navigazione per passare a qualsiasi predecessore nello spazio della pagina. Gli utenti possono anche digitare URL e percorsi da esplorare. |
| Albero delle cartelle                      | Fornisce una nuova versione di un controllo struttura ad albero, ottimizzata per spazi di pagine di grandi dimensioni.                                                                                                                  |
| Viaggi                           | Abilita lo spostamento relativo tramite pulsanti di tipo Web, ad **esempio Indietro** e **Avanti.**                                                                                                    |
| Titolo                            | Visualizza il nome e il contesto correnti della finestra di esplorazione.                                                                                                                                            |
| Spazio pagine                        | Visualizza il ramo corrente dello spazio pagine. Le pagine possono essere ordinate in base a criteri diversi. Gli utenti possono fare clic su una pagina per passarla.                                                        |



 

## <a name="command-controls"></a>Controlli dei comandi

I controlli dei comandi annunciano agli utenti le funzionalità Windows Explorer. Questi controlli eseguono azioni generali o azioni specifiche di uno o più elementi selezionati.



| Controllo dei comandi | Descrizione                                                                                                                                                                                        |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Barra degli strumenti         | Visualizza i pulsanti per i comandi di uso comune (una nuova versione di una barra degli strumenti dei comandi). Le opzioni di personalizzazione includono pulsanti a discesa, pulsanti di divisione, testo descrittivo facoltativo e un'area di overflow. |
| Banner            | Viene visualizzato come singolo controllo personalizzato facoltativo al centro della barra degli strumenti. Rappresenta il comando primario per il contesto corrente.                                                             |
| Barra dei menu        | Visualizza i comandi tramite i menu.                                                                                                                                                                   |
| Menu di scelta rapida    | Elenca un subset contestualmente pertinente dei comandi disponibili che vengono visualizzati come risultato del clic con il pulsante destro del mouse su un elemento.                                                                               |



 

## <a name="property-and-preview-controls"></a>Controlli delle proprietà e dell'anteprima

I controlli proprietà e anteprima vengono usati per visualizzare in anteprima gli elementi e per visualizzare e modificare le proprietà degli elementi.



| Controllo    | Descrizione                                                                                                                                                                                                                                        |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Anteprima    | Visualizza un'anteprima dell'elemento selezionato, ad esempio un'anteprima o un'icona dinamica.                                                                                                                                                                       |
| Proprietà | Visualizza le proprietà dell'elemento selezionato. Per più selezioni, visualizza un riepilogo delle proprietà per il gruppo selezionato di elementi. Per una selezione Null, visualizza un riepilogo delle proprietà per la pagina corrente (contenuto della visualizzazione elenco). |



 

## <a name="filtering-and-view-controls"></a>Applicazione di filtri e controlli di visualizzazione

I controlli filtro e visualizzazione vengono usati per modificare il set di elementi nella visualizzazione elenco e per modificare la presentazione degli elementi nella visualizzazione elenco.



| Controllo   | Descrizione                                                                                                                 |
|-----------|-----------------------------------------------------------------------------------------------------------------------------|
| Filtro    | Filtra o dispone gli elementi in una visualizzazione elenco in base alle proprietà elencate come colonne. Facendo clic su una colonna, l'ordinamento viene ordinato in base a tale proprietà. |
| Ruota di parole | Filtra in modo dinamico e incrementale gli elementi visualizzati in una visualizzazione elenco in base a una stringa di testo di input.                      |
| Visualizzazione      | Consente all'utente di modificare la modalità di visualizzazione di un controllo listview. Un dispositivo di scorrimento può essere usato per determinare le dimensioni dell'icona.                |



 

## <a name="listview-control"></a>Controllo Listview

Il controllo listview viene usato per visualizzare un set di elementi in una delle quattro modalità di visualizzazione seguenti: dettagli, riquadri, icone o panorama. Il controllo listview consente inoltre all'utente di selezionare e attivare uno o più elementi.

> [!Caution]  
> Anche se alcuni di questi controlli hanno nomi e/o funzionalità simili ai controlli Windows Presentation Foundation (WPF) standard disponibili nel sistema. Windows. Controlla lo spazio dei nomi, sono classi distinte.

 

Questi controlli separati funzionano in gran parte tramite eventi generati dall'interazione dell'utente o dai controlli stessi. La tabella seguente illustra le tre categorie di eventi principali.



| Categoria evento | Esempio                                                       |
|----------------|---------------------------------------------------------------|
| Spostamento     | Da una pagina all'altra.                               |
| Selezione      | Modifica della selezione corrente nella visualizzazione elenco.               |
| Modifica della visualizzazione    | Modifica dell'ordine di presentazione o della modalità di visualizzazione nella visualizzazione elenco. |



 

 

 
