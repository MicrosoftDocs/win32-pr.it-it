---
description: Le tabelle seguenti elencano i GUID del sottotipo di supporto per l'audio. Ove applicabile, ogni tabella elenca il tag di formato equivalente, dichiarato in mmreg. h.
ms.assetid: 55012be5-2d61-4d38-aab7-0c42f161f555
title: Sottotipi audio
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82b9ccbe83a20f23976e506124c674119eee3a96
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481573"
---
# <a name="audio-subtypes"></a>Sottotipi audio

Le tabelle seguenti elencano i GUID del sottotipo di supporto per l'audio. Ove applicabile, ogni tabella elenca il tag di formato equivalente, dichiarato in mmreg. h.

## <a name="uncompressed-audio-types"></a>Tipi audio non compressi



| GUID                          | Descrizione                | Intestazione  | Tag di formato equivalente                  |
|-------------------------------|----------------------------|---------|----------------------------------------|
| **MEDIASUBTYPE \_ IEEE \_ float** | Audio a virgola mobile IEEE. | UUIDs. h | **Wave \_ FORMATO \_ IEEE \_ float** (0x0003) |
| **\_PCM MEDIASUBTYPE**         | Audio PCM.                 | UUIDs. h | **Wave \_ FORMATO \_ PCM** (0x0001)         |



 

## <a name="mpeg-4-and-aac-audio-types"></a>Tipi audio MPEG-4 e AAC



| GUID                              | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               | Intestazione       | Tag di formato equivalente                      |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|--------------------------------------------|
| **MEDIASUBTYPE \_ MPEG \_ ADTS \_ AAC** | Audio AAC (Advanced Audio Coding) nel formato ADTS (Audio Data Transport Stream).<br/> Il blocco di formato è una struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) con **wFormatTag** uguale **al \_ formato Wave \_ MPEG \_ ADTS \_ AAC**.<br/> La struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) specifica la frequenza di campionamento AAC-LC di base e il numero di canali, prima di applicare gli strumenti di replica a banda spettrale (SBR) o parametrico stereo (PS), se presenti.<br/> Non sono necessari dati aggiuntivi dopo la struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .<br/>                                                                                                                                                                 | wmcodecdsp. h | **Wave \_ FORMATTARE \_ MPEG \_ ADTS \_ AAC** (0x1600) |
| **MEDIASUBTYPE \_ MPEG \_ HEAAC**     | High-Efficiency flusso di codifica audio avanzato (HE-AAC).<br/> Il blocco di formato è una struttura [**HEAACWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-heaacwaveformat) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | wmcodecdsp. h | **Wave \_ FORMATTARE \_ MPEG \_ HEAAC** (0x1610)     |
| **MEDIASUBTYPE \_ MPEG \_ LOAS**      | Flusso di trasporto audio MPEG-4 con un livello di sincronizzazione (LOAS) e un livello multiplex (LATM).<br/> Il blocco di formato è una struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) con **wFormatTag** uguale **al \_ formato Wave \_ MPEG \_ LOAS**.<br/> La struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) specifica la frequenza di campionamento AAC-LC di base e il numero di canali, prima di applicare gli strumenti SBR o PS spettrale, se presenti.<br/> Non sono necessari dati aggiuntivi dopo la struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .<br/>                                                                                                                                                                                             | wmcodecdsp. h | **Wave \_ FORMATTARE \_ MPEG \_ LOAS** (0x1602)      |
| **MEDIASUBTYPE \_ RAW \_ AAC1**       | AAC non elaborato.<br/> Il blocco di formato è una struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) con **wFormatTag** uguale **al \_ formato Wave \_ RAW \_ AAC1**.<br/> La struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) specifica la frequenza di campionamento e il numero di canali nell'audio decodificato dopo l'applicazione degli strumenti SBR e PS, se presenti.<br/> La struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) è seguita da byte aggiuntivi che contengono i dati di AudioSpecificConfig (), come definito da ISO/IEC 14496-3 (audio MPEG-4). <br/> La lunghezza dei dati di AudioSpecificConfig () è di 2 byte per AAC-LC o HE-AAC con segnalazione implicita di SBR/PS. È più di 2 byte per HE-AAC con segnalazione esplicita di SBR/PS.<br/> | wmcodecdps. h | **Wave \_ FORMATO \_ RAW \_ AAC1** (0x00FF)       |



 

## <a name="dolby-audio-types"></a>Tipi audio Dolby



| GUID                                | Descrizione                                                                                                                                                                                                             | Intestazione       | Tag di formato equivalente                        |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|----------------------------------------------|
| **MEDIASUBTYPE \_ Dolby \_ DDPLUS**     | Audio Dolby Digital Plus.                                                                                                                                                                                               | wmcodecdsp. h | n/d                                          |
| **MEDIASUBTYPE \_ Dolby \_ AC3**        | Audio Dolby Digital (AC-3).                                                                                                                                                                                             | ksuuids. h    | n/d                                          |
| **MEDIASUBTYPE \_ Dolby \_ AC3 \_ SPDIF** | Dolby AC-3 su S/PDIF.                                                                                                                                                                                                 | UUIDs. h      | **Wave \_ FORMATO \_ Dolby \_ AC3 \_ SPDIF** (0x0092) |
| **\_DVM MEDIASUBTYPE**               | Codec DVM AC-3. Usato per la riproduzione di file AVI con audio Dolby Digital.<br/> Il blocco di formato è una struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) con il tag di formato uguale al **\_ formato Wave \_ DVM**.<br/> | wmcodecdsp. h | **Wave \_ FORMATO \_ DVM** (0x2000)               |
| **MEDIASUBTYPE \_ RAW \_ sport**        | AC-3 su S/PDIF; vedere la sezione Osservazioni.                                                                                                                                                                                          | UUIDs. h      | **Wave \_ FORMATO \_ RAW \_ sport** (0x0240)        |
| **\_ \_ 241h Tag SPDIF \_ MEDIASUBTYPE**  | AC-3 su S/PDIF; vedere la sezione Osservazioni.                                                                                                                                                                                          | UUIDs. h      | **Wave \_ FORMATO \_ ESST \_ AC3** (0x0241)         |



 

Per specificare AC-3 imbottito, usare il sottotipo **MEDIASUBTYPE \_ Dolby \_ AC3 \_ SPDIF**, che corrisponde a un tag format di 0x0092 (Wave \_ Format \_ Dolby \_ AC3 \_ SPDIF). I valori 0x240 e 0x241 sono stati usati anche per indicare un AC-3 imbottito, ma Microsoft incoraggia l'uso di 0x0092.

## <a name="miscellaneous-audio-types"></a>Tipi audio vari



| GUID                                | Descrizione                                                                                                                                                                                                                                                                          | Intestazione       | Tag di formato equivalente           |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|---------------------------------|
| **\_Audio DRM \_ MEDIASUBTYPE**        | Audio con protezione Digital Rights Management (DRM).                                                                                                                                                                                                                               | UUIDs. h      | **Wave \_ FORMATO \_ DRM** (ad esempio 0x0009)  |
| **\_DTS MEDIASUBTYPE**               | Audio di Digital Theater Systems (DTS).<br/> Il blocco di formato è una struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) con il tag di formato uguale al **\_ formato Wave \_ Unknown**.<br/>                                                                                              | ksuuids. h    | n/d                             |
| **\_DTS2 MEDIASUBTYPE**              | Audio di Digital Theater Systems (DTS).<br/> Il blocco di formato è una struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) con il tag di formato uguale al **\_ formato Wave \_ DTS2**.<br/> Questo sottotipo è equivalente a **MEDIASUBTYPE \_ DTS** ma usa un tag di formato diverso.<br/> | wmcodecdsp. h | **Wave \_ FORMATO \_ DTS2** (0x2001) |
| **\_audio MEDIASUBTYPE DVD \_ LPCM \_**  | Dati audio DVD.                                                                                                                                                                                                                                                                      | ksuuids. h    | n/d                             |
| **\_MPEG1AUDIOPAYLOAD MEDIASUBTYPE** | Payload audio MPEG-1.                                                                                                                                                                                                                                                                | UUIDs. h      | **Wave \_ FORMATO \_ MPEG** (0x0050) |
| **\_MPEG1PACKET MEDIASUBTYPE**       | Pacchetto audio MPEG1.                                                                                                                                                                                                                                                                  | UUIDs. h      | n/d                             |
| **\_MPEG1PAYLOAD MEDIASUBTYPE**      | Payload audio MPEG1.                                                                                                                                                                                                                                                                 | UUIDs. h      | n/d                             |
| **\_Audio MPEG2 \_ MEDIASUBTYPE**      | Dati audio MPEG-2.                                                                                                                                                                                                                                                                   | ksuuids. h    | n/d                             |



 

## <a name="audio-format-tags"></a>Tag di formato audio

Il campo **wFormatTag** nella struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) specifica il tipo di formato audio. Gli esempi di supporti sono in genere un numero intero di campioni, come specificato nel campo **wBitsPerSample** della struttura **WAVEFORMATEX** . Questa operazione non è necessariamente valida per gli esempi audio MPEG che possono provenire da flussi in pacchetti e pertanto non sono necessariamente inclusi nei limiti di campionamento/frame. Per MPEG audio il timestamp in un esempio multimediale è il timestamp del primo frame il cui primo byte è contenuto nell'esempio di supporto.

I sottotipi di supporto vengono definiti per ogni **wFormatTag** come segue:

-   Il sottocampo Data1 del GUID del sottotipo corrisponde al valore **wFormatTag** .
-   Il campo data 2 è 0.
-   Il campo data 3 è 0x0010.
-   Il campo data 4 è 0x80, 0x00, 0x00, 0xAA, 0x00, 0x38, 0x9B, 0x71.

Quindi, per l'audio PCM il GUID del sottotipo (definito in UUIDs. h come **\_ PCM MEDIASUBTYPE**) è:

`{00000001-0000-0010-8000-00AA00389B71}`

La funzione [**CreateAudioMediaType**](createaudiomediatype.md) può essere usata per creare una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) da una struttura **WAVEFORMATEX** .

## <a name="obsolete-audio-types"></a>Tipi audio obsoleti

I sottotipi audio seguenti sono obsoleti e non devono essere usati:

-   **MEDIASUBTYPE \_ MPEG \_ RAW \_ AAC**
-   **\_PCMAUDIOOBSOLETE MEDIASUBTYPE**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_tipo di supporto am \_**](/windows/win32/api/strmif/ns-strmif-am_media_type)
</dt> <dt>

[Tipi di supporto](media-types.md)
</dt> </dl>

 

