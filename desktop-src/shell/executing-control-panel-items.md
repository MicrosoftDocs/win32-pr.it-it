---
description: Vengono illustrati i metodi di apertura di un elemento del pannello di controllo per i sistemi Windows Vista e versioni successive, nonché per i comandi del pannello di controllo legacy.
ms.assetid: c17167ab-e9a0-4290-955c-484d038b82af
title: Esecuzione degli elementi del pannello di controllo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaaac4b782273e0b4444fb2b5b6d3cab0b3599ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994933"
---
# <a name="executing-control-panel-items"></a>Esecuzione degli elementi del pannello di controllo

> [!Note]  
> Se si cerca l'elenco di nomi di moduli e Canonical per gli elementi del pannello di controllo, vedere [nomi canonici degli elementi del pannello di controllo](controlpanel-canonical-names.md).

 

Esistono due modi per aprire un elemento del pannello di controllo:

-   L'utente può aprire il pannello di controllo e quindi aprire un elemento facendo clic o facendo doppio clic sull'icona dell'elemento.
-   L'utente o un'applicazione può avviare un elemento del pannello di controllo eseguendolo direttamente dal prompt della riga di comando.

Un'applicazione può aprire il pannello di controllo a livello di codice tramite la funzione [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) .


```
WinExec("c:\windows\system32\control.exe", SW_NORMAL);
```



Nell'esempio seguente viene illustrato come un'applicazione può avviare l'elemento del pannello di controllo denominato **MyCpl.cpl** tramite la funzione [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) .


```
WinExec("c:\windows\system32\control.exe MyCpl.cpl", SW_NORMAL);
```



Quando un elemento del pannello di controllo viene aperto tramite una riga di comando, è possibile indicarlo all'apertura di una particolare scheda nell'elemento. A causa dell'aggiunta e della rimozione di alcune schede in alcuni elementi del pannello di controllo di Windows Vista, è possibile che la numerazione delle schede sia cambiata rispetto a quella di Windows XP. Nell'esempio seguente, ad esempio, viene avviata la quarta scheda dell'elemento di sistema in Windows XP e la terza scheda in Windows Vista.


```
control.exe sysdm.cpl,,3
```



In questo argomento vengono trattati i seguenti temi:

-   [Nomi canonici di Windows Vista](#windows-vista-canonical-names)
-   [Nuovi comandi per Windows Vista](#new-commands-for-windows-vista)
-   [Comandi del pannello di controllo legacy](#legacy-control-panel-commands)
-   [Argomenti correlati](#related-topics)

## <a name="windows-vista-canonical-names"></a>Nomi canonici di Windows Vista

In Windows Vista e versioni successive, il metodo preferito per l'avvio di un elemento del pannello di controllo da una riga di comando consiste nell'utilizzare il nome canonico dell'elemento del pannello di controllo. Un nome canonico è una stringa non localizzata dichiarata dall'elemento del pannello di controllo nel registro di sistema. Il valore di usando un nome canonico è che estrae il nome del modulo dell'elemento del pannello di controllo. Un elemento può essere implementato in un file con estensione dll e successivamente reimplementato come file con estensione exe o modificare il nome del modulo. Fino a quando il nome canonico rimane lo stesso, non è necessario aggiornare tutti i programmi che lo aprono usando tale nome canonico.

Per convenzione, il nome canonico è formato "Corporationname. ControlPanelItemName".

Nell'esempio seguente viene illustrato come un'applicazione può avviare l'elemento del pannello di controllo **Windows Update** con [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec).


```
WinExec("%systemroot%\system32\control.exe /name Microsoft.WindowsUpdate", SW_NORMAL);
```



Per avviare un elemento del pannello di controllo con il nome canonico, utilizzare: "% SystemRoot% \\ system32 \\control.exe/Name *CanonicalName*"

Per aprire una pagina secondaria specifica in un elemento o per aprirla con parametri aggiuntivi, usare: "% SystemRoot% \\ system32 \\control.exe/Name **CanonicalName** /Page **pageName**"

Un'applicazione può inoltre implementare il metodo [**IOpenControlPanel:: Open**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iopencontrolpanel-open) per avviare gli elementi del pannello di controllo, inclusa la possibilità di aprire una pagina secondaria specifica.

Per un elenco completo dei nomi canonici degli elementi del pannello di controllo, vedere [nomi canonici degli elementi del pannello di controllo](controlpanel-canonical-names.md).

## <a name="new-commands-for-windows-vista"></a>Nuovi comandi per Windows Vista

In Windows Vista alcune opzioni a cui è stato eseguito l'accesso a un modulo. cpl in Windows XP sono ora implementate come file con estensione exe. In questo modo viene fornita una maggiore sicurezza consentendo agli utenti standard di fornire le credenziali di amministratore quando si tenta di avviare i file. Le stesse righe di comando utilizzate in Windows XP hanno accesso a opzioni che non richiedono una maggiore sicurezza. Di seguito è riportato un elenco di comandi utilizzati in Windows Vista per accedere a schede specifiche degli elementi del pannello di controllo:

### <a name="personalization"></a>Personalization

-   Dimensioni del carattere e DPI:% windir% \\ system32 \\DpiScaling.exe
-   Risoluzione dello schermo:% windir% \\ system32 \\control.exe desk.cpl, Settings,@Settings
-   Impostazioni di visualizzazione:% windir% \\ system32 \\control.exe desk.cpl, Settings,@Settings
-   Temi:% windir% \\ system32 \\control.exe desk.cpl, temi,@Themes
-   Salvaschermo:% windir% \\ system32 \\control.exe desk.cpl, screensaver,@screensaver
-   Multimonitor:% windir% \\ system32 \\control.exe desk.cpl, monitoraggio,@Monitor
-   Combinazione colori:% windir% \\ system32 \\control.exe/name Microsoft. Personalizzazione/Page pageColorization
-   Sfondo del desktop:% windir% \\ system32 \\control.exe/name Microsoft. personalizzazione/page pageWallpaper

> [!Note]  
> Le edizioni Starter e Basic non supportano control.exe comando/name Microsoft. personalizzazione.

 

### <a name="system"></a>Sistema

-   Prestazioni:% windir% \\ system32 \\SystemPropertiesPerformance.exe
-   Accesso remoto:% windir% \\ system32 \\SystemPropertiesRemote.exe
-   Nome computer:% windir% \\ system32 \\SystemPropertiesComputerName.exe
-   Protezione del sistema:% windir% \\ system32 \\SystemPropertiesProtection.exe
-   Proprietà di sistema avanzate:% windir% \\ system32 \\SystemPropertiesAdvanced.exe

### <a name="programs-and-features"></a>Programmi e funzionalità

-   Aggiungere o rimuovere programmi:% windir% \\ system32 \\control.exe/name Microsoft. ProgramsAndFeatures
-   Funzionalità di Windows:% windir% \\ system32 \\OptionalFeatures.exe

### <a name="regional-and-language-options"></a>Opzioni internazionali e della lingua

-   Tastiera:% systemroot% \\ system32 \\control.exe/name Microsoft. RegionalAndLanguageOptions/page/p: "Keyboard"
-   Percorso:% systemroot% \\ system32 \\control.exe/name Microsoft. RegionalAndLanguageOptions/page/p: "location"
-   Amministrazione:% systemroot% \\ system32 \\control.exe/name Microsoft. RegionalAndLanguageOptions/page/p: "Administrative"

### <a name="folder-options"></a>Opzioni cartella

-   Ricerca cartella:% windir% \\ system32 \\rundll32.exe shell32.dll, opzioni \_ rundll 2
-   Associazioni file:% windir% \\ system32 \\control.exe/name Microsoft. DefaultPrograms/page pageFileAssoc
-   Visualizzazione:% windir% \\ system32 \\rundll32.exe shell32.dll, opzioni \_ rundll 7
-   Generale:% windir% \\ system32 \\rundll32.exe shell32.dll, opzioni \_ rundll 0

### <a name="power-options"></a>Opzioni risparmio energia

-   Modifica le impostazioni del piano corrente:% windir% \\ system32 \\control.exe/name Microsoft. PowerOptions/page pagePlanSettings
-   Impostazioni di sistema:% windir% \\ system32 \\control.exe/name Microsoft. PowerOptions/page pageGlobalSettings
-   Creare una combinazione per il risparmio di energia:% windir% \\ system32 \\control.exe/name Microsoft. PowerOptions/page pageCreateNewPlan
-   Non esiste alcun comando canonico per la pagina Impostazioni avanzate, a cui è possibile accedere nel modo precedente:% windir% \\ system32 \\control.exe powercfg.cpl,, 3

## <a name="legacy-control-panel-commands"></a>Comandi del pannello di controllo legacy

Quando si usa la funzione [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) , il sistema è in grado di riconoscere comandi speciali del pannello di controllo. Questi comandi predatano Windows Vista.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>control.exe desktop</td>
<td>Avvia la finestra <strong>proprietà di visualizzazione</strong> .
<blockquote>
[!Note]<br />
Le edizioni Starter e Basic non supportano questo comando.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Colore control.exe</td>
<td>Apre la finestra <strong>proprietà di visualizzazione</strong> con la scheda <strong>aspetto</strong> preselezionata.</td>
</tr>
<tr class="odd">
<td>Data/ora control.exe</td>
<td>Viene avviata la finestra <strong>Proprietà data e ora</strong> .</td>
</tr>
<tr class="even">
<td>control.exe internazionale</td>
<td>Avvia la finestra <strong>Opzioni internazionali e della lingua</strong> .</td>
</tr>
<tr class="odd">
<td>Mouse control.exe</td>
<td>Avvia la finestra <strong>proprietà del mouse</strong> .</td>
</tr>
<tr class="even">
<td>Tastiera control.exe</td>
<td>Avvia la finestra <strong>Proprietà tastiera</strong> .</td>
</tr>
<tr class="odd">
<td>Stampanti control.exe</td>
<td>Consente di visualizzare la cartella <strong>stampanti e fax</strong> .</td>
</tr>
<tr class="even">
<td>Tipi di carattere control.exe</td>
<td>Consente di visualizzare la cartella <strong>Fonts</strong> .</td>
</tr>
</tbody>
</table>



 

Per i sistemi Windows 2000 e versioni successive:



|                            |                                                          |
|----------------------------|----------------------------------------------------------|
| Cartelle di control.exe        | Avvia la finestra **Opzioni cartella** .                  |
| control.exe NetWare        | Avvia la finestra **Novell NetWare** (se installata).   |
| Telefonia control.exe      | Avvia la finestra **Opzioni telefono e modem** .         |
| control.exe AdminTools     | Consente di visualizzare la cartella **strumenti di amministrazione** .            |
| control.exe schedtasks     | Consente di visualizzare la cartella **attività pianificate** .                 |
| control.exe netconnections | Consente di visualizzare la cartella **connessioni di rete** .             |
| control.exe infrarossi       | Avvia la finestra di **monitoraggio a infrarossi** (se installata). |
| control.exe userpasswords  | Avvia la finestra **account utente** .                   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Elementi del pannello di controllo](control-panel-applications.md)
</dt> <dt>

[Linee guida sull'esperienza utente](user-experience-guidelines.md)
</dt> <dt>

[Registrazione degli elementi del pannello di controllo](registering-control-panel-items.md)
</dt> <dt>

[Uso di CPLApplet](using-cplapplet.md)
</dt> <dt>

[Elaborazione del messaggio del pannello di controllo](message-processing.md)
</dt> <dt>

[Estensione degli elementi del pannello di controllo di sistema](extending-system-control-panel-items.md)
</dt> <dt>

[Assegnazione delle categorie del pannello di controllo](assigning-control-panel-categories.md)
</dt> <dt>

[Creazione di collegamenti alle attività ricercabili per un elemento del pannello di controllo](creating-searchable-task-links.md)
</dt> <dt>

[Accesso al pannello di controllo in modalità provvisoria in Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 
