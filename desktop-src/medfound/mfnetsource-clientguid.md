---
description: Identificatore univoco con cui il server identifica il client.
ms.assetid: 490a2b03-aba8-4510-80c5-ca12f4037747
title: Proprietà MFNETSOURCE_CLIENTGUID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc5df46741d4a0b9a6a125396b6f93dd32bfadf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130118"
---
# <a name="mfnetsource_clientguid-property"></a>\_Proprietà CLIENTGUID di MFNETSOURCE

Identificatore univoco con cui il server identifica il client.



Tipo di dati

Tipo PROPVARIANT (VT)

membro PROPVARIANT

**GUID**

\_CLSID VT

**puuid**



## <a name="remarks"></a>Commenti

La costante **MFNETSOURCE \_ CLIENTGUID** definisce il GUID per la chiave della proprietà. L'identificatore di proprietà (PID) è zero. Per impostare questa proprietà nell'origine di rete, passare un puntatore **IPropertyStore** al resolver di origine. Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).

Se non è impostato o impostato come **GUID \_ NULL**, Microsoft Media Foundation genera un GUID anonimo per sessione che garantisce la privacy dell'utente.

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

 

 




