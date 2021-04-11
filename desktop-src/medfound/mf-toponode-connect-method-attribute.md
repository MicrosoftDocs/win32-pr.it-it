---
description: Specifica il modo in cui il caricatore della topologia connette il nodo della topologia e se il nodo è facoltativo.
ms.assetid: 8d70e1af-607b-47c3-9808-091c95fd05b7
title: Attributo MF_TOPONODE_CONNECT_METHOD (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3db5fef529ef451fa02ac4a29e62002b0a1996a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233347"
---
# <a name="mf_toponode_connect_method-attribute"></a>\_Attributo del \_ metodo di connessione MF TOPONODE \_

Specifica il modo in cui il caricatore della topologia connette il nodo della topologia e se il nodo è facoltativo.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Questo attributo si applica a tutti i tipi di nodo.

Il **valore dell'attributo è un operatore OR** bit per bit di flag dell'enumerazione del [**\_ \_ Metodo MF Connect**](/windows/desktop/api/mfidl/ne-mfidl-mf_connect_method) . Se questo attributo non è impostato, il valore predefinito è **MF \_ Connect \_ allow \_ decoder**.

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

 

 




