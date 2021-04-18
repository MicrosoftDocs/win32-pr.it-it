---
description: Il valore della seconda parte del \# campo &0034; CS (User-Agent) &\# 0034; che l'origine di rete usa per la registrazione.
ms.assetid: c662a6d6-5e0b-4c28-841d-5774d4103d4b
title: Proprietà MFNETSOURCE_PLAYERUSERAGENT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9f4d06eaea566e22e1239ed04594f2f592c7cd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307960"
---
# <a name="mfnetsource_playeruseragent-property"></a>\_Proprietà PLAYERUSERAGENT di MFNETSOURCE

Valore della seconda parte del campo "CS (User-Agent)" utilizzato dall'origine di rete per la registrazione. Le applicazioni possono impostare questa proprietà su qualsiasi valore stringa.



Tipo di dati

Tipo PROPVARIANT (VT)

membro PROPVARIANT

Stringa di caratteri wide (**WCHAR** \* )

\_LPWSTR VT

**pwszVal**



## <a name="remarks"></a>Commenti

La costante **MFNETSOURCE \_ PLAYERUSERAGENT** definisce il GUID per la chiave della proprietà. L'identificatore di proprietà (PID) è zero.

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
</dt> <dt>

[**\_BROWSERUSERAGENT MFNETSOURCE**](mfnetsource-browseruseragent-property.md)
</dt> </dl>

 

 




