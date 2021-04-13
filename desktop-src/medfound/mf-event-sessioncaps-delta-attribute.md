---
description: Contiene flag che indicano quali funzionalità sono state modificate nella sessione multimediale, in base alla presentazione corrente.
ms.assetid: aa01d17f-f2ac-4504-b278-3edd90ab8a23
title: Attributo MF_EVENT_SESSIONCAPS_DELTA (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 284a31a8d3fc661c15e7de991972455468efbd40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401665"
---
# <a name="mf_event_sessioncaps_delta-attribute"></a>\_ \_ Attributo Delta SESSIONCAPS dell'evento MF \_

Contiene flag che indicano quali funzionalità sono state modificate nella sessione multimediale, in base alla presentazione corrente.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Questo attributo contiene una maschera di maschera che indica i flag delle funzionalità che sono stati modificati. Per un elenco dei flag possibili, vedere [**IMFMediaSession:: GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities). BITS viene impostato su 1 nella maschera di bit per uno dei motivi seguenti:

-   Il bit di funzionalità corrispondente è stato modificato da 0 a 1.
-   Il bit di funzionalità corrispondente è stato modificato da 1 a 0.
-   Il bit delle funzionalità corrispondente è rimasto 1, ma i dettagli della funzionalità sono stati modificati. Ad esempio, è stata modificata la velocità massima di riproduzione.

Questo attributo viene utilizzato con l'evento [MESessionCapabilitiesChanged](mesessioncapabilitieschanged.md) .

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

[**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: seuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




