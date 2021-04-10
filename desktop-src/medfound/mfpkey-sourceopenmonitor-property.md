---
description: Contiene un puntatore all'interfaccia IMFSourceOpenMonitor delle applicazioni.
ms.assetid: 5b94ae87-91fc-49d6-9355-83327cfdb3f3
title: Proprietà MFPKEY_SourceOpenMonitor (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a49826ee16a733993b9052e12d9e6fcd5003410
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131226"
---
# <a name="mfpkey_sourceopenmonitor-property"></a>\_Proprietà SourceOpenMonitor di MFPKEY

Contiene un puntatore all'interfaccia [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) dell'applicazione.



Tipo di dati

Tipo PROPVARIANT (VT)

membro PROPVARIANT

Puntatore **IUnknown**

VT \_ sconosciuto

**punkVal**



## <a name="remarks"></a>Commenti

Le applicazioni possono passare questa proprietà al resolver di origine per ottenere le notifiche degli eventi dall'origine di rete.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




