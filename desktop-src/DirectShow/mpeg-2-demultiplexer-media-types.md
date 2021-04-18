---
description: Tipi di supporti di Demultiplexer MPEG-2
ms.assetid: 240d1753-df8c-45fe-b5a7-9faa96fc5b18
title: Tipi di supporti di Demultiplexer MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b21eecff138b987c791ecd97056fb4cf417dd98d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320694"
---
# <a name="mpeg-2-demultiplexer-media-types"></a>Tipi di supporti di Demultiplexer MPEG-2

Il filtro [di MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) riconosce i seguenti tipi di supporti.

### <a name="input-types"></a>Tipi di input

Il tipo principale è sempre **\_ flusso MEDIATYPE**. Il sottotipo può essere uno dei seguenti.



| GUID                                             | Descrizione                                                                                                                                                                                               |
|--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **KSDATAFORMAT \_ sottotipo \_ BDA \_ \_ trasporto MPEG2** | Flusso di trasporto da un filtro di periferica BDA (Broadcast Driver Architecture). Il Demultiplexer MPEG-2 considera questo sottotipo in modo identico al **\_ \_ trasporto MEDIASUBTYPE MPEG2**.                                |
| **\_Programma MEDIASUBTYPE MPEG2 \_**                 | Flusso di programma                                                                                                                                                                                            |
| **\_Trasporto MPEG2 \_ MEDIASUBTYPE**               | Flusso di trasporto (TS), con pacchetti da 188 byte                                                                                                                                                              |
| **\_ \_ Stride trasporto MPEG2 \_ MEDIASUBTYPE**       | Flusso di trasporto con pacchetti "con stride". Questo sottotipo indica che i pacchetti di Servizi terminal possono essere riempiti con byte aggiuntivi. Per ulteriori informazioni, vedere la pagina relativa allo [**\_ \_ stride del trasporto MPEG2**](mpeg2-transport-stride.md). |



 

Per i pacchetti di trasporto con Stride (**MEDIASUBTYPE \_ MPEG2 \_ Transport \_ stride**), ogni esempio di supporto deve contenere un numero integrale di pacchetti di trasporto, come descritto nello [**\_ \_ stride del trasporto MPEG2**](mpeg2-transport-stride.md). Per tutti gli altri tipi di input, non sono previste restrizioni sui limiti di esempio; i singoli pacchetti possono estendersi sui limiti di esempio.

### <a name="output-types"></a>Tipi di output

Il Demultiplexer MPEG-2 non convalida i tipi di output. il filtro downstream è responsabile dell'analisi dei dati ricevuti dal Demultiplexer. Tuttavia, i tipi seguenti sono comunemente accettati dai filtri downstream come output del Demultiplexer.

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
<li><strong>MEDIASUBTYPE_ATSC_SI</strong>: informazioni sul servizio ATSC.</li>
<li><strong>MEDIASUBTYPE_DVB_SI</strong>: informazioni sul servizio DVB.</li>
<li><strong>MEDIASUBTYPE_ISDB_SI</strong>: informazioni sul servizio Integrated Services Digital Broadcasting (ISDB).</li>
<li><strong>MEDIASUBTYPE_MPEG2DATA</strong>: dati della sezione MPEG-2.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Tipo di formato</td>
<td>nessuno</td>
</tr>
</tbody>
</table>



 

### <a name="mpeg-2-video"></a>Video MPEG-2



|                  |                                          |
|------------------|------------------------------------------|
| Tipo principale       | **Video di MEDIATYPE \_**                     |
| Subtype          | **VIDEO di MEDIASUBTYPE \_ MPEG2 \_**           |
| Tipo di formato      | **FORMATO \_ mpeg2video**                   |
| Struttura Format | [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) |



 

### <a name="mpeg-2-audio"></a>Audio MPEG-2



|                  |                                      |
|------------------|--------------------------------------|
| Tipo principale       | **\_Audio MEDIATYPE**                 |
| Subtype          | **\_Audio MPEG2 \_ MEDIASUBTYPE**       |
| Tipo di formato      | **FORMATO \_ WAVEFORMATEX**             |
| Struttura Format | [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di supporti MPEG-2](mpeg-2-media-types.md)
</dt> </dl>

 

 
