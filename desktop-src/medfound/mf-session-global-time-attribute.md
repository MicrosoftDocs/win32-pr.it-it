---
description: Specifica se le topologie hanno una data e un'ora di inizio e di fine globali.
ms.assetid: 6810a22c-f091-423c-97dd-c04fdabdb9bb
title: Attributo MF_SESSION_GLOBAL_TIME (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b930ed47c5f314b12aba0075cdc9120d2179325
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314537"
---
# <a name="mf_session_global_time-attribute"></a>\_ \_ Attributo time globale della sessione MF \_

Specifica se le topologie hanno una data e un'ora di inizio e di fine globali.

## <a name="data-type"></a>Tipo di dati

**UINT32**

Considera come valore booleano.

## <a name="remarks"></a>Commenti

È possibile impostare questo attributo quando si crea il file multimediale sesison utilizzando il parametro *pConfiguration* della funzione [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) o [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) .

Se questo attributo è presente e diverso da zero, tutte le topologie passate alla sessione multimediale devono avere gli attributi della topologia [**MF \_ \_ PROJECTSTART**](mf-topology-projectstart-attribute.md) e MF topologia [**\_ \_ PROJECTSTOP**](mf-topology-projectstop-attribute.md) . Questi attributi specificano l'ora di inizio e di fine per la topologia relativa all'intera presentazione.

Se questo attributo è assente o **false**, le topologie non devono avere l'attributo [**MF \_ topologia \_ PROJECTSTART**](mf-topology-projectstart-attribute.md) o [**MF \_ topologia \_ PROJECTSTOP**](mf-topology-projectstop-attribute.md) .

Utilizzare questo attributo per creare sequenze di modifica. Per altre informazioni, vedere [tempi di presentazione della sequenza](sequence-presentation-times.md).

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

[Attributi della sessione multimediale](media-session-attributes.md)
</dt> <dt>

[Tempi di presentazione sequenza](sequence-presentation-times.md)
</dt> <dt>

[**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: seuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**\_PROJECTSTART topologia MF \_**](mf-topology-projectstart-attribute.md)
</dt> <dt>

[**\_PROJECTSTOP topologia MF \_**](mf-topology-projectstop-attribute.md)
</dt> </dl>

 

 




