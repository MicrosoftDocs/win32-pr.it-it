---
description: Il valore del campo &\# 0034; c-hostexe&\# 0034; che l'origine di rete usa per la registrazione.
ms.assetid: 82a49719-b9b3-4868-bbcf-9e376f35d4c4
title: Proprietà MFNETSOURCE_HOSTEXE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0ac786fe08ede556537703d2eb886b30be39207
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759074"
---
# <a name="mfnetsource_hostexe-property"></a>\_Proprietà HOSTEXE di MFNETSOURCE

Valore del campo "c-hostexe" utilizzato dall'origine di rete per la registrazione. Le applicazioni possono impostare questa proprietà sul nome dell'applicazione host. Ad esempio, il valore potrebbe essere "iexplore.exe" se l'applicazione è ospitata in una pagina Web.



Tipo di dati

Tipo PROPVARIANT (VT)

membro PROPVARIANT

Stringa di caratteri wide (**WCHAR** \* )

\_LPWSTR VT

**pwszVal**



## <a name="remarks"></a>Commenti

La costante **MFNETSOURCE \_ HOSTEXE** definisce il GUID per la chiave della proprietà. L'identificatore di proprietà (PID) è zero.

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

 

 




