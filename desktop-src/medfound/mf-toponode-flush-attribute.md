---
description: Specifica quando viene scaricata una trasformazione.
ms.assetid: 1e87f58f-546f-4dd4-b218-1458ff17db53
title: MF_TOPONODE_FLUSH attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67e02c297efa68c6e6c585837675a46b729ec2382be072828059fd795d1c67a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663881"
---
# <a name="mf_toponode_flush-attribute"></a>Attributo MF \_ TOPONODE \_ FLUSH

Specifica quando viene scaricata una trasformazione.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Questo attributo si applica ai nodi di trasformazione (**MF \_ TOPOLOGY \_ TRANSFORM \_ NODE**).

Il valore dell'attributo è un membro dell'enumerazione [**\_ MF TOPONODE \_ FLUSH \_**](/windows/desktop/api/mfidl/ne-mfidl-mf_toponode_flush_mode) MODE. Se questo attributo non è impostato, il valore predefinito è **MF \_ TOPONODE \_ FLUSH \_ ALWAYS**.

Lo scaricamento viene eseguito chiamando [**IMFTransform::P rocessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) nella trasformazione con il messaggio [**MFT \_ MESSAGE COMMAND \_ \_ FLUSH.**](mft-message-command-flush.md) Per altre informazioni, vedere [**Enumerazione MFT \_ MESSAGE \_ TYPE.**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)

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

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Attributi del nodo della topologia](topology-node-attributes.md)
</dt> </dl>

 

 




