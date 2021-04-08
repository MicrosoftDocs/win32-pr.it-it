---
description: Specifica l'ora di arresto per una topologia, relativa all'inizio della prima topologia nella sequenza.
ms.assetid: 7669f97e-87ad-4a64-a2a5-62b8ce450d80
title: Attributo MF_TOPOLOGY_PROJECTSTART (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34a7e3d50bd89e0fdfc032f9854c1a183276f04a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880225"
---
# <a name="mf_topology_projectstart-attribute"></a>\_Attributo PROJECTSTART della topologia MF \_

Specifica l'ora di arresto per una topologia, relativa all'inizio della prima topologia nella sequenza.

## <a name="data-type"></a>Tipo di dati

**UINT64**

Considera come valore **LONGLONG** .

## <a name="remarks"></a>Commenti

Il valore è espresso in unità di 100 nanosecondi.

Se la sessione multimediale è stata creata con l'attributo dell' [**\_ \_ \_ ora globale della sessione MF**](mf-session-global-time-attribute.md) uguale a **true**, tutte le topologie devono contenere l'attributo **\_ \_ PROJECTSTART della topologia MF** . In caso contrario, le topologie non devono contenere l'attributo **\_ \_ PROJECTSTART della topologia MF** . Per altre informazioni, vedere [tempi di presentazione della sequenza](sequence-presentation-times.md).

Questo attributo è un valore con segno, sebbene venga archiviato come **UInt64**.

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

[Tempi di presentazione sequenza](sequence-presentation-times.md)
</dt> <dt>

[Attributi della topologia](topology-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUInt64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**IMFAttributes:: UINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[**\_PROJECTSTOP topologia MF \_**](mf-topology-projectstop-attribute.md)
</dt> </dl>

 

 




