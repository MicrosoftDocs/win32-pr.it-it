---
description: Contiene un puntatore all'interfaccia IMFSourceOpenMonitor delle applicazioni.
ms.assetid: 5b94ae87-91fc-49d6-9355-83327cfdb3f3
title: MFPKEY_SourceOpenMonitor proprietà (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45594e1929e66982d3e518c4ba098d2ca4b22e854e033dc69025aaf3ec5d5cc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117872992"
---
# <a name="mfpkey_sourceopenmonitor-property"></a>MFPKEY \_ SourceOpenMonitor - proprietà

Contiene un puntatore all'interfaccia [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) dell'applicazione.



Tipo di dati

Tipo PROPVARIANT (vt)

membro PROPVARIANT

**Puntatore IUnknown**

VT \_ UNKNOWN

**valvalore**



## <a name="remarks"></a>Commenti

Le applicazioni possono passare questa proprietà al resolver di origine per ottenere notifiche degli eventi dall'origine di rete.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 




