---
description: A partire da Windows Vista, la visualizzazione delle categorie del pannello di controllo fornisce collegamenti alle attività sotto ogni icona dell'elemento del pannello di controllo, come illustrato qui.
ms.assetid: 54a03536-6fe6-4304-a555-58e5bca128b9
title: Creazione di collegamenti alle attività ricercabili per un elemento del pannello di controllo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b4e98e8a6e07f84e8012b58cefe8e0d249fc069
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878770"
---
# <a name="creating-searchable-task-links-for-a-control-panel-item"></a>Creazione di collegamenti alle attività ricercabili per un elemento del pannello di controllo

A partire da Windows Vista, la visualizzazione delle categorie del pannello di controllo fornisce collegamenti alle attività sotto ogni icona dell'elemento del pannello di controllo, come illustrato qui.

![collegamenti alle attività nella pagina della categoria sistema e manutenzione](images/controlpaneltasklinks.png)

Quando un utente immette testo nella casella di **ricerca** nella parte superiore destra della finestra, i risultati della ricerca includono i collegamenti delle attività indicati di seguito per una ricerca nella parola "display".

![collegamenti alle attività nei risultati della ricerca del pannello di controllo](images/controlpanelsearchresults.png)

In questo argomento vengono trattati i seguenti temi:

-   [Procedure consigliate per il collegamento alle attività](#task-link-best-practices)
-   [Creazione di un file XML di attività](#creating-a-task-xml-file)
-   [Localizzazione di collegamenti alle attività](#localizing-task-links)
-   [Parole chiave e ricerca](#keywords-and-searching)
-   [Argomenti correlati](#related-topics)

## <a name="task-link-best-practices"></a>Procedure consigliate per il collegamento alle attività

È consigliabile fornire collegamenti alle attività per gli elementi del pannello di controllo come supporto per gli utenti che cercano funzionalità. È anche possibile aggiungere parole chiave ai collegamenti alle attività in modo che un utente possa trovarle anche senza conoscere il titolo o la terminologia di un'attività.

I collegamenti alle attività migliori servono tre scopi:

1.  Consente di specificare un collegamento alla funzionalità dell'elemento del pannello di controllo.
2.  Fornire parole chiave in modo che gli utenti possano eseguire ricerche usando la propria lingua. Un utente potrebbe voler digitare "compattazione" perché conosce il termine tecnico. Un utente può digitare "DB troppo grande" o "database Filesize". L'aggiunta di parole chiave appropriate all'attività significa che gli utenti possono trovare l'elemento del pannello di controllo.
3.  Fornire suggerimenti sull'elemento del pannello di controllo. Quando un utente Visualizza i collegamenti sotto l'icona di un elemento del pannello di controllo, può ottenere ulteriori informazioni sull'elemento utilizzato dal pannello di controllo, oltre al nome e all'icona che possono essere forniti da soli.

I collegamenti alle attività devono essere mirati all'utente finale, non alla tecnologia o alla funzionalità. Ad esempio, la "Abilitazione della compattazione del database" potrebbe non essere una formulazione valida perché si tratta di un gergo tecnico non noto alla maggior parte degli utenti. "Rendere il file di database più piccolo" è preferibile perché menziona l'obiettivo finale effettivo dell'utente anziché il meccanismo per ottenerlo. L'obiettivo non è quello di semplificare eccessivamente, ma piuttosto di formulare l'attività in termini di ciò che l'utente desidera eseguire.

## <a name="creating-a-task-xml-file"></a>Creazione di un file XML di attività

I collegamenti alle attività sono definiti in un file XML. In questa sezione vengono forniti i dettagli di un file XML di esempio che definisce tre collegamenti alle attività per un elemento del pannello di controllo denominato **blocco note**. Definisce i titoli, le parole chiave e le righe di comando per i collegamenti alle attività. Viene inoltre illustrato come specificare quali collegamenti alle attività vengono visualizzati nella categoria. Un elemento del pannello di controllo registrato per essere visualizzato in più di una categoria consente di visualizzare collegamenti diversi a seconda della categoria. Le spiegazioni dei vari elementi e delle informazioni fornite vengono fornite come commenti nel codice XML stesso.


```
<?xml version="1.0" ?>
<applications xmlns="http://schemas.microsoft.com/windows/cpltasks/v1" 
              xmlns:sh="http://schemas.microsoft.com/windows/tasks/v1">
    
    <!-- Notepad -->
    <application id="{0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}"> 
    <!-- This GUID must match the GUID you created for your Control Panel item,
         and registered in namespace -->
    
        <!-- Solitaire -->
        <sh:task id="{3B75A7AE-C4E4-4E5A-9420-7CECCDA75425}"> 
            <!-- This is a generated GUID, specific to this task link -->
            <sh:name>Play solitaire</sh:name>
            <sh:keywords>solitare;game;cards;ace;diamond;heart;club;single</sh:keywords>
            <sh:command>%ProgramFiles%\Microsoft Games\Solitaire\solitaire.exe</sh:command>
        </sh:task>

        <!-- Task Manager -->
        <sh:task id="{BF46D6AA-B5E6-4EE1-9E5B-ED017272B9F9}" needsElevation="true"> 
            <!-- This is a generated GUID, specific to this task link -->
            <!-- The needsElevation="true" attribute means that the task 
                 appears with a shield icon next to it. Adding this attribute 
                 does not cause the .exe to require elevation - it just adds an 
                 icon to tell users that the command already requires it -->
            <sh:name>See running processes</sh:name>
            <sh:keywords>taskmgr;taskman;running processes;threads;cpu;</sh:keywords>
            <sh:command>taskmgr.exe</sh:command>
        </sh:task>

        <!-- IE -->
        <sh:task id="{DE3A6DCC-C18A-4BBF-9227-11856D7B4422}">
            <sh:name>Open Internet Explorer</sh:name>
            <sh:keywords>IE;web;browser;net;Internet;ActiveX;plug-in;plugin</sh:keywords>
            <sh:command>iexplore.exe</sh:command>
        </sh:task>
        
        <!-- Category assignments -->

        <!-- Appearance and Personalization -->
        <category id="1"> 
        <!-- These idref attributes refer to the GUIDs of the tasks defined above. A maximum of five tasks are shown per category. -->
            <sh:task idref="{3B75A7AE-C4E4-4E5A-9420-7CECCDA75425}"/>   
            <sh:task idref="{BF46D6AA-B5E6-4EE1-9E5B-ED017272B9F9}"/>
            <sh:task idref="{DE3A6DCC-C18A-4BBF-9227-11856D7B4422}"/>
        </category>
        
        <!-- Programs -->
        <category id="8"> 
            <sh:task idref="{3B75A7AE-C4E4-4E5A-9420-7CECCDA75425}">
                <sh:name>Click here to play</sh:name>
                <!-- This overrides the defined text. When the Notepad Control 
                     Panel item appears in the Programs category, it uses the 
                     "Click here to play" text for this Solitaire link, instead 
                     of "Play solitaire". -->
            </sh:task>
            <sh:task idref="{BF46D6AA-B5E6-4EE1-9E5B-ED017272B9F9}"/>
            <sh:task idref="{DE3A6DCC-C18A-4BBF-9227-11856D7B4422}"/>
       </category>
   </application>
</applications>
```



> [!Note]  
> A partire da Windows 7, un elemento del pannello di controllo può essere identificato dal relativo nome canonico anziché dal nome eseguibile: è possibile usare l'elemento **<SH: controlpanel>** al posto di **<sh: Command>**. L'elemento **<SH: controlpanel>** fornisce anche un attributo per specificare la pagina dell'elemento a cui deve essere aperto. Di seguito viene illustrato un esempio dell'elemento **<SH: controlpanel>** :

 


```
<sh:controlpanel name="Microsoft.Presentation" page="pageWallpaper"/>
```



## <a name="localizing-task-links"></a>Localizzazione di collegamenti alle attività

Il testo per i titoli e le parole chiave dei collegamenti alle attività può essere archiviato in una tabella di stringhe nel modulo dell'elemento del pannello di controllo. In tal caso, il formato utilizzato nel file XML diventa:


```
<sh:task id="{3B75A7AE-C4E4-4E5A-9420-7CECCDA75425}"> 
    <!-- This is a generated GUID, specific to this task link -->
    <sh:name>@myTextResources.dll,-100</sh:name>
    <sh:keywords>@myTextResources.dll,-101</sh:keywords>
    <sh:command>%ProgramFiles%\Microsoft Games\Solitaire\solitaire.exe</sh:command>
</sh:task>
```



In questo esempio, il testo per il nome dell'attività viene visualizzato nell'ID risorsa stringa 100 in myTextResources.dll e il testo per le parole chiave viene visualizzato in stringa ID 101.

## <a name="keywords-and-searching"></a>Parole chiave e ricerca

La ricerca nel pannello di controllo consente di trovare i collegamenti alle attività in base al nome e anche alle parole chiave corrispondenti. Corrisponde a ogni parola nella ricerca con il prefisso delle parole nel nome e nelle parole chiave. Ad esempio, la stringa di query "CPU" corrisponderà all'attività "vedere processi in esecuzione" nell'esempio precedente perché "CPU" si trova nell'elenco di parole chiave. La stringa di query "Pro" troverà anche il risultato perché la parola "processes" del titolo inizia con tale stringa. Si noti che la query corrisponde solo ai prefissi. La stringa di query "rocess" non corrisponde a un risultato perché tale stringa, mentre parte della parola del titolo "Process", non inizia la parola.

Quando una query di ricerca contiene più token, per un risultato tutti i token devono corrispondere al prefisso di una parola chiave o di una parte del titolo dell'attività. La query "livello CPU" non corrisponde, perché "Level" non è presente nella parola chiave impostata. La query "esecuzione CPU" darebbe un risultato, perché "CPU" corrisponde a una parola chiave e "Run" è il prefisso della parola "Running" nel titolo dell'attività.

Il pannello di controllo non fornisce automaticamente la correzione ortografica o le variazioni, ad esempio plurali o sillabazione. Anche le corrispondenze non fanno distinzione tra maiuscole e minuscole. Per garantire un elenco di parole chiave con esito positivo, è consigliabile fornire le variazioni manualmente, ad esempio per questo collegamento di attività che include screen saver: "Screensavers; Screen saver; screen saver;"

Non è necessario aggiungere il "salvaschermo" singolare, perché una query che trova "salvaschermi" troverà anche "salvaschermo" a causa della corrispondenza del prefisso. Un utente che digita anche parte della parola, ad esempio "schermate", visualizzerà comunque una corrispondenza in un collegamento a un'attività con "salvaschermi" come parola chiave. Per le lingue in cui i form plurali cambiano la parola, è necessario inserire tutti i form che un utente potrebbe ragionevolmente prevedere di digitare nelle parole chiave.

Come convenzione, Microsoft ha omesso le piccole parole come "How do I" o "voglio" dal set di parole chiave. Si prevede che la maggior parte degli utenti digitano semplicemente le parole più importanti, ad esempio "mouse", "contrasto elevato" o "driver video" per ottenere risultati.

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

[Esecuzione degli elementi del pannello di controllo](executing-control-panel-items.md)
</dt> <dt>

[Estensione degli elementi del pannello di controllo di sistema](extending-system-control-panel-items.md)
</dt> <dt>

[Assegnazione delle categorie del pannello di controllo](assigning-control-panel-categories.md)
</dt> <dt>

[Accesso al pannello di controllo in modalità provvisoria in Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 



