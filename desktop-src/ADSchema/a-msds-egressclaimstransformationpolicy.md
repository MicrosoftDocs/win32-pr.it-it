---
title: Attributo ms-DS-Egress-Claims-Transformation-Policy
description: Si tratta di un collegamento a un oggetto criteri di trasformazione delle attestazioni per le attestazioni in uscita (attestazioni che lasciano questa foresta) al dominio trusted.
ms.assetid: 693ebb45-e90c-4629-8afc-f048c83b4b95
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo ms-DS-Egress-Claims-Transformation-Policy
- Schema AD dell'attributo msDS-EgressClaimsTransformationPolicy
topic_type:
- apiref
api_name:
- ms-DS-Egress-Claims-Transformation-Policy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99ec71308c0ebc17942b3400d8ddd9e87ff88ea29d4f21e93047c3aa80f77128
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118014654"
---
# <a name="ms-ds-egress-claims-transformation-policy-attribute"></a>Attributo ms-DS-Egress-Claims-Transformation-Policy

Si tratta di un collegamento a un oggetto criteri di trasformazione delle attestazioni per le attestazioni in uscita (attestazioni che lasciano questa foresta) al dominio trusted. Questo è applicabile solo per un trust tra foreste in ingresso o bidirezionale. Quando questo collegamento non è presente, tutte le attestazioni possono essere in uscita così come sono.



| Voce | Valore |
|-------------------|-------------------------------------------|
| CN                | ms-DS-Egress-Claims-Transformation-Policy |
| Ldap-Display-Name | msDS-EgressClaimsTransformationPolicy     |
| Dimensione              | \-                                        |
| Aggiorna privilegio  | \-                                        |
| Frequenza di aggiornamento  | \-                                        |
| Attribute-Id      | 1.2.840.113556.1.4.2192                   |
| System-Id-Guid    | c137427e-9a73-b040-9190-1b095bb43288      |
| Sintassi            | [**Object(DS-DN)**](s-object-ds-dn.md)   |



## <a name="implementations"></a>Implementazioni

-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|------------------------------------------------------|
| ID collegamento                | 2192                                                 |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| Is-Single-Valued       | Vero                                                 |
| Indicizzato             | Falso                                                |
| Nel catalogo globale      | Falso                                                |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Classi usate in        | [**Dominio trusted**](c-trusteddomain.md)<br/> |



 

 





