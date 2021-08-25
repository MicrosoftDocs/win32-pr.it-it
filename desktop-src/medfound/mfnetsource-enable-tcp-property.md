---
description: Specifica se il trasporto TCP è abilitato per l'origine di rete.
ms.assetid: ba655505-dcac-4cea-8ad5-ccd1b55ee9d4
title: MFNETSOURCE_ENABLE_TCP proprietà (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcd5fe37ab423bd48af8aad45bdbb5c2b09b2d9b4b59fd40d85429d1fa1913ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954802"
---
# <a name="mfnetsource_enable_tcp-property"></a>MFNETSOURCE \_ ENABLE - proprietà \_ TCP

Specifica se il trasporto TCP è abilitato per l'origine di rete.



Tipo di dati

Tipo PROPVARIANT (vt)

membro PROPVARIANT

Boolean (**LONG**)

VT \_ I4

**lVal**



## <a name="remarks"></a>Commenti

La costante **MFNETSOURCE \_ ACCELERATEDSTREAMINGDURATION** definisce il GUID per questa chiave di proprietà. L'identificatore di proprietà (PID) è zero.

Le applicazioni possono usare questa proprietà per configurare l'origine di rete. Per impostare la proprietà, passare un **puntatore IPropertyStore** al sistema di risoluzione di origine. Per altre informazioni, vedere [Configurazione di un'origine multimediale](configuring-a-media-source.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> <dt>

[Rete in Media Foundation](networking-in-media-foundation.md)
</dt> <dt>

[Protocolli supportati](supported-protocols.md)
</dt> </dl>

 

 




