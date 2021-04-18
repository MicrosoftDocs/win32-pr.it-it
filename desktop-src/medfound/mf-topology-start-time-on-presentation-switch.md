---
description: Specifica l'ora di inizio per le presentazioni accodate dopo la prima presentazione.
ms.assetid: 087f5d61-b3e6-4fdf-98e6-b018de7b237f
title: Attributo MF_TOPOLOGY_START_TIME_ON_PRESENTATION_SWITCH (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5f4c50271ad2da9682be9d259ad855352e844af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308455"
---
# <a name="mf_topology_start_time_on_presentation_switch-attribute"></a>\_Ora di inizio della topologia MF \_ \_ \_ sull' \_ attributo del \_ comcambio di presentazione

Specifica l'ora di inizio per le presentazioni accodate dopo la prima presentazione.

## <a name="data-type"></a>Tipo di dati

**Int64** archiviato come **UInt64**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)SetAttribute.

## <a name="applies-to"></a>Si applica a

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Commenti

Quando l'applicazione Accoda la prima presentazione nella sessione multimediale, l'applicazione specifica l'ora di inizio nel parametro *pvarStartPosition* del metodo [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) . Per tutte le presentazioni successive, tuttavia, l'ora di inizio viene assegnata dall' \_ ora di inizio della topologia MF \_ \_ \_ sull'attributo del \_ comcambio di presentazione \_ nella topologia. L'ora di inizio è specificata in unità 100-nanosecondi rispetto all'inizio della presentazione. Se, ad esempio, il valore è 50 milioni, la riproduzione inizia 5 secondi nella presentazione. Se questo attributo non è impostato, l'ora di inizio predefinita è zero.

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                         |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi della topologia](topology-attributes.md)
</dt> </dl>

 

 




