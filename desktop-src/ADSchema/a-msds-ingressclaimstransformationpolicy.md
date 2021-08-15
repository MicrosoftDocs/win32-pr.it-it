---
title: Attributo ms-DS-Ingress-Claims-Transformation-Policy
description: Si tratta di un collegamento a un oggetto criteri di trasformazione delle attestazioni per le attestazioni in ingresso (attestazioni che entrano in questa foresta) dal dominio trusted.
ms.assetid: 67f87782-85ed-41bb-a60d-f6c11fcda80e
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo ms-DS-Ingress-Claims-Transformation-Policy
- Schema AD dell'attributo msDS-IngressClaimsTransformationPolicy
topic_type:
- apiref
api_name:
- ms-DS-Ingress-Claims-Transformation-Policy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52d631e2f342302f8089a43a329ac3982cf7874b46ab0f60d3e4399855f573e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118960750"
---
# <a name="ms-ds-ingress-claims-transformation-policy-attribute"></a>Attributo ms-DS-Ingress-Claims-Transformation-Policy

Si tratta di un collegamento a un oggetto criteri di trasformazione delle attestazioni per le attestazioni in ingresso (attestazioni che entrano in questa foresta) dal dominio trusted. Questo è applicabile solo per un trust tra foreste in uscita o bidirezionale. Se questo collegamento è assente, tutte le attestazioni in ingresso vengono eliminate.



| Voce | Valore |
|-------------------|--------------------------------------------|
| CN                | ms-DS-Ingress-Claims-Transformation-Policy |
| Ldap-Display-Name | msDS-IngressClaimsTransformationPolicy     |
| Dimensione              | \-                                         |
| Aggiorna privilegio  | \-                                         |
| Frequenza di aggiornamento  | \-                                         |
| Attribute-Id      | 1.2.840.113556.1.4.2191                    |
| System-Id-Guid    | 86284c08-0c6e-1540-8b15-75147d23d20d       |
| Sintassi            | [**Object(DS-DN)**](s-object-ds-dn.md)    |



## <a name="implementations"></a>Implementazioni

-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|------------------------------------------------------|
| ID collegamento                | 2190                                                 |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| A valore singolo       | Vero                                                 |
| Indicizzato             | Falso                                                |
| Nel catalogo globale      | Falso                                                |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Classi usate in        | [**Dominio trusted**](c-trusteddomain.md)<br/> |



 

 





