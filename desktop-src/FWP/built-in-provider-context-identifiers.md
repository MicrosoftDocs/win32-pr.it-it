---
title: Identificatori di contesto del provider predefiniti (Fwpmu.h)
description: I contesti provider predefiniti identificano i criteri predefiniti da usare con i socket sicuri.
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
ms.openlocfilehash: c0247b58b38de55eb67479c68e0c0955fb9d2a56a793215330366ca8ccfbe4e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951330"
---
# <a name="built-in-provider-context-identifiers"></a>Identificatori di contesto del provider predefiniti

Gli identificatori per i contesti del provider incorporati in Windows Filtering Platform (WFP) sono rappresentati da un GUID. Questi contesti provider predefiniti identificano i criteri predefiniti da usare con i socket sicuri.

Questi identificatori sono definiti come indicato di seguito.

<dl> <dt>

<span id="FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_AUTHIP"></span><span id="fwpm_provider_context_secure_socket_authip"></span>**FWPM \_ PROVIDER \_ CONTEXT \_ SECURE \_ SOCKET \_ AUTHIP**
</dt> <dd> <dl> <dt>



Authenticated Internet Protocol criteri predefiniti in modalità principale (AuthIP) per i socket sicuri.


</dt> </dl> </dd> <dt>

<span id="FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_IPSEC"></span><span id="fwpm_provider_context_secure_socket_ipsec"></span>**IPSEC SECURE \_ \_ SOCKET DEL CONTESTO \_ \_ DEL \_ PROVIDER FWPM**
</dt> <dd> <dl> <dt>



Criteri predefiniti in modalità rapida IPsec (Internet Protocol Security) per i socket sicuri.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Fwpmu.h</dt> </dl> |



 

 





