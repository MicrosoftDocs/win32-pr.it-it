---
description: Specifica l'ora di inizio di una topologia, relativa all'inizio della prima topologia nella sequenza.
ms.assetid: 1ca3709e-88ea-40ca-8da4-c2259365122b
title: MF_TOPOLOGY_PROJECTSTOP attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03ab227f1fdcda99148be3106b2ea724578f30bd9fd83756cd3b9d16f46ef993
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117875398"
---
# <a name="mf_topology_projectstop-attribute"></a>Attributo MF \_ TOPOLOGY \_ PROJECTSTOP

Specifica l'ora di inizio di una topologia, relativa all'inizio della prima topologia nella sequenza.

## <a name="data-type"></a>Tipo di dati

**UINT64**

Considera come **valore LONGLONG.**

## <a name="remarks"></a>Commenti

Il valore è specificato in unità di 100 nanosecondi.

Se la sessione multimediale è stata creata con [**l'attributo MF \_ SESSION GLOBAL \_ \_ TIME**](mf-session-global-time-attribute.md) uguale a **TRUE,** tutte le topologie devono contenere l'attributo **MF \_ TOPOLOGY \_ PROJECTSTOP.** In caso contrario, le topologie non devono contenere **l'attributo \_ MF TOPOLOGY \_ PROJECTSTOP.** Per altre informazioni, vedere [Sequenza dei tempi di presentazione.](sequence-presentation-times.md)

Questo attributo è un valore con segno, anche se viene archiviato come **UINT64.**

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Sequenza dei tempi di presentazione](sequence-presentation-times.md)
</dt> <dt>

[Attributi della topologia](topology-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[**PROGETTO DI \_ TOPOLOGIA MFAVVIO \_**](mf-topology-projectstart-attribute.md)
</dt> </dl>

 

 




