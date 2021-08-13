---
description: Valore del campo &\# 0034;c-hostexe&0034; utilizzato dall'origine \# di rete per la registrazione.
ms.assetid: 82a49719-b9b3-4868-bbcf-9e376f35d4c4
title: MFNETSOURCE_HOSTEXE proprietà (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a6dbde4b4b445e88a0cb6e7ebe45b8b88f386c208854057f209d9c36b7e0024
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119463651"
---
# <a name="mfnetsource_hostexe-property"></a>Proprietà HOSTEXE di MFNETSOURCE \_

Valore del campo "c-hostexe" utilizzato dall'origine di rete per la registrazione. Le applicazioni possono impostare questa proprietà sul nome dell'applicazione host. Ad esempio, il valore potrebbe essere "iexplore.exe" se l'applicazione è ospitata in una pagina Web.



Tipo di dati

Tipo PROPVARIANT (vt)

membro PROPVARIANT

Stringa di caratteri wide (**WCHAR** \* )

VT \_ LPWSTR

**pwszVal**



## <a name="remarks"></a>Commenti

La costante **MFNETSOURCE \_ HOSTEXE** definisce il GUID per questa chiave di proprietà. L'identificatore di proprietà (PID) è zero.

Le applicazioni possono usare questa proprietà per configurare l'origine di rete. Per impostare la proprietà, passare un **puntatore IPropertyStore** al sistema di risoluzione di origine. Per altre informazioni, vedere [Configurazione di un'origine multimediale](configuring-a-media-source.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Registrazione client](client-logging.md)
</dt> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> <dt>

[Rete in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




