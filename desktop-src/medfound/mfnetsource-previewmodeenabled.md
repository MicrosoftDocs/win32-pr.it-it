---
description: Abilita o disabilita la modalità di anteprima, che consente all'applicazione di sovrascrivere la logica iniziale di memorizzazione nel buffer.
ms.assetid: 8aa8c6ac-8746-4bf6-9f57-b1426495a275
title: MFNETSOURCE_PREVIEWMODEENABLED proprietà (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e03940828c6fa32b9e0367a03f960d4d64d88edf691100817ed31883013ce1b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663861"
---
# <a name="mfnetsource_previewmodeenabled-property"></a>Proprietà PREVIEWMODEENABLED di MFNETSOURCE \_

Abilita o disabilita la modalità di anteprima, che consente all'applicazione di sovrascrivere la logica iniziale di memorizzazione nel buffer.



Tipo di dati

Tipo PROPVARIANT (vt)

membro PROPVARIANT

**Bool**

VT \_ BOOL

**lVal**



## <a name="remarks"></a>Commenti

La costante **MFNETSOURCE \_ PREVIEWMODEENABLED** definisce il GUID per la chiave della proprietà. L'identificatore di proprietà (PID) è zero. Questa proprietà viene impostata nell'origine di rete passando un **puntatore IPropertyStore** al sistema di risoluzione di origine. Per altre informazioni, vedere [Configurazione di un'origine multimediale](configuring-a-media-source.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> <dt>

[Rete in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




