---
description: Specifica se il localizzatore proxy deve usare un server proxy per indirizzi locali.
ms.assetid: 384343f5-5919-44da-b8ea-0c994b4743a8
title: Proprietà MFNETSOURCE_PROXYBYPASSFORLOCAL (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9476571ddd593b7930be1aa4376a836de3d75206
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749194"
---
# <a name="mfnetsource_proxybypassforlocal-property"></a>\_Proprietà PROXYBYPASSFORLOCAL di MFNETSOURCE

Specifica se il localizzatore proxy deve usare un server proxy per indirizzi locali.



Tipo di dati

Tipo PROPVARIANT (VT)

membro PROPVARIANT

Booleano (**Long**)

VT \_ I4

**lVal**



## <a name="remarks"></a>Commenti

La costante **MFNETSOURCE \_ PROXYBYPASSFORLOCAL** definisce il GUID per la chiave della proprietà. L'identificatore di proprietà (PID) è zero.

Le applicazioni possono usare questa proprietà per configurare il localizzatore proxy durante la creazione dell'oggetto localizzatore proxy. Per impostare la proprietà, passare un puntatore **IPropertyStore** nel parametro *PProxyConfig* della funzione [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) . Il valore deve essere impostato su 0 se il server proxy deve essere utilizzato per gli indirizzi locali; in caso contrario, un valore diverso da zero configura il localizzatore proxy predefinito in modo da ignorare il server proxy per gli indirizzi locali.

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

 

 




