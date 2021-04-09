---
description: Specifica l'impostazione di configurazione per il localizzatore proxy predefinito.
ms.assetid: 85f2bd02-8a2f-46b5-b765-1a0bc5b6ccc3
title: Proprietà MFNETSOURCE_PROXYSETTINGS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1330773ab33674e58ef07b95a53c4493e6e6f6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130710"
---
# <a name="mfnetsource_proxysettings-property"></a>\_Proprietà PROXYSETTINGS di MFNETSOURCE

Specifica l'impostazione di configurazione per il localizzatore proxy predefinito. Il valore di questa proprietà è un membro dell'enumerazione [**MFNET \_ PROXYSETTINGS**](/windows/desktop/api/mfidl/ne-mfidl-mfnet_proxysettings) .



Tipo di dati

Tipo PROPVARIANT (VT)

membro PROPVARIANT

**LONG**

VT \_ I4

**lVal**



## <a name="remarks"></a>Commenti

La costante **MFNETSOURCE \_ PROXYSETTINGS** definisce il GUID per la chiave della proprietà. L'identificatore di proprietà (PID) è zero.

Le applicazioni possono usare questa proprietà per configurare il localizzatore proxy durante la creazione dell'oggetto localizzatore proxy predefinito. Per impostare la proprietà, passare un puntatore **IPropertyStore** nel parametro *PProxyConfig* della funzione [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Rete in Media Foundation](networking-in-media-foundation.md)
</dt> <dt>

[Supporto del proxy per le origini di rete](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




