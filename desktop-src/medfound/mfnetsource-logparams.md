---
description: Matrice di stringhe con i parametri da inviare al server di log.
ms.assetid: 36d711c7-a1ff-4ef2-b633-5f9f1662801e
title: Proprietà MFNETSOURCE_LOGPARAMS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec30f3f4d85f44905288601ba73ee6c246d8a9db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967036"
---
# <a name="mfnetsource_logparams-property"></a>\_Proprietà LOGPARAMS di MFNETSOURCE

Matrice di stringhe con i parametri da inviare al server di log.



Tipo di dati

Tipo PROPVARIANT (VT)

membro PROPVARIANT

**WCHAR \** _

\_LPWSTR VT

_ *pwszVal**



## <a name="remarks"></a>Commenti

La costante **MFNETSOURCE \_ LOGPARAMS** definisce il GUID per la chiave della proprietà. L'identificatore di proprietà (PID) è zero. Per impostare questa proprietà nell'origine di rete, passare un puntatore **IPropertyStore** al resolver di origine. Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                         |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Rete in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




