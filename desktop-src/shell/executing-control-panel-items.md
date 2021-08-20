---
description: Vengono illustrati i metodi di apertura di un Pannello di controllo per Windows Vista e sistemi successivi e vengono illustrati i comandi Pannello di controllo legacy.
ms.assetid: c17167ab-e9a0-4290-955c-484d038b82af
title: Esecuzione di Pannello di controllo elementi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bb941bb7542b0d786d682e6626e8d78faea8bd7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478417"
---
# <a name="executing-control-panel-items"></a>Esecuzione di Pannello di controllo elementi

> [!Note]  
> Se si sta cercando l'elenco dei nomi canonici e dei moduli per Pannello di controllo, vedere [Nomi canonici Pannello di controllo elementi](controlpanel-canonical-names.md).

 

È possibile aprire un elemento Pannello di controllo due modi:

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



Quando un Pannello di controllo elemento viene aperto tramite una riga di comando, è possibile indicarvi di aprirlo in una scheda specifica dell'elemento. A causa dell'aggiunta e della rimozione di determinate schede in alcuni elementi Windows Vista Pannello di controllo, la numerazione delle schede potrebbe essere stata modificata rispetto a quella in Windows XP. Ad esempio, nell'esempio seguente viene avviata la quarta scheda nell'elemento System Windows XP e la terza scheda in Windows Vista.


```
control.exe sysdm.cpl,,3
```



In questo argomento vengono trattati i seguenti temi:

-   [Windows Nomi canonici di Vista](#windows-vista-canonical-names)
-   [Nuovi comandi per Windows Vista](#new-commands-for-windows-vista)
-   [Comandi Pannello di controllo legacy](#legacy-control-panel-commands)
-   [Argomenti correlati](#related-topics)

## <a name="windows-vista-canonical-names"></a>Windows Nomi canonici di Vista

In Windows Vista e versioni successive, il metodo preferito per avviare un elemento Pannello di controllo da una riga di comando è usare il Pannello di controllo canonico dell'elemento. Un nome canonico è una stringa non localizzata dichiarata Pannello di controllo elemento nel Registro di sistema. Il valore dell'uso di un nome canonico è che astrae il nome del modulo Pannello di controllo elemento. Un elemento può essere implementato in un .dll e successivamente reimplementato come .exe o modificarne il nome del modulo. Finché il nome canonico rimane invariato, non è necessario aggiornare qualsiasi programma che lo apre usando tale nome canonico.

Per convenzione, il nome canonico è formato come "CorporationName.ControlPanelItemName".

L'esempio seguente illustra come un'applicazione può avviare Pannello di controllo'Windows **update** con [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec).


```
WinExec("%systemroot%\system32\control.exe /name Microsoft.WindowsUpdate", SW_NORMAL);
```



Per avviare un Pannello di controllo con il nome canonico, usare: "%systemroot% \\ system32 \\control.exe /name *canonicalName*"

Per aprire una pagina secondaria specifica in un elemento o per aprirla con parametri aggiuntivi, usare: "%systemroot% \\ system32 \\control.exe /name **canonicalName** **/page PageName**"

Un'applicazione può anche implementare il metodo [**IOpenControlPanel::Open**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iopencontrolpanel-open) per avviare Pannello di controllo elementi, inclusa la possibilità di aprire una pagina secondaria specifica.

Per un elenco completo dei Pannello di controllo canonici degli elementi, vedere [Nomi canonici Pannello di controllo elementi](controlpanel-canonical-names.md).

## <a name="new-commands-for-windows-vista"></a>Nuovi comandi per Windows Vista

In Windows Vista alcune opzioni accessibili da un modulo .cpl in Windows XP vengono ora implementate come .exe file. Ciò garantisce maggiore sicurezza consentendo agli utenti standard di fornire le credenziali di amministratore quando tentano di avviare i file. Le stesse righe di comando usate in Windows XP sono accessibili alle opzioni che non richiedono una maggiore sicurezza. Di seguito è riportato un elenco di comandi usati in Windows Vista per accedere a schede specifiche Pannello di controllo elementi:

### <a name="personalization"></a>Personalization

-   Dimensioni del carattere e DPI: %windir% \\ system32 \\DpiScaling.exe
-   Risoluzione dello schermo: %windir% \\ system32 \\control.exe desk.cpl,Impostazioni,@Settings
-   Impostazioni di visualizzazione: %windir% \\ system32 \\control.exe desk.cpl,Impostazioni,@Settings
-   Temi: %windir% \\ system32 \\control.exe desk.cpl,Temi,@Themes
-   Screensaver: %windir% \\ system32 \\control.exe desk.cpl,screensaver,@screensaver
-   Multi-monitor: %windir% \\ system32 \\control.exe desk.cpl,Monitor,@Monitor
-   Combinazione colori: %windir% \\ system32 \\control.exe /name Microsoft.Personalization /pageColorization
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

-   Aggiungere o rimuovere programmi: %windir% \\ system32 \\control.exe /name Microsoft.ProgramsAndFeatures
-   Windows funzionalità: %windir% \\ system32 \\OptionalFeatures.exe

### <a name="regional-and-language-options"></a>Opzioni internazionali e della lingua

-   Tastiera: %systemroot% \\ system32 \\control.exe /name Microsoft.RegionalAndLanguageOptions /page /p:"keyboard"
-   Percorso: %systemroot% \\ system32 \\control.exe /name Microsoft.RegionalAndLanguageOptions /page /p:"location"
-   Amministrativo: %systemroot% \\ system32 \\control.exe /name Microsoft.RegionalAndLanguageOptions /page /p:"administrative"

### <a name="folder-options"></a>Opzioni cartella

-   Ricerca di cartelle: %windir% \\ system32 \\rundll32.exe shell32.dll,Opzioni \_ RunDLL 2
-   Associazioni di file: %windir% \\ system32 \\control.exe /name Microsoft.DefaultPrograms /pageFileAssoc
-   Visualizzazione: %windir% \\ system32 \\rundll32.exe shell32.dll,Opzioni \_ RunDLL 7
-   Generale: %windir% \\ system32 \\rundll32.exe shell32.dll,Opzioni \_ RunDLL 0

### <a name="power-options"></a>Opzioni risparmio energia

-   Modificare le impostazioni correnti del piano: %windir% \\ system32 \\control.exe /name Microsoft.PowerOptions /page pagePlanSettings
-   Impostazioni di sistema: %windir% \\ system32 \\control.exe /name Microsoft.PowerOptions /pageGlobalSettings
-   Creare una combinazione per il risparmio di energia: %windir% \\ system32 \\control.exe /name Microsoft.PowerOptions /pageCreateNewPlan
-   Non è disponibile alcun comando canonico per la pagina Impostazioni avanzate, a cui si accede nel modo precedente: %windir% \\ system32 \\control.exe powercfg.cpl,3

## <a name="legacy-control-panel-commands"></a>Comandi Pannello di controllo legacy

Quando si usa la [**funzione WinExec,**](/windows/win32/api/winbase/nf-winbase-winexec) il sistema può riconoscere comandi Pannello di controllo comando. Questi comandi precedono Windows Vista.




| | | control.exe desktop | Avvia la finestra <strong>Proprietà dello schermo</strong> dati.<blockquote>[!Note]<br />Le edizioni Starter e Basic non supportano questo comando.</blockquote><br /> | | control.exe colore | Avvia la finestra <strong>Proprietà dello schermo</strong> con la <strong>scheda Aspetto</strong> preselezionata. | | control.exe data/ora | Avvia la finestra <strong>Proprietà data e</strong> ora. | | control.exe internazionale | Avvia la finestra <strong>Opzioni internazionali e della</strong> lingua. | | control.exe mouse | Avvia la finestra <strong>Proprietà mouse.</strong> | | control.exe tastiera | Avvia la finestra <strong>Proprietà tastiera.</strong> | | control.exe stampanti | Visualizza la <strong>cartella Stampanti e</strong> fax. | | control.exe tipi di carattere | Visualizza la <strong>cartella Tipi di</strong> carattere. | 




 

Per Windows 2000 e versioni successive:



| Comando                    | Descrizione                                              |
|----------------------------|----------------------------------------------------------|
| control.exe cartelle        | Avvia la **finestra Opzioni** cartella.                  |
| control.exe netware        | Avvia la finestra **di Novell NetWare** (se installata).   |
| control.exe telefonia      | Avvia la finestra **Telefono opzioni modem** e modem.         |
| control.exe admintools     | Visualizza la **cartella Strumenti di** amministrazione.            |
| control.exe schedtasks     | Visualizza la **cartella Attività** pianificate.                 |
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

[Estensione degli elementi di Pannello di controllo sistema](extending-system-control-panel-items.md)
</dt> <dt>

[Assegnazione di Pannello di controllo categorie](assigning-control-panel-categories.md)
</dt> <dt>

[Creazione di collegamenti di attività ricercabili per un Pannello di controllo ricerca](creating-searchable-task-links.md)
</dt> <dt>

[Accesso al Pannello di controllo in modalità Cassaforte in Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 
