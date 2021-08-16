---
description: Identificatore univoco in base al quale il server identifica il client.
ms.assetid: 490a2b03-aba8-4510-80c5-ca12f4037747
title: MFNETSOURCE_CLIENTGUID proprietà (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9585f5ac9cd69148272cb986746f6849aad4c3aa048b46baf2f75aeaba77c092
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118738990"
---
# <a name="mfnetsource_clientguid-property"></a>MFNETSOURCE \_ - proprietà CLIENTGUID

Identificatore univoco in base al quale il server identifica il client.



Tipo di dati

Tipo PROPVARIANT (vt)

membro PROPVARIANT

**GUID**

VT \_ CLSID

**puuid**



## <a name="remarks"></a>Commenti

La **costante \_ CLIENTGUID MFNETSOURCE** definisce il GUID per la chiave di proprietà. L'identificatore di proprietà (PID) è zero. Per impostare questa proprietà nell'origine di rete, passare un **puntatore IPropertyStore** al resolver di origine. Per altre informazioni, vedere [Configurazione di un'origine multimediale.](configuring-a-media-source.md)

Se non è impostato o impostato come **GUID \_ NULL,** Microsoft Media Foundation genera un GUID anonimo per sessione che garantisce la privacy dell'utente.

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

 

 




