---
description: Identificatore di classe (CLSID) della trasformazione Media Foundation (MFT) associata a questo nodo della topologia.
ms.assetid: 6aa6e649-d23d-4d8d-be80-2b8814b07a57
title: Attributo MF_TOPONODE_TRANSFORM_OBJECTID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ea96e09a75374bfe048b531492fc913f764d364
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527420"
---
# <a name="mf_toponode_transform_objectid-attribute"></a>\_ \_ Attributo ObjectID della trasformazione MF TOPONODE \_

Identificatore di classe (CLSID) della trasformazione Media Foundation (MFT) associata a questo nodo della topologia.

## <a name="data-type"></a>Tipo di dati

**GUID**

## <a name="remarks"></a>Commenti

Questo attributo si applica ai nodi di trasformazione (**\_ nodo di \_ trasformazione \_ della topologia MF**).

Le applicazioni possono utilizzare questo attributo per inizializzare un nodo transfrom. Se si imposta questo attributo, non è necessario chiamare [**IMFTopologyNode::**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) SetAttribute con un puntatore a un oggetto MFT o Activation. Viceversa, se si chiama **seobject**, non è necessario impostare questo attributo. Per ulteriori informazioni, vedere [creazione di topologie](creating-topologies.md).

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

[**IMFAttributes:: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**IMFAttributes:: Seguid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Attributi di Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[Creazione di topologie](creating-topologies.md)
</dt> <dt>

[Attributi del nodo della topologia](topology-node-attributes.md)
</dt> </dl>

 

 




