---
title: Attributo ms-DS-Logon-Time-Sync-Interval
description: Questo attributo controlla la granularità, in giorni, con cui l'ora dell'ultimo accesso per un utente o un computer, registrata nell'attributo lastLogonTimestamp, viene replicata in tutti i controller di dominio in un dominio.
ms.assetid: f1f9f1f8-df60-44b5-965d-631c4dd4ef84
ms.tgt_platform: multiple
keywords:
- Attributo MS-DS-Logon-Time-Sync-Interval Schema DI AD
- Schema AD dell'attributo msDS-LogonTimeSyncInterval
topic_type:
- apiref
api_name:
- ms-DS-Logon-Time-Sync-Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa27a1d6281eda7eea9f88a11c4ca6632422a1cfd9f0cb471aab513018c56150
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118684635"
---
# <a name="ms-ds-logon-time-sync-interval-attribute"></a>Attributo ms-DS-Logon-Time-Sync-Interval

Questo attributo controlla la granularità, in giorni, con cui l'ora dell'ultimo accesso per un utente o un computer, registrata nell'attributo lastLogonTimestamp, viene replicata in tutti i controller di dominio in un dominio.



| Voce | Valore |
|-------------------|------------------------------------------------------------------------------------------------------------|
| CN                | ms-DS-Logon-Time-Sync-Interval                                                                             |
| Ldap-Display-Name | msDS-LogonTimeSyncInterval                                                                                 |
| Dimensione              | 4 byte                                                                                                    |
| Aggiorna privilegio  | Amministratore di dominio                                                                                       |
| Frequenza di aggiornamento  | Raramente, poiché si tratta di un'impostazione di criteri, viene aggiornata solo quando si desidera una modifica nei criteri a livello di dominio. |
| Attribute-Id      | 1.2.840.113556.1.4.1784                                                                                    |
| System-Id-Guid    | ad7940f8-e43a-4a42-83bc-d688e59ea605                                                                       |
| Sintassi            | [**Enumerazione**](s-enumeration.md)                                                                       |



## <a name="implementations"></a>Implementazioni

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|----------------------------------------------|
| ID collegamento                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| Is-Single-Valued       | Vero                                         |
| Indicizzato             | Falso                                        |
| Nel catalogo globale      | Falso                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classi usate in        | [**Sam-Domain**](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|----------------------------------------------|
| ID collegamento                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| Is-Single-Valued       | Vero                                         |
| Indicizzato             | Falso                                        |
| Nel catalogo globale      | Falso                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classi usate in        | [**Sam-Domain**](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|----------------------------------------------|
| ID collegamento                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| Is-Single-Valued       | Vero                                         |
| Indicizzato             | Falso                                        |
| Nel catalogo globale      | Falso                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classi usate in        | [**Sam-Domain**](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|----------------------------------------------|
| ID collegamento                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| Is-Single-Valued       | Vero                                         |
| Indicizzato             | Falso                                        |
| Nel catalogo globale      | Falso                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classi usate in        | [**Sam-Domain**](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|----------------------------------------------|
| ID collegamento                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| Is-Single-Valued       | Vero                                         |
| Indicizzato             | Falso                                        |
| Nel catalogo globale      | Falso                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classi usate in        | [**Sam-Domain**](c-samdomain.md)<br/> |



 

 





