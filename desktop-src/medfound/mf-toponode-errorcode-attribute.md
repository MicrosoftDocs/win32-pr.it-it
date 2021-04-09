---
description: Contiene il codice di errore dell'errore di connessione più recente per questo nodo di topologia.
ms.assetid: fae90e06-0ae0-43a1-aaf2-7a2d1dabc79b
title: Attributo MF_TOPONODE_ERRORCODE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b4b28c8f630d06f3545ca44c5b064c0bb6dac32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130143"
---
# <a name="mf_toponode_errorcode-attribute"></a>\_Attributo MF TOPONODE \_ ErrorCode

Contiene il codice di errore dell'errore di connessione più recente per questo nodo di topologia.

## <a name="data-type"></a>Tipo di dati

**UINT32**

Ttreat come valore **HRESULT** .

## <a name="remarks"></a>Commenti

Questo attributo si applica a tutti i tipi di nodo.

Il valore di questo attributo è un valore **HRESULT** .

La sessione multimediale o il caricatore della topologia potrebbe impostare l'attributo. Le applicazioni in genere leggono questo attributo ma non lo impostano.

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

 

 




