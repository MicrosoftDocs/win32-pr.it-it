---
title: Dispositivi e tipi di dati
description: Dispositivi e tipi di dati
ms.assetid: 46247983-19c3-4c7a-a615-ba6cd8bd3289
keywords:
- audio Waveform, apertura di dispositivi di output
- waveform-interfaccia audio, apertura di dispositivi di output
- apertura della forma d'onda-dispositivi di output audio
- audio Waveform, esecuzione di query sui dispositivi di output
- waveform-interfaccia audio, esecuzione di query sui dispositivi di output
- esecuzione di query su dispositivi di output audio
- audio Waveform, handle del dispositivo
- waveform-interfaccia audio, handle del dispositivo
- audio della forma d'onda, identificatori del dispositivo
- waveform-interfaccia audio, identificatori del dispositivo
- audio Waveform, tipi di dati di output
- waveform-interfaccia audio, tipi di dati di output
- audio Waveform, formati di dati
- waveform-interfaccia audio, formati di dati
- scrittura dei dati audio della forma d'onda
- audio Waveform, scrittura di dati
- waveform-interfaccia audio, scrittura di dati
- Forma d'onda PCM-dati audio
- audio Waveform, dati PCM
- waveform-interfaccia audio, dati PCM
- audio della forma d'onda, chiusura dei dispositivi di output
- waveform-interfaccia audio, chiusura dei dispositivi di output
- chiusura della forma d'onda-dispositivi di output audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29561a74695fb8bde950e2e75a430803a1a0351b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299762"
---
# <a name="devices-and-data-types"></a>Dispositivi e tipi di dati

Questa sezione descrive l'uso di dispositivi audio e di forme d'onda e include informazioni su come aprire, chiudere ed eseguire query su di essi per le funzionalità. Viene inoltre descritto come tenere traccia dei dispositivi in un sistema utilizzando handle di dispositivo e identificatori di dispositivo.

## <a name="opening-waveform-audio-output-devices"></a>Apertura di dispositivi di output Waveform-Audio

Usare la funzione [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) per aprire un dispositivo di output waveform-audio per la riproduzione. Questa funzione apre il dispositivo associato all'identificatore di dispositivo specificato e restituisce un handle del dispositivo aperto scrivendo l'handle di una posizione di memoria specificata.

Alcuni computer multimediali hanno più dispositivi di output dell'audio e della forma d'onda. A meno che non si voglia aprire un dispositivo di output dell'audio e della forma d'onda specifico in un sistema, è necessario usare il \_ flag di mapping di Wave per l'identificatore del dispositivo quando si apre un dispositivo. La funzione **waveOutOpen** sceglie il dispositivo nel sistema più idoneo per riprodurre il formato dati specificato.

## <a name="querying-audio-devices"></a>Esecuzione di query su dispositivi audio

Windows fornisce le funzioni seguenti per determinare il numero di dispositivi di un determinato tipo disponibili in un sistema.



| Funzione                                       | Descrizione                                                                  |
|------------------------------------------------|------------------------------------------------------------------------------|
| [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs)         | Recupera il numero di dispositivi di output ausiliari presenti nel sistema.      |
| [**waveInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs)   | Recupera il numero di dispositivi di input audio e di forma d'onda presenti nel sistema.  |
| [**waveOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs) | Recupera il numero di dispositivi di output audio e di forma d'onda presenti nel sistema. |



 

I dispositivi audio sono identificati da un identificatore di dispositivo. L'identificatore del dispositivo è determinato in modo implicito dal numero di dispositivi presenti in un sistema. Gli identificatori di dispositivo sono compresi tra zero e uno inferiore al numero di dispositivi presenti. Se, ad esempio, in un sistema sono presenti due dispositivi Waveform-Audio output, gli identificatori di dispositivo validi sono 0 e 1.

Dopo aver determinato il numero di dispositivi di un determinato tipo presenti in un sistema, è possibile usare una delle funzioni seguenti per eseguire query sulle funzionalità di ogni dispositivo.



| Funzione                                       | Descrizione                                                             |
|------------------------------------------------|-------------------------------------------------------------------------|
| [**auxGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps)         | Recupera le funzionalità di un dispositivo di output ausiliario specificato.      |
| [**waveInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps)   | Recupera le funzionalità di un dispositivo di input audio di forma d'onda specificato.  |
| [**waveOutGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetdevcaps) | Recupera le funzionalità di un dispositivo di output dell'audio e della forma d'onda specificato. |



 

Ognuna di queste funzioni riempie una struttura con informazioni sulle funzionalità di un dispositivo specifico. Nella tabella seguente sono elencate le strutture che corrispondono a ognuna di queste funzioni.



|                                                |                                    |
|------------------------------------------------|------------------------------------|
| Funzione                                       | Struttura                          |
| [**auxGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps)         | [**AUXCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-auxcaps)         |
| [**waveInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps)   | [**WAVEINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps)   |
| [**waveOutGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetdevcaps) | [**WAVEOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps) |



 

I formati standard sono elencati nel membro **dwFormats** della struttura **WAVEOUTCAPS** . Waveform-i dispositivi audio possono supportare formati non standard. Per determinare se un determinato formato (standard o non standard) è supportato da un dispositivo, è possibile chiamare la funzione [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) con il \_ flag di query del formato Wave \_ . Questo flag non apre il dispositivo. Il formato in questione viene specificato nella struttura [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) a cui punta il parametro *Pwfx* passato a **waveOutOpen**.

Waveform-i dispositivi di output audio variano nelle funzionalità supportate. Il membro **dwSupport** della struttura [**WAVEOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps) indica se un dispositivo supporta tali funzionalità come modifiche al volume e al passo.

## <a name="device-handles-and-device-identifiers"></a>Handle di dispositivo e identificatori di dispositivo

Ogni funzione che apre un dispositivo audio specifica un identificatore di dispositivo, un puntatore a una posizione di memoria e alcuni parametri univoci per ogni tipo di dispositivo. La posizione di memoria viene riempita con un handle di dispositivo. Usare questo handle di dispositivo per identificare il dispositivo audio aperto quando si chiamano altre funzioni audio.

La differenza tra gli identificatori e gli handle per i dispositivi audio è sottile ma importante:

-   Gli identificatori di dispositivo sono determinati in modo implicito dal numero di dispositivi presenti in un sistema. Questo numero viene ottenuto tramite la funzione [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs), [**waveInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs)o [**waveOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs) .
-   Gli handle di dispositivo vengono restituiti quando i driver di dispositivo vengono aperti tramite la funzione [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) o [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) .

Non sono disponibili funzioni che aprono o chiudono dispositivi audio ausiliari. Non è necessario aprire e chiudere i dispositivi audio ausiliari, come i dispositivi audio Waveform, perché non è associato alcun trasferimento dati continuo. Tutte le funzioni audio ausiliarie usano identificatori di dispositivo per identificare i dispositivi.

## <a name="waveform-audio-output-data-types"></a>Tipi di dati di output Waveform-Audio

I tipi di dati seguenti sono definiti per le funzioni di output dell'audio e della forma d'onda.



| Tipo                                 | Descrizione                                                                                                                                                   |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HWAVEOUT**                         | Handle per un dispositivo di output Open Waveform-Audio.                                                                                                               |
| [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) | Struttura che specifica i formati di dati supportati da un dispositivo di input audio e di forma d'onda particolare. Questa struttura è anche usedfor waveform-dispositivi di input audio. |
| [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)           | Struttura utilizzata come intestazione per un blocco di dati di input audio e di forma d'onda. Questa struttura viene usata anche per i dispositivi di input audio e di forma d'onda.                            |
| [**WAVEOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps)   | Struttura usata per eseguire una query sulle funzionalità di un dispositivo di output dell'audio e della forma d'onda particolare.                                                                        |



 

## <a name="specifying-waveform-audio-data-formats"></a>Specifica di Waveform-Audio formati di dati

Quando si chiama la funzione [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) per aprire un driver di dispositivo per la riproduzione o per eseguire una query su se il driver supporta un particolare formato dati, usare il parametro *pwfx* per specificare un puntatore a una struttura [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) che contiene il formato di dati waveform-audio richiesto. **WAVEFORMATEX** sostituisce le strutture [**WaveFormat**](/windows/win32/api/mmreg/ns-mmreg-waveformat) e [**PCMWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat) .

Per i dati audio suddivisi in più di due canali o con una dimensione di esempio che non è un multiplo di 8, è necessario usare [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible). Questa struttura configura semplicemente i byte aggiuntivi a cui punta il membro **cbSize** di **WAVEFORMATEX** per fornire informazioni aggiuntive sul formato. È possibile eseguire il cast di **WAVEFORMATEXTENSIBLE** come **WAVEFORMATEX**.

Sono anche disponibili due formati di appunti che è possibile usare per rappresentare i dati audio: CF \_ Wave e CF \_ riff. Usare il \_ formato Wave CF per rappresentare i dati in uno dei formati standard, ad esempio un PCM a 11 kHz o a 22 kHz. Usare il \_ formato CF riff per rappresentare formati di dati più complessi che non possono essere rappresentati come file audio con forma d'onda standard.

## <a name="writing-waveform-audio-data"></a>Scrittura di dati di Waveform-Audio

Dopo aver aperto correttamente un driver di dispositivo Waveform-Audio output, è possibile iniziare a riprodurre un suono. Windows fornisce la funzione [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) per l'invio di blocchi di dati ai dispositivi di output dell'audio e della forma d'onda.

Usare la struttura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) per specificare il blocco di dati waveform-audio che si sta inviando usando **waveOutWrite**. Questa struttura contiene un puntatore a un blocco di dati bloccato, la lunghezza del blocco di dati e alcuni flag. È necessario preparare questo blocco di dati prima di utilizzarlo; per informazioni sulla preparazione di un blocco di dati, vedere la pagina relativa ai [blocchi di dati audio](audio-data-blocks.md).

Dopo aver inviato un blocco di dati a un dispositivo di output usando **waveOutWrite**, è necessario attendere il completamento del blocco di dati da parte del driver di dispositivo prima di liberarlo. Se si inviano più blocchi di dati, è necessario monitorare il completamento dei blocchi di dati per capire quando inviare blocchi aggiuntivi. Per ulteriori informazioni sui blocchi di dati, vedere la pagina relativa ai [blocchi di dati audio](audio-data-blocks.md).

## <a name="pcm-waveform-audio-data-format"></a>Formato dati Waveform-Audio PCM

Il membro **lpData** della struttura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) pointsetts gli esempi di dati dell'audio e della forma d'onda. Per i dati PCM a 8 bit, ciascun campione è rappresentato da un singolo byte di dati senza segno. Per i dati PCM a 16 bit, ciascun campione è rappresentato da un valore con segno a 16 bit. Nella tabella seguente sono riepilogati i valori massimo, minimo e medio per i dati audio e la forma d'onda PCM.



|             |                 |                  |                |
|-------------|-----------------|------------------|----------------|
| Formato dati | Valore massimo   | Valore minimo    | Valore medio |
| PCM a 8 bit   | 255 (0xFF)      | 0                | 128 (0x80)     |
| PCM a 16 bit  | 32.767 (0x7FFF) | – 32.768 (0x8000) | 0              |



 

## <a name="pcm-data-packing"></a>Compressione dei dati PCM

L'ordine dei byte di dati varia a seconda del formato a 8 bit e a 16 bit e tra i formati mono e stereo. L'elenco seguente descrive la compressione dei dati per i diversi formati di dati di forma d'onda PCM-audio.



| Forma d'onda PCM-formato audio | Descrizione                                                                                                                                                                                                                                                                                                                                     |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| mono a 8 bit                | Ogni campione è 1 byte corrispondente a un singolo canale audio. Il campione 1 è seguito dagli esempi 2, 3, 4 e così via.                                                                                                                                                                                                                           |
| stereo a 8 bit              | Ogni campione è di 2 byte. Il campione 1 è seguito dagli esempi 2, 3, 4 e così via. Per ogni esempio, il primo byte è il canale 0 (il canale sinistro) e il secondo byte è il canale 1 (il canale destro).                                                                                                                                               |
| mono a 16 bit               | Ogni campione è di 2 byte. Il campione 1 è seguito dagli esempi 2, 3, 4 e così via. Per ogni esempio, il primo byte è il byte di ordine inferiore del canale 0 e il secondo byte è il byte di ordine superiore del canale 0.                                                                                                                                         |
| stereo a 16 bit             | Ogni campione è di 4 byte. Il campione 1 è seguito dagli esempi 2, 3, 4 e così via. Per ogni esempio, il primo byte è il byte di ordine inferiore del canale 0 (canale sinistro); il secondo byte è il byte di ordine superiore del canale 0; il terzo byte è il byte di ordine inferiore del canale 1 (canale destro); il quarto byte è il byte di ordine superiore del canale 1. |
| Altro                    | Ogni esempio è contenuto in un blocco costituito da un multiplo di 4 byte, ma è possibile che gli esempi non siano allineati a byte. La disposizione dei canali è specificata da una maschera. Per ulteriori informazioni, vedere [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible).                                                                                                 |



 

## <a name="closing-waveform-audio-output-devices"></a>Chiusura di Waveform-Audio dispositivi di output

Dopo aver completato la riproduzione dell'audio e della forma d'onda, chiamare [**waveOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose) per chiudere il dispositivo di output. Se viene chiamato **waveOutClose** mentre è in corso la riproduzione di un file audio in forma d'onda, l'operazione di chiusura non riesce e la funzione restituisce un codice di errore che indica che il dispositivo non è stato chiuso. Se non si vuole attendere la fine della riproduzione prima di chiudere il dispositivo, chiamare la funzione [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) prima di chiudere. Questa operazione termina la riproduzione e consente la chiusura del dispositivo. Assicurarsi di usare la funzione [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) per pulire la preparazione su tutti i blocchi di dati prima di chiudere il dispositivo.

 

 