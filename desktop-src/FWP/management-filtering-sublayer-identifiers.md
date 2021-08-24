---
title: Filtro degli identificatori dei sottolivelli (Fwpmu.h)
description: Costanti dell'identificatore del livello secondario di filtro dell'API WFP.
ms.assetid: 4c8dbe35-e84b-4490-bf7a-7ff8b94e2022
topic_type:
- apiref
api_name:
- FWPM_SUBLAYER_EDGE_TRAVERSAL / FWPM_SUBLAYER_TEREDO
- FWPM_SUBLAYER_INSPECTION
- FWPM_SUBLAYER_IPSEC_DOSP
- FWPM_SUBLAYER_IPSEC_FORWARD_OUTBOUND_TUNNEL
- FWPM_SUBLAYER_IPSEC_TUNNEL
- FWPM_SUBLAYER_LIPS
- FWPM_SUBLAYER_RPC_AUDIT
- FWPM_SUBLAYER_SECURE_SOCKET
- FWPM_SUBLAYER_TCP_CHIMNEY_OFFLOAD
- FWPM_SUBLAYER_TCP_TEMPLATES
- FWPM_SUBLAYER_UNIVERSAL
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d597fa1b75f6c965da9cf8d71bcc3e729d0b0b2f4f4220c984a1be8c94c09d39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068881"
---
# <a name="filtering-sublayer-identifiers"></a>Filtro degli identificatori dei sottolivelli

Gli Windows del livello secondario della piattaforma di filtro dei filtri di sicurezza (WFP, Windows Filtering Platform) sono rappresentati da un GUID.

Questi identificatori sono definiti nel modo seguente.

<dl> <dt>

<span id="FWPM_SUBLAYER_EDGE_TRAVERSAL________________________FWPM_SUBLAYER_TEREDO"></span><span id="fwpm_sublayer_edge_traversal________________________fwpm_sublayer_teredo"></span>**FWPM \_ SUBLAYER \_ EDGE \_ TRAVERSAL / FWPM \_ SUBLAYER \_ TEREDO**
</dt> <dd> <dl> <dt>



I filtri di attraversamento dei bordi vengono aggiunti a questo sottolivelli.

> [!Note]  
> Per Windows 7 e versioni successive, usare **FWPM \_ SUBLAYER \_ EDGE \_ TRAVERSAL**.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_INSPECTION"></span><span id="fwpm_sublayer_inspection"></span>**ISPEZIONE DEL SOTTOLIVELLI FWPM \_ \_**
</dt> <dd> <dl> <dt>



Si tratta del sottolivelli più basso ponderato. Viene usato solo per i filtri di ispezione.


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_IPSEC_DOSP"></span><span id="fwpm_sublayer_ipsec_dosp"></span>**FWPM \_ SUBLAYER \_ IPSEC \_ DOSP**
</dt> <dd> <dl> <dt>



A questo livello secondario vengono aggiunti filtri protezione DoS IPsec.

> [!Note]  
> Disponibile solo in Windows Vista con SP1, Windows Server 2008 e versioni successive.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_IPSEC_FORWARD_OUTBOUND_TUNNEL"></span><span id="fwpm_sublayer_ipsec_forward_outbound_tunnel"></span>**FWPM \_ SUBLAYER \_ IPSEC \_ FORWARD \_ OUTBOUND \_ TUNNEL**
</dt> <dd> <dl> <dt>



I filtri del tunnel in uscita di inoltro IPsec vengono aggiunti a questo livello secondario.

> [!Note]  
> Disponibile solo in Windows 7, Windows Server 2008 R2 e versioni successive.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_IPSEC_TUNNEL"></span><span id="fwpm_sublayer_ipsec_tunnel"></span>**FWPM \_ SUBLAYER \_ IPSEC \_ TUNNEL**
</dt> <dd> <dl> <dt>



I filtri del tunnel IPsec vengono aggiunti a questo sottolivelli.


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_LIPS"></span><span id="fwpm_sublayer_lips"></span>**FWPM \_ SUBLAYER \_ PIÙ RECENTE**
</dt> <dd> <dl> <dt>



A questo sottolivelli vengono aggiunti filtri IPsec legacy.


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_RPC_AUDIT"></span><span id="fwpm_sublayer_rpc_audit"></span>**CONTROLLO \_ RPC DEL SUBLAYER FWPM \_ \_**
</dt> <dd> <dl> <dt>



A questo livello secondario vengono aggiunti filtri di controllo RPC. Questi filtri controllano le chiamate RPC in ingresso come parte di C2 e la conformità ai criteri comuni.


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_SECURE_SOCKET"></span><span id="fwpm_sublayer_secure_socket"></span>**FWPM \_ SUBLAYER \_ SECURE \_ SOCKET**
</dt> <dd> <dl> <dt>



I filtri secure socket vengono aggiunti a questo sottolivente.


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_TCP_CHIMNEY_OFFLOAD"></span><span id="fwpm_sublayer_tcp_chimney_offload"></span>**FWPM \_ SUBLAYER \_ TCP \_ CHIMNEY \_ OFFLOAD**
</dt> <dd> <dl> <dt>



TCP Chimney Offload filtri vengono aggiunti a questo sottolivelli.


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_TCP_TEMPLATES______________________"></span><span id="fwpm_sublayer_tcp_templates______________________"></span>**MODELLI \_ TCP DEL SUBLAYER FWPM \_ \_** 
</dt> <dd> <dl> <dt>



A questo sottolivelli vengono aggiunti filtri di modello TCP.

> [!Note]  
> Disponibile solo in Windows 8, Windows Server 2012 e versioni successive.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_UNIVERSAL"></span><span id="fwpm_sublayer_universal"></span>**FWPM \_ SUBLAYER \_ UNIVERSAL**
</dt> <dd> <dl> <dt>



Questo sottolivelli ospita tutti i filtri non assegnati ad altri sottolivelli.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Fwpmu.h</dt> </dl> |



 

 





