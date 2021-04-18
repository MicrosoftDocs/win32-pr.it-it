---
description: Offset tra il timestamp di ogni campione ricevuto dal grabber di esempio e l'ora in cui l'esempio Grabber presenta l'esempio.
ms.assetid: 8d06b415-aafc-4276-9a88-4b7262df62f1
title: Attributo MF_SAMPLEGRABBERSINK_SAMPLE_TIME_OFFSET (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d99f65c5023bbe8705e21269dfb07d6f24db4190
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308456"
---
# <a name="mf_samplegrabbersink_sample_time_offset-attribute"></a>\_Attributo di \_ offset dell'ora di esempio MF SAMPLEGRABBERSINK \_ \_

Offset tra il timestamp di ogni campione ricevuto dal grabber di esempio e l'ora in cui l'esempio Grabber presenta l'esempio.

## <a name="data-type"></a>Tipo di dati

**UINT64**

## <a name="remarks"></a>Commenti

È possibile impostare questo attributo sull'oggetto [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) restituito dalla funzione [**MFCreateSampleGrabberSinkActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesamplegrabbersinkactivate) . Questo attributo consente alla funzione di callback del grabber di esempio di ricevere esempi prima dell'ora di presentazione.

Quando l'esempio Grabber riceve un nuovo esempio, viene visualizzato il valore di esempio at time *t* - *offset*, dove *t* è il timestamp dell'esempio e *offset* è il valore di questo attributo. Se questo attributo non è impostato, il valore predefinito è zero.

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUInt64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**IMFAttributes:: UINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[**IMFSampleGrabberSinkCallback**](/windows/desktop/api/mfidl/nn-mfidl-imfsamplegrabbersinkcallback)
</dt> <dt>

[Attributi di Media Foundation](media-foundation-attributes.md)
</dt> </dl>

 

 




