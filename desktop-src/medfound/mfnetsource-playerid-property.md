---
description: Valore del campo &\# 0034;c-playerid&0034; utilizzato dall'origine di rete per \# la registrazione.
ms.assetid: de52cc34-9b88-41ae-b8b8-ef5dff85892c
title: MFNETSOURCE_PLAYERID proprietà (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1fc9afc79dec48a3ee19b007d2d1e04c0ccc35ab9a2bdd04c6699cd1ff65fea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874615"
---
# <a name="mfnetsource_playerid-property"></a>MFNETSOURCE \_ PLAYERID - proprietà

Valore del campo "c-playerid" utilizzato dall'origine di rete per la registrazione. Le applicazioni possono impostare questa proprietà su qualsiasi valore stringa.



Tipo di dati

Tipo PROPVARIANT (vt)

membro PROPVARIANT

Stringa di caratteri wide (**WCHAR** \* )

VT \_ LPWSTR

**pwszVal**



## <a name="remarks"></a>Commenti

La costante **MFNETSOURCE \_ PLAYERID** definisce il GUID per questa chiave di proprietà. L'identificatore di proprietà (PID) è zero.

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

 

 




