---
title: UAS-Compat attributo
description: Indica se la sicurezza account manager le dimensioni dei dati per rendere compatibile Active Directory con il sistema di account utente LanManager.
ms.assetid: 745e271e-28f4-4012-83a8-606d88de0221
ms.tgt_platform: multiple
keywords:
- UAS-Compat schema AD dell'attributo
- Schema AD dell'attributo uASCompat
topic_type:
- apiref
api_name:
- UAS-Compat
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72fa7a0cb7b8787a55c710f283dbcd37bbe0f6a296505c75a5335bf35ea69c34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118681540"
---
# <a name="uas-compat-attribute"></a>UAS-Compat attributo

Indica se la sicurezza account manager le dimensioni dei dati per rendere compatibile Active Directory con il sistema di account utente LanManager. Se questo valore è 0, non vengono applicati limiti. Se questo valore è 1, vengono applicati i limiti seguenti.



| Valore                          | Length                         |
|--------------------------------|--------------------------------|
| Password<br/>            | Da 0 a 14 caratteri<br/>  |
| Nome account<br/>        | Da 0 a 20 caratteri<br/>  |
| Nome dominio<br/>         | Da 0 a 15 caratteri<br/>  |
| Nome computer<br/>       | Da 0 a 15 caratteri<br/>  |
| Commenti<br/>            | Da 0 a 48 caratteri<br/>  |
| Home directory<br/>      | Da 0 a 256 caratteri<br/> |
| Percorso script<br/>         | Da 0 a 256 caratteri<br/> |
| Unità di tempo per settimana<br/> | 168 bit (21 byte)<br/> |



 



| Voce | Valore |
|-------------------|--------------------------------------|
| CN                | UAS-Compat                           |
| Ldap-Display-Name | uASCompat                            |
| Dimensione              | \-                                   |
| Privilegio di aggiornamento  | Eseguita da un amministratore.       |
| Frequenza di aggiornamento  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.155               |
| System-Id-Guid    | bf967a61-0de6-11d0-a285-00aa003049e2 |
| Sintassi            | [**Enumerazione**](s-enumeration.md) |



## <a name="implementations"></a>Implementazioni

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Voce | Valore |
|------------------------|-------------------------------------------------------|
| ID collegamento                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | Falso                                                 |
| Is-Single-Valued       | Vero                                                  |
| Indicizzato             | Falso                                                 |
| Nel catalogo globale      | Falso                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000010                                            |
| Classi usate in        | [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|-------------------------------------------------------|
| ID collegamento                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | Falso                                                 |
| Is-Single-Valued       | Vero                                                  |
| Indicizzato             | Falso                                                 |
| Nel catalogo globale      | Falso                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000010                                            |
| Classi usate in        | [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|-------------------------------------------------------|
| ID collegamento                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | Falso                                                 |
| Is-Single-Valued       | Vero                                                  |
| Indicizzato             | Falso                                                 |
| Nel catalogo globale      | Falso                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000010                                            |
| Classi usate in        | [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|-------------------------------------------------------|
| ID collegamento                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | Falso                                                 |
| Is-Single-Valued       | Vero                                                  |
| Indicizzato             | Falso                                                 |
| Nel catalogo globale      | Falso                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000010                                            |
| Classi usate in        | [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|-------------------------------------------------------|
| ID collegamento                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | Falso                                                 |
| Is-Single-Valued       | Vero                                                  |
| Indicizzato             | Falso                                                 |
| Nel catalogo globale      | Falso                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000010                                            |
| Classi usate in        | [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|-------------------------------------------------------|
| ID collegamento                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | Falso                                                 |
| Is-Single-Valued       | Vero                                                  |
| Indicizzato             | Falso                                                 |
| Nel catalogo globale      | Falso                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000010                                            |
| Classi usate in        | [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



 

 





