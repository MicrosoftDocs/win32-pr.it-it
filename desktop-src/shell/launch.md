---
description: Dopo che l'applicazione ha individuato un oggetto file, il passaggio successivo consiste spesso nell'agire in qualche modo su di esso.
ms.assetid: d774c3b2-4caf-460a-ac32-0ed603491d5f
title: Avvio di applicazioni (ShellExecute, ShellExecuteEx, SHELLEXECUTEINFO)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3ae5640acdbf4d959b97607cc66a4fd8fe8ac24
ms.sourcegitcommit: 89aa14b1f685f8d65d56ecbdb8bef12246c33cf9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/08/2021
ms.locfileid: "113508612"
---
# <a name="launching-applications-shellexecute-shellexecuteex-shellexecuteinfo"></a>Avvio di applicazioni (ShellExecute, ShellExecuteEx, SHELLEXECUTEINFO)

Dopo che l'applicazione ha individuato un oggetto file, il passaggio successivo consiste spesso nell'agire in qualche modo su di esso. Ad esempio, l'applicazione potrebbe voler avviare un'altra applicazione che consente all'utente di modificare un file di dati. Se il file di interesse è un eseguibile, è possibile che l'applicazione voglia semplicemente avviarlo. Questo documento illustra come usare [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) o [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) per eseguire queste attività.

-   [Uso di ShellExecute e ShellExecuteEx](#using-shellexecute-and-shellexecuteex)
    -   [Verbi oggetto](#object-verbs)
    -   [Uso di ShellExecuteEx per fornire servizi di attivazione da un sito](#using-shellexecuteex-to-provide-activation-services-from-a-site)
    -   [Uso di ShellExecute per avviare la finestra di dialogo Di ricerca](#using-shellexecute-to-launch-the-search-dialog-box)
-   [Esempio semplice di come usare ShellExecuteEx](#a-simple-example-of-how-to-use-shellexecuteex)

## <a name="using-shellexecute-and-shellexecuteex"></a>Uso di ShellExecute e ShellExecuteEx

Per usare [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) o [**ShellExecuteEx,**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)l'applicazione deve specificare l'oggetto file o cartella su cui intervenire e un *verbo* che specifica l'operazione. Per **ShellExecute assegnare** questi valori ai parametri appropriati. Per **ShellExecuteEx** compilare i membri appropriati di una [**struttura SHELLEXECUTEINFO.**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) Esistono anche diversi altri membri o parametri che possono essere usati per ottimizzare il comportamento delle due funzioni.

Gli oggetti file e cartelle possono far parte dell'file system o degli oggetti virtuali e possono essere identificati da percorsi o puntatori agli elenchi di identificatori di elemento (PID).

### <a name="object-verbs"></a>Verbi oggetto

I verbi disponibili per un oggetto sono essenzialmente gli elementi disponibili nel menu di scelta rapida di un oggetto. Per trovare i verbi disponibili, cercare nel Registro di sistema in

**HKEY \_ CLASS \_ ROOT** \\ **CLSID** \\ *{object \_ clsid}* \\ **Verbo shell** \\ 

dove *object \_ clsid* è l'identificatore di classe (CLSID) dell'oggetto e *verbo* è il nome del verbo disponibile. La *sottochiave* del comando del verbo contiene i dati \\  che indicano cosa accade quando viene richiamato tale verbo.

Per scoprire quali verbi sono disponibili per [gli oggetti shell predefiniti,](handlers.md)cercare nel Registro di sistema in

**HKEY \_ Verbo \_ shell classes root** \\ *\_ nome* \\  \\ *oggetto*

dove *nome \_ oggetto* è il nome dell'oggetto Shell predefinito. Anche in questo caso, *la sottochiave* del comando del verbo contiene i dati che indicano \\  cosa accade quando viene richiamato tale verbo.

I verbi disponibili comunemente includono:



| Verbo       | Descrizione                                                                                              |
|------------|----------------------------------------------------------------------------------------------------------|
| modifica       | Avvia un editor e apre il documento per la modifica.                                                   |
| trovare       | Avvia una ricerca a partire dalla directory specificata.                                                |
| apre       | Avvia un'applicazione. Se questo file non è un file eseguibile, viene avviata l'applicazione associata. |
| print      | Stampa il file di documento.                                                                                |
| properties | Visualizza le proprietà dell'oggetto.                                                                        |
| RunAs      | Avvia un'applicazione come amministratore. Controllo dell'account utente richiederà all'utente il consenso per eseguire l'applicazione con privilegi elevati o immissione delle credenziali di un account amministratore usato per eseguire l'applicazione. |



Ogni verbo corrisponde al comando che verrebbe usato per avviare l'applicazione da una finestra della console. Il  verbo aperto è un buon esempio, in quanto è comunemente supportato. Per .exe file, **apri avvia** semplicemente l'applicazione. Tuttavia, viene usato più comunemente per avviare un'applicazione che opera su un file specifico. Ad esempio, .txt file possono essere aperti da Microsoft WordPad. Il **verbo** open per un .txt file corrisponderebbe quindi a qualcosa di simile al comando seguente:


```C++
C:\Program Files\Windows NT\Accessories\Wordpad.exe" "%1"
```



Quando si usa [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) o [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) per aprire un file .txt, Wordpad.exe viene avviato con il file specificato come argomento. Alcuni comandi possono avere argomenti aggiuntivi, ad esempio flag, che possono essere aggiunti in base alle esigenze per avviare correttamente l'applicazione. Per altre informazioni sui menu di scelta rapida e sui verbi, vedere [Estensione dei menu di scelta rapida](context.md).

In generale, il tentativo di determinare l'elenco di verbi disponibili per un determinato file è piuttosto complesso. In molti casi, è sufficiente impostare il *parametro lpVerb* su **NULL,** che richiama il comando predefinito per il tipo di file. Questa procedura equivale in genere all'impostazione *di lpVerb* su "open", ma alcuni tipi di file possono avere un comando predefinito diverso. Per altre informazioni, vedere [Estensione dei menu di scelta rapida](context.md) e la documentazione di riferimento [**shellExecuteEx.**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)

### <a name="using-shellexecuteex-to-provide-activation-services-from-a-site"></a>Uso di ShellExecuteEx per fornire servizi di attivazione da un sito

I servizi di una catena di siti possono controllare molti comportamenti di attivazione degli elementi. A Windows 8, è possibile fornire un puntatore alla catena del sito a [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) per abilitare questi comportamenti. Per fornire il sito a **ShellExecuteEx:**

-   Specificare il flag SEE \_ MASK \_ FLAG \_ HINST \_ IS SITE nel membro \_ **fMask** di [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa).
-   Specificare [**IUnknown nel**](/windows/win32/api/unknwn/nn-unknwn-iunknown) membro **hInstApp** di [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa).

### <a name="using-shellexecute-to-launch-the-search-dialog-box"></a>Uso di ShellExecute per avviare la finestra di dialogo Di ricerca

Quando un utente fa clic con il pulsante destro del mouse sull'icona di una cartella Windows Explorer, una delle voci di menu è "Cerca". Se selezionano tale elemento, Shell avvia l'utilità Di ricerca. Questa utilità visualizza una finestra di dialogo che può essere usata per cercare nei file una stringa di testo specificata. Un'applicazione può avviare a livello di codice l'utilità di ricerca per una directory chiamando [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), con "find" come parametro *lpVerb* e il percorso della directory come *parametro lpFile.* Ad esempio, la riga di codice seguente avvia l'utilità di ricerca per la directory c: \\ MyPrograms.


```C++
ShellExecute(hwnd, "find", "c:\\MyPrograms", NULL, NULL, 0);
```



## <a name="a-simple-example-of-how-to-use-shellexecuteex"></a>Esempio semplice di come usare ShellExecuteEx

L'applicazione console di esempio seguente illustra l'uso di [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa). La maggior parte del codice di controllo degli errori è stata omessa per maggiore chiarezza.


```C++
#include <shlobj.h>
#include <shlwapi.h>
#include <objbase.h>

main()
{
    LPITEMIDLIST pidlWinFiles = NULL;
    LPITEMIDLIST pidlItems = NULL;
    IShellFolder *psfWinFiles = NULL;
    IShellFolder *psfDeskTop = NULL;
    LPENUMIDLIST ppenum = NULL;
    STRRET strDispName;
    TCHAR pszParseName[MAX_PATH];
    ULONG celtFetched;
    SHELLEXECUTEINFO ShExecInfo;
    HRESULT hr;
    BOOL fBitmap = FALSE;

    hr = SHGetFolderLocation(NULL, CSIDL_WINDOWS, NULL, NULL, &pidlWinFiles);

    hr = SHGetDesktopFolder(&psfDeskTop);

    hr = psfDeskTop->BindToObject(pidlWinFiles, NULL, IID_IShellFolder, (LPVOID *) &psfWinFiles);
    hr = psfDeskTop->Release();

    hr = psfWinFiles->EnumObjects(NULL,SHCONTF_FOLDERS | SHCONTF_NONFOLDERS, &ppenum);

    while( hr = ppenum->Next(1,&pidlItems, &celtFetched) == S_OK && (celtFetched) == 1)
    {
        psfWinFiles->GetDisplayNameOf(pidlItems, SHGDN_FORPARSING, &strDispName);
        StrRetToBuf(&strDispName, pidlItems, pszParseName, MAX_PATH);
        CoTaskMemFree(pidlItems);
        if(StrCmpI(PathFindExtension(pszParseName), TEXT( ".bmp")) == 0)
        {
            fBitmap = TRUE;
            break;
        }
    }

    ppenum->Release();

    if(fBitmap)
    {
        ShExecInfo.cbSize = sizeof(SHELLEXECUTEINFO);
        ShExecInfo.fMask = NULL;
        ShExecInfo.hwnd = NULL;
        ShExecInfo.lpVerb = NULL;
        ShExecInfo.lpFile = pszParseName;
        ShExecInfo.lpParameters = NULL;
        ShExecInfo.lpDirectory = NULL;
        ShExecInfo.nShow = SW_MAXIMIZE;
        ShExecInfo.hInstApp = NULL;

        ShellExecuteEx(&ShExecInfo);
    }

    CoTaskMemFree(pidlWinFiles);
    psfWinFiles->Release();

    return 0;
}
```



L'applicazione recupera innanzitutto il file PIDL della directory Windows ed enumera il relativo contenuto finché non trova il primo file .bmp file. A differenza dell'esempio precedente, [**IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) viene usato per recuperare il nome di analisi del file anziché il nome visualizzato. Poiché si tratta di file system, il nome di analisi è un percorso completo, che è quello necessario per [**ShellExecuteEx.**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)

Dopo aver individuato il .bmp file, i valori appropriati vengono assegnati ai membri di una [**struttura SHELLEXECUTEINFO.**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) Il **membro lpFile** è impostato sul nome di analisi del file e il membro **lpVerb** su **NULL** per avviare l'operazione predefinita. In questo caso, l'operazione predefinita è "open". La struttura viene quindi passata a [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), che avvia il gestore predefinito per i file bitmap, in genere MSPaint.exe, per aprire il file. Al termine della funzione, gli PID vengono liberati e Windows'interfaccia [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) della cartella.

 

 
