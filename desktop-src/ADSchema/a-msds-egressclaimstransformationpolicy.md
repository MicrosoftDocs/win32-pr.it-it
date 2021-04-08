---
title: attributo ms-DS-uscita-Claims-Transformation-Policy
description: Si tratta di un collegamento a un oggetto Criteri di trasformazione delle attestazioni per le attestazioni in uscita (attestazioni che lasciano questa foresta) al dominio trusted.
ms.assetid: 693ebb45-e90c-4629-8afc-f048c83b4b95
ms.tgt_platform: multiple
keywords:
- ms-DS-uscita-Claims-Transformation-schema AD dell'attributo Policy
- attributo msDS-EgressClaimsTransformationPolicy-schema AD
topic_type:
- apiref
api_name:
- ms-DS-Egress-Claims-Transformation-Policy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3978944b6ae85fcc5fd33682abec7dd3fff0057
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103965268"
---
# <a name="ms-ds-egress-claims-transformation-policy-attribute"></a>attributo ms-DS-uscita-Claims-Transformation-Policy

Si tratta di un collegamento a un oggetto Criteri di trasformazione delle attestazioni per le attestazioni in uscita (attestazioni che lasciano questa foresta) al dominio trusted. Questa operazione è applicabile solo a un trust tra foreste in ingresso o bidirezionale. Quando questo collegamento non è presente, tutte le attestazioni possono essere in uscita così come sono.



| Voce | Valore |
|-------------------|-------------------------------------------|
| CN                | ms-DS-uscita-Claims-Transformation-Policy |
| LDAP-Display-Name | msDS-EgressClaimsTransformationPolicy     |
| Dimensione              | \-                                        |
| Privilegio aggiornamento  | \-                                        |
| Frequenza di aggiornamento  | \-                                        |
| Attribute-Id      | 1.2.840.113556.1.4.2192                   |
| System-ID-GUID    | c137427e-9a73-b040-9190-1b095bb43288      |
| Sintassi            | [**Object(DS-DN)**](s-object-ds-dn.md)   |



## <a name="implementations"></a>Implementazioni

-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|------------------------------------------------------|
| ID collegamento                | 2192                                                 |
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



 

 





