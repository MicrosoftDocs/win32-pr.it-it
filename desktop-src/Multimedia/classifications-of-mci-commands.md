---
title: Classificazioni dei comandi MCI
description: Classificazioni dei comandi MCI
ms.assetid: e03edfab-06c9-4337-935b-9effd2996c2e
keywords:
- comandi MCI, classificazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72b532c56d1cdecac50cb24b14bf4f1b51c401dd5bb2501d1c421064659f1ef2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807930"
---
# <a name="classifications-of-mci-commands"></a>Classificazioni dei comandi MCI

MCI definisce quattro classificazioni dei comandi: sistema, obbligatorio, di base ed esteso. L'elenco seguente descrive queste classificazioni dei comandi:

-   *I comandi* di sistema vengono gestiti direttamente da MCI, anziché dal driver.
-   *I comandi* necessari vengono gestiti dal driver. Tutti i driver MCI devono supportare i comandi e i flag necessari.
-   *I comandi* di base (o facoltativi) vengono usati da alcuni dispositivi. Se un dispositivo supporta un comando di base, deve supportare un set definito di flag per tale comando.
-   *I comandi estesi* sono specifici di un tipo di dispositivo o di un driver. I comandi estesi includono comandi, ad esempio i comandi [**put**](put.md) ([**MCI \_ PUT**](mci-put.md)) e [**where**](where.md) ([**MCI \_ WHERE**](mci-where.md)) per i tipi di dispositivo **digitalvideo** e **overlay,** e le estensioni ai comandi esistenti ,ad esempio il flag "stretch" del comando [**status**](status.md) ([**MCI \_ STATUS**](mci-status.md)) per il tipo di dispositivo di sovrapposizione.

Anche se i comandi di sistema e obbligatori sono il set di comandi minimo per qualsiasi driver MCI, i comandi di base ed estesi non sono supportati da tutti i driver. L'applicazione può sempre usare i comandi di sistema e obbligatori e i relativi flag, ma se deve usare un comando o un flag di base o esteso, deve prima eseguire una query sul driver usando il comando della funzionalità [**(**](capability.md) [**MCI \_ GETDEVCAPS).**](mci-getdevcaps.md) Le sezioni seguenti riepilogano i comandi specifici in ogni categoria.

## <a name="system-commands"></a>Comandi di sistema

MCI elabora direttamente i comandi di sistema seguenti, anziché passarli ai dispositivi MCI.



| string                 | Message                             | Descrizione                            |
|------------------------|-------------------------------------|----------------------------------------|
| [**Pausa**](break.md) | [**INTERRUZIONE \_ MCI**](mci-break.md)     | Imposta una chiave di interruzione per un dispositivo MCI.    |
| [Sysinfo](sysinfo.md) | [**MCI \_ SYSINFO**](mci-sysinfo.md) | Restituisce informazioni sui dispositivi MCI. |



 

## <a name="required-commands"></a>Comandi obbligatori

Tutti i dispositivi MCI supportano i comandi necessari seguenti.



| string                           | Message                                   | Descrizione                                                                                                               |
|----------------------------------|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**Capacità**](capability.md) | [**MCI \_ GETDEVCAPS**](mci-getdevcaps.md) | Ottiene le funzionalità di un dispositivo.                                                                                     |
| [**Vicino**](close.md)           | [**MCI \_ CLOSE**](mci-close.md)           | Chiude il dispositivo.                                                                                                        |
| [**Informazioni**](info.md)             | [**INFORMAZIONI \_ MCI**](mci-info.md)             | Ottiene informazioni testuali da un dispositivo.                                                                                |
| [**apre**](open.md)             | [**MCI \_ OPEN**](mci-open.md)             | Inizializza il dispositivo.                                                                                                   |
| [**Stato**](status.md)         | [**STATO \_ MCI**](mci-status.md)         | Ottiene informazioni sullo stato dal dispositivo. Alcuni flag di questo comando non sono obbligatori, quindi è anche un comando di base. |



 

I dispositivi devono inoltre supportare un set standard di flag di comando per i comandi necessari.

## <a name="basic-commands"></a>Comandi di base

L'elenco seguente riepiloga i comandi di base. L'uso di questi comandi da parte di un dispositivo MCI è facoltativo.



| string                   | Message                           | Descrizione                                                                                                                                                                                                                             |
|--------------------------|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Carico**](load.md)     | [**CARICO \_ MCI**](mci-load.md)     | Carica i dati da un file.                                                                                                                                                                                                                 |
| [**Pausa**](pause.md)   | [**MCI \_ PAUSE**](mci-pause.md)   | Interrompe la riproduzione. La riproduzione o la registrazione possono essere ripresi nella posizione corrente.                                                                                                                                                            |
| [**Giocare**](play.md)     | [**MCI \_ PLAY**](mci-play.md)     | Avvia la trasmissione dei dati di output.                                                                                                                                                                                                        |
| [**Registrazione**](record.md) | [**MCI \_ RECORD**](mci-record.md) | Avvia la registrazione dei dati di input.                                                                                                                                                                                                            |
| [**riassumere**](resume.md) | [**RIPRESA \_ MCI**](mci-resume.md) | Riprende la riproduzione o la registrazione in un dispositivo sospeso.                                                                                                                                                                                        |
| [**Salvare**](save.md)     | [**MCI \_ SAVE**](mci-save.md)     | Salva i dati in un file su disco.                                                                                                                                                                                                              |
| [**Cercare**](seek.md)     | [**MCI \_ SEEK**](mci-seek.md)     | Cerca in avanti o all'indietro.                                                                                                                                                                                                              |
| [**Impostare**](set.md)       | [**MCI \_ SET**](mci-set.md)       | Imposta lo stato operativo del dispositivo.                                                                                                                                                                                                 |
| [**Stato**](status.md) | [**STATO MCI**](mci-status.md)  | Ottiene informazioni sullo stato del dispositivo. Si tratta anche di un comando obbligatorio. Poiché alcuni dei flag non sono obbligatori, è elencato anche qui. Gli elementi facoltativi supportano i dispositivi che usano supporti lineari con posizioni identificabili. |
| [**Fermare**](stop.md)     | [**ARRESTO \_ MCI**](mci-stop.md)     | Interrompe la riproduzione.                                                                                                                                                                                                                          |



 

Se un driver supporta un comando di base, deve supportare anche un set standard di flag per il comando.

## <a name="extended-commands"></a>Comandi estesi

Alcuni dispositivi MCI hanno comandi aggiuntivi o aggiungono flag ai comandi esistenti. Anche se alcuni comandi estesi si applicano solo a un driver di dispositivo specifico, la maggior parte di essi si applica a tutti i driver di un determinato tipo di dispositivo. Ad esempio, il set di comandi per il tipo di dispositivo sequencer estende il [**comando set**](set.md) ([**MCI \_ SET**](mci-set.md)) per aggiungere i formati di ora necessari per i **sequencer** MIDI.

Non è consigliabile presupporre che il dispositivo supporti i comandi o i flag estesi. È possibile usare il comando [**capability**](capability.md) ([**MCI \_ GETDEVCAPS**](mci-getdevcaps.md)) per determinare se è supportata una funzionalità specifica e l'applicazione deve essere pronta per gestire i valori restituiti "comando non supportato" o "funzione non supportata".

I comandi estesi seguenti sono disponibili con i tipi di dispositivo elencati.



| string                         | Message                                 | Tipi di dispositivi            | Descrizione                                                                                       |
|--------------------------------|-----------------------------------------|-------------------------|---------------------------------------------------------------------------------------------------|
| [**Configurare**](configure.md) | [**CONFIGURAZIONE \_ MCI**](mci-configure.md) | digitalvideo            | Visualizza una finestra di dialogo di configurazione.                                                              |
| [**segnale**](cue.md)             | [**MCI \_ CUE**](mci-cue.md)             | digitalvideo, waveaudio | Si prepara per la riproduzione o la registrazione.                                                                |
| [**Elimina**](delete.md)       | [**MCI \_ DELETE**](mci-delete.md)       | Waveaudio               | Elimina un segmento di dati dal file multimediale.                                                       |
| [Fuga](escape.md)           | [**MCI \_ ESCAPE**](mci-escape.md)       | videodisc               | Invia informazioni personalizzate a un dispositivo.                                                             |
| [**Congelare**](freeze.md)       | [**BLOCCO \_ MCI**](mci-freeze.md)       | overlay                 | Disabilita l'acquisizione di video nel buffer dei fotogrammi.                                                   |
| [**Mettere**](put.md)             | [**MCI PUT**](mci-put.md)              | digitalvideo, overlay   | Definisce le finestre di origine, di destinazione e cornice.                                               |
| [**Realizzare**](realize.md)     | [**MCI \_ REALIZE**](mci-realize.md)     | digitalvideo            | Indica al dispositivo di selezionare e realizzare la tavolozza in un contesto di dispositivo della finestra visualizzata. |
| [**setaudio**](setaudio.md)   | [**MCI \_ SETAUDIO**](mci-setaudio.md)  | digitalvideo            | Imposta i parametri audio per il video.                                                                  |
| [**setvideo**](setvideo.md)   | [**MCI \_ SETVIDEO**](mci-setvideo.md)  | digitalvideo            | Imposta i parametri video.                                                                            |
| [**Segnale**](signal.md)       | [**SEGNALE \_ MCI**](mci-signal.md)       | digitalvideo            | Identifica una posizione specificata con un segnale.                                                    |
| [**giro**](spin.md)           | [**MCI \_ SPIN**](mci-spin.md)           | videodisc               | Avvia la rotazione del disco o arresta la rotazione del disco.                                         |
| [**Passo**](step.md)           | [**PASSAGGIO \_ MCI**](mci-step.md)           | digitalvideo, videodisc | Consente di riprodurre uno o più fotogrammi in avanti o inversa.                                             |
| [**Sbloccare**](unfreeze.md)   | [**MCI \_ UNFREEZE**](mci-unfreeze.md)   | overlay                 | Consente al buffer dei fotogrammi di acquisire dati video.                                                   |
| [**Aggiornamento**](update.md)       | [**AGGIORNAMENTO \_ MCI**](mci-update.md)       | digitalvideo            | Ridisegna il frame corrente nel contesto di dispositivo.                                               |
| [**Dove**](where.md)         | [**MCI WHERE**](mci-where.md)          | digitalvideo, overlay   | Ottiene il rettangolo che specifica l'area di origine, di destinazione o cornice.                          |
| [**Finestra**](window.md)       | [**FINESTRA \_ MCI**](mci-window.md)       | digitalvideo, overlay   | Controlla la finestra di visualizzazione.                                                                      |



 

 

 




