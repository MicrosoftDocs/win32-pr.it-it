---
description: Specifica quando una trasformazione viene svuotata.
ms.assetid: 68332106-d1fe-467b-8baa-1e592b9cc243
title: Attributo MF_TOPONODE_DRAIN (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 679b87d626738b82f4504673392bd0fe159e2722
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308453"
---
# <a name="mf_toponode_drain-attribute"></a>\_Attributo di \_ scaricamento MF TOPONODE

Specifica quando una trasformazione viene svuotata.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Questo attributo si applica ai nodi di trasformazione (**\_ nodo di \_ trasformazione \_ della topologia MF**).

Il valore dell'attributo è un membro dell'enumerazione [**MF \_ TOPONODE \_ drain \_ mode**](/windows/desktop/api/mfidl/ne-mfidl-mf_toponode_drain_mode) . Se questo attributo non è impostato, il valore predefinito è **MF \_ TOPONODE \_ drain \_ default**.

Lo svuotamento viene eseguito chiamando [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) nella trasformazione con il messaggio di [**\_ svuotamento del \_ comando \_ del messaggio MFT**](mft-message-command-drain.md) . Per ulteriori informazioni, vedere l'enumerazione del [**\_ \_ tipo di messaggio MFT**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type) .

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

[**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: seuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Attributi del nodo della topologia](topology-node-attributes.md)
</dt> </dl>

 

 




