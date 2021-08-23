---
description: Descrive il contenuto di un flusso elementare all'interno di un flusso di trasporto MPEG-2. Questa enumerazione viene usata nell'interfaccia IMPEG2PIDMap, implementata sui pin di output del demultiplexer MPEG-2.
ms.assetid: 989ad56b-b5af-4811-889e-c79fcd3f7f01
title: MEDIA_SAMPLE_CONTENT enumerazione (Bdatypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MEDIA_SAMPLE_CONTENT
api_type:
- HeaderDef
api_location:
- bdatypes.h
ms.openlocfilehash: 1dead22b2c8ea3cf7da665e01a4b36554b8282922a1d2b2a12d59f429f2acac4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684991"
---
# <a name="media_sample_content-enumeration"></a>Enumerazione MEDIA \_ SAMPLE \_ CONTENT

Descrive il contenuto di un flusso elementare all'interno di un flusso di trasporto MPEG-2. Questa enumerazione viene utilizzata [**nell'interfaccia IMPEG2PIDMap,**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap) implementata sui pin di output del [demultiplexer MPEG-2.](mpeg-2-demultiplexer.md)

## <a name="syntax"></a>Sintassi


```C++
typedef enum  { 
  MEDIA_TRANSPORT_PACKET,
  MEDIA_ELEMENTARY_STREAM,
  MEDIA_MPEG2_PSI,
  MEDIA_TRANSPORT_PAYLOAD
} MEDIA_SAMPLE_CONTENT;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="MEDIA_TRANSPORT_PACKET"></span><span id="media_transport_packet"></span>**PACCHETTO \_ DI TRASPORTO \_ MULTIMEDIALE**
</dt> <dd>

Specifica un pacchetto di flusso di trasporto completo da passare senza elaborazione.

</dd> <dt>

<span id="MEDIA_ELEMENTARY_STREAM"></span><span id="media_elementary_stream"></span>**FLUSSO \_ ELEMENTARE \_ MULTIMEDIALE**
</dt> <dd>

Specifica un payload PES audio o video.

</dd> <dt>

<span id="MEDIA_MPEG2_PSI"></span><span id="media_mpeg2_psi"></span>**MEDIA \_ MPEG2 \_ PSI**
</dt> <dd>

Specifica un flusso di dati PAT, PMT, CAT o Private. Si tratta di sezioni PSI complete che non devono essere riassemblate.

</dd> <dt>

<span id="MEDIA_TRANSPORT_PAYLOAD"></span><span id="media_transport_payload"></span>**PAYLOAD DEL \_ TRASPORTO \_ MULTIMEDIALE**
</dt> <dd>

Specifica i payload dei pacchetti TS raccolti, ad esempio i pacchetti PES.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Bdatypes.h (include Bdaiface.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[DirectShow Tipi enumerati](directshow-enumerated-types.md)
</dt> </dl>

 

 




