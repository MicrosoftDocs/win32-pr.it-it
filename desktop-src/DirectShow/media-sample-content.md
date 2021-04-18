---
description: Descrive il contenuto di un flusso elementare all'interno di un flusso di trasporto MPEG-2. Questa enumerazione viene utilizzata nell'interfaccia IMPEG2PIDMap, implementata nei pin di output del Demultiplexer MPEG-2.
ms.assetid: 989ad56b-b5af-4811-889e-c79fcd3f7f01
title: Enumerazione MEDIA_SAMPLE_CONTENT (Bdatypes. h)
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
ms.openlocfilehash: 9065f2af948ff28d181b24842673b086882837bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325920"
---
# <a name="media_sample_content-enumeration"></a>Enumerazione del contenuto di \_ esempio multimediale \_

Descrive il contenuto di un flusso elementare all'interno di un flusso di trasporto MPEG-2. Questa enumerazione viene utilizzata nell'interfaccia [**IMPEG2PIDMap**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap) , implementata nei pin di output del [Demultiplexer MPEG-2](mpeg-2-demultiplexer.md).

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

<span id="MEDIA_TRANSPORT_PACKET"></span><span id="media_transport_packet"></span>**\_pacchetto di trasporto multimediale \_**
</dt> <dd>

Specifica un pacchetto del flusso di trasporto completo da passare senza elaborazione.

</dd> <dt>

<span id="MEDIA_ELEMENTARY_STREAM"></span><span id="media_elementary_stream"></span>**\_flusso elementare \_ multimediale**
</dt> <dd>

Specifica il payload di un file audio o video.

</dd> <dt>

<span id="MEDIA_MPEG2_PSI"></span><span id="media_mpeg2_psi"></span>**MEDIA \_ MPEG2 \_ PSI**
</dt> <dd>

Specifica un flusso di dati PAT, PMT, CAT o private. Si tratta di sezioni PSI complete che non è necessario riassemblare.

</dd> <dt>

<span id="MEDIA_TRANSPORT_PAYLOAD"></span><span id="media_transport_payload"></span>**\_payload del trasporto multimediale \_**
</dt> <dd>

Specifica i payload di pacchetti TS raccolti, ad esempio i pacchetti PES.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Bdatypes. h (include Bdaiface. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tipi enumerati DirectShow](directshow-enumerated-types.md)
</dt> </dl>

 

 




