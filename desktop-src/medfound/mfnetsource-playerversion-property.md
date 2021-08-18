---
description: Valore del campo &\# 0034;c-playerversion&\# 0034; utilizzato dall'origine di rete per la registrazione.
ms.assetid: 7bc485de-345b-475c-bbae-0776aa63c93a
title: MFNETSOURCE_PLAYERVERSION proprietà (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71828db44eca7c4318dbdb11e7934871911b06dbc4547f83723a9944f139ae26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118738970"
---
# <a name="mfnetsource_playerversion-property"></a>MFNETSOURCE \_ PLAYERVERSION - proprietà

Valore del campo "c-playerversion" utilizzato dall'origine di rete per la registrazione. Le applicazioni possono impostare questa proprietà sul numero di versione dell'applicazione.



Tipo di dati

Tipo PROPVARIANT (vt)

membro PROPVARIANT

**LONGLONG**

VT \_ I8

**hVal**



## <a name="remarks"></a>Commenti

La costante **MFNETSOURCE \_ PLAYERVERSION** definisce il GUID per questa chiave di proprietà. L'identificatore di proprietà (PID) è zero.

Le applicazioni possono usare questa proprietà per configurare l'origine di rete. Per impostare la proprietà, passare un **puntatore IPropertyStore** al sistema di risoluzione di origine. Per altre informazioni, vedere [Source Resolver](source-resolver.md).

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

 

 




