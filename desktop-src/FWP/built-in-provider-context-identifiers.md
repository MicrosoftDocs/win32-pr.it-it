---
title: Identificatori di contesto del provider predefiniti (Fwpmu. h)
description: I contesti provider predefiniti identificano i criteri predefiniti da usare con i socket protetti.
ms.assetid: 439a5abc-08ac-4514-a126-d738e5311003
topic_type:
- apiref
api_name:
- FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_AUTHIP
- FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_IPSEC
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 942ed1d21d2acd46f0dc6b303049e0936e3cf63d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475106"
---
# <a name="built-in-provider-context-identifiers"></a>Identificatori di contesto del provider predefiniti

Gli identificatori per i contesti del provider incorporati in Windows Filtering Platform (WFP) sono rappresentati da un GUID. Questi contesti provider predefiniti identificano i criteri predefiniti da usare con i socket protetti.

Questi identificatori sono definiti nel modo seguente.

<dl> <dt>

<span id="FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_AUTHIP"></span><span id="fwpm_provider_context_secure_socket_authip"></span>**\_ \_ \_ \_ AUTHIP socket sicuro del contesto del provider FWPM \_**
</dt> <dd> <dl> <dt>



Authenticated Internet Protocol (AuthIP) criterio predefinito della modalità principale per i socket protetti.


</dt> </dl> </dd> <dt>

<span id="FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_IPSEC"></span><span id="fwpm_provider_context_secure_socket_ipsec"></span>**\_ \_ \_ \_ IPSec socket sicuro del contesto del provider FWPM \_**
</dt> <dd> <dl> <dt>



Criteri predefiniti della modalità rapida IPsec (Internet Protocol Security) per i socket protetti.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Fwpmu. h</dt> </dl> |



 

 





