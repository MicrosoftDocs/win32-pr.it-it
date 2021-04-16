---
title: Classificazioni di comandi MCI
description: Classificazioni di comandi MCI
ms.assetid: e03edfab-06c9-4337-935b-9effd2996c2e
keywords:
- Comandi MCI, classificazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1524e6aa2094679e91acddb9dbfbb8cb480eb39f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515508"
---
# <a name="classifications-of-mci-commands"></a>Classificazioni di comandi MCI

MCI definisce quattro classificazioni comandi: System, required, Basic ed Extended. L'elenco seguente descrive le classificazioni dei comandi seguenti:

-   I *comandi di sistema* vengono gestiti direttamente da MCI, anziché dal driver.
-   I *comandi obbligatori* vengono gestiti dal driver. Tutti i driver MCI devono supportare i comandi e i flag richiesti.
-   I *comandi di base* (o i comandi facoltativi) vengono usati da alcuni dispositivi. Se un dispositivo supporta un comando di base, deve supportare un set di flag definito per quel comando.
-   I *comandi estesi* sono specifici di un driver o di un tipo di dispositivo. I comandi estesi includono comandi, ad esempio i comandi [**put**](put.md) ([**MCI \_ put**](mci-put.md)) e [**where**](where.md) ([**MCI \_ where**](mci-where.md)) per i tipi di dispositivo **digitalvideo** e **overlay** ed estensioni ai comandi esistenti, ad esempio il flag "Stretch" del comando [**status**](status.md) ([**MCI \_ status**](mci-status.md)) per il tipo di dispositivo overlay.

Mentre il sistema e i comandi obbligatori sono il set di comandi minimo per tutti i driver MCI, i comandi di base e quelli estesi non sono supportati da tutti i driver. L'applicazione può sempre usare i comandi di sistema e richiesti e i relativi flag, ma se è necessario usare un comando o un flag di base o esteso, deve prima eseguire una query sul driver usando il comando [**Capability**](capability.md) ([**MCI \_ GETDEVCAPS**](mci-getdevcaps.md)). Le sezioni seguenti riepilogano i comandi specifici in ogni categoria.

## <a name="system-commands"></a>Comandi di sistema

MCI elabora direttamente i comandi di sistema seguenti, anziché passarli ai dispositivi MCI.



| string                 | Message                             | Descrizione                            |
|------------------------|-------------------------------------|----------------------------------------|
| [**interruzione**](break.md) | [**\_interruzioni MCI**](mci-break.md)     | Imposta un tasto di pausa per un dispositivo MCI.    |
| [sysinfo](sysinfo.md) | [**\_sysinfo MCI**](mci-sysinfo.md) | Restituisce informazioni sui dispositivi MCI. |



 

## <a name="required-commands"></a>Comandi obbligatori

Tutti i dispositivi MCI supportano i seguenti comandi obbligatori.



| string                           | Message                                   | Descrizione                                                                                                               |
|----------------------------------|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**funzionalità**](capability.md) | [**\_GETDEVCAPS MCI**](mci-getdevcaps.md) | Ottiene le funzionalità di un dispositivo.                                                                                     |
| [**vicino**](close.md)           | [**\_chiusura MCI**](mci-close.md)           | Chiude il dispositivo.                                                                                                        |
| [**informazioni**](info.md)             | [**\_informazioni MCI**](mci-info.md)             | Ottiene le informazioni testuali da un dispositivo.                                                                                |
| [**aprire**](open.md)             | [**\_aperto MCI**](mci-open.md)             | Inizializza il dispositivo.                                                                                                   |
| [**stato**](status.md)         | [**\_stato MCI**](mci-status.md)         | Ottiene le informazioni sullo stato dal dispositivo. Alcuni dei flag di questo comando non sono obbligatori, quindi è anche un comando di base. |



 

I dispositivi devono inoltre supportare un set standard di flag di comando per i comandi richiesti.

## <a name="basic-commands"></a>Comandi di base

Nell'elenco seguente vengono riepilogati i comandi di base. L'uso di questi comandi da parte di un dispositivo MCI è facoltativo.



| string                   | Message                           | Descrizione                                                                                                                                                                                                                             |
|--------------------------|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**carico**](load.md)     | [**\_carico MCI**](mci-load.md)     | Carica i dati da un file.                                                                                                                                                                                                                 |
| [**pause**](pause.md)   | [**\_pausa MCI**](mci-pause.md)   | Interrompe la riproduzione. La riproduzione o la registrazione può essere ripresa nella posizione corrente.                                                                                                                                                            |
| [**Play**](play.md)     | [**\_riproduzione MCI**](mci-play.md)     | Avvia la trasmissione dei dati di output.                                                                                                                                                                                                        |
| [**record**](record.md) | [**\_record MCI**](mci-record.md) | Avvia la registrazione dei dati di input.                                                                                                                                                                                                            |
| [**riprendere**](resume.md) | [**\_ripresa MCI**](mci-resume.md) | Riprende la riproduzione o la registrazione in un dispositivo sospeso.                                                                                                                                                                                        |
| [**salvare**](save.md)     | [**salvataggio di MCI \_**](mci-save.md)     | Salva i dati in un file su disco.                                                                                                                                                                                                              |
| [**cercare**](seek.md)     | [**\_ricerca MCI**](mci-seek.md)     | Cerca avanti o indietro.                                                                                                                                                                                                              |
| [**set**](set.md)       | [**SET di MCI \_**](mci-set.md)       | Imposta lo stato operativo del dispositivo.                                                                                                                                                                                                 |
| [**stato**](status.md) | [**STATO MCI**](mci-status.md)  | Ottiene informazioni sullo stato del dispositivo. Si tratta anche di un comando obbligatorio. Poiché alcuni dei relativi flag non sono obbligatori, sono elencati anche qui. Gli elementi facoltativi supportano i dispositivi che utilizzano supporti lineari con posizioni identificabili. |
| [**arrestare**](stop.md)     | [**\_arresto MCI**](mci-stop.md)     | Interrompe la riproduzione.                                                                                                                                                                                                                          |



 

Se un driver supporta un comando di base, deve supportare anche un set standard di flag per il comando.

## <a name="extended-commands"></a>Comandi estesi

Alcuni dispositivi MCI hanno comandi aggiuntivi o aggiungono flag ai comandi esistenti. Sebbene alcuni comandi estesi si applichino solo a un driver di dispositivo specifico, la maggior parte di essi si applica a tutti i driver di un particolare tipo di dispositivo. Ad esempio, il set di comandi per il tipo di dispositivo **sequencer** estende il comando [**set**](set.md) ([**MCI \_ set**](mci-set.md)) per aggiungere i formati di ora necessari per i sequencer MIDI.

Non è necessario presupporre che il dispositivo supporti i comandi estesi o i flag. È possibile usare il comando [**Capability**](capability.md) ([**MCI \_ GETDEVCAPS**](mci-getdevcaps.md)) per determinare se una funzionalità specifica è supportata e l'applicazione deve essere pronta per gestire i valori restituiti "comando non supportato" o "funzione non supportata".

I comandi estesi seguenti sono disponibili con i tipi di dispositivi elencati.



| string                         | Message                                 | Tipi di dispositivi            | Descrizione                                                                                       |
|--------------------------------|-----------------------------------------|-------------------------|---------------------------------------------------------------------------------------------------|
| [**configurare**](configure.md) | [**configurazione di MCI \_**](mci-configure.md) | digitalvideo            | Consente di visualizzare una finestra di dialogo di configurazione.                                                              |
| [**segnale**](cue.md)             | [**\_cue MCI**](mci-cue.md)             | digitalvideo, WaveAudio | Prepara la riproduzione o la registrazione.                                                                |
| [**eliminare**](delete.md)       | [**eliminazione di MCI \_**](mci-delete.md)       | WaveAudio               | Elimina un segmento di dati dal file multimediale.                                                       |
| [fuga](escape.md)           | [**\_escape MCI**](mci-escape.md)       | videodisco               | Invia informazioni personalizzate a un dispositivo.                                                             |
| [**congelare**](freeze.md)       | [**\_blocco MCI**](mci-freeze.md)       | overlay                 | Disabilita l'acquisizione di video nel buffer del frame.                                                   |
| [**mettere**](put.md)             | [**PUT MCI**](mci-put.md)              | digitalvideo, sovrimpressione   | Definisce le finestre di origine, di destinazione e di cornice.                                               |
| [**tenere presente**](realize.md)     | [**realizzazione di MCI \_**](mci-realize.md)     | digitalvideo            | Indica al dispositivo di selezionare e realizzare la relativa tavolozza in un contesto di dispositivo della finestra visualizzata. |
| [**SetAudio**](setaudio.md)   | [**sefonica MCI \_**](mci-setaudio.md)  | digitalvideo            | Imposta i parametri audio per il video.                                                                  |
| [**video**](setvideo.md)   | [**VIDEO su MCI \_**](mci-setvideo.md)  | digitalvideo            | Imposta i parametri del video.                                                                            |
| [**signal**](signal.md)       | [**\_segnale MCI**](mci-signal.md)       | digitalvideo            | Identifica una posizione specificata con un segnale.                                                    |
| [**selezione**](spin.md)           | [**\_rotazione MCI**](mci-spin.md)           | videodisco               | Avvia la rotazione del disco o interrompe la rotazione del disco.                                         |
| [**passo**](step.md)           | [**\_passaggio MCI**](mci-step.md)           | digitalvideo, videodisco | Esegue la riproduzione di uno o più frame avanti o indietro.                                             |
| [**Sblocca**](unfreeze.md)   | [**\_Sblocca MCI**](mci-unfreeze.md)   | overlay                 | Consente al buffer del frame di acquisire dati video.                                                   |
| [**aggiornamento**](update.md)       | [**aggiornamento di MCI \_**](mci-update.md)       | digitalvideo            | Ridisegna il frame corrente nel contesto di dispositivo.                                               |
| [**dove**](where.md)         | [**MCI DOVE**](mci-where.md)          | digitalvideo, sovrimpressione   | Ottiene il rettangolo che specifica l'area di origine, la destinazione o il frame.                          |
| [**finestra**](window.md)       | [**\_finestra MCI**](mci-window.md)       | digitalvideo, sovrimpressione   | Controlla la finestra di visualizzazione.                                                                      |



 

 

 




