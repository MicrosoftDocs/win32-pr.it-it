---
description: Specifica il protocollo di trasporto utilizzato dall'origine di rete.
ms.assetid: 7c8598ff-f408-42d0-9eee-3ef1e82f0466
title: MFNETSOURCE_TRANSPORT proprietà (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 933c4051cd3d008082c3b7811fcd88f8b118e51a9e864d947750813c11883b67
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663471"
---
# <a name="mfnetsource_transport-property"></a>MFNETSOURCE \_ TRANSPORT - proprietà

Specifica il protocollo di trasporto utilizzato dall'origine di rete. Il valore di questa proprietà è un membro [**dell'enumerazione MFNETSOURCE \_ TRANSPORT \_ TYPE.**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_transport_type)



Tipo di dati

Tipo PROPVARIANT (vt)

membro PROPVARIANT

**LONG**

VT \_ I4

**lVal**



## <a name="remarks"></a>Commenti

La costante **MFNETSOURCE \_ TRANSPORT** definisce il GUID per questa chiave di proprietà. L'identificatore di proprietà (PID) è zero.

Questa proprietà è di sola lettura. Per recuperare questa proprietà, eseguire una query sull'origine di rete **per l'interfaccia IPropertyStore** e **chiamare IPropertyStore::GetValue**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> <dt>

[Rete in Media Foundation](networking-in-media-foundation.md)
</dt> <dt>

[Protocolli supportati](supported-protocols.md)
</dt> </dl>

 

 




