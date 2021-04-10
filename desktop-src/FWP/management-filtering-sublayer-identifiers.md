---
title: Filtraggio degli identificatori di sottolivello (Fwpmu. h)
description: Gestione API PAM filtro delle costanti dell'identificatore di sottolivello.
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
ms.openlocfilehash: e015d590c19395987bbd47d1c3c4b918296ab5f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874301"
---
# <a name="filtering-sublayer-identifiers"></a>Filtraggio degli identificatori di sottolivello

Gli identificatori del sottolivello Windows Filtering Platform (WFP) sono rappresentati da un GUID.

Questi identificatori sono definiti nel modo seguente.

<dl> <dt>

<span id="FWPM_SUBLAYER_EDGE_TRAVERSAL________________________FWPM_SUBLAYER_TEREDO"></span><span id="fwpm_sublayer_edge_traversal________________________fwpm_sublayer_teredo"></span>**FWPM sublayer \_ \_ Edge \_ Traversal/FWPM \_ sottolivello \_ TEREDO**
</dt> <dd> <dl> <dt>



I filtri di attraversamento bordi vengono aggiunti a questo sottolivello.

> [!Note]  
> Per Windows 7 e versioni successive, usare l' **\_ \_ \_ attraversamento dei confini del sottolivello FWPM**.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_INSPECTION"></span><span id="fwpm_sublayer_inspection"></span>**\_ispezione del SOTTOLIVELLO FWPM \_**
</dt> <dd> <dl> <dt>



Si tratta del sottolivello ponderato più basso. Viene usato solo per i filtri di ispezione.


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_IPSEC_DOSP"></span><span id="fwpm_sublayer_ipsec_dosp"></span>**\_DoSP IPSec FWPM SUBlayer \_ \_**
</dt> <dd> <dl> <dt>



I filtri di protezione DoS IPsec vengono aggiunti a questo sottolivello.

> [!Note]  
> Disponibile solo in Windows Vista con SP1, Windows Server 2008 e versioni successive.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_IPSEC_FORWARD_OUTBOUND_TUNNEL"></span><span id="fwpm_sublayer_ipsec_forward_outbound_tunnel"></span>**\_ \_ \_ tunnel in uscita da IPSec in \_ uscita \_ del sottolivello FWPM**
</dt> <dd> <dl> <dt>



I filtri di tunneling in uscita IPsec vengono aggiunti a questo sottolivello.

> [!Note]  
> Disponibile solo in Windows 7, Windows Server 2008 R2 e versioni successive.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_IPSEC_TUNNEL"></span><span id="fwpm_sublayer_ipsec_tunnel"></span>**\_tunnel IPSec del SOTTOLIVELLO FWPM \_ \_**
</dt> <dd> <dl> <dt>



I filtri del tunnel IPsec vengono aggiunti a questo sottolivello.


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_LIPS"></span><span id="fwpm_sublayer_lips"></span>**\_labbri sottostrato FWPM \_**
</dt> <dd> <dl> <dt>



I filtri IPsec legacy vengono aggiunti a questo sottolivello.


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_RPC_AUDIT"></span><span id="fwpm_sublayer_rpc_audit"></span>**\_controllo RPC SOTTOLIVELLO FWPM \_ \_**
</dt> <dd> <dl> <dt>



I filtri di controllo RPC vengono aggiunti a questo sottolivello. Questi filtri controllano le chiamate in ingresso RPC come parte di C2 e la conformità ai criteri comuni.


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_SECURE_SOCKET"></span><span id="fwpm_sublayer_secure_socket"></span>**\_socket sicuro del SOTTOLIVELLO FWPM \_ \_**
</dt> <dd> <dl> <dt>



I filtri socket protetti vengono aggiunti a questo sottolivello.


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_TCP_CHIMNEY_OFFLOAD"></span><span id="fwpm_sublayer_tcp_chimney_offload"></span>**\_ \_ TCP \_ Chimney \_ OFFLOAD di FWPM sublayer**
</dt> <dd> <dl> <dt>



I filtri TCP Chimney Offload vengono aggiunti a questo sottolivello.


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_TCP_TEMPLATES______________________"></span><span id="fwpm_sublayer_tcp_templates______________________"></span>**\_modelli TCP del SOTTOLIVELLO FWPM \_ \_** 
</dt> <dd> <dl> <dt>



I filtri dei modelli TCP vengono aggiunti a questo sottolivello.

> [!Note]  
> Disponibile solo in Windows 8, Windows Server 2012 e versioni successive.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_SUBLAYER_UNIVERSAL"></span><span id="fwpm_sublayer_universal"></span>**FWPM \_ sublayer \_ universale**
</dt> <dd> <dl> <dt>



Questo sottolivello ospita tutti i filtri che non sono assegnati ad alcun altro sottolivello.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Fwpmu. h</dt> </dl> |



 

 





