---
description: Tipi di supporti demultiplexer MPEG-2
ms.assetid: 240d1753-df8c-45fe-b5a7-9faa96fc5b18
title: Tipi di supporti demultiplexer MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99b46b52580f96ec931f3a7eaf7d5bbf1462d4faa1862a330e501476fc92867a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952300"
---
# <a name="mpeg-2-demultiplexer-media-types"></a>Tipi di supporti demultiplexer MPEG-2

Il [filtro MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) riconosce i tipi di supporti seguenti.

### <a name="input-types"></a>Tipi di input

Il tipo principale è sempre **MEDIATYPE \_ Stream**. Il sottotipo può essere uno dei seguenti.



| GUID                                             | Descrizione                                                                                                                                                                                               |
|--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SOTTOTIPO KSDATAFORMAT \_ \_ BDA \_ MPEG2 \_ TRANSPORT** | Flusso di trasporto da un filtro di dispositivo BDA (Broadcast Driver Architecture). Il demultiplexer MPEG-2 considera questo sottotipo in modo identico a **MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT**.                                |
| **PROGRAMMA \_ MPEG2 \_ MEDIASUBTYPE**                 | Flusso del programma                                                                                                                                                                                            |
| **MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT**               | Flusso di trasporto (TS), con pacchetti da 188 byte                                                                                                                                                              |
| **MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT \_ STRIDE**       | Flusso di trasporto con pacchetti "strided". Questo sottotipo indica che i pacchetti TS possono essere riempiti con byte aggiuntivi. Per altre informazioni, vedere [**MPEG2 \_ TRANSPORT \_ STRIDE**](mpeg2-transport-stride.md). |



 

Per i pacchetti di trasporto strided (**MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT \_ STRIDE**), ogni campione di supporti deve contenere un numero integrale di pacchetti di trasporto, come descritto in [**MPEG2 \_ TRANSPORT \_ STRIDE**](mpeg2-transport-stride.md). Per tutti gli altri tipi di input, non sono presenti restrizioni sui limiti del campione. I singoli pacchetti possono estendersi a limiti di esempio.

### <a name="output-types"></a>Tipi di output

Il demultiplexer MPEG-2 non convalida i tipi di output. il filtro downstream è responsabile dell'analisi dei dati ricevuti dal demultiplexer. Tuttavia, i tipi seguenti sono comunemente accettati dai filtri downstream come output dal demultiplexer.

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
<td>Nessuno</td>
</tr>
</tbody>
</table>



 

### <a name="mpeg-2-video"></a>MPEG-2 Video



| Etichetta | Valore |
|------------------|------------------------------------------|
| Tipo principale       | **MEDIATYPE \_ Video**                     |
| Subtype          | **MEDIASUBTYPE \_ MPEG2 \_ VIDEO**           |
| Tipo di formato      | **FORMAT \_ MPEG2Video**                   |
| Struttura del formato | [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) |



 

### <a name="mpeg-2-audio"></a>MPEG-2 Audio



| Etichetta | Valore |
|------------------|--------------------------------------|
| Tipo principale       | **MEDIATYPE \_ Audio**                 |
| Subtype          | **MEDIASUBTYPE \_ MPEG2 \_ AUDIO**       |
| Tipo di formato      | **FORMAT \_ WaveFormatEx**             |
| Struttura del formato | [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di supporti MPEG-2](mpeg-2-media-types.md)
</dt> </dl>

 

 
