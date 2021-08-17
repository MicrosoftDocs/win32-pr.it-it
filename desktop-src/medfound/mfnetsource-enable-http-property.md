---
description: Specifica se il protocollo HTTP è abilitato nell'origine di rete.
ms.assetid: dcc4db5c-0274-4a8a-89a4-66cda62e1520
title: MFNETSOURCE_ENABLE_HTTP proprietà (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09d033594e223b8219f168e86d82ef02012bfafd4be9d758a438d042356735f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874767"
---
# <a name="mfnetsource_enable_http-property"></a>MFNETSOURCE \_ ENABLE - proprietà \_ HTTP

Specifica se il protocollo HTTP è abilitato nell'origine di rete.



Tipo di dati

Tipo PROPVARIANT (vt)

membro PROPVARIANT

Boolean (**LONG**)

VT \_ I4

**lVal**



## <a name="remarks"></a>Commenti

La costante **MFNETSOURCE \_ ENABLE \_ HTTP** definisce il GUID per questa chiave di proprietà. L'identificatore di proprietà (PID) è zero.

Le applicazioni possono usare questa proprietà per configurare l'origine di rete. Per impostare la proprietà, passare un **puntatore IPropertyStore** al resolver di origine. Per altre informazioni, vedere [Configurazione di un'origine multimediale.](configuring-a-media-source.md)

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

 

 




