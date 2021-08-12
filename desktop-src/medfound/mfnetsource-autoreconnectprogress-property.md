---
description: Numero di tentativi di riconnessione dell'origine di rete alla rete.
ms.assetid: e3410e68-6358-4f00-8039-833a4ccdf7fa
title: MFNETSOURCE_AUTORECONNECTPROGRESS proprietà (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cfbf0bac147b3608145d3ef38eb328a44de1c064899a5e7800acbadfadcf709
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118243875"
---
# <a name="mfnetsource_autoreconnectprogress-property"></a>MFNETSOURCE \_ AUTORECONNECTPROGRESS - proprietà

Numero di tentativi di riconnessione dell'origine di rete alla rete.



Tipo di dati

Tipo PROPVARIANT (vt)

membro PROPVARIANT

**DWORD** (archiviato come **LONG)**

VT \_ I4

**lVal**



## <a name="remarks"></a>Commenti

La costante **MFNETSOURCE \_ AUTORECONNECTPROGRESS** definisce il GUID per questa chiave di proprietà. L'identificatore di proprietà (PID) è zero.

Questa proprietà è di sola lettura. Per recuperare questa proprietà, eseguire una query sull'origine di rete **per l'interfaccia IPropertyStore** e **chiamare IPropertyStore::GetValue**.

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

[Funzionalità dell'origine di rete](network-source-features.md)
</dt> <dt>

[Rete in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




