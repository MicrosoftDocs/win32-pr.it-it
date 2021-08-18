---
description: Matrice di stringhe con i parametri da inviare al server di log.
ms.assetid: 36d711c7-a1ff-4ef2-b633-5f9f1662801e
title: MFNETSOURCE_LOGPARAMS proprietà (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba557c4fb0bf77693669e8cb46af269ec3a4f2ed72c536e4bdab53a0778dc038
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113521"
---
# <a name="mfnetsource_logparams-property"></a>MFNETSOURCE \_ LOGPARAMS - proprietà

Matrice di stringhe con i parametri da inviare al server di log.



Tipo di dati

Tipo PROPVARIANT (vt)

membro PROPVARIANT

**Wchar\***

VT \_ LPWSTR

**pwszVal**



## <a name="remarks"></a>Commenti

La **costante MFNETSOURCE \_ LOGPARAMS** definisce il GUID per la chiave di proprietà. L'identificatore di proprietà (PID) è zero. Per impostare questa proprietà nell'origine di rete, passare un **puntatore IPropertyStore** al resolver di origine. Per altre informazioni, vedere [Configurazione di un'origine multimediale.](configuring-a-media-source.md)

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

 

 




