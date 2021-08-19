---
description: Specifica se la sessione multimediale tenta di modificare la topologia quando cambia il formato di un flusso.
ms.assetid: 8272ded7-9d27-4652-877b-40fc76426ffc
title: MF_TOPOLOGY_DYNAMIC_CHANGE_NOT_ALLOWED attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb2e984b45abc55246c9b1ae291c535c7fbb00f01f9405d827b7fe833b57a368
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117875734"
---
# <a name="mf_topology_dynamic_change_not_allowed-attribute"></a>ATTRIBUTO MF TOPOLOGY DYNAMIC CHANGE NOT ALLOWED (MODIFICA DINAMICA DELLA TOPOLOGIA MF \_ \_ NON \_ \_ \_ CONSENTITA)

Specifica se la sessione multimediale tenta di modificare la topologia quando cambia il formato di un flusso.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Si applica a

[**Topologia IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Commenti

Questo attributo controlla la modalità di risposta della sessione multimediale se il formato di un flusso cambia durante lo streaming.

Se il formato cambia e l'attributo MF TOPOLOGY DYNAMIC CHANGE NOT ALLOWED è FALSE, la sessione multimediale potrebbe inserire nuovi nodi nella topologia in modo che \_ \_ \_ \_ \_ corrispondano al nuovo formato.  Ad esempio, se le dimensioni del video cambiano, la sessione multimediale potrebbe aggiungere una trasformazione Media Foundation (MFT) che ridimensiona il video. In caso contrario, se l'attributo **è TRUE,** la sessione multimediale non modificherà la topologia.

Il valore predefinito di questo attributo è **FALSE.** Il valore consigliato è **FALSE.**

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi della topologia](topology-attributes.md)
</dt> </dl>

 

 




