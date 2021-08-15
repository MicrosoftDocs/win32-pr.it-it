---
description: Elenco di URL a cui l'origine di rete invierà le informazioni di registrazione.
ms.assetid: 772c5b57-273d-4289-9229-ef7a199c6473
title: MFNETSOURCE_LOGURL proprietà (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b855475e17264682ffc49a391894bb6acc6a721712b8ce6e4c01d98b1d216d48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874635"
---
# <a name="mfnetsource_logurl-property"></a>MFNETSOURCE \_ LOGURL - proprietà

Elenco di URL a cui l'origine di rete invierà le informazioni di registrazione.



Tipo di dati

Tipo PROPVARIANT (vt)

membro PROPVARIANT

Matrice di stringhe di caratteri wide (**CALPWSTR**)

VT \_ VECTOR \| VT \_ LPWSTR

**calpwstr**



## <a name="remarks"></a>Commenti

La costante **MFNETSOURCE \_ LOGURL** definisce il GUID per questa chiave di proprietà. L'identificatore di proprietà (PID) è zero.

Le applicazioni possono usare questa proprietà per configurare l'origine di rete. Per impostare la proprietà, passare un **puntatore IPropertyStore** al resolver di origine. Per altre informazioni, vedere [Configurazione di un'origine multimediale.](configuring-a-media-source.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> <dt>

[Rete in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




