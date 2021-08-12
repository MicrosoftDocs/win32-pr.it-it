---
description: Valore del campo &\# 0034;c-hostexever&0034; utilizzato dall'origine di rete per \# la registrazione.
ms.assetid: eee93457-483d-41dc-91c5-c12382d03152
title: MFNETSOURCE_HOSTVERSION proprietà (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d5f78a277de4fc5b0609be31f21f684357806dbb8609657a930cdc4816b1e43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118243461"
---
# <a name="mfnetsource_hostversion-property"></a>Proprietà MFNETSOURCE \_ HOSTVERSION

Valore del campo "c-hostexever" utilizzato dall'origine di rete per la registrazione. Le applicazioni possono impostare questa proprietà sul numero di versione dell'applicazione host. L'applicazione host è .exe file identificato dal campo c-hostexe.



Tipo di dati

Tipo PROPVARIANT (vt)

membro PROPVARIANT

**LONGLONG**

VT \_ I8

**hVal**



## <a name="remarks"></a>Commenti

La costante **MFNETSOURCE \_ HOSTVERSION** definisce il GUID per questa chiave di proprietà. L'identificatore di proprietà (PID) è zero.

Le applicazioni possono usare questa proprietà per configurare l'origine di rete. Per impostare la proprietà, passare un **puntatore IPropertyStore** al resolver di origine. Per altre informazioni, vedere [Configurazione di un'origine multimediale.](configuring-a-media-source.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Registrazione client](client-logging.md)
</dt> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> <dt>

[Rete in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




