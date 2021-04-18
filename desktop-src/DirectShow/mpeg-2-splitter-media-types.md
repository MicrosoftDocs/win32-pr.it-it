---
description: Tipi di supporto per la barra di divisione MPEG-2
ms.assetid: d0ff2011-4ee3-4f5e-8bd0-af9f4c6346e8
title: Tipi di supporto per la barra di divisione MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb10310bd126346c8e1558801200682792836d92
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320597"
---
# <a name="mpeg-2-splitter-media-types"></a>Tipi di supporto per la barra di divisione MPEG-2

Il filtro [splitter MPEG-2](mpeg-2-splitter.md) supporta attualmente audio e video. Dolby AC-3 è supportato come sottoflusso come definito da DVD. Il filtro supporta anche audio MPEG-2. I tipi di supporto variano a seconda che il separatore MPEG-2 stia distribuendo pacchetti PES o payload di PES.

### <a name="video"></a>Video

Per il video MPEG-2, i tipi di supporto sono i seguenti.



|                  |                                          |                                |
|------------------|------------------------------------------|--------------------------------|
|                  | Output PES                               | Output payload                 |
| Tipo principale       | **\_PES MEDIATYPE MPEG2 \_**                | **Video di MEDIATYPE \_**           |
| Subtype          | **VIDEO di MEDIASUBTYPE \_ MPEG2 \_**           | **VIDEO di MEDIASUBTYPE \_ MPEG2 \_** |
| Tipo di formato      | **FORMATO \_ mpeg2video**                   | **FORMATO \_ mpeg2video**         |
| Struttura Format | [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) | **MPEG2VIDEOINFO**             |



 

### <a name="ac-3-audio"></a>Audio AC-3

Per l'audio AC-3, i tipi di supporto sono i seguenti.



|                  |                                      |                              |
|------------------|--------------------------------------|------------------------------|
|                  | Output PES                           | Output payload               |
| Tipo principale       | \_PES MEDIATYPE MPEG2 \_                | **\_Audio MEDIATYPE**         |
| Subtype          | MEDIASUBTYPE \_ Dolby \_ AC3             | **MEDIASUBTYPE \_ Dolby \_ AC3** |
| Tipo di formato      | FORMATO \_ WAVEFORMATEX                 | **FORMATO \_ WAVEFORMATEX**     |
| Struttura Format | [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) | **WAVEFORMATEX**             |



 

Il membro **wFormatTag** della struttura **WAVEFORMATEX** per AC-3 è attualmente **\_ \_ sconosciuto nel formato Wave**, ma questo potrebbe cambiare.

### <a name="mpeg-2-audio"></a>Audio MPEG-2

Per l'audio MPEG-2, i tipi di supporto sono i seguenti.



|                  |                               |                                |
|------------------|-------------------------------|--------------------------------|
|                  | Output PES                    | Output payload                 |
| Tipo principale       | **\_PES MEDIATYPE MPEG2 \_**     | **\_Audio MEDIATYPE**           |
| Subtype          | **\_Audio MPEG2 \_ MEDIASUBTYE** | **\_Audio MPEG2 \_ MEDIASUBTYPE** |
| Tipo di formato      | **FORMATO \_ WAVEFORMATEX**      | **FORMATO \_ WAVEFORMATEX**       |
| Struttura Format | **WAVEFORMATEX**              | **WAVEFORMATEX**               |



 

Il membro **wFormatTag** della struttura **WAVEFORMATEX** per l'audio MPEG-2 è **attualmente \_ \_ sconosciuto**, ma questo potrebbe cambiare.

Il separatore MPEG-2 presuppone che i flussi da D0 a DF vengano usati per il flusso di estensioni multicanale, come per l'audio MPEG-2 DVD. Pertanto, ogni volta che si seleziona Stream C *x* , la barra di divisione inoltra anche i pacchetti per il flusso D *x* .

### <a name="lpcm-audio"></a>Audio LPCM

Per l'audio LPCM, i tipi di supporto sono i seguenti.



|                  |                                    |                                    |
|------------------|------------------------------------|------------------------------------|
|                  | Output PES                         | Output payload                     |
| Tipo principale       | **\_PES MEDIATYPE MPEG2 \_**          | **\_Audio MEDIATYPE**               |
| Subtype          | **\_audio MEDIASUBTYPE DVD \_ LPCM \_** | **\_audio MEDIASUBTYPE DVD \_ LPCM \_** |
| Tipo di formato      | **FORMATO \_ WAVEFORMATEX**           | **FORMATO \_ WAVEFORMATEX**           |
| Struttura Format | **WAVEFORMATEX**                   | **WAVEFORMATEX**                   |



 

Il membro **wFormatTag** della struttura **WAVEFORMATEX** per l'audio LPCM è **attualmente \_ \_ sconosciuto**, ma questo potrebbe cambiare.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di supporti MPEG-2](mpeg-2-media-types.md)
</dt> </dl>

 

 
