---
description: Specifica l'ora di arresto di una topologia rispetto all'inizio della prima topologia nella sequenza.
ms.assetid: 7669f97e-87ad-4a64-a2a5-62b8ce450d80
title: MF_TOPOLOGY_PROJECTSTART attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f295f68b3ac94bf29fa4607eb2b5ba00ea8eab19774bcaa0af150ef6d3fbe1f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117875408"
---
# <a name="mf_topology_projectstart-attribute"></a>Attributo PROJECTSTART della TOPOLOGIA MF \_ \_

Specifica l'ora di arresto di una topologia rispetto all'inizio della prima topologia nella sequenza.

## <a name="data-type"></a>Tipo di dati

**UINT64**

Considerare come **valore LONGLONG.**

## <a name="remarks"></a>Commenti

Il valore viene specificato in unità di 100 nanosecondi.

Se la sessione multimediale è stata creata con l'attributo [**MF \_ SESSION GLOBAL \_ \_ TIME**](mf-session-global-time-attribute.md) uguale a **TRUE,** tutte le topologie devono contenere l'attributo **\_ \_ PROJECTSTART** della topologia MF. In caso contrario, le topologie non devono contenere **l'attributo \_ \_ PROJECTSTART della topologia MF.** Per altre informazioni, vedere Sequenza [dei tempi di presentazione.](sequence-presentation-times.md)

Questo attributo è un valore con segno, anche se viene archiviato come **UINT64.**

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Tempi di presentazione delle sequenze](sequence-presentation-times.md)
</dt> <dt>

[Attributi della topologia](topology-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[**MF \_ TOPOLOGY \_ PROJECTSTOP**](mf-topology-projectstop-attribute.md)
</dt> </dl>

 

 




