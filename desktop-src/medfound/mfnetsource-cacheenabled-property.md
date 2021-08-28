---
description: Specifica se l'origine di rete memorizza nella cache il contenuto.
ms.assetid: f9a36315-083c-4ebb-9d36-d55fc1f21621
title: MFNETSOURCE_CACHEENABLED proprietà (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6954359ed91fe402d785fec9e63f470c31abc85432e519b2e06bcb1d679933dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113631"
---
# <a name="mfnetsource_cacheenabled-property"></a>MFNETSOURCE \_ CACHEENABLED - proprietà

Specifica se l'origine di rete memorizza nella cache il contenuto.



Tipo di dati

Tipo PROPVARIANT (vt)

membro PROPVARIANT

Boolean (**LONG**)

VT \_ I4

**lVal**



## <a name="remarks"></a>Commenti

La costante **MFNETSOURCE \_ CACHEENABLED** definisce il GUID per questa chiave di proprietà. L'identificatore di proprietà (PID) è zero.

Le applicazioni possono usare questa proprietà per configurare l'origine di rete. Per impostare la proprietà, passare un **puntatore IPropertyStore** al sistema di risoluzione di origine. Per altre informazioni, vedere [Configurazione di un'origine multimediale](configuring-a-media-source.md).

Il valore predefinito di questa proprietà è **TRUE.**

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
</dt> </dl>

 

 




