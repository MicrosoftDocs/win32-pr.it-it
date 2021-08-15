---
description: Vengono illustrati i metodi di apertura di Pannello di controllo elemento per Windows Vista e sistemi successivi, nonché vengono illustrati i comandi Pannello di controllo legacy.
ms.assetid: c17167ab-e9a0-4290-955c-484d038b82af
title: Esecuzione di Pannello di controllo elementi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1e2bc84ce5225176585f2da221fab6110ce79f9ff68dfc83b3c66125d623d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118224277"
---
# <a name="executing-control-panel-items"></a>Esecuzione di Pannello di controllo elementi

> [!Note]  
> Se si sta cercando l'elenco di nomi canonici e di moduli per Pannello di controllo elementi, vedere [Nomi canonici di Pannello di controllo elementi](controlpanel-canonical-names.md).

 

Esistono due modi per aprire un elemento Pannello di controllo seguente:

-   L'utente può aprire Pannello di controllo e quindi aprire un elemento facendo clic o facendo doppio clic sull'icona dell'elemento.
-   L'utente o un'applicazione può avviare Pannello di controllo elemento eseguendolo direttamente dal prompt della riga di comando.

Un'applicazione può aprire il Pannello di controllo a livello di codice usando la [**funzione WinExec.**](/windows/win32/api/winbase/nf-winbase-winexec)


```
WinExec("c:\windows\system32\control.exe", SW_NORMAL);
```



L'esempio seguente illustra come un'applicazione può avviare Pannello di controllo elemento denominato **MyCpl.cpl** usando la [**funzione WinExec.**](/windows/win32/api/winbase/nf-winbase-winexec)


```
WinExec("c:\windows\system32\control.exe MyCpl.cpl", SW_NORMAL);
```



Quando un Pannello di controllo viene aperto tramite una riga di comando, è possibile indicarlo di aprire una scheda specifica nell'elemento. A causa dell'aggiunta e della rimozione di alcune schede in alcuni elementi Windows Vista Pannello di controllo, la numerazione delle schede potrebbe essere stata modificata rispetto a quella in Windows XP. Ad esempio, nell'esempio seguente viene avviata la quarta scheda nell'elemento System Windows XP e la terza scheda in Windows Vista.


```
control.exe sysdm.cpl,,3
```



In questo argomento vengono trattati i seguenti temi:

-   [Windows Vista Canonical Names](#windows-vista-canonical-names)
-   [Nuovi comandi per Windows Vista](#new-commands-for-windows-vista)
-   [Comandi Pannello di controllo legacy](#legacy-control-panel-commands)
-   [Argomenti correlati](#related-topics)

## <a name="windows-vista-canonical-names"></a>Windows Vista Canonical Names

In Windows Vista e versioni successive, il metodo preferito per avviare un elemento Pannello di controllo da una riga di comando è usare il nome canonico Pannello di controllo dell'elemento. Un nome canonico è una stringa non localizzata dichiarata Pannello di controllo'elemento nel Registro di sistema. Il valore dell'uso di un nome canonico è che estrae il nome del modulo dell'Pannello di controllo elemento. Un elemento può essere implementato in un .dll e successivamente reimplementato come .exe o modificarne il nome del modulo. Finché il nome canonico rimane invariato, non è necessario aggiornare qualsiasi programma che lo apre usando tale nome canonico.

Per convenzione, il nome canonico è formato come "CorporationName.ControlPanelItemName".

L'esempio seguente illustra come un'applicazione può avviare l Pannello di controllo'elemento Windows **Update** con [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec).


```
WinExec("%systemroot%\system32\control.exe /name Microsoft.WindowsUpdate", SW_NORMAL);
```



Per avviare un Pannello di controllo con il nome canonico, usare: "%systemroot% \\ system32 \\control.exe /name *canonicalName*"

Per aprire una pagina secondaria specifica in un elemento o per aprirla con parametri aggiuntivi, usare: "%systemroot% \\ system32 \\control.exe /name **canonicalName** /page **pageName**"

Un'applicazione può anche implementare il metodo [**IOpenControlPanel::Open**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iopencontrolpanel-open) per avviare elementi Pannello di controllo, inclusa la possibilità di aprire una pagina secondaria specifica.

Per un elenco completo dei Pannello di controllo canonici degli elementi, vedere [Canonical Names of Pannello di controllo Items](controlpanel-canonical-names.md).

## <a name="new-commands-for-windows-vista"></a>Nuovi comandi per Windows Vista

In Windows Vista alcune opzioni accessibili da un modulo .cpl in Windows XP vengono ora implementate come .exe file. In questo modo si garantisce una maggiore sicurezza, consentendo agli utenti standard di specificare le credenziali di amministratore quando tentano di avviare i file. Le stesse righe di comando usate in Windows XP sono accessibili alle opzioni che non richiedono una maggiore sicurezza. Di seguito è riportato un elenco di comandi usati in Windows Vista per accedere a schede specifiche di Pannello di controllo elementi:

### <a name="personalization"></a>Personalization

-   Dimensioni carattere e DPI: %windir% \\ system32 \\DpiScaling.exe
-   Risoluzione dello schermo: %windir% \\ system32 \\control.exe desk.cpl,Impostazioni,@Settings
-   Impostazioni di visualizzazione: %windir% \\ system32 \\control.exe desk.cpl,Impostazioni,@Settings
-   Temi: %windir% \\ system32 \\control.exe desk.cpl,Themes,@Themes
-   Screensaver: %windir% \\ system32 \\control.exe desk.cpl,screensaver,@screensaver
-   Multi-monitor: %windir% \\ system32 \\control.exe desk.cpl,Monitor,@Monitor
-   Combinazione colori: %windir% \\ system32 \\control.exe /name Microsoft.Personalization /page pageColorization
-   Sfondo del desktop: %windir% \\ system32 \\control.exe /name Microsoft.Personalization /pageWallpaper

> [!Note]  
> Le edizioni Starter e Basic non supportano control.exe comando /name Microsoft.Personalization.

 

### <a name="system"></a>Sistema

-   Prestazioni: %windir% \\ system32 \\SystemPropertiesPerformance.exe
-   Accesso remoto: %windir% \\ system32 \\SystemPropertiesRemote.exe
-   Nome computer: %windir% \\ system32 \\SystemPropertiesComputerName.exe
-   Protezione del sistema: %windir% \\ system32 \\SystemPropertiesProtection.exe
-   Proprietà di sistema avanzate: %windir% \\ system32 \\SystemPropertiesAdvanced.exe

### <a name="programs-and-features"></a>Programmi e funzionalità

-   Installazione applicazioni: %windir% \\ system32 \\control.exe /name Microsoft.ProgramsAndFeatures
-   Windows funzionalità seguenti: %windir% \\ system32 \\OptionalFeatures.exe

### <a name="regional-and-language-options"></a>Opzioni internazionali e della lingua

-   Tastiera: %systemroot% \\ system32 \\control.exe /name Microsoft.RegionalAndLanguageOptions /page /p:"keyboard"
-   Percorso: %systemroot% \\ system32 \\control.exe /name Microsoft.RegionalAndLanguageOptions /page /p:"location"
-   Amministrativo: %systemroot% \\ system32 \\control.exe /name Microsoft.RegionalAndLanguageOptions /page /p:"administrative"

### <a name="folder-options"></a>Opzioni cartella

-   Ricerca nella cartella: %windir% \\ system32 \\rundll32.exe shell32.dll,Opzioni \_ RunDLL 2
-   Associazioni di file: %windir% \\ system32 \\control.exe /name Microsoft.DefaultPrograms /pageFileAssoc
-   Visualizzazione: %windir% \\ system32 \\rundll32.exe shell32.dll,Opzioni \_ RunDLL 7
-   Generale: %windir% \\ system32 \\rundll32.exe shell32.dll,Opzioni \_ RunDLL 0

### <a name="power-options"></a>Opzioni risparmio energia

-   Modificare le impostazioni del piano corrente: %windir% \\ system32 \\control.exe /name Microsoft.PowerOptions /page pagePlanSettings
-   Impostazioni di sistema: %windir% \\ system32 \\control.exe /name Microsoft.PowerOptions /page pageGlobalSettings
-   Creare una combinazione per il risparmio di energia: %windir% \\ system32 \\control.exe /name Microsoft.PowerOptions /page pageCreateNewPlan
-   Non esiste alcun comando canonico per la pagina Advanced Impostazioni, a cui si accede nel modo precedente: %windir% \\ system32 \\control.exe powercfg.cpl,,3

## <a name="legacy-control-panel-commands"></a>Comandi Pannello di controllo legacy

Quando si usa la [**funzione WinExec,**](/windows/win32/api/winbase/nf-winbase-winexec) il sistema è in grado di riconoscere Pannello di controllo comandi. Questi comandi Windows Vista.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>control.exe desktop</td>
<td>Avvia la finestra <strong>Proprietà dello schermo</strong> corrente.
<blockquote>
[!Note]<br />
Le edizioni Starter e Basic non supportano questo comando.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>control.exe colore</td>
<td>Avvia la finestra <strong>Proprietà dello schermo</strong> con la <strong>scheda Aspetto</strong> preselezionata.</td>
</tr>
<tr class="odd">
<td>control.exe data/ora</td>
<td>Apre la finestra <strong>Proprietà data e</strong> ora.</td>
</tr>
<tr class="even">
<td>control.exe internazionale</td>
<td>Apre la finestra <strong>Opzioni internazionali e della</strong> lingua.</td>
</tr>
<tr class="odd">
<td>control.exe mouse</td>
<td>Avvia la finestra <strong>Proprietà mouse.</strong></td>
</tr>
<tr class="even">
<td>control.exe tastiera</td>
<td>Apre la finestra <strong>Proprietà tastiera.</strong></td>
</tr>
<tr class="odd">
<td>control.exe stampanti</td>
<td>Consente di <strong>visualizzare la cartella Stampanti e fax.</strong></td>
</tr>
<tr class="even">
<td>control.exe tipi di carattere</td>
<td>Visualizza la <strong>cartella Tipi di</strong> carattere.</td>
</tr>
</tbody>
</table>



 

Per Windows 2000 e versioni successive:



| Comando                    | Descrizione                                              |
|----------------------------|----------------------------------------------------------|
| control.exe cartelle        | Apre la **finestra Opzioni** cartella.                  |
| control.exe netware        | Avvia la finestra **di Novell NetWare** (se installata).   |
| control.exe telefonia      | Avvia la finestra **Telefono e Opzioni** modem.         |
| control.exe admintools     | Consente di visualizzare **la cartella Strumenti di** amministrazione .            |
| control.exe schedtasks     | Consente di visualizzare **la cartella Attività pianificate** .                 |
| control.exe netconnections | Visualizza la **cartella Connessioni di** rete.             |
| control.exe a raggi infrarossi       | Avvia la finestra **Monitoraggio a raggi** raggi(se installato). |
| control.exe userpasswords  | Avvia la **finestra Account** utente.                   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pannello di controllo elementi](control-panel-applications.md)
</dt> <dt>

[Linee guida sull'esperienza utente](user-experience-guidelines.md)
</dt> <dt>

[Registrazione di Pannello di controllo elementi](registering-control-panel-items.md)
</dt> <dt>

[Uso di CPLApplet](using-cplapplet.md)
</dt> <dt>

[Pannello di controllo di messaggi](message-processing.md)
</dt> <dt>

[Estensione degli elementi Pannello di controllo sistema](extending-system-control-panel-items.md)
</dt> <dt>

[Assegnazione di Pannello di controllo categorie](assigning-control-panel-categories.md)
</dt> <dt>

[Creazione di collegamenti di attività ricercabili per un Pannello di controllo elemento](creating-searchable-task-links.md)
</dt> <dt>

[Accesso al Pannello di controllo in Cassaforte in Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 
