---
description: Il valore del campo &\# 0034; c-playerversion&\# 0034; che l'origine di rete usa per la registrazione.
ms.assetid: 7bc485de-345b-475c-bbae-0776aa63c93a
title: Proprietà MFNETSOURCE_PLAYERVERSION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ddaee0fe3e476b2b6e078551b1191fe9fc96cf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759668"
---
# <a name="mfnetsource_playerversion-property"></a>\_Proprietà PLAYERVERSION di MFNETSOURCE

Valore del campo "c-playerversion" utilizzato dall'origine di rete per la registrazione. Le applicazioni possono impostare questa proprietà sul numero di versione dell'applicazione.



Tipo di dati

Tipo PROPVARIANT (VT)

membro PROPVARIANT

**LONGLONG**

\_I8 VT

**hVal**



## <a name="remarks"></a>Commenti

La costante **MFNETSOURCE \_ PLAYERVERSION** definisce il GUID per la chiave della proprietà. L'identificatore di proprietà (PID) è zero.

Le applicazioni possono usare questa proprietà per configurare l'origine di rete. Per impostare la proprietà, passare un puntatore **IPropertyStore** al resolver di origine. Per ulteriori informazioni, vedere [resolver di origine](source-resolver.md).

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

 

 




