---
description: Wilogutl.exe facilita l'analisi dei file di log da un'installazione di Windows Installer e visualizza le soluzioni suggerite agli errori rilevati in un file di log.
ms.assetid: 09aa03ba-992f-47ab-999b-ebdfe85c1ea7
title: Wilogutl.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec81c3c82299a08fd947fbbecc7afd8a373252b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319951"
---
# <a name="wilogutlexe"></a>Wilogutl.exe

Wilogutl.exe facilita l'analisi dei file di log da un'installazione di Windows Installer e visualizza le soluzioni suggerite agli errori rilevati in un file di log.

Gli errori non critici non vengono visualizzati. Wilogutl.exe possono essere eseguiti in modalità non interattiva o con un'interfaccia utente (UI). Lo strumento genera report come file di testo sia nell'interfaccia utente che nelle modalità non interattiva. Funziona meglio con i file di log dettagliati Windows Installer, ma funziona anche con log non dettagliati. Per altre informazioni, vedere [Registrazione](logging.md).

Questo strumento è disponibile solo nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md).

## <a name="syntax"></a>Sintassi

**wilogutl.exe***\[<options>\]\[<source file>\]\[<options>\]\[<report file directory>\]*

È possibile utilizzare le seguenti righe di comando per eseguire in modalità non interattiva.

**Wilogutl/q/l** *c: \\ mymsilog. log* **/o** *c \\ OutputDir \\*

**Wilogutl/q/l** *c: \\ mymsilog. log*

## <a name="command-line-options"></a>Opzioni della riga di comando

Wilogutl.exe usa le seguenti opzioni della riga di comando senza distinzione tra maiuscole e minuscole. È possibile usare un delimitatore di trattino al posto di una barra.



| Opzione | Descrizione                                                                                                                                                                                     |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nessuno   | Viene eseguito in modalità interfaccia utente, senza opzioni della riga di comando.                                                                                                                                                   |
| /q     | Specifica la modalità non interattiva. Wilogutl.exe genera file di report e non visualizza un'interfaccia utente.                                                                                            |
| /l     | Specifica il nome del file di log da analizzare. Questa opzione è obbligatoria quando si usa la modalità non interattiva.                                                                                           |
| /o     | Specifica la directory di output per i file di report. Questo percorso di output viene usato solo quando è in esecuzione in modalità non interattiva. Se l'opzione non è presente, i report vengono inseriti nella directory C: \\ WiLogResults |



 

Quando viene eseguito in modalità interfaccia utente, Wilogutl.exe Visualizza le seguenti finestre di dialogo.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Nome</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Analizzatore log dettagliato Windows Installer</td>
<td>La finestra di dialogo analizzatore log dettagliato di Windows Installer consente agli utenti di selezionare un file di log per l'analisi:
<ul>
<li>Il pulsante <strong>Apri</strong> apre il file nel blocco note. È possibile utilizzare l'area di anteprima per verificare che sia stato selezionato il file di log corretto.</li>
<li>Il pulsante <strong>analizza</strong> avvia l'analisi dei file di log e visualizza la finestra di dialogo visualizzazione file di log dettagliata.</li>
</ul></td>
</tr>
<tr class="even">
<td>Visualizzazione dettagliata del file di log</td>
<td>Nella finestra di dialogo visualizzazione file di log dettagliata vengono visualizzate le informazioni sull'errore registrate. Usare i pulsanti <strong>indietro</strong> e <strong>Avanti</strong> per spostarsi tra più errori. Per visualizzare gli errori non critici, selezionare la casella di controllo <strong>Mostra errori di debug ignorati</strong> . Viene visualizzata la versione del programma di installazione nel computer utilizzato per eseguire l'installazione registrata. Se l'installazione registrata è stata eseguita con autorizzazioni elevate, la casella di controllo <strong>installazione con privilegi elevati</strong> è selezionata e le informazioni vengono fornite nelle caselle di testo Dettagli <strong>privilegi lato client</strong> e <strong>privilegi lato server</strong> . Nella finestra di dialogo visualizzazione file di log dettagliata sono disponibili i pulsanti seguenti:<br/>
<ul>
<li><strong>Stati</strong> - di Consente di visualizzare la finestra di dialogo stati componenti e funzionalità.</li>
<li><strong>Proprietà</strong> - di Visualizza la finestra di dialogo Proprietà.</li>
<li><strong>Criteri</strong> - di Mostra la finestra di dialogo criteri.</li>
<li>Log con annotazioni <strong>HTML</strong> - Mostra log come file HTML con annotazioni.</li>
<li><strong>Salva risultati</strong> - Consente di salvare i file di report nella directory specificata.</li>
<li>Guida del messaggio di <strong>errore</strong> - Mostra la guida del messaggio di errore del programma di installazione.</li>
<li><strong>Guida</strong> - di Mostra la guida per Windows Installer Setup Log Analyzer.</li>
<li><strong>Come leggere un file</strong> - di log Visualizzare il documento della guida del file di log.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Stati di funzionalità e componenti</td>
<td>Nella finestra di dialogo <strong>stati funzionalità e</strong> componenti vengono visualizzati gli Stati delle funzionalità e dei componenti di:
<ul>
<li>Nella colonna <strong>funzionalità</strong> viene visualizzato il nome della funzionalità nel pacchetto di installazione.</li>
<li>Nella colonna <strong>componente</strong> viene visualizzato il nome del componente nel pacchetto di installazione.</li>
<li>Nella colonna <strong>installato</strong> viene visualizzato lo stato della funzionalità o del componente alla fine dell'installazione.</li>
<li>Nella colonna <strong>richiesta</strong> viene visualizzata la selezione dell'utente durante l'installazione per lo stato della funzionalità o del componente.</li>
<li>Nella colonna <strong>azione</strong> viene visualizzata l'azione eseguita dal programma di installazione per la funzionalità o il componente.</li>
</ul>
Per ulteriori informazioni, vedere <a href="/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea"><strong>MsiGetComponentState</strong></a> e <a href="/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea"><strong>MsiGetFeatureState</strong></a>.<br/></td>
</tr>
<tr class="even">
<td>Proprietà</td>
<td>Nella finestra di dialogo proprietà vengono visualizzate Windows Installer <a href="properties.md">Proprietà</a> e i relativi valori alla fine dell'installazione. È possibile ordinare le proprietà in base al nome o al valore:
<ul>
<li>La scheda <strong>client</strong> Mostra le proprietà e i valori durante la parte lato client dell'installazione.</li>
<li>La scheda <strong>Server</strong> Mostra le proprietà e i valori durante la parte relativa al server dell'installazione.</li>
<li>La scheda <strong>nidificata</strong> Mostra le proprietà e i valori di tutte le <a href="concurrent-installations.md">installazioni simultanee</a>.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Criteri</td>
<td>Nella finestra di dialogo criteri viene visualizzato il set di <a href="system-policy.md">criteri di sistema</a> dopo l'installazione:
<ul>
<li>Il valore 0 (zero) impostato per il criterio indica che i criteri non sono abilitati.</li>
<li>Il valore 1 (uno) indica che i criteri sono abilitati.</li>
<li>Valore? (punto interrogativo) indica che il valore dei criteri non è registrato nel log.</li>
</ul>
Se è necessario un valore dei criteri non presente nel log, provare a usare Regedit.exe per verificare se le chiavi del registro di sistema nel computer non sono presenti nell'installazione.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="report-files"></a>File di report

Quando si esegue un'analisi in modalità non interattiva o si fa clic sul pulsante **Salva risultati** nella finestra di dialogo **visualizzazione file di log dettagliata** , il Windows Installer strumento Analizzatore configurazione genera tre file di testo e un file di log con annotazioni HTML.

Nella tabella seguente vengono identificati i nomi e il contenuto dei file di report.



| Nome                      | Descrizione                                                                                                                    |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| LogFileName \_summary.txt  | Riepiloga il file di log. Elenca le informazioni visualizzate nella finestra di dialogo visualizzazione file di log dettagliata e il primo errore.         |
| LogFileName \_errors.txt   | Identifica il numero di errori, gli errori e le soluzioni consigliate. In questo file vengono elencati errori critici e non critici. |
| LogFileName \_policies.txt | Identifica i nomi dei criteri e i valori impostati alla fine dell'installazione come nella finestra di dialogo criteri.                       |
| Dettagli \_logfilename.htm  | Log con annotazioni HTML con una legenda per la codifica a colori.                                                                      |



 

## <a name="return-values"></a>Valori restituiti

Se vengono passati argomenti della riga di comando non validi per le operazioni in modalità non interattiva, Wilogutl.exe non esegue alcuna operazione e il processo restituisce uno dei valori indicati nella tabella seguente.



| Valore | Significato                                                                 |
|-------|-------------------------------------------------------------------------|
| 1     | È stata specificata una directory di output non valida.                                      |
| 2     | Il nome del file di log specificato non è valido.                                         |
| 3     | Passato/q, ma non è presente l'opzione richiesta/l per il nome del file di log. |
| 4     | È stato passato/l, ma manca l'opzione obbligatoria/q per la modalità non interattiva.        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Versioni rilasciate, strumenti e ridistribuibili](released-versions-tools-and-redistributables.md)
</dt> <dt>

[Strumenti di sviluppo Windows Installer](windows-installer-development-tools.md)
</dt> </dl>

 

 




