---
description: Tipi di supporti splitter MPEG-2
ms.assetid: d0ff2011-4ee3-4f5e-8bd0-af9f4c6346e8
title: Tipi di supporti splitter MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b29151e5128531cbd2e71c6eda0f2b4b16658c8e68577de0fbb0542189c2931f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748581"
---
# <a name="mpeg-2-splitter-media-types"></a>Tipi di supporti splitter MPEG-2

Il [filtro mpeg-2 splitter](mpeg-2-splitter.md) supporta attualmente audio e video. Dolby AC-3 è supportato come flusso secondario come definito da DVD. Il filtro supporta anche l'audio MPEG-2. I tipi di supporti variano a seconda che lo splitter MPEG-2 consegnerà pacchetti PES o payload PES.

### <a name="video"></a>Video

Per i video MPEG-2, i tipi di supporti sono i seguenti.


|                | Output PES | Output del payload
|------------------|------------------------------------------|--------------------------------|
| **Tipo principale**       | **MEDIATYPE \_ MPEG2 \_ PES**                | **MEDIATYPE \_ Video**           |
| **Sottotipo**          | **MEDIASUBTYPE \_ MPEG2 \_ VIDEO**           | **MEDIASUBTYPE \_ MPEG2 \_ VIDEO** |
| **Tipo di formato**      | **FORMAT \_ MPEG2Video**                   | **FORMAT \_ MPEG2Video**         |
| **Struttura del formato** | [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) | **MPEG2VIDEOINFO**             |



 

### <a name="ac-3-audio"></a>AC-3 Audio

Per l'audio AC-3, i tipi di supporti sono i seguenti.

| | Output PES | Output del payload |
|------------------|--------------------------------------|------------------------------|
| **Tipo principale**       | **MEDIATYPE \_ MPEG2 \_ PES**                | **MEDIATYPE \_ Audio**         |
| **Sottotipo**          | **MEDIASUBTYPE \_ DOLBY \_ AC3**             | **MEDIASUBTYPE \_ DOLBY \_ AC3** |
| **Tipo di formato**      | FORMAT \_ WaveFormatEx                 | **FORMAT \_ WaveFormatEx**     |
| **Struttura del formato** | [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) | **WAVEFORMATEX**             |



 

Il membro **wFormatTag** della struttura **WAVEFORMATEX** per AC-3 è attualmente **WAVE FORMAT \_ \_ UNKNOWN,** ma potrebbe cambiare.

### <a name="mpeg-2-audio"></a>MPEG-2 Audio

Per l'audio MPEG-2, i tipi di supporti sono i seguenti.



|  | Output PES | Output del payload |
|------------------|-------------------------------|--------------------------------|
| **Tipo principale**       | **MEDIATYPE \_ MPEG2 \_ PES**     | **MEDIATYPE \_ Audio**           |
| **Sottotipo**          | **MEDIASUBTYE \_ MPEG2 \_ AUDIO** | **MEDIASUBTYPE \_ MPEG2 \_ AUDIO** |
| **Tipo di formato**      | **FORMAT \_ WaveFormatEx**      | **FORMAT \_ WaveFormatEx**       |
| **Struttura del formato** | **WAVEFORMATEX**              | **WAVEFORMATEX**               |



 

Il membro **wFormatTag** della struttura **WAVEFORMATEX** per MPEG-2 Audio è attualmente **WAVE FORMAT \_ \_ UNKNOWN,** ma potrebbe cambiare.

Lo splitter MPEG-2 presuppone che i flussi da D0 a DF siano usati per il flusso di estensione multicanale, come per l'audio MPEG-2 DVD. Pertanto, ogni volta che si seleziona il flusso C *x,* la barra di divisione inoltra anche i pacchetti per il flusso D *x.*

### <a name="lpcm-audio"></a>Audio di Gestione configurazione locale

Per l'audio LPCM, i tipi di supporti sono i seguenti.



|  | Output PES | Output del payload |
|------------------|------------------------------------|------------------------------------|
| **Tipo principale**       | **MEDIATYPE \_ MPEG2 \_ PES**          | **MEDIATYPE \_ Audio**               |
| **Sottotipo**          | **MEDIASUBTYPE \_ DVD \_ LPCM \_ AUDIO** | **MEDIASUBTYPE \_ DVD \_ LPCM \_ AUDIO** |
| **Tipo di formato**      | **FORMAT \_ WaveFormatEx**           | **FORMAT \_ WaveFormatEx**           |
| **Struttura del formato** | **WAVEFORMATEX**                   | **WAVEFORMATEX**                   |



 

Il membro **wFormatTag** della struttura **WAVEFORMATEX** per l'audio LPCM è attualmente **WAVE FORMAT \_ \_ UNKNOWN,** ma potrebbe cambiare.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di supporti MPEG-2](mpeg-2-media-types.md)
</dt> </dl>

 

 
