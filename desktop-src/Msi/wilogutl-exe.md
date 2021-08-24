---
description: Wilogutl.exe l'analisi dei file di log da un'installazione del programma di installazione di Windows e visualizza le soluzioni suggerite per gli errori rilevati in un file di log.
ms.assetid: 09aa03ba-992f-47ab-999b-ebdfe85c1ea7
title: Wilogutl.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74ee29553cba4105b5e6ff250f5b388adc964b9477bde5d1f25d073bbf2b1355
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119786596"
---
# <a name="wilogutlexe"></a>Wilogutl.exe

Wilogutl.exe l'analisi dei file di log da un'installazione del programma di installazione di Windows e visualizza le soluzioni suggerite per gli errori rilevati in un file di log.

Gli errori non critici non vengono visualizzati. Wilogutl.exe può essere eseguito in modalità non interattiva o con un'interfaccia utente. Lo strumento genera report come file di testo sia nell'interfaccia utente che in modalità non interattiva. Funziona meglio con i file di log Windows installer, ma funziona anche con i log non dettagliati. Per altre informazioni, vedere [Registrazione](logging.md).

Questo strumento è disponibile solo nei componenti di [Windows SDK per Windows programma di installazione](platform-sdk-components-for-windows-installer-developers.md).

## <a name="syntax"></a>Sintassi

**wilogutl.exe***\[<options>\]\[<source file>\]\[<options>\]\[<report file directory>\]*

È possibile usare le righe di comando seguenti per l'esecuzione in modalità non interattiva.

**wilogutl /q /l** *c: \\ mymsilog.log* **/o** *c \\ outputdir \\*

**wilogutl /q /l** *c: \\ mymsilog.log*

## <a name="command-line-options"></a>Opzioni della riga di comando

Wilogutl.exe usa le opzioni della riga di comando senza distinzione tra maiuscole e minuscole seguenti. È possibile usare un delimitatore di trattini al posto di una barra.



| Opzione | Descrizione                                                                                                                                                                                     |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nessuno   | Viene eseguito in modalità interfaccia utente, senza opzioni della riga di comando.                                                                                                                                                   |
| /q     | Specifica la modalità non interattiva. Wilogutl.exe genera file di report e non visualizza un'interfaccia utente.                                                                                            |
| /l     | Specifica il nome del file di log da analizzare. Questa opzione è obbligatoria quando si usa la modalità non interattiva.                                                                                           |
| /o     | Specifica la directory di output per i file di report. Questo percorso di output viene usato solo quando viene eseguito in modalità non interattiva. Se l'opzione non è presente, i report vengono inseriti nella directory C: \\ WiLogResults. |



 

Quando viene eseguita in modalità interfaccia utente, Wilogutl.exe le finestre di dialogo seguenti.



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
<td>Windows Analizzatore di log dettagliato del programma di installazione</td>
<td>La Windows finestra di dialogo Installer Verbose Log Analyzer consente agli utenti di selezionare un file di log per l'analisi:
<ul>
<li>Il <strong>pulsante</strong> Apri apre il file in Blocco note. L'area di anteprima può essere usata per verificare che sia stato selezionato il file di log corretto.</li>
<li>Il <strong>pulsante Analizza</strong> avvia l'analisi del file di log e visualizza la finestra di dialogo Visualizzazione file di log dettagliata .</li>
</ul></td>
</tr>
<tr class="even">
<td>Visualizzazione dettagliata del file di log</td>
<td>Nella finestra di dialogo Visualizzazione dettagliata file di log vengono visualizzate le informazioni sugli errori registrati. Usare i <strong>pulsanti Indietro</strong> <strong>e</strong> Avanti per spostarsi tra più errori. Per visualizzare gli errori non critici, selezionare la casella di controllo Mostra <strong>errori di debug</strong> ignorati . Viene visualizzata la versione del programma di installazione nel computer utilizzato per eseguire l'installazione registrata. Se l'installazione registrata è stata <strong></strong> eseguita con autorizzazioni elevate, la casella di controllo Installazione <strong></strong> con privilegi elevati è selezionata e le informazioni vengono fornite nelle caselle di testo Dettagli privilegi lato <strong>client</strong> e Dettagli privilegi lato server. La finestra di dialogo Visualizzazione dettagliata file di log contiene i pulsanti seguenti:<br/>
<ul>
<li><strong>Stati</strong> - Visualizzare la finestra di dialogo Stati funzionalità e componente.</li>
<li><strong>Proprietà</strong> - Visualizzare la finestra di dialogo Proprietà.</li>
<li><strong>Criteri</strong> - Visualizzare la finestra di dialogo Criteri.</li>
<li><strong>Log con annotazioni HTML</strong> - Mostra log come file HTML con annotazioni.</li>
<li><strong>Salvare i risultati</strong> - Salvare i file di report nella directory specificata.</li>
<li><strong>Guida ai messaggi di errore</strong> - Visualizzare la Guida del messaggio di errore del programma di installazione.</li>
<li><strong>Guida</strong> - Visualizzare la Guida per l'Windows Log Analyzer del programma di installazione.</li>
<li><strong>Come leggere un file di log</strong> - Visualizzare il documento della Guida del file di log.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Stati delle funzionalità e dei componenti</td>
<td>Nella <strong>finestra di dialogo Stati funzionalità e</strong> componenti vengono visualizzati gli stati delle funzionalità e dei componenti:
<ul>
<li>La <strong>colonna Funzionalità</strong> mostra il nome della funzionalità nel pacchetto di installazione.</li>
<li>La <strong>colonna</strong> Componente mostra il nome del componente nel pacchetto di installazione.</li>
<li>La <strong>colonna Installato</strong> mostra lo stato della funzionalità o del componente alla fine dell'installazione.</li>
<li>La <strong>colonna Richiesta</strong> mostra la selezione dell'utente durante l'installazione per lo stato della funzionalità o del componente.</li>
<li>La <strong>colonna Azione</strong> mostra l'azione eseguita dal programma di installazione per la funzionalità o il componente.</li>
</ul>
Per altre informazioni, vedere <a href="/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea"><strong>MsiGetComponentState</strong></a> e <a href="/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea"><strong>MsiGetFeatureState.</strong></a><br/></td>
</tr>
<tr class="even">
<td>Proprietà</td>
<td>La finestra di dialogo Proprietà mostra Windows del programma <a href="properties.md">di installazione e</a> i relativi valori alla fine dell'installazione. È possibile ordinare le proprietà in base al nome o al valore:
<ul>
<li>La <strong>scheda Client</strong> mostra le proprietà e i valori durante la parte lato client dell'installazione.</li>
<li>La <strong>scheda Server</strong> mostra le proprietà e i valori durante la parte del server dell'installazione.</li>
<li>La <strong>scheda Annidati</strong> mostra le proprietà e i valori di <a href="concurrent-installations.md">qualsiasi installazione simultanea.</a></li>
</ul></td>
</tr>
<tr class="odd">
<td>Criteri</td>
<td>Nella finestra di dialogo Criteri viene visualizzato il set <a href="system-policy.md">di criteri di</a> sistema dopo l'installazione:
<ul>
<li>Il valore 0 (zero) impostato per il criterio indica che il criterio non è abilitato.</li>
<li>Il valore 1 (uno) indica che i criteri sono abilitati.</li>
<li>Il valore di ? (punto interrogativo) indica che il valore dei criteri non viene registrato nel log.</li>
</ul>
Se è necessario un valore di criteri non presente nel log, provare a usare Regedit.exe per controllare le chiavi del Registro di sistema nel computer in cui l'installazione ha esito negativo.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="report-files"></a>File di report

Quando si esegue un'analisi  in modalità  non interattiva o si fa clic sul pulsante Salva risultati nella finestra di dialogo Visualizzazione file di log dettagliata, lo strumento Windows Installer Setup Analyzer genera tre file di testo e un file di log con annotazioni HTML.

La tabella seguente identifica i nomi e il contenuto nei file di report.



| Nome                      | Descrizione                                                                                                                    |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| logfilename \_summary.txt  | Riepiloga il file di log. Elenca le informazioni visualizzate nella finestra di dialogo Visualizzazione file di log dettagliata e il primo errore.         |
| logfilename \_errors.txt   | Identifica il numero di errori, gli errori e le soluzioni consigliate. Questo file elenca gli errori critici e non critici. |
| logfilename \_policies.txt | Identifica i nomi e i valori dei criteri impostati alla fine dell'installazione come nella finestra di dialogo Criteri .                       |
| dettagli \_logfilename.htm  | Log con annotazioni HTML con una legenda per la codifica a colori.                                                                      |



 

## <a name="return-values"></a>Valori restituiti

Se vengono passati argomenti della riga di comando non validi per le operazioni in modalità non interattiva, Wilogutl.exe non esegue alcuna operazione e il processo restituisce uno dei valori nella tabella seguente.



| Valore | Significato                                                                 |
|-------|-------------------------------------------------------------------------|
| 1     | È stata specificata una directory di output non valido.                                      |
| 2     | È stato specificato un nome file di log non valido.                                         |
| 3     | È stato passato /q, ma manca l'opzione obbligatoria /l per il nome del file di log. |
| 4     | È stato passato /l, ma manca l'opzione obbligatoria /q per la modalità non interattiva.        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Versioni rilasciate, strumenti e ridistribuibili](released-versions-tools-and-redistributables.md)
</dt> <dt>

[Windows Strumenti di sviluppo del programma di installazione](windows-installer-development-tools.md)
</dt> </dl>

 

 




