---
description: Identificatore di classe (CLSID) della trasformazione Media Foundation (MFT) associata a questo nodo della topologia.
ms.assetid: 6aa6e649-d23d-4d8d-be80-2b8814b07a57
title: MF_TOPONODE_TRANSFORM_OBJECTID attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9b5013bc43f07e08e1a2c26530e9325595e62666986516029ef9d76e2c72ffe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118244315"
---
# <a name="mf_toponode_transform_objectid-attribute"></a>Attributo \_ \_ OBJECTID MF TOPONODE TRANSFORM \_

Identificatore di classe (CLSID) della trasformazione Media Foundation (MFT) associata a questo nodo della topologia.

## <a name="data-type"></a>Tipo di dati

**GUID**

## <a name="remarks"></a>Commenti

Questo attributo si applica ai nodi di trasformazione (**MF \_ TOPOLOGY \_ TRANSFORM \_ NODE**).

Le applicazioni possono usare questo attributo per inizializzare un nodo transfrom. Se si imposta questo attributo, non è necessario chiamare [**IMFTopologyNode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) con un puntatore a un oggetto MFT o attivazione. Viceversa, se si chiama **SetObject**, non è necessario impostare questo attributo. Per altre informazioni, vedere [Creazione di topologie.](creating-topologies.md)

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

[**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Media Foundation attributi](media-foundation-attributes.md)
</dt> <dt>

[Creazione di topologie](creating-topologies.md)
</dt> <dt>

[Attributi del nodo della topologia](topology-node-attributes.md)
</dt> </dl>

 

 




