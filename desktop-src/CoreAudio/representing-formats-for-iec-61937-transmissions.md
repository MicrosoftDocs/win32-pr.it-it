---
description: Con l'aumento dei dispositivi di archiviazione multimediale che richiedono formati audio compressi, le applicazioni devono identificare, descrivere e usare un'ampia gamma di nuovi contenuti audio codificati per la trasmissione di contenuto dai PC a dispositivi come HDMI o ricevitore DisplayPort.
ms.assetid: 86f3396c-b32a-4d70-9f21-e38a745f78bf
title: Rappresentazione dei formati per le trasmissioni IEC 61937
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0de8fb8910ee3534d8878cdab2c35a01f17115de477ba30ea821e89ae11b8b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018289"
---
# <a name="representing-formats-for-iec-61937-transmissions"></a>Rappresentazione dei formati per le trasmissioni IEC 61937

Con l'aumento dei dispositivi di archiviazione multimediale che richiedono formati audio compressi, le applicazioni devono identificare, descrivere e usare un'ampia gamma di nuovi contenuti audio codificati per la trasmissione di contenuto dai PC a dispositivi come HDMI o ricevitore DisplayPort.

Per rappresentare un flusso audio codificato da trasmettere tramite un'interfaccia compatibile con IEC 61937, un'applicazione deve fornire:

-   Caratteristiche di un flusso audio codificato da trasmettere.

-   Caratteristiche di un flusso audio decodificato nel dispositivo di destinazione.

In Windows Vista e nei sistemi operativi Windows precedenti un'applicazione può dedurre il livello di qualità di un formato audio dal numero di canali, dalle dimensioni del campione e dalla velocità dei dati di un flusso audio che usa il formato. Per un formato PCM, queste informazioni sono disponibili dai membri **nChannels**, **nSamplesPerSec** **e nAvgBytesPerSec** della struttura **WAVEFORMATEX** che specifica il formato. Per un formato non PCM, a questi tre membri è stato eseguito il comando di archiviare le informazioni sui dati compressi nel flusso audio. Di conseguenza, la struttura **WAVEFORMATEX** non dispone di informazioni sul numero effettivo di canali, sulle dimensioni del campione e sulla velocità dei dati del flusso audio non PCM dopo la decompressità e la riproduzione del flusso. In base alle informazioni contenute in questa struttura, un utente o un'applicazione potrebbe avere difficoltà a dedurre il livello di qualità del flusso non PCM.

**WAVEFORMATEX è** stato esteso alla **struttura WAVEFORMATEXTENSIBLE** per fornire le caratteristiche aggiuntive del flusso. Tuttavia, questa struttura non è adeguata anche per descrivere il flusso per le trasmissioni IEC 61937 perché era progettata per rappresentare un singolo set di caratteristiche e usata per i dati PCM non compressi e multicanale.

In Windows 7 il sistema operativo risolve questo problema fornendo il supporto per una nuova struttura, **WAVEFORMATEXTENSIBLE \_ IEC61937,** che estende la struttura **WAVEFORMATEXTENSIBLE** per archiviare due set di caratteristiche del flusso audio: il formato audio codificato prima della trasmissione e le caratteristiche del flusso audio dopo la decodifica. La nuova struttura specifica in modo esplicito il numero effettivo di canali, le dimensioni del campione e la velocità dei dati di un formato non PCM. Con queste informazioni, un'applicazione può dedurre il livello di qualità del flusso non PCM dopo che è stato decompresso e riprodotto.

La **struttura WAVEFORMATEXTENSIBLE \_ IEC61937** viene dichiarata nell'intestazione KsMedia.h inclusa in Windows 7 SDK. Il **membro FormatExt** è la **struttura WAVEFORMATEXTENSIBLE** che archivia le caratteristiche del flusso da trasmettere. Il **membro Format** della struttura **WAVEFORMATEXTENSIBLE** è la **struttura WAVEFORMATEX.** Il contenuto di **questa struttura WAVEFORMATEX** e **WAVEFORMATEXTENSIBLE** indica a un'applicazione se la struttura può essere interpretata come struttura **WAVEFORMATEXTENSIBLE \_ IEC61937.** Per una **struttura WAVEFORMATEXTENSIBLE \_ IEC61937:**

-   Il **membro wFormatTag** di **WAVEFORMATEX** deve contenere WAVE \_ FORMAT \_ EXTENSIBLE ( `FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE` ).

-   Il **membro SubFormat** della **struttura WAVEFORMATEXTENSIBLE** specifica il GUID del formato codificato da trasmettere. Ad esempio, `FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL` indica il formato Dolby Digital Plus. Per i GUID supportati, vedere GUID SubFormat.

-   La dimensione indicata dal **membro cbSize** di WAVEFORMATEX è di 34 byte. (`FormatExt.Format.cbSize = 34`). La dimensione totale di **WAVEFORMATEXTENSIBLE \_ IEC61937** è di 52 byte.

I membri **dwEncodedSamplesPerSec**, **dwEncodedChannelCount** e **dwAverageBytesPerSec** di **WAVEFORMATEXTENSIBLE \_ IEC61937** descrivono la frequenza di campionamento, il numero di canali e la velocità in bit del flusso audio dopo la decodifica.

## <a name="subformat-guids"></a>GUID subformat

In Windows 7 l'intestazione KsMedia.h contiene le definizioni per i GUID SubFormat per i formati audio compressi definiti da CEA-861-D. I GUID vengono specificati nel membro SubFormat di **WAVEFORMATEXTENSIBLE**, specificato nel membro **FormatExt** della struttura **WAVEFORMATEXTENSIBLE \_ IEC61937** ( `WAVEFORMATEXTENSIBLE_IEC61937.FormatExt.Subformat` ).

Nella tabella seguente sono elencati i GUID per i formati audio compressi disponibili come formati audio standard con codifica IEC 61937. Questi formati sono simili alle rappresentazioni dei formati Active Coding 3 (AC-3) e Digital Sound (DTS) esistenti in Windows.



| Tipo CEA 861 | SubFormat GUID                                                                                                          | Descrizione                                  |
|--------------|-------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| 0x00         |                                                                                                                         | Fare riferimento al flusso .                         |
| 0x01         | 00000000-0000-0010-8000-00aa00389b71<br/> SOTTOTIPO KSDATAFORMAT \_ \_ WAVEFORMATEX<br/>                          | IEC 60958 PCM                                |
| 0x02         | 00000092-0000-0010-8000-00aa00389b71<br/> SOTTOTIPO KSDATAFORMAT \_ \_ IEC61937 \_ DOLBY \_ DIGITAL<br/>              | AC-3                                         |
| 0x03         | 00000003-0cea-0010-8000-00aa00389b71<br/> SOTTOTIPO KSDATAFORMAT \_ \_ IEC61937 \_ MPEG1<br/>                       | MPEG-1 (livello 1 & 2)                         |
| 0x04         | 00000004-0cea-0010-8000-00aa00389b71<br/> SOTTOTIPO KSDATAFORMAT \_ \_ IEC61937 \_ MPEG3<br/>                       | MPEG-3 (livello 3)                             |
| 0x05         | 00000005-0cea-0010-8000-00aa00389b71<br/> SOTTOTIPO KSDATAFORMAT \_ \_ IEC61937 \_ MPEG2 <br/>                      | MPEG-2 (multicanale)                         |
| 0x06         | 00000006-0cea-0010-8000-00aa00389b71<br/> SOTTOTIPO KSDATAFORMAT \_ \_ IEC61937 \_ AAC<br/>                         | Codifica audio avanzata (MPEG-2/4 AAC in ADTS) |
| 0x07         | 00000008-0000-0010-8000-00aa00389b71<br/> SOTTOTIPO KSDATAFORMAT \_ \_ IEC61937 \_ DTS<br/>                         | DTS                                          |
| 0x0a         | 0000000a-0cea-0010-8000-00aa00389b71<br/> SOTTOTIPO KSDATAFORMAT \_ \_ IEC61937 \_ DOLBY \_ DIGITAL \_ PLUS<br/>        | Dolby Digital Plus                           |
| 0x0a         | 0000010a-0cea-0010-8000-00aa00389b71<br/> SOTTOTIPO KSDATAFORMAT \_ \_ IEC61937 \_ DOLBY \_ DIGITAL PLUS \_ \_ ATMOS<br/> | Dolby Atmos codificato con Dolby Digital Plus  |
| 0x0b         | 0000000b-0cea-0010-8000-00aa00389b71<br/> SOTTOTIPO KSDATAFORMAT \_ \_ IEC61937 \_ DTS \_ HD<br/> | DTS HD  |
| 0x0b         | 0000010b-0cea-0010-8000-00aa00389b71<br/> SOTTOTIPO KSDATAFORMAT \_ \_ IEC61937 \_ DTSX \_ E1<br/> | DTS:X E1  |
| 0x0b         | 0000030b-0cea-0010-8000-00aa00389b71<br/> SOTTOTIPO KSDATAFORMAT \_ \_ IEC61937 \_ DTSX \_ E2<br/> | DTS:X E2  |
| 0x0f         |                                                                                                                         | Riservato non usato                              |



 

Nella tabella seguente sono elencati i GUID per i formati audio compressi trasmessi in pacchetti di esempio audio a velocità in bit elevata.



| Tipo CEA 861 | SubFormat GUID                                                                                           | Descrizione                                                                                                                     |
|--------------|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| 0x0b         | 0000000b-0cea-0010-8000-00aa00389b71<br/> SOTTOTIPO KSDATAFORMAT \_ \_ IEC61937 \_ DTS \_ HD<br/>      | DTS-HD (24 bit, 96Khz)                                                                                                          |
| 0x0c         | 0000000c-0cea-0010-8000-00aa00389b71<br/> SOTTOTIPO KSDATAFORMAT \_ \_ IEC61937 \_ DOLBY \_ MLP<br/>   | Dolby MAT 1.0:<br/> Dolby TrueHD (MLP - Meridian Lossless Packing) - 24 bit 192KHz/fino a 18 Mbps, 8 canali) <br/> |
| 0x0c         | 0000010c-0cea-0010-8000-00aa00389b71<br/> SOTTOTIPO KSDATAFORMAT \_ \_ IEC61937 \_ DOLBY \_ MAT20<br/> | Dolby MAT 2.0: <br/> Dolby TrueHD: 24 bit a 192 KHz/fino a 18 Mbps, 8 canali o LPCM fino a 24 Mbps. <br/>           |
| 0x0c         | 0000030c-0cea-0010-8000-00aa00389b71<br/> SOTTOTIPO KSDATAFORMAT \_ \_ IEC61937 \_ DOLBY \_ MAT21<br/> | Dolby MAT 2.1: <br/> Dolby TrueHD: 24 bit a 192 KHz/fino a 18 Mbps, 8 canali o LPCM fino a 24 Mbps. <br/>           |
| 0x0e         | 00000164-0000-0010-8000-00aa00389b71<br/> SOTTOTIPO KSDATAFORMAT \_ \_ IEC61937 \_ WMA \_ PRO<br/>     | Windows Audio multimediale (WMA) Pro                                                                                                   |



 

Il driver di classe HD Audio fornito da Microsoft supporta i formati PCM, AC3, DTS, AAC, Dolby Digital Plus, WMA Pro, MAT(MLP). Nella tabella seguente sono elencati i GUID per i formati audio compressi non supportati dal driver della classe audio HD e che possono essere implementati da soluzioni di terze parti.



| Tipo CEA 861 | SubFormat GUID                                                                                              | Descrizione                                                                    |
|--------------|-------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| 0x08         | 00000008-0cea-0010-8000-00aa00389b71<br/> SOTTOTIPO KSDATAFORMAT \_ \_ IEC61937 \_ ATRAC<br/>           | Codifica acustica di trasformazione adattiva (ATRAC)                                     |
| 0x09         | 00000009-0cea-0010-8000-00aa00389b71<br/> SOTTOTIPO KSDATAFORMAT \_ \_ IEC61937 \_ AUDIO A UN \_ \_ BIT<br/> | One-Bit audio                                                                  |
| 0x0d         | 0000000d-0cea-0010-8000-00aa00389b71<br/> SOTTOTIPO KSDATAFORMAT \_ \_ IEC61937 \_ DST<br/>             | Direct Stream Transport (DST): DSD compresso senza perdita (Direct Stream Digital). |



 

## <a name="dolby-digital-plus-format"></a>Dolby Digital Plus Format

Quando il contenuto Dolby Digital Plus viene trasmesso tramite IEC 60958, la frequenza di campionamento dei collegamenti deve essere quattro volte superiore alla frequenza di campionamento del contenuto. Dolby Digital Plus supporta frequenze di campionamento del contenuto di 32 KHz, 44,1 KHz e 48 KHz. Le interfacce come HDMI non supportano 128 KHz (32 KHz x 4), pertanto è possibile supportare solo frequenze di campionamento del contenuto a 44,1 e 48 KHz.

I valori impostati da un'applicazione nella struttura WAVEFORMATEXTENSIBLE IEC61937 per rappresentare il formato Dolby Digital Plus con una frequenza di campionamento del contenuto di \_ 48 KHz sono illustrati nell'esempio seguente.


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 2;              // One IEC 60958 Line.
wfext.FormatExt.Format.nSamplesPerSec = 192000;    // Link runs at 192 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 768000;   // 192 KHz * 4.
wfext.FormatExt.Format.nBlockAlign = 4;            // 16 bits * 2 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;        // Always at 16 bits over IEC 60958.
wfext.FormatExt.Format.cbSize = 34;                // Indicates that Format is part of a 
                                                   // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_5POINT1;    // Dolby 5.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL_PLUS;
wfext.dwEncodedSamplesPerSec = 48000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 6;                            // Encoded data contains 6 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



## <a name="dolby-truehd-mat"></a>Dolby TrueHD (MAT)

Il contenuto Dolby TrueHD viene trasmesso tramite IEC 60958 a 176,4 kHz/8 canali (che richiedono una frequenza fotogrammi IEC 60958 di 705,6 kHz) per frequenze di campionamento del contenuto di 44,1, 88,2 e 176,4 kHz e 192 kHz/8 canali (che richiedono una frequenza fotogrammi IEC 60958 di 768 kHz) per frequenze di campionamento del contenuto di 48, 96 e 192 kHz.

I valori impostati da un'applicazione nella struttura WAVEFORMATEXTENSIBLE \_ IEC61937 per rappresentare Dolby TrueHD a una frequenza di campionamento del contenuto di 96 KHz sono illustrati negli esempi seguenti.

Dolby MAT 1.0


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 8;                // Four IEC 60958 Lines.
wfext.FormatExt.Format.nSamplesPerSec = 192000;      // Link runs at 192 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 3072000;    // 192 KHz * 16.
wfext.FormatExt.Format.nBlockAlign = 16;             // 16-bits * 8 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;          // Always at 16 bits over IEC 60958.
wfext.FormatExt.Format.cbSize = 34;                  // Indicates that Format is part of a 
                                                     // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_7POINT1;    // Dolby 7.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_MLP; // This structure indicates MLP (MAT 1.0) support.
wfext.dwEncodedSamplesPerSec = 96000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 8;                            // Encoded data contains 8 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



Dolby MAT 2.0


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 8;                // Four IEC 60958 Lines.
wfext.FormatExt.Format.nSamplesPerSec = 192000;      // Link runs at 192 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 3072000;    // 192 KHz * 16.
wfext.FormatExt.Format.nBlockAlign = 16;             // 16-bits * 8 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;          // Always at 16 bits over IEC 60958.
wfext.FormatExt.Format.cbSize = 34;                  // Indicates that Format is part of a 
                                                     // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_7POINT1;    // Dolby 7.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_MAT20; // This structure indicates MAT 2.0 support.
wfext.dwEncodedSamplesPerSec = 96000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 8;                            // Encoded data contains 8 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



Dolby MAT 2.1


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 8;                // Four IEC 60958 Lines.
wfext.FormatExt.Format.nSamplesPerSec = 192000;      // Link runs at 192 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 3072000;    // 192 KHz * 16.
wfext.FormatExt.Format.nBlockAlign = 16;             // 16-bits * 8 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;          // Always at 16 bits over IEC 60958.
wfext.FormatExt.Format.cbSize = 34;                  // Indicates that Format is part of a 
                                                     // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_7POINT1;    // Dolby 7.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_MAT21; // This structure indicates MAT 2.1 support.
wfext.dwEncodedSamplesPerSec = 96000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 8;                            // Encoded data contains 8 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



> [!Note]  
> Il supporto per una versione di Dolby MAT non implica il supporto per Dolby MAT con un numero di versione inferiore. Poiché Dolby MAT 2.1 è compatibile con le versioni precedenti di Dolby MAT, un driver di classe che indica il supporto per Dolby MAT 2.1 indicherà in genere anche il supporto per Dolby MAT 2.0 e Dolby MAT 1.0, usando una struttura IEC61937 WAVEFORMATEXTENSIBLE separata per ogni \_ versione.

 

## <a name="wma-pro"></a>WMA Pro

I Pro audio WMA possono essere codificati in uno dei quattro profili elencati nella tabella seguente.



| Profilo | Proprietà - Valore                                                                                                                                                                                                                                                      | Descrizione                                                                                                                         |
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| M0      | Velocità in bit massima : 192000 bps <br/> Frequenza di campionamento massima : 48 KHz <br/> Numero massimo di canali : 2 <br/> Dimensioni massime del buffer : 600 \* 1024 bit <br/> Numero massimo di campioni per frame - 2048 <br/> Numero massimo di bit per frame - 655536<br/>   | Consigliato per la musica e lo streaming over-the-air.<br/> La velocità in bit massima in un fotogramma audio è 1536000 bps.<br/>          |
| M1      | Velocità in bit massima : 385000 bps <br/> Frequenza di campionamento massima : 48 KHz <br/> Numero massimo di canali : 6 <br/> Dimensioni massime del buffer : 600 \* 1024 bit <br/> Numero massimo di campioni per frame - 4096 <br/> Numero massimo di bit per frame - 131072<br/>   | Consigliato per i film con definizione standard surround.<br/> La velocità in bit massima in un fotogramma audio è 1536000 bps.<br/> |
| M2      | Velocità in bit massima : 769000 bps <br/> Frequenza di campionamento massima : 96 KHz <br/> Numero massimo di canali : 6 <br/> Dimensioni massime del buffer : 1200 \* 1024 bit <br/> Numero massimo di campioni per frame - 4096 <br/> Numero massimo di bit per frame - 131072<br/>  | Consigliato per i film in alta definizione con audio surround.<br/> La frequenza massima in un fotogramma audio è 3072000 bps.<br/>         |
| M3      | Velocità in bit massima : 3000000 bps <br/> Frequenza di campionamento massima : 96 KHz <br/> Numero massimo di canali : 8 <br/> Dimensioni massime del buffer : 2400 \* 1024 bit <br/> Numero massimo di campioni per frame - 4096 <br/> Numero massimo di bit per frame - 131072<br/> | Consigliato per il digital theater.<br/> La frequenza massima in un fotogramma audio è 3072000 bps.<br/>                               |



 

I profili M0 e M1 rientrano in un flusso IEC 60958 a 48 KHz/16 bit/Stereo (1536000 bps). I profili M2 e M3 rientrano in un flusso IEC 60958 a 96 KHz/16 bit/Stereo (3072000 bps).

I valori impostati da un'applicazione nella struttura WAVEFORMATEXTENSIBLE IEC61937 per rappresentare il Pro WMA come profilo M2 sono illustrati \_ nell'esempio seguente.


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 2;             // One IEC 60958 Line.
wfext.FormatExt.Format.nSamplesPerSec = 96000;    // Link runs at 96 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 384000;  // 96 KHz * 4.
wfext.FormatExt.Format.nBlockAlign = 4;           // 16 bits * 8 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;       // Always at 16 bits over link.
wfext.FormatExt.Format.cbSize = 34;               // Indicates that Format is part of a 
                                                  // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_5POINT1;    // 5.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_WMA_PRO;
wfext.dwEncodedSamplesPerSec = 96000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 6;                            // Encoded data contains 6 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Formati dei dispositivi](device-formats.md)
</dt> </dl>

 

 




