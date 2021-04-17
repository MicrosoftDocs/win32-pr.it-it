---
title: attributo ms-DS-ingress-Claims-Transformation-Policy
description: Si tratta di un collegamento a un oggetto Criteri di trasformazione delle attestazioni per le attestazioni in ingresso (attestazioni che accedono a questa foresta) dal dominio trusted.
ms.assetid: 67f87782-85ed-41bb-a60d-f6c11fcda80e
ms.tgt_platform: multiple
keywords:
- ms-DS-ingress-Claims-Transformation-schema AD dell'attributo Policy
- attributo msDS-IngressClaimsTransformationPolicy-schema AD
topic_type:
- apiref
api_name:
- ms-DS-Ingress-Claims-Transformation-Policy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e50e3c187a4cb3b2a465257b408a1f5603c756ba
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519853"
---
# <a name="ms-ds-ingress-claims-transformation-policy-attribute"></a>attributo ms-DS-ingress-Claims-Transformation-Policy

Si tratta di un collegamento a un oggetto Criteri di trasformazione delle attestazioni per le attestazioni in ingresso (attestazioni che accedono a questa foresta) dal dominio trusted. Questa operazione è applicabile solo per un trust tra foreste in uscita o bidirezionale. Se questo collegamento è assente, vengono eliminate tutte le attestazioni in ingresso.



| Voce | Valore |
|-------------------|--------------------------------------------|
| CN                | ms-DS-ingress-Claims-Transformation-Policy |
| LDAP-Display-Name | msDS-IngressClaimsTransformationPolicy     |
| Dimensione              | \-                                         |
| Privilegio aggiornamento  | \-                                         |
| Frequenza di aggiornamento  | \-                                         |
| Attribute-Id      | 1.2.840.113556.1.4.2191                    |
| System-ID-GUID    | 86284c08-0c6e-1540-8b15-75147d23d20d       |
| Sintassi            | [**Object(DS-DN)**](s-object-ds-dn.md)    |



## <a name="implementations"></a>Implementazioni

-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|------------------------------------------------------|
| ID collegamento                | 2190                                                 |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| È a valore singolo       | Vero                                                 |
| Indicizzato             | Falso                                                |
| Nel catalogo globale      | Falso                                                |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Classi utilizzate in        | [**Dominio trusted**](c-trusteddomain.md)<br/> |



 

 





