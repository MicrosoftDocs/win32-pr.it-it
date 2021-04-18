---
description: Contiene il tipo di supporto principale per un nodo di topologia. Questo attributo viene impostato quando la topologia non viene caricata perché non è stato possibile trovare il decodificatore corretto.
ms.assetid: eb837fe6-12c9-479c-a0be-63b24093e6fd
title: Attributo MF_TOPONODE_ERROR_MAJORTYPE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd68ace0cd3bec4f32536e7d0d8d29bcea60d997
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308451"
---
# <a name="mf_toponode_error_majortype-attribute"></a>\_ \_ Attributo MAJORTYPE dell'errore MF TOPONODE \_

Contiene il tipo di supporto principale per un nodo di topologia. Questo attributo viene impostato quando la topologia non viene caricata perché non è stato possibile trovare il decodificatore corretto.

## <a name="data-type"></a>Tipo di dati

**GUID**

## <a name="remarks"></a>Commenti

Questo attributo si applica a tutti i tipi di nodo.

Il caricatore della topologia potrebbe impostare l'attributo. Le applicazioni in genere leggono questo attributo ma non lo impostano.

Per un elenco di valori possibili, vedere [principali tipi di supporti](media-type-guids.md).

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

[Attributi del nodo della topologia](topology-node-attributes.md)
</dt> </dl>

 

 




