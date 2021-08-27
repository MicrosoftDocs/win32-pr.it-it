---
title: Dispositivi e tipi di dati
description: Dispositivi e tipi di dati
ms.assetid: 46247983-19c3-4c7a-a615-ba6cd8bd3289
keywords:
- audio waveform, apertura di dispositivi di output
- interfaccia waveform-audio, apertura di dispositivi di output
- apertura di dispositivi di output audio waveform
- audio waveform, esecuzione di query su dispositivi di output
- interfaccia waveform-audio, esecuzione di query sui dispositivi di output
- esecuzione di query su dispositivi di output audio-waveform
- audio waveform, handle del dispositivo
- interfaccia waveform-audio, handle di dispositivo
- audio waveform, identificatori di dispositivo
- interfaccia audio waveform, identificatori di dispositivo
- audio waveform, tipi di dati di output
- interfaccia waveform-audio, tipi di dati di output
- audio waveform, formati di dati
- interfaccia waveform-audio, formati di dati
- scrittura di dati audio waveform
- audio waveform, scrittura di dati
- interfaccia audio waveform, scrittura di dati
- Dati audio waveform PCM
- audio waveform, dati PCM
- interfaccia audio waveform,dati PCM
- audio waveform, chiusura di dispositivi di output
- interfaccia waveform-audio, chiusura di dispositivi di output
- chiusura di dispositivi di output audio-forma d'onda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 165f740e260c4e1a25fbd40cac9b8efd66ccd401c3e166dd1119b92c7b9999f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118941269"
---
# <a name="devices-and-data-types"></a>Dispositivi e tipi di dati

Questa sezione descrive l'uso dei dispositivi audio waveform e include informazioni su come aprirli, chiuderli ed eseguire query per le relative funzionalità. Descrive anche come tenere traccia dei dispositivi in un sistema usando handle di dispositivo e identificatori di dispositivo.

## <a name="opening-waveform-audio-output-devices"></a>Apertura Waveform-Audio di output

Usare la [**funzione waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) per aprire un dispositivo di output audio-forma d'onda per la riproduzione. Questa funzione apre il dispositivo associato all'identificatore di dispositivo specificato e restituisce un handle del dispositivo aperto scrivendo l'handle di un percorso di memoria specificato.

Alcuni computer multimediali hanno più dispositivi di output audio waveform. A meno che non si voglia aprire un dispositivo di output audio-forma d'onda specifico in un sistema, è necessario usare il flag WAVE MAPPER per l'identificatore di dispositivo quando si \_ apre un dispositivo. La **funzione waveOutOpen** sceglie il dispositivo nel sistema in grado di riprodurre al meglio il formato dati specificato.

## <a name="querying-audio-devices"></a>Esecuzione di query su dispositivi audio

Windows fornisce le funzioni seguenti per determinare il numero di dispositivi di un determinato tipo disponibili in un sistema.



| Funzione                                       | Descrizione                                                                  |
|------------------------------------------------|------------------------------------------------------------------------------|
| [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs)         | Recupera il numero di dispositivi di output ausiliari presenti nel sistema.      |
| [**waveInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs)   | Recupera il numero di dispositivi di input audio-forma d'onda presenti nel sistema.  |
| [**waveOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs) | Recupera il numero di dispositivi di output audio-waveform presenti nel sistema. |



 

I dispositivi audio sono identificati da un identificatore di dispositivo. L'identificatore del dispositivo viene determinato in modo implicito dal numero di dispositivi presenti in un sistema. Gli identificatori dei dispositivi sono da zero a uno in meno rispetto al numero di dispositivi presenti. Ad esempio, se sono presenti due dispositivi di output audio-waveform in un sistema, gli identificatori di dispositivo validi sono 0 e 1.

Dopo aver determinato il numero di dispositivi di un determinato tipo presenti in un sistema, è possibile usare una delle funzioni seguenti per eseguire query sulle funzionalità di ogni dispositivo.



| Funzione                                       | Descrizione                                                             |
|------------------------------------------------|-------------------------------------------------------------------------|
| [**auxGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps)         | Recupera le funzionalità di un dispositivo di output ausiliario specificato.      |
| [**waveInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps)   | Recupera le funzionalità di un dispositivo di input audio-forma d'onda specificato.  |
| [**waveOutGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetdevcaps) | Recupera le funzionalità di un dispositivo di output audio-forma d'onda specificato. |



 

Ognuna di queste funzioni riempie una struttura con informazioni sulle funzionalità di un dispositivo specificato. Nella tabella seguente sono elencate le strutture che corrispondono a ognuna di queste funzioni.



|  Funzione                                              |  Struttura                                  |
|------------------------------------------------|------------------------------------|
| [**auxGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps)         | [**AUXCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-auxcaps)         |
| [**waveInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps)   | [**WAVEINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps)   |
| [**waveOutGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetdevcaps) | [**WAVEOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps) |



 

I formati standard sono **elencati nel membro dwFormats** della **struttura WAVEOUTCAPS.** I dispositivi audio Waveform possono supportare formati non standard. Per determinare se un particolare formato (standard o non standard) è supportato da un dispositivo, è possibile chiamare la funzione [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) con il flag WAVE \_ FORMAT \_ QUERY. Questo flag non apre il dispositivo. Specificare il formato in questione nella struttura [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) a cui punta il *parametro pwfx* passato **a waveOutOpen.**

I dispositivi di output audio waveform variano in base alle funzionalità supportate. Il **membro dwSupport** della struttura [**WAVEOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps) indica se un dispositivo supporta funzionalità come le modifiche al volume e al passo.

## <a name="device-handles-and-device-identifiers"></a>Handle di dispositivo e identificatori di dispositivo

Ogni funzione che apre un dispositivo audio specifica un identificatore di dispositivo, un puntatore a una posizione di memoria e alcuni parametri univoci per ogni tipo di dispositivo. La posizione di memoria viene riempita con un handle di dispositivo. Usare questo handle di dispositivo per identificare il dispositivo audio aperto quando si chiamano altre funzioni audio.

La differenza tra identificatori e handle per i dispositivi audio è sottile ma importante:

-   Gli identificatori di dispositivo vengono determinati in modo implicito dal numero di dispositivi presenti in un sistema. Questo numero viene ottenuto usando la [**funzione auxGetNumDevs,**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs) [**waveInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs)o [**waveOutGetNumDevs.**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs)
-   Gli handle di dispositivo vengono restituiti quando i driver di dispositivo vengono aperti tramite la [**funzione waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) o [**waveOutOpen.**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen)

Non sono disponibili funzioni che aprono o chiudono i dispositivi audio ausiliari. I dispositivi audio ausiliari non devono essere aperti e chiusi come dispositivi audio waveform perché non è associato alcun trasferimento dati continuo. Tutte le funzioni audio ausiliarie usano gli identificatori di dispositivo per identificare i dispositivi.

## <a name="waveform-audio-output-data-types"></a>Waveform-Audio di dati di output

Per le funzioni di output audio-waveform vengono definiti i tipi di dati seguenti.



| Tipo                                 | Descrizione                                                                                                                                                   |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HWAVEOUT**                         | Handle per un dispositivo di output audio waveform aperto.                                                                                                               |
| [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) | Struttura che specifica i formati di dati supportati da un particolare dispositivo di input audio-forma d'onda. Questa struttura viene usata anche per i dispositivi di input audio-forma d'onda. |
| [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)           | Struttura utilizzata come intestazione per un blocco di dati di input audio-forma d'onda. Questa struttura viene usata anche per i dispositivi di input audio-forma d'onda.                            |
| [**WAVEOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps)   | Struttura usata per eseguire query sulle funzionalità di un particolare dispositivo di output audio-forma d'onda.                                                                        |



 

## <a name="specifying-waveform-audio-data-formats"></a>Specifica di Waveform-Audio dati personalizzati

Quando si chiama la funzione [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) per aprire un driver di dispositivo per la riproduzione o per verificare se il driver supporta un formato dati specifico, usare il *parametro pwfx* per specificare un puntatore a [**una struttura WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) contenente il formato dati waveform-audio richiesto. **WAVEFORMATEX** sostituisce le [**strutture WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) e [**PCMWAVEFORMAT.**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat)

Per i dati audio separati in più di due canali o con una dimensione di campionamento diversa da un multiplo di 8, è consigliabile usare [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible). Questa struttura configura semplicemente i byte aggiuntivi a cui punta il membro **cbSize** di **WAVEFORMATEX** per fornire informazioni aggiuntive sul formato. È possibile eseguire il cast di **WAVEFORMATEXTENSIBLE** come **WAVEFORMATEX**.

Esistono anche due formati di Appunti che è possibile usare per rappresentare i dati audio: CF \_ WAVE e CF \_ RIFF. Usare il formato CF WAVE per rappresentare i dati in uno dei formati standard, ad esempio \_ PCM a 11 kHz o 22 kHz. Usare il formato CF RIFF per rappresentare formati di dati più complessi che \_ non possono essere rappresentati come file audio con forma d'onda standard.

## <a name="writing-waveform-audio-data"></a>Scrittura Waveform-Audio dati

Dopo aver aperto correttamente un driver di dispositivo di output waveform-audio, è possibile iniziare a riprodurre un suono. Windows fornisce la [**funzione waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) per l'invio di blocchi di dati ai dispositivi di output waveform-audio.

Usare la [**struttura WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) per specificare il blocco di dati waveform-audio che si sta inviando usando **waveOutWrite**. Questa struttura contiene un puntatore a un blocco di dati bloccato, la lunghezza del blocco di dati e alcuni flag. Questo blocco di dati deve essere preparato prima di usarlo. Per informazioni sulla preparazione di un blocco di dati, vedere [Blocchi di dati audio](audio-data-blocks.md).

Dopo aver inviato un blocco di dati a un dispositivo di output usando **waveOutWrite,** è necessario attendere il completamento del driver di dispositivo con il blocco di dati prima di liberarlo. Se si inviano più blocchi di dati, è necessario monitorare il completamento dei blocchi di dati per sapere quando inviare blocchi aggiuntivi. Per altre informazioni sui blocchi di dati, vedere [Blocchi di dati audio](audio-data-blocks.md).

## <a name="pcm-waveform-audio-data-format"></a>Formato dati Waveform-Audio PCM

Il **membro lpData** della struttura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) punta agli esempi di dati waveform-audio. Per i dati PCM a 8 bit, ogni campione è rappresentato da un singolo byte di dati senza segno. Per i dati PCM a 16 bit, ogni esempio è rappresentato da un valore con segno a 16 bit. La tabella seguente riepiloga i valori massimo, minimo e medio per i dati audio della forma d'onda PCM.



| Formato dati | Valore massimo   | Valore minimo    | Valore del punto medio |
|-------------|-----------------|------------------|----------------|
| PCM a 8 bit   | 255 (0xFF)      | 0                | 128 (0x80)     |
| PCM a 16 bit  | 32.767 (0x7FFF) | –32.768 (0x8000) | 0              |



 

## <a name="pcm-data-packing"></a>Pacchetto di dati PCM

L'ordine dei byte di dati varia tra i formati a 8 bit e a 16 bit e tra i formati mono e stereo. L'elenco seguente descrive la creazione di un pacchetto di dati per i diversi formati di dati audio-forma d'onda PCM.



| Formato waveform-audio PCM | Descrizione                                                                                                                                                                                                                                                                                                                                     |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mono a 8 bit                | Ogni campione è di 1 byte che corrisponde a un singolo canale audio. L'esempio 1 è seguito dagli esempi 2, 3, 4 e così via.                                                                                                                                                                                                                           |
| Stereo a 8 bit              | Ogni esempio è di 2 byte. L'esempio 1 è seguito dagli esempi 2, 3, 4 e così via. Per ogni esempio, il primo byte è il canale 0 (canale sinistro) e il secondo byte è il canale 1 (canale destro).                                                                                                                                               |
| Mono a 16 bit               | Ogni esempio è di 2 byte. L'esempio 1 è seguito dagli esempi 2, 3, 4 e così via. Per ogni esempio, il primo byte è il byte di ordine basso del canale 0 e il secondo è il byte di ordine superiore del canale 0.                                                                                                                                         |
| Stereo a 16 bit             | Ogni esempio è di 4 byte. L'esempio 1 è seguito dagli esempi 2, 3, 4 e così via. Per ogni esempio, il primo byte è il byte di ordine inferiore del canale 0 (canale sinistro); il secondo byte è il byte di ordine superiore del canale 0. il terzo byte è il byte di ordine inferiore del canale 1 (canale destro); e il quarto byte è il byte di ordine superiore del canale 1. |
| Altro                    | Ogni esempio è contenuto in un blocco che è un multiplo di 4 byte, ma gli esempi possono essere non allineati a byte. La disposizione dei canali viene specificata da una maschera. Per altre informazioni, vedere [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible).                                                                                                 |



 

## <a name="closing-waveform-audio-output-devices"></a>Chiusura Waveform-Audio dispositivi di output

Al termine della riproduzione waveform-audio, chiamare [**waveOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose) per chiudere il dispositivo di output. Se **waveOutClose viene** chiamato durante la riproduzione di un file waveform-audio, l'operazione di chiusura ha esito negativo e la funzione restituisce un codice di errore che indica che il dispositivo non è stato chiuso. Se non si vuole attendere la fine della riproduzione prima di chiudere il dispositivo, chiamare la [**funzione waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) prima della chiusura. La riproduzione termina e consente la chiusura del dispositivo. Assicurarsi di usare la [**funzione waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) per pulire la preparazione in tutti i blocchi di dati prima di chiudere il dispositivo.

 

 