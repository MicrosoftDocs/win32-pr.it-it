---
description: Identifica il nodo della topologia per un sink di flusso.
ms.assetid: 9aa6ca66-5122-4d05-94b9-32be194e9eb3
title: Attributo MF_EVENT_OUTPUT_NODE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02c484ea55841f4057bf0855dd51b90db951acb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309565"
---
# <a name="mf_event_output_node-attribute"></a>\_Attributo del \_ nodo di output evento MF \_

Identifica il nodo della topologia per un sink di flusso.

## <a name="data-type"></a>Tipo di dati

**UINT64**

Considera come [**TOPOID**](topoid.md).

## <a name="remarks"></a>Commenti

Il valore di questo attributo è un identificatore di nodo per un nodo di output nella topologia corrente. Per ottenere un puntatore al nodo associato, chiamare [**IMFTopology:: GetNodeByID**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getnodebyid) nella topologia.

Questo attributo viene usato con gli eventi seguenti:

-   [MESessionStreamSinkFormatChanged](mesessionstreamsinkformatchanged.md)
-   [MESinkInvalidated](mesinkinvalidated.md)

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi dell'evento](event-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUInt64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**IMFAttributes:: UINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




