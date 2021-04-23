---
description: Tipi di supporti con separatore MPEG-2
ms.assetid: d0ff2011-4ee3-4f5e-8bd0-af9f4c6346e8
title: Tipi di supporti con separatore MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e878acaea8bc87bee2bf5c46a6f7e66c7aa0a485
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909428"
---
# <a name="mpeg-2-splitter-media-types"></a>Tipi di supporti con separatore MPEG-2

Il [filtro mpeg-2 splitter](mpeg-2-splitter.md) supporta attualmente audio e video. Dolby AC-3 è supportato come flusso secondario come definito da DVD. Il filtro supporta anche l'audio MPEG-2. I tipi di supporti variano a seconda che la barra di divisione MPEG-2 invii pacchetti PES o payload PES.

### <a name="video"></a>Video

Per i video MPEG-2, i tipi di file multimediali sono i seguenti.



| Label | Valore |
|------------------|------------------------------------------|--------------------------------|
|                  | Output PES                               | Output del payload                 |
| Tipo principale       | **MEDIATYPE \_ MPEG2 \_ PES**                | **MEDIATYPE \_ Video**           |
| Subtype          | **MEDIASUBTYPE \_ MPEG2 \_ VIDEO**           | **MEDIASUBTYPE \_ MPEG2 \_ VIDEO** |
| Tipo di formato      | **FORMAT \_ MPEG2Video**                   | **FORMAT \_ MPEG2Video**         |
| Struttura del formato | [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) | **MPEG2VIDEOINFO**             |



 

### <a name="ac-3-audio"></a>AC-3 Audio

Per l'audio AC-3, i tipi di supporti sono i seguenti.



| Label | Valore |
|------------------|--------------------------------------|------------------------------|
|                  | Output PES                           | Output del payload               |
| Tipo principale       | MEDIATYPE \_ MPEG2 \_ PES                | **MEDIATYPE \_ Audio**         |
| Subtype          | MEDIASUBTYPE \_ DOLBY \_ AC3             | **MEDIASUBTYPE \_ DOLBY \_ AC3** |
| Tipo di formato      | FORMAT \_ WaveFormatEx                 | **FORMAT \_ WaveFormatEx**     |
| Struttura del formato | [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) | **WAVEFORMATEX**             |



 

Il membro **wFormatTag** della struttura **WAVEFORMATEX** per AC-3 è attualmente **WAVE FORMAT \_ \_ UNKNOWN,** ma potrebbe cambiare.

### <a name="mpeg-2-audio"></a>MPEG-2 Audio

Per l'audio MPEG-2, i tipi di supporti sono i seguenti.



| Label | Valore |
|------------------|-------------------------------|--------------------------------|
|                  | Output PES                    | Output del payload                 |
| Tipo principale       | **MEDIATYPE \_ MPEG2 \_ PES**     | **MEDIATYPE \_ Audio**           |
| Subtype          | **MEDIASUBTYE \_ MPEG2 \_ AUDIO** | **MEDIASUBTYPE \_ MPEG2 \_ AUDIO** |
| Tipo di formato      | **FORMAT \_ WaveFormatEx**      | **FORMAT \_ WaveFormatEx**       |
| Struttura del formato | **WAVEFORMATEX**              | **WAVEFORMATEX**               |



 

Il membro **wFormatTag** della struttura **WAVEFORMATEX** per l'audio MPEG-2 è attualmente **WAVE FORMAT \_ \_ UNKNOWN,** ma questo potrebbe cambiare.

Lo splitter MPEG-2 presuppone che i flussi da D0 a DF siano usati per il flusso di estensione multicanale, come per l'audio DVD MPEG-2. Pertanto, ogni volta che viene selezionato il flusso C *x,* la barra di divisione inoltra anche i pacchetti per il flusso D *x.*

### <a name="lpcm-audio"></a>Audio di Gestione configurazione locale

Per l'audio di Gestione configurazione locale, i tipi di supporti sono i seguenti.



| Label | Valore |
|------------------|------------------------------------|------------------------------------|
|                  | Output PES                         | Output del payload                     |
| Tipo principale       | **MEDIATYPE \_ MPEG2 \_ PES**          | **MEDIATYPE \_ Audio**               |
| Subtype          | **MEDIASUBTYPE \_ DVD \_ LPCM \_ AUDIO** | **MEDIASUBTYPE \_ DVD \_ LPCM \_ AUDIO** |
| Tipo di formato      | **FORMAT \_ WaveFormatEx**           | **FORMAT \_ WaveFormatEx**           |
| Struttura del formato | **WAVEFORMATEX**                   | **WAVEFORMATEX**                   |



 

Il membro **wFormatTag** della struttura **WAVEFORMATEX** per l'audio LPCM è attualmente **WAVE FORMAT \_ \_ UNKNOWN,** ma potrebbe cambiare.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di supporti MPEG-2](mpeg-2-media-types.md)
</dt> </dl>

 

 
