---
description: Specifica quando una trasformazione viene scaricata.
ms.assetid: 1e87f58f-546f-4dd4-b218-1458ff17db53
title: Attributo MF_TOPONODE_FLUSH (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cea241227d70d967f6f41ccd994176e9ddbbacbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308447"
---
# <a name="mf_toponode_flush-attribute"></a>\_Attributo di \_ scaricamento MF TOPONODE

Specifica quando una trasformazione viene scaricata.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Questo attributo si applica ai nodi di trasformazione (**\_ nodo di \_ trasformazione \_ della topologia MF**).

Il valore dell'attributo è un membro dell'enumerazione della [**\_ \_ \_ modalità di scaricamento MF TOPONODE**](/windows/desktop/api/mfidl/ne-mfidl-mf_toponode_flush_mode) . Se questo attributo non è impostato, il valore predefinito è **MF \_ TOPONODE \_ Flush \_ Always**.

Lo svuotamento viene eseguito chiamando [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) nella trasformazione con il messaggio di [**\_ \_ \_ scaricamento del comando del messaggio MFT**](mft-message-command-flush.md) . Per ulteriori informazioni, vedere l'enumerazione del [**\_ \_ tipo di messaggio MFT**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type) .

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

 

 




