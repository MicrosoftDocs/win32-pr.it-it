---
description: Con l'aumento dei dispositivi di archiviazione multimediale che richiedono formati audio compressi, le applicazioni devono identificare, descrivere e usare un'ampia gamma di nuovi contenuti audio codificati per la trasmissione di contenuto da PC a dispositivi come il ricevitore HDMI o DisplayPort.
ms.assetid: 86f3396c-b32a-4d70-9f21-e38a745f78bf
title: Rappresentazione di formati per trasmissioni IEC 61937
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0700329aafe7e7bc0e09b532c1ac29b9957ca905
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304958"
---
# <a name="representing-formats-for-iec-61937-transmissions"></a>Rappresentazione di formati per trasmissioni IEC 61937

Con l'aumento dei dispositivi di archiviazione multimediale che richiedono formati audio compressi, le applicazioni devono identificare, descrivere e usare un'ampia gamma di nuovi contenuti audio codificati per la trasmissione di contenuto da PC a dispositivi come il ricevitore HDMI o DisplayPort.

Per rappresentare un flusso audio codificato da trasmettere tramite un'interfaccia compatibile con IEC 61937, un'applicazione deve fornire:

-   Caratteristiche di un flusso audio codificato da trasmettere.

-   Caratteristiche di un flusso audio decodificato nel dispositivo di destinazione.

In Windows Vista e nei sistemi operativi Windows precedenti, un'applicazione può dedurre il livello di qualità di un formato audio dal numero di canali, le dimensioni del campione e la velocità dati di un flusso audio che usa il formato. Per un formato PCM, queste informazioni sono disponibili dai membri **nChannels**, **nSamplesPerSec** e **nAvgBytesPerSec** della struttura **WAVEFORMATEX** che specifica il formato. Per un formato non PCM, questi tre membri sono stati requisiti per archiviare le informazioni sui dati compressi nel flusso audio. Quindi, la struttura **WAVEFORMATEX** non dispone di informazioni sul numero effettivo di canali, le dimensioni del campione e la velocità dati del flusso audio non PCM dopo che il flusso è stato decompresso e riprodotto. In base alle informazioni contenute in questa struttura, un utente o un'applicazione potrebbe avere difficoltà a dedurre il livello di qualità del flusso non PCM.

Il **WAVEFORMATEX** è stato esteso alla struttura **WAVEFORMATEXTENSIBLE** per fornire le caratteristiche di flusso aggiuntive. Questa struttura non è tuttavia adatta per la descrizione del flusso per trasmissioni IEC 61937, poiché è stata progettata per rappresentare un singolo set di caratteristiche e utilizzato per dati PCM non compressi e multicanale.

In Windows 7, il sistema operativo risolve questo problema fornendo supporto per una nuova struttura, **WAVEFORMATEXTENSIBLE \_ IEC61937** , che estende la struttura **WAVEFORMATEXTENSIBLE** per archiviare due set di caratteristiche di flusso audio: il formato audio codificato prima della trasmissione e le caratteristiche del flusso audio dopo che è stato decodificato. La nuova struttura specifica in modo esplicito il numero effettivo di canali, le dimensioni del campione e la velocità dati di un formato non PCM. Con queste informazioni, un'applicazione può dedurre il livello di qualità del flusso non PCM dopo che è stato decompresso e riprodotto.

La struttura **WAVEFORMATEXTENSIBLE \_ IEC61937** è dichiarata nell'intestazione KsMedia. h inclusa in Windows 7 SDK. Il membro **FormatExt** è la struttura **WAVEFORMATEXTENSIBLE** che archivia le caratteristiche del flusso da trasmettere. Il **formato** membro della struttura **WAVEFORMATEXTENSIBLE** è la struttura **WAVEFORMATEX** . Il contenuto di **WAVEFORMATEX** e **WAVEFORMATEXTENSIBLE** indica a un'applicazione se la struttura può essere interpretata come una struttura **WAVEFORMATEXTENSIBLE \_ IEC61937** . Per una **struttura \_ IEC61937 di WAVEFORMATEXTENSIBLE** :

-   Il membro **wFormatTag** di **WAVEFORMATEX** deve contenere il \_ formato Wave \_ estendibile ( `FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE` ).

-   Il membro del **sottoformato** della struttura **WAVEFORMATEXTENSIBLE** specifica il GUID del formato codificato da trasmettere. Ad esempio, `FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL` indica il formato Dolby Digital Plus. Per i GUID supportati, vedere GUID di sottoformato.

-   Le dimensioni indicate dal membro **cbSize** di WAVEFORMATEX sono 34 byte. (`FormatExt.Format.cbSize = 34`). Le dimensioni totali di **WAVEFORMATEXTENSIBLE \_ IEC61937** sono pari a 52 byte.

I membri **dwEncodedSamplesPerSec**, **dwEncodedChannelCount** e **dwAverageBytesPerSec** di **WAVEFORMATEXTENSIBLE \_ IEC61937** descrivono la frequenza di campionamento, il numero di canali e la velocità in bit, in byte, del flusso audio dopo che è stato decodificato.

## <a name="subformat-guids"></a>GUID di sottoforma

In Windows 7, l'intestazione KsMedia. h contiene le definizioni dei GUID di sottoformato per i formati audio compressi definiti da CEA-861-D. I GUID vengono specificati nel membro subformat di **WAVEFORMATEXTENSIBLE**, specificato nel membro **FormatExt** della struttura **WAVEFORMATEXTENSIBLE \_ IEC61937** ( `WAVEFORMATEXTENSIBLE_IEC61937.FormatExt.Subformat` ).

Nella tabella seguente sono elencati i GUID per i formati audio compressi disponibili come formati audio con codifica IEC 61937 standard. Questi formati sono simili alle rappresentazioni del codice attivo esistente 3 (AC-3) e del formato DTS (Digital Theater Sound) in Windows.



| Tipo CEA 861 | GUID del sottoformato                                                                                                          | Descrizione                                  |
|--------------|-------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| 0x00         |                                                                                                                         | Fare riferimento al flusso.                         |
| 0x01         | 00000000-0000-0010-8000-00aa00389b71<br/> \_sottotipo KSDATAFORMAT \_ WAVEFORMATEX<br/>                          | PCM IEC 60958                                |
| 0x02         | 00000092-0000-0010-8000-00aa00389b71<br/> \_Sottotipo KSDATAFORMAT \_ IEC61937 \_ Dolby \_ Digital<br/>              | AC-3                                         |
| 0x03         | 00000003-0cea-0010-8000-00aa00389b71<br/> \_Sottotipo KSDATAFORMAT \_ IEC61937 \_ MPEG1<br/>                       | MPEG-1 (livello 1 & 2)                         |
| 0x04         | 00000004-0cea-0010-8000-00aa00389b71<br/> \_Sottotipo KSDATAFORMAT \_ IEC61937 \_ MPEG3<br/>                       | MPEG-3 (livello 3)                             |
| 0x05         | 00000005-0cea-0010-8000-00aa00389b71<br/> \_Sottotipo KSDATAFORMAT \_ IEC61937 \_ MPEG2 <br/>                      | MPEG-2 (multicanale)                         |
| 0x06         | 00000006-0cea-0010-8000-00aa00389b71<br/> \_Sottotipo KSDATAFORMAT \_ IEC61937 \_ AAC<br/>                         | Codifica audio avanzata (MPEG-2/4 AAC in ADTS) |
| 0x07         | 00000008-0000-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ sottotipo \_ IEC61937 \_ DTS<br/>                         | DTS                                          |
| 0x0A         | 0000000a-0cea-0010-8000-00aa00389b71<br/> \_Sottotipo KSDATAFORMAT \_ IEC61937 \_ Dolby \_ Digital \_ Plus<br/>        | Dolby Digital Plus                           |
| 0x0A         | 0000010a-0cea-0010-8000-00aa00389b71<br/> \_Sottotipo KSDATAFORMAT \_ IEC61937 \_ Dolby \_ Digital \_ Plus \_ ATMOS<br/> | Dolby Atmos codificato con Dolby Digital Plus  |
| 0x0F         |                                                                                                                         | Riservato non usato                              |



 

Nella tabella seguente sono elencati i GUID per i formati audio compressi trasmessi nei pacchetti di esempio audio ad alta velocità in bit.



| Tipo CEA 861 | GUID del sottoformato                                                                                           | Descrizione                                                                                                                     |
|--------------|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| 0x0B         | 0000000b-0cea-0010-8000-00aa00389b71<br/> \_Sottotipo KSDATAFORMAT \_ IEC61937 \_ DTS \_ HD<br/>      | DTS-HD (24 bit, 96Khz)                                                                                                          |
| 0x0c         | 0000000c-0cea-0010-8000-00aa00389b71<br/> \_Sottotipo KSDATAFORMAT \_ IEC61937 \_ Dolby \_ MLP<br/>   | Dolby MAT 1,0:<br/> Dolby TrueHD (MLP-Meridian Lossless Packing) – 192KHz a 24 bit/fino a 18 Mbps, 8 canali <br/> |
| 0x0c         | 0000010c-0cea-0010-8000-00aa00389b71<br/> \_Sottotipo KSDATAFORMAT \_ IEC61937 \_ Dolby \_ MAT20<br/> | Dolby MAT 2,0: <br/> Dolby TrueHD – 192KHz a 24 bit/fino a 18 Mbps, 8 canali o LPCM fino a 24 Mbps. <br/>           |
| 0x0c         | 0000030c-0cea-0010-8000-00aa00389b71<br/> \_Sottotipo KSDATAFORMAT \_ IEC61937 \_ Dolby \_ MAT21<br/> | Dolby MAT 2,1: <br/> Dolby TrueHD – 192KHz a 24 bit/fino a 18 Mbps, 8 canali o LPCM fino a 24 Mbps. <br/>           |
| 0x0E         | 00000164-0000-0010-8000-00aa00389b71<br/> \_Sottotipo KSDATAFORMAT \_ IEC61937 \_ WMA \_ Pro<br/>     | Windows Media Audio (WMA) Pro                                                                                                   |



 

Il driver di classe audio HD fornito da Microsoft supporta i formati PCM, AC3, DTS, AAC, Dolby Digital Plus, WMA Pro, MAT (MLP). Nella tabella seguente sono elencati i GUID per i formati audio compressi che non sono supportati dal driver della classe audio HD e possono essere implementati da soluzioni di terze parti.



| Tipo CEA 861 | GUID del sottoformato                                                                                              | Descrizione                                                                    |
|--------------|-------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| 0x08         | 00000008-0cea-0010-8000-00aa00389b71<br/> \_Sottotipo KSDATAFORMAT \_ IEC61937 \_ ATRAC<br/>           | Codifica acustica Adaptive Transform (ATRAC)                                     |
| 0x09         | 00000009-0cea-0010-8000-00aa00389b71<br/> KSDATAFORMAT \_ sottotipo \_ IEC61937 \_ One \_ bit \_ audio<br/> | Audio One-Bit                                                                  |
| 0x0D         | 0000000d-0cea-0010-8000-00aa00389b71<br/> \_Sottotipo KSDATAFORMAT \_ IEC61937 \_ DST<br/>             | Direct Stream Transport (DST): la DSD compressa Lossless (Direct Stream Digital). |



 

## <a name="dolby-digital-plus-format"></a>Formato Dolby Digital Plus

Quando il contenuto Dolby Digital Plus viene trasmesso tramite IEC 60958, la frequenza di campionamento del collegamento deve essere quattro volte la frequenza di campionamento del contenuto. Dolby Digital Plus supporta la frequenza di campionamento del contenuto di 32 KHz, 44,1 KHz e 48 KHz. Le interfacce come HDMI non supportano 128 KHz (32 KHz x 4), pertanto è possibile supportare solo le frequenze di campionamento del contenuto 44,1 e 48 KHz.

Nell'esempio seguente vengono illustrati i valori impostati da un'applicazione nella \_ struttura IEC61937 di WAVEFORMATEXTENSIBLE per rappresentare il formato Dolby Digital Plus a una frequenza di campionamento del contenuto di 48 kHz.


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

Il contenuto Dolby TrueHD viene trasmesso tramite IEC 60958 a 176,4 kHz/8 canali (che richiedono una frequenza di fotogrammi IEC 60958 pari a 705,6 kHz) per le frequenze di esempio del contenuto di 44,1, 88,2 e 176,4 kHz e 192 kHz/8 canali (che richiedono una frequenza dei fotogrammi IEC 60958 di 768 kHz) per le frequenze di esempio del contenuto di 48, 96 e 192 kHz.

Gli esempi seguenti illustrano i valori impostati da un'applicazione nella \_ struttura IEC61937 di WAVEFORMATEXTENSIBLE per rappresentare Dolby TrueHD a una frequenza di campionamento del contenuto di 96 kHz.

Dolby MAT 1,0


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



Dolby MAT 2,0


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



Dolby MAT 2,1


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
> Il supporto per una versione di Dolby MAT non implica il supporto per Dolby MAT con un numero di versione inferiore. Poiché Dolby MAT 2,1 è compatibile con le versioni precedenti di Dolby MAT, un driver di classe che indica il supporto per Dolby MAT 2,1 indicherà in genere anche il supporto per Dolby MAT 2,0 e Dolby MAT 1,0, usando una \_ struttura WAVEFORMATEXTENSIBLE IEC61937 separata per ogni versione.

 

## <a name="wma-pro"></a>WMA Pro

Il contenuto audio WMA Pro può essere codificato in uno dei quattro profili elencati nella tabella seguente.



| Profilo | Valore proprietà                                                                                                                                                                                                                                                      | Descrizione                                                                                                                         |
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| M0      | Velocità in bit massima-192000 BPS <br/> Frequenza di campionamento massima-48 KHz <br/> Numero massimo di canali-2 <br/> Dimensioni massime buffer-600 \* bit 1024 <br/> Numero massimo di campioni per fotogramma-2048 <br/> Numero massimo di bit per fotogramma-655536<br/>   | Consigliato per la musica e lo streaming in modalità radio.<br/> La velocità in bit massima in un frame audio è 1536000 bps.<br/>          |
| M1      | Velocità in bit massima-385000 BPS <br/> Frequenza di campionamento massima-48 KHz <br/> Numero massimo di canali-6 <br/> Dimensioni massime buffer-600 \* bit 1024 <br/> Numero massimo di campioni per fotogramma-4096 <br/> Numero massimo di bit per fotogramma-131072<br/>   | Consigliato per i filmati con definizione standard del suono surround.<br/> La velocità in bit massima in un frame audio è 1536000 bps.<br/> |
| M2      | Velocità in bit massima-769000 BPS <br/> Frequenza di campionamento massima-96 KHz <br/> Numero massimo di canali-6 <br/> Dimensioni massime buffer-1200 \* bit 1024 <br/> Numero massimo di campioni per fotogramma-4096 <br/> Numero massimo di bit per fotogramma-131072<br/>  | Consigliato per i filmati ad alta definizione audio surround.<br/> La frequenza massima in un frame audio è 3072000 bps.<br/>         |
| M3      | Velocità in bit massima-3 milioni BPS <br/> Frequenza di campionamento massima-96 KHz <br/> Numero massimo di canali-8 <br/> Dimensioni massime buffer-2400 \* bit 1024 <br/> Numero massimo di campioni per fotogramma-4096 <br/> Numero massimo di bit per fotogramma-131072<br/> | Consigliato per Digital Theater.<br/> La frequenza massima in un frame audio è 3072000 bps.<br/>                               |



 

I profili M0 e M1 rientrano in un flusso IEC 60958 a 48 KHz/16 bit/stereo (1536000 BPS). I profili m2 e M3 rientrano in un flusso IEC 60958 a 96 KHz/16 bit/stereo (3072000 BPS).

Nell'esempio seguente vengono illustrati i valori impostati da un'applicazione nella \_ struttura IEC61937 di WAVEFORMATEXTENSIBLE per rappresentare WMA Pro come profilo m2.


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

[Formati di dispositivo](device-formats.md)
</dt> </dl>

 

 




