---
description: Valore della prima parte del campo &\# 0034;cs(User-Agent)&0034; utilizzato dall'origine di rete per \# la registrazione.
ms.assetid: b6c33cc8-ff43-4a19-a333-51a7f9b265a9
title: MFNETSOURCE_BROWSERUSERAGENT proprietà (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf46fde925dbe2d94643a0843d105726f0976ba7a84f47773ef35e32ae8dfde7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954861"
---
# <a name="mfnetsource_browseruseragent-property"></a>MFNETSOURCE \_ BROWSERUSERAGENT - proprietà

Valore della prima parte del campo "cs(User-Agent)" utilizzato dall'origine di rete per la registrazione. Le applicazioni possono impostare questa proprietà su qualsiasi valore stringa.



Tipo di dati

Tipo PROPVARIANT (vt)

membro PROPVARIANT

Stringa di caratteri wide (**WCHAR** \* )

VT \_ LPWSTR

**pwszVal**



## <a name="remarks"></a>Commenti

La costante **MFNETSOURCE \_ BROWSERUSERAGENT** definisce il GUID per questa chiave di proprietà. L'identificatore di proprietà (PID) è zero.

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
</dt> <dt>

[**MFNETSOURCE \_ PLAYERUSERAGENT**](mfnetsource-playeruseragent-property.md)
</dt> </dl>

 

 




