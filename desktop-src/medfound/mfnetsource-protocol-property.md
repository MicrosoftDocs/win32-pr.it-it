---
description: Specifica il protocollo di controllo utilizzato dall'origine di rete.
ms.assetid: 4de8b8ba-97d9-4269-a16c-1853dc02f674
title: MFNETSOURCE_PROTOCOL proprietà (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae15ce40e7c049552cbb0f4916f5f4ff70ef6e55746528ebe0083eee69b22a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118243323"
---
# <a name="mfnetsource_protocol-property"></a>MFNETSOURCE \_ PROTOCOL - proprietà

Specifica il protocollo di controllo utilizzato dall'origine di rete. Il valore di questa proprietà è un membro [**dell'enumerazione MFNETSOURCE \_ PROTOCOL \_ TYPE.**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type)



Tipo di dati

Tipo PROPVARIANT (vt)

membro PROPVARIANT

**LONG**

VT \_ I4

**lVal**



## <a name="remarks"></a>Commenti

La costante **MFNETSOURCE \_ PROTOCOL** definisce il GUID per questa chiave di proprietà. L'identificatore di proprietà (PID) è zero.

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

 

 




