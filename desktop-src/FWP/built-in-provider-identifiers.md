---
title: Identificatori di provider predefiniti (Fwpmu.h)
description: Gli identificatori per i provider incorporati in Windows Filtering Platform (WFP) sono rappresentati da un GUID.
ms.assetid: 61bc1e2d-f6ee-45db-892f-c49680d27072
topic_type:
- apiref
api_name:
- FWPM_PROVIDER_IKEEXT
- FWPM_PROVIDER_IPSEC_DOS_CONFIG
- FWPM_PROVIDER_TCP_CHIMNEY_OFFLOAD
- FWPM_PROVIDER_TCP_TEMPLATES
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8982fe6ebbe3f4cf5135f2b67f07826ddf9d3f970ca0568c7095931c617cdce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951310"
---
# <a name="built-in-provider-identifiers"></a>Identificatori di provider predefiniti

Gli identificatori per i provider incorporati in Windows Filtering Platform (WFP) sono rappresentati da un GUID.

Questi identificatori sono definiti nel modo seguente.

<dl> <dt>

<span id="FWPM_PROVIDER_IKEEXT"></span><span id="fwpm_provider_ikeext"></span>**FWPM \_ PROVIDER \_ IKEEXT**
</dt> <dd> <dl> <dt>

{10ad9216-ccde-456c-8b16-e9f04e60a90b}
</dt> <dt>



Usato per identificare tutti i filtri aggiunti da IKE/AuthIP.


</dt> </dl> </dd> <dt>

<span id="FWPM_PROVIDER_IPSEC_DOS_CONFIG"></span><span id="fwpm_provider_ipsec_dos_config"></span>**CONFIGURAZIONE \_ \_ DOS IPSEC DEL PROVIDER \_ FWPM \_**
</dt> <dd> <dl> <dt>

{3c6c0519-c05c-4bb9-8338-2327814ce8bf}
</dt> <dt>



Usato per identificare tutti i filtri aggiunti da Protezione DoS IPsec.

> [!Note]  
> Disponibile solo in Windows 7 e Windows Server 2008 R2.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_PROVIDER_TCP_CHIMNEY_OFFLOAD"></span><span id="fwpm_provider_tcp_chimney_offload"></span>**FWPM \_ PROVIDER \_ TCP \_ CHIMNEY \_ OFFLOAD**
</dt> <dd> <dl> <dt>

{896aa19e-9a34-4bcb-ae79-beb9127c84b9}
</dt> <dt>



Usato per identificare tutti i filtri aggiunti da TCP Chimney Offload.


</dt> </dl> </dd> <dt>

<span id="FWPM_PROVIDER_TCP_TEMPLATES"></span><span id="fwpm_provider_tcp_templates"></span>**MODELLI TCP DEL PROVIDER FWPM \_ \_ \_**
</dt> <dd> <dl> <dt>

{76cfcd30-3394-432d-bed3-441ae50e63c3}
</dt> <dt>



Consente di identificare tutti i filtri aggiunti dai modelli TCP.

> [!Note]  
> Disponibile solo in Windows 8 e Windows Server 2012.

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Fwpmu.h</dt> </dl> |



 

 





