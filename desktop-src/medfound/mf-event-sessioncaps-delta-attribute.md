---
description: Contiene flag che indicano quali funzionalità sono state modificate nella sessione multimediale, in base alla presentazione corrente.
ms.assetid: aa01d17f-f2ac-4504-b278-3edd90ab8a23
title: MF_EVENT_SESSIONCAPS_DELTA attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a2e227e5608296a9b30fa2fc68f37215d687349516367d8689b20825e1ed4e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714842"
---
# <a name="mf_event_sessioncaps_delta-attribute"></a>Attributo MF \_ EVENT \_ SESSIONCAPS \_ DELTA

Contiene flag che indicano quali funzionalità sono state modificate nella sessione multimediale, in base alla presentazione corrente.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Questo attributo contiene una maschera di bit che indica quali flag di funzionalità sono stati modificati. Per un elenco dei flag possibili, vedere [**IMFMediaSession::GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities). I bit vengono impostati su 1 nella maschera di bit per uno dei motivi seguenti:

-   Il bit delle funzionalità corrispondente è cambiato da 0 a 1.
-   Il bit delle funzionalità corrispondente è cambiato da 1 a 0.
-   Il bit di funzionalità corrispondente è rimasto 1, ma i dettagli della funzionalità sono cambiati. Ad esempio, la velocità di riproduzione massima è cambiata.

Questo attributo viene usato con [l'evento MESessionCapabilitiesChanged.](mesessioncapabilitieschanged.md)

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi dell'evento](event-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




