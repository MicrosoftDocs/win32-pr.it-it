---
description: Specifica se la sessione multimediale tenta di modificare la topologia quando il formato di un flusso viene modificato.
ms.assetid: 8272ded7-9d27-4652-877b-40fc76426ffc
title: Attributo MF_TOPOLOGY_DYNAMIC_CHANGE_NOT_ALLOWED (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ade7308c4fadef315fae0828a5c2cb29575b03a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484804"
---
# <a name="mf_topology_dynamic_change_not_allowed-attribute"></a>Attributo per la \_ modifica dinamica della topologia MF \_ \_ \_ non \_ consentito

Specifica se la sessione multimediale tenta di modificare la topologia quando il formato di un flusso viene modificato.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.

## <a name="applies-to"></a>Si applica a

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Commenti

Questo attributo controlla il modo in cui la sessione multimediale risponde se il formato di un flusso cambia durante il flusso.

Se il formato viene modificato e l' \_ attributo della modifica dinamica della topologia MF \_ \_ \_ non \_ è consentito è **false**, la sessione multimediale potrebbe inserire nuovi nodi nella topologia in modo che corrispondano al nuovo formato. Se, ad esempio, le dimensioni del video cambiano, la sessione multimediale potrebbe aggiungere una trasformazione Media Foundation (MFT) che ridimensiona il video. In caso contrario, se l'attributo è **true**, la topologia non verrà modificata dalla sessione multimediale.

Il valore predefinito di questo attributo è **false**. Il valore consigliato è **false**.

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

 

 




