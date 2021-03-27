---
description: Una volta che l'applicazione ha individuato un oggetto file, il passaggio successivo è spesso quello di intervenire in qualche modo.
ms.assetid: d774c3b2-4caf-460a-ac32-0ed603491d5f
title: Avvio di applicazioni (ShellExecute, ShellExecuteEx, SHELLEXECUTEINFO)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e528e6c816040a83d57864999fbb2d683f9fea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880770"
---
# <a name="launching-applications-shellexecute-shellexecuteex-shellexecuteinfo"></a>Avvio di applicazioni (ShellExecute, ShellExecuteEx, SHELLEXECUTEINFO)

Una volta che l'applicazione ha individuato un oggetto file, il passaggio successivo è spesso quello di intervenire in qualche modo. Ad esempio, l'applicazione potrebbe voler avviare un'altra applicazione che consente all'utente di modificare un file di dati. Se il file di interesse è un eseguibile, è possibile che l'applicazione voglia semplicemente avviarla. Questo documento illustra come usare [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) o [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) per eseguire queste attività.

-   [Uso di ShellExecute e ShellExecuteEx](#using-shellexecute-and-shellexecuteex)
    -   [Verbi oggetto](#object-verbs)
    -   [Uso di ShellExecuteEx per fornire servizi di attivazione da un sito](#using-shellexecuteex-to-provide-activation-services-from-a-site)
    -   [Utilizzo di ShellExecute per avviare la finestra di dialogo di ricerca](#using-shellexecute-to-launch-the-search-dialog-box)
-   [Esempio semplice di utilizzo di ShellExecuteEx](#a-simple-example-of-how-to-use-shellexecuteex)

## <a name="using-shellexecute-and-shellexecuteex"></a>Uso di ShellExecute e ShellExecuteEx

Per usare [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) o [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), l'applicazione deve specificare l'oggetto file o cartella di cui eseguire l'azione e un *verbo* che specifica l'operazione. Per **ShellExecute**, assegnare questi valori ai parametri appropriati. Per **ShellExecuteEx**, compilare i membri appropriati di una struttura [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) . Sono inoltre disponibili diversi altri membri o parametri che possono essere utilizzati per ottimizzare il comportamento delle due funzioni.

Gli oggetti file e cartella possono far parte del file system o degli oggetti virtuali e possono essere identificati da percorsi o puntatori a elenchi di identificatori di elemento (PIDL).

### <a name="object-verbs"></a>Verbi oggetto

I verbi disponibili per un oggetto sono essenzialmente gli elementi individuati nel menu di scelta rapida di un oggetto. Per individuare i verbi disponibili, cercare nel registro di sistema

**HKEY \_ Verbi \_ radice delle classi** \\ **CLSID** \\ *{Object \_ CLSID}* \\ **Shell** \\ 

dove l' *oggetto \_ CLSID* è l'identificatore di classe (CLSID) dell'oggetto e *Verb* è il nome del verbo disponibile. La  \\ sottochiave del **comando** verb contiene i dati che indicano cosa accade quando il verbo viene richiamato.

Per scoprire quali verbi sono disponibili per [gli oggetti della shell predefiniti](handlers.md), cercare nel registro di sistema in

**HKEY \_ \_** \\ *\_* Verbo della \\ **Shell** \\  del nome dell'oggetto radice delle classi

dove *\_ nome oggetto* è il nome dell'oggetto shell predefinito. Anche in questo caso, la \\ sottochiave del **comando** verb contiene i dati che indicano cosa accade quando il verbo viene richiamato.

I verbi comunemente disponibili includono:



| Verbo       | Descrizione                                                                                              |
|------------|----------------------------------------------------------------------------------------------------------|
| modifica       | Avvia un editor e apre il documento per la modifica.                                                   |
| trovare       | Avvia una ricerca a partire dalla directory specificata.                                                |
| apre       | Avvia un'applicazione. Se il file non è un file eseguibile, viene avviata l'applicazione associata. |
| print      | Stampa il file di documento.                                                                                |
| properties | Consente di visualizzare le proprietà dell'oggetto.                                                                        |
| RunAs      | Avvia un'applicazione come amministratore. Il controllo dell'account utente (UAC) richiederà all'utente il consenso per |
|            | eseguire l'applicazione con privilegi elevati o immettere le credenziali di un account amministratore usato per eseguire il        |
|            | nell'applicazione Aha!.                                                                                             |

 

Ogni verbo corrisponde al comando da usare per avviare l'applicazione da una finestra della console. Il verbo **Open** è un esempio valido, in quanto è generalmente supportato. Per i file con estensione exe, **Apri** avvia semplicemente l'applicazione. Tuttavia, viene usato più di frequente per avviare un'applicazione che opera su un file specifico. Ad esempio, i file con estensione txt possono essere aperti da Microsoft WordPad. Il verbo **Open** per un file con estensione txt corrisponderebbe quindi a un comando simile al seguente:


```C++
C:\Program Files\Windows NT\Accessories\Wordpad.exe" "%1"
```



Quando si usa [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) o [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) per aprire un file con estensione txt, Wordpad.exe viene avviato con il file specificato come argomento. Alcuni comandi possono avere argomenti aggiuntivi, ad esempio flag, che possono essere aggiunti in base alle esigenze per avviare correttamente l'applicazione. Per ulteriori informazioni sui menu di scelta rapida e sui verbi, vedere [estensione dei menu di scelta rapida](context.md).

In generale, il tentativo di determinare l'elenco dei verbi disponibili per un determinato file è piuttosto complesso. In molti casi, è possibile semplicemente impostare il parametro *lpVerb* su **null**, che richiama il comando predefinito per il tipo di file. Questa procedura è in genere equivalente all'impostazione di *lpVerb* su "Open", ma alcuni tipi di file possono avere un comando predefinito diverso. Per ulteriori informazioni, vedere [estensione dei menu di scelta rapida](context.md) e la documentazione di riferimento di [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) .

### <a name="using-shellexecuteex-to-provide-activation-services-from-a-site"></a>Uso di ShellExecuteEx per fornire servizi di attivazione da un sito

I servizi di una catena di siti possono controllare molti comportamenti di attivazione dell'elemento. A partire da Windows 8, è possibile fornire un puntatore alla catena di siti per [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) per abilitare questi comportamenti. Per fornire il sito a **ShellExecuteEx**:

-   Specificare il flag \_ See \_ mask \_ hInst \_ is \_ site flag nel membro **fmask** di [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa).
-   Fornire [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) nel membro **hInstApp** di [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa).

### <a name="using-shellexecute-to-launch-the-search-dialog-box"></a>Utilizzo di ShellExecute per avviare la finestra di dialogo di ricerca

Quando un utente fa clic con il pulsante destro del mouse su un'icona di cartella in Esplora risorse, una delle voci di menu è "Search". Se selezionano l'elemento, la shell avvia l'utilità di ricerca. Questa utilità consente di visualizzare una finestra di dialogo che può essere utilizzata per cercare una stringa di testo specificata nei file. Un'applicazione può avviare l'utilità di ricerca a livello di codice per una directory chiamando [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), con "Find" come parametro *lpVerb* e il percorso della directory come parametro *lpFile* . Ad esempio, la riga di codice seguente avvia l'utilità di ricerca per la directory c: \\ programmi.


```C++
ShellExecute(hwnd, "find", "c:\\MyPrograms", NULL, NULL, 0);
```



## <a name="a-simple-example-of-how-to-use-shellexecuteex"></a>Esempio semplice di utilizzo di ShellExecuteEx

Nell'applicazione console di esempio seguente viene illustrato l'uso di [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa). La maggior parte del codice di controllo degli errori è stata omessa per maggiore chiarezza.


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



L'applicazione recupera prima di tutto il PIDL della directory di Windows ed enumera il contenuto finché non trova il primo file con estensione bmp. A differenza dell'esempio precedente, [**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) viene usato per recuperare il nome di analisi del file anziché il nome visualizzato. Poiché si tratta di una cartella file system, il nome di analisi è un percorso completo, ovvero ciò che è necessario per [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).

Una volta individuato il primo file con estensione bmp, i valori appropriati vengono assegnati ai membri di una struttura [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) . Il membro **lpFile** è impostato sul nome di analisi del file e il membro **lpVerb** su **null** per iniziare l'operazione predefinita. In questo caso, l'operazione predefinita è "Open". La struttura viene quindi passata a [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), che avvia il gestore predefinito per i file bitmap, in genere MSPaint.exe, per aprire il file. Dopo la restituzione della funzione, i PIDL vengono liberati e viene rilasciata l'interfaccia [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) della cartella Windows.

 

 
