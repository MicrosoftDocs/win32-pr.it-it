---
description: Per diversi GUID del tipo di supporto MPEG-2, il DDK Windows definisce nomi diversi dai nomi usati in DirectShow. La tabella seguente illustra i nomi DirectShow (definiti in Ksuuids.h) e i nomi corrispondenti in modalità kernel (definiti in Ksmedia.h).
ms.assetid: ecf94552-5a0f-464c-9f9b-4861faa38d05
title: Tipi di supporti del kernel MPEG-2 (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41cfbbd93bfb4d9c21a7ab2b496e69458e2754d95ae4427ad163c4f2a06e4165
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952260"
---
# <a name="mpeg-2-kernel-media-types"></a>Tipi di supporti del kernel MPEG-2

Per diversi GUID del tipo di supporto MPEG-2, il DDK Windows definisce nomi diversi dai nomi usati in DirectShow. La tabella seguente illustra i nomi DirectShow (definiti in Ksuuids.h) e i nomi corrispondenti in modalità kernel (definiti in Ksmedia.h).



| Nome in Ksuuids.h              | Nome in Ksmedia.h                          |
|--------------------------------|--------------------------------------------|
| FORMAT \_ WaveFormatEx           | IDENTIFICATORE KSDATAFORMAT \_ \_ WAVEFORMATEX      |
| FORMAT \_ MPEG2Video             | \_ \_ VIDEO MPEG2 DELL'IDENTIFICATORE \_ KSDATAFORMAT      |
| MEDIASUBTYPE \_ ATSC \_ SI         | SOTTOTIPO KSDATAFORMAT \_ \_ ATSC \_ SI            |
| MEDIASUBTYPE \_ DOLBY \_ AC3       | SOTTOTIPO KSDATAFORMAT \_ \_ AC3 \_ AUDIO          |
| MEDIASUBTYPE \_ DVB \_ SI          | KSDATAFORMAT \_ SUBTYPE \_ DVB \_ SI             |
| MEDIASUBTYPE \_ DVD \_ LPCM \_ AUDIO | SOTTOTIPO KSDATAFORMAT \_ \_ LPCM \_ AUDIO         |
| MEDIASUBTYPE \_ MPEG2 \_ AUDIO     | SOTTOTIPO \_ \_ MPEG2 DI KSDATAFORMAT \_        |
| PROGRAMMA \_ MPEG2 \_ MEDIASUBTYPE   | PROGRAMMA \_ \_ MPEG2 DI TIPO KSDATAFORMAT \_ \_ STATICO |
| MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT | TRASPORTO \_ \_ MPEG2 DI TIPO KSDATAFORMAT \_       |
| MEDIASUBTYPE \_ MPEG2 \_ VIDEO     | VIDEO SUL \_ SOTTOTIPO KSDATAFORMAT \_ MPEG2 \_        |
| SEZIONI \_ MPEG2 \_ MEDIATYPE     | SEZIONI \_ \_ MPEG2 DI TIPO KSDATAFORMAT \_        |
| MEDIATYPE \_ Audio               | AUDIO DI TIPO KSDATAFORMAT \_ \_                  |
| MEDIATYPE \_ MPEG2 \_ PES          | KSDATAFORMAT \_ TYPE \_ MPEG2 \_ PES             |
| MEDIATYPE \_ Video               | VIDEO DI TIPO KSDATAFORMAT \_ \_                  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tipi di supporti MPEG-2](mpeg-2-media-types.md)
</dt> </dl>

 

 




