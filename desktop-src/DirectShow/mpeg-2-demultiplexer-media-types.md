---
description: MpEG-2 Tipi di supporti demultiplexer
ms.assetid: 240d1753-df8c-45fe-b5a7-9faa96fc5b18
title: MpEG-2 Tipi di supporti demultiplexer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9b5276b975771ba62118976c8e63b4d5faa53d
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909999"
---
# <a name="mpeg-2-demultiplexer-media-types"></a>MpEG-2 Tipi di supporti demultiplexer

Il [filtro MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) riconosce i tipi di supporti seguenti.

### <a name="input-types"></a>Tipi di input

Il tipo principale è sempre **MEDIATYPE \_ Stream.** Il sottotipo può essere uno dei seguenti.



| GUID                                             | Descrizione                                                                                                                                                                                               |
|--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **TRASPORTO \_ \_ MPEG2 DEL SOTTOTIPO KSDATAFORMAT \_ \_** | Flusso di trasporto da un filtro di dispositivo BDA (Broadcast Driver Architecture). Il demultiplex MPEG-2 tratta questo sottotipo in modo identico a **MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT.**                                |
| **PROGRAMMA \_ MPEG2 \_ MEDIASUBTYPE**                 | Flusso del programma                                                                                                                                                                                            |
| **MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT**               | Flusso di trasporto (TS), con pacchetti da 188 byte                                                                                                                                                              |
| **MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT \_ STRIDE**       | Flusso di trasporto con pacchetti "strided". Questo sottotipo indica che i pacchetti TS possono essere riempiti con byte aggiuntivi. Per altre informazioni, vedere [**MPEG2 \_ TRANSPORT \_ STRIDE.**](mpeg2-transport-stride.md) |



 

Per i pacchetti di trasporto strided **(MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT \_ STRIDE),** ogni campione di supporti deve contenere un numero integrale di pacchetti di trasporto, come descritto in [**MPEG2 \_ TRANSPORT \_ STRIDE**](mpeg2-transport-stride.md). Per tutti gli altri tipi di input, non sono presenti restrizioni sui limiti di esempio. I singoli pacchetti possono estendersi oltre i limiti del campione.

### <a name="output-types"></a>Tipi di output

Il demultiplexer MPEG-2 non convalida i tipi di output. Il filtro downstream è responsabile dell'analisi dei dati ricevuti dal demultiplexer. Tuttavia, i tipi seguenti sono comunemente accettati dai filtri downstream come output dal demultiplexer.

### <a name="mpeg-2-sections"></a>Sezioni MPEG-2



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Tipo principale</td>
<td><strong>MEDIATYPE_MPEG2_SECTIONS</strong></td>
</tr>
<tr class="even">
<td>Subtype</td>
<td>Uno dei casi seguenti:<br/>
<ul>
<li><strong>MEDIASUBTYPE_ATSC_SI:</strong>informazioni sul servizio ATSC.</li>
<li><strong>MEDIASUBTYPE_DVB_SI:</strong>informazioni sul servizio DVB.</li>
<li><strong>MEDIASUBTYPE_ISDB_SI:</strong>Informazioni sul servizio ISDB (Integrated Services Digital Broadcasting).</li>
<li><strong>MEDIASUBTYPE_MPEG2DATA:</strong>dati della sezione MPEG-2.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Tipo di formato</td>
<td>nessuno</td>
</tr>
</tbody>
</table>



 

### <a name="mpeg-2-video"></a>MPEG-2 Video



| Label | Valore |
|------------------|------------------------------------------|
| Tipo principale       | **MEDIATYPE \_ Video**                     |
| Subtype          | **MEDIASUBTYPE \_ MPEG2 \_ VIDEO**           |
| Tipo di formato      | **FORMAT \_ MPEG2Video**                   |
| Struttura del formato | [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) |



 

### <a name="mpeg-2-audio"></a>MPEG-2 Audio



| Label | Valore |
|------------------|--------------------------------------|
| Tipo principale       | **MEDIATYPE \_ Audio**                 |
| Subtype          | **MEDIASUBTYPE \_ MPEG2 \_ AUDIO**       |
| Tipo di formato      | **FORMAT \_ WaveFormatEx**             |
| Struttura del formato | [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di supporti MPEG-2](mpeg-2-media-types.md)
</dt> </dl>

 

 
