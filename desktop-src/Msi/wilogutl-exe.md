---
description: Wilogutl.exe assiste l'analisi dei file di log da un'installazione del programma di installazione di Windows e visualizza le soluzioni suggerite per gli errori rilevati in un file di log.
ms.assetid: 09aa03ba-992f-47ab-999b-ebdfe85c1ea7
title: Wilogutl.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6734b22afa6aa5d464f3d6b01555e54f240e006b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476027"
---
# <a name="wilogutlexe"></a>Wilogutl.exe

Wilogutl.exe assiste l'analisi dei file di log da un'installazione del programma di installazione di Windows e visualizza le soluzioni suggerite per gli errori rilevati in un file di log.

Gli errori non critici non vengono visualizzati. Wilogutl.exe può essere eseguito in modalità non interattiva o con un'interfaccia utente. Lo strumento genera report come file di testo sia nell'interfaccia utente che in modalità non interattiva. Funziona meglio con i file di log Windows programma di installazione, ma funziona anche con i log non dettagliati. Per altre informazioni, vedere [Registrazione](logging.md).

Questo strumento è disponibile solo in componenti Windows [SDK per sviluppatori Windows Programma di installazione](platform-sdk-components-for-windows-installer-developers.md).

## <a name="syntax"></a>Sintassi

**wilogutl.exe***\[<options>\]\[<source file>\]\[<options>\]\[<report file directory>\]*

È possibile usare le righe di comando seguenti per l'esecuzione in modalità non interattiva.

**wilogutl /q /l** *c: \\ mymsilog.log* **/o** *c \\ outputdir \\*

**wilogutl /q /l** *c: \\ mymsilog.log*

## <a name="command-line-options"></a>Opzioni della riga di comando

Wilogutl.exe usa le opzioni della riga di comando seguenti senza distinzione tra maiuscole e minuscole. È possibile usare un delimitatore trattino al posto di una barra.



| Opzione | Descrizione                                                                                                                                                                                     |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nessuno   | Viene eseguito in modalità interfaccia utente, senza opzioni della riga di comando.                                                                                                                                                   |
| /q     | Specifica la modalità non interattiva. Wilogutl.exe genera file di report e non visualizza un'interfaccia utente.                                                                                            |
| /l     | Specifica il nome del file di log da analizzare. Questa opzione è obbligatoria quando si usa la modalità non interattiva.                                                                                           |
| /o     | Specifica la directory di output per i file di report. Questo percorso di output viene usato solo quando viene eseguito in modalità non interattiva. Se l'opzione non è presente, i report vengono inseriti nella directory C: \\ WiLogResults. |



 

Quando viene eseguito in modalità interfaccia utente, Wilogutl.exe vengono visualizzate le finestre di dialogo seguenti.




| Nome | Descrizione | 
|------|-------------|
| Windows Installer Verbose Log Analyzer | La Windows finestra di dialogo Installer Verbose Log Analyzer consente agli utenti di selezionare un file di log per l'analisi:<ul><li>Il <strong>pulsante</strong> Apri apre il file in Blocco note. L'area di anteprima può essere usata per verificare che sia stato selezionato il file di log corretto.</li><li>Il <strong>pulsante Analizza</strong> avvia l'analisi dei file di log e visualizza la finestra di dialogo Visualizzazione dettagliata file di log .</li></ul> | 
| Visualizzazione dettagliata dei file di log | Nella finestra di dialogo Visualizzazione dettagliata file di log vengono visualizzate le informazioni sugli errori registrati. Usare i <strong>pulsanti Indietro</strong> <strong>e Avanti</strong> per spostarsi tra più errori. Per visualizzare errori non critici, selezionare la <strong>casella di controllo Mostra errori di debug</strong> ignorati . Viene visualizzata la versione del programma di installazione nel computer utilizzato per eseguire l'installazione registrata. Se l'installazione registrata è stata <strong></strong> eseguita con autorizzazioni elevate, la casella di controllo Installazione con privilegi elevati è selezionata e le informazioni vengono fornite nelle caselle di testo Client Side Privilege Details (Dettagli privilegi lato <strong>client)</strong> e <strong>Server Side Privilege Details (Dettagli</strong> privilegi lato server). La finestra di dialogo Visualizzazione dettagliata file di log contiene i pulsanti seguenti:<br /><ul><li><strong>Stati:</strong> consente di visualizzare la finestra di dialogo Stati funzionalità e componenti .</li><li><strong>Proprietà</strong> : consente di visualizzare la finestra di dialogo Proprietà.</li><li><strong>Criteri</strong> : consente di visualizzare la finestra di dialogo Criteri.</li><li><strong>Log con annotazioni HTML:</strong> mostra il log come file HTML con annotazioni.</li><li><strong>Salva risultati:</strong> consente di salvare i file di report nella directory specificata.</li><li><strong>Guida ai messaggi di errore:</strong> mostra la Guida del messaggio di errore del programma di installazione.</li><li><strong>Guida:</strong> visualizza la Guida per l'Windows programma di installazione di Log Analyzer.</li><li><strong>Come leggere un file di log:</strong> visualizzare il documento della Guida del file di log.</li></ul> | 
| Stati delle funzionalità e dei componenti | Nella <strong>finestra di dialogo Stati funzionalità e</strong> componenti vengono visualizzati gli stati delle funzionalità e dei componenti:<ul><li>La <strong>colonna</strong> Funzionalità mostra il nome della funzionalità nel pacchetto di installazione.</li><li>La <strong>colonna</strong> Componente mostra il nome del componente nel pacchetto di installazione.</li><li>La <strong>colonna</strong> Installato mostra lo stato della funzionalità o del componente alla fine dell'installazione.</li><li>La <strong>colonna</strong> Richiesta mostra la selezione dell'utente durante l'installazione per lo stato della funzionalità o del componente.</li><li>La <strong>colonna Azione</strong> mostra l'azione eseguita dal programma di installazione per la funzionalità o il componente.</li></ul>Per altre informazioni, vedere <a href="/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea"><strong>MsiGetComponentState</strong></a> e <a href="/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea"><strong>MsiGetFeatureState.</strong></a><br /> | 
| Proprietà | La finestra di dialogo Proprietà Windows <a href="properties.md">proprietà del programma di installazione</a> e i relativi valori al termine dell'installazione. È possibile ordinare le proprietà in base al nome o al valore:<ul><li>La <strong>scheda Client</strong> mostra le proprietà e i valori durante la parte lato client dell'installazione.</li><li>La <strong>scheda Server</strong> mostra le proprietà e i valori durante la parte server dell'installazione.</li><li>La <strong>scheda Annidati</strong> mostra le proprietà e i valori di <a href="concurrent-installations.md">tutte le installazioni simultanee.</a></li></ul> | 
| Criteri | La finestra di dialogo Criteri visualizza i <a href="system-policy.md">criteri di sistema</a> impostati dopo l'installazione:<ul><li>Il valore 0 (zero) impostato per il criterio indica che il criterio non è abilitato.</li><li>Il valore 1 (uno) indica che i criteri sono abilitati.</li><li>Il valore ? (punto interrogativo) indica che il valore dei criteri non viene registrato nel log.</li></ul>Se è necessario un valore di criteri non presente nel log, provare a usare Regedit.exe per controllare le chiavi del Registro di sistema nel computer in cui l'installazione ha esito negativo.<br /> | 




 

## <a name="report-files"></a>File di report

Quando si esegue un'analisi  in modalità  non interattiva o si fa clic sul pulsante Salva risultati nella finestra di dialogo Visualizzazione dettagliata file di log, lo strumento Windows Installer Setup Analyzer genera tre file di testo e un file di log con annotazioni HTML.

Nella tabella seguente vengono identificati i nomi e il contenuto dei file di report.



| Nome                      | Descrizione                                                                                                                    |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| logfilename \_summary.txt  | Riepiloga il file di log. Elenca le informazioni visualizzate nella finestra di dialogo Visualizzazione dettagliata file di log e il primo errore.         |
| logfilename \_errors.txt   | Identifica il numero di errori, gli errori e le soluzioni consigliate. Questo file elenca sia gli errori critici che gli errori non critici. |
| logfilename \_policies.txt | Identifica i nomi e i valori dei criteri impostati alla fine dell'installazione come nella finestra di dialogo Criteri .                       |
| Dettagli \_logfilename.htm  | Log con annotazioni HTML con una legenda per la codifica a colori.                                                                      |



 

## <a name="return-values"></a>Valori restituiti

Se vengono passati argomenti della riga di comando non validi per le operazioni in modalità non interattiva, Wilogutl.exe non esegue alcuna operazione e il processo restituisce uno dei valori nella tabella seguente.



| valore | Significato                                                                 |
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

 

 




