---
description: Il valore della prima parte del \# campo &0034; CS (User-Agent) &\# 0034; che l'origine di rete usa per la registrazione.
ms.assetid: b6c33cc8-ff43-4a19-a333-51a7f9b265a9
title: Proprietà MFNETSOURCE_BROWSERUSERAGENT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f8cbb4dcd5558c59da20e75209529c16fc0c147
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527385"
---
# <a name="mfnetsource_browseruseragent-property"></a>\_Proprietà BROWSERUSERAGENT di MFNETSOURCE

Il valore della prima parte del campo "CS (User-Agent)" usato dall'origine di rete per la registrazione. Le applicazioni possono impostare questa proprietà su qualsiasi valore stringa.



Tipo di dati

Tipo PROPVARIANT (VT)

membro PROPVARIANT

Stringa di caratteri wide (**WCHAR** \* )

\_LPWSTR VT

**pwszVal**



## <a name="remarks"></a>Commenti

La costante **MFNETSOURCE \_ BROWSERUSERAGENT** definisce il GUID per la chiave della proprietà. L'identificatore di proprietà (PID) è zero.

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

[**\_PLAYERUSERAGENT MFNETSOURCE**](mfnetsource-playeruseragent-property.md)
</dt> </dl>

 

 




