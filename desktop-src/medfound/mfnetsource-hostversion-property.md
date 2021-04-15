---
description: Il valore del campo &\# 0034; c-hostexever&\# 0034; che l'origine di rete usa per la registrazione.
ms.assetid: eee93457-483d-41dc-91c5-c12382d03152
title: Proprietà MFNETSOURCE_HOSTVERSION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f10c1a66bc2ab52455140733a6b60f25863c8f3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485204"
---
# <a name="mfnetsource_hostversion-property"></a>\_Proprietà HOSTVERSION di MFNETSOURCE

Valore del campo "c-hostexever" utilizzato dall'origine di rete per la registrazione. Le applicazioni possono impostare questa proprietà sul numero di versione dell'applicazione host. L'applicazione host è il file con estensione exe identificato dal campo c-hostexe.



Tipo di dati

Tipo PROPVARIANT (VT)

membro PROPVARIANT

**LONGLONG**

\_I8 VT

**hVal**



## <a name="remarks"></a>Commenti

La costante **MFNETSOURCE \_ HOSTVERSION** definisce il GUID per la chiave della proprietà. L'identificatore di proprietà (PID) è zero.

Le applicazioni possono usare questa proprietà per configurare l'origine di rete. Per impostare la proprietà, passare un puntatore **IPropertyStore** al resolver di origine. Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Registrazione client](client-logging.md)
</dt> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Rete in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




