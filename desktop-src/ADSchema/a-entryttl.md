---
title: Attributo Entry-TTL
description: Questo attributo operativo viene gestito dal server e sembra essere presente in ogni voce dinamica.
ms.assetid: cac0e52e-243d-4822-9419-2af8b9352cee
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo Entry-TTL
- Schema AD dell'attributo entryTTL
topic_type:
- apiref
api_name:
- Entry-TTL
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbcd3e06304824ba51431b00b6a5b90d24d7719194dd84974470a101d5f6a1c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118961560"
---
# <a name="entry-ttl-attribute"></a>Attributo Entry-TTL

Questo attributo operativo viene gestito dal server e sembra essere presente in ogni voce dinamica. L'attributo non è presente quando la voce non contiene la classe di oggetti dynamicObject. Il valore di questo attributo è il tempo, in secondi, in cui la voce continuerà a esistere prima di scomparire dalla directory. In assenza di operazioni di "aggiornamento", i valori restituiti leggendo l'attributo in due ricerche successive sono garantiti come non increati. Il valore minimo consentito è 0, che indica che la voce potrebbe scomparire senza avviso. L'attributo è contrassegnato come NO-USER-MODIFICATION perché può essere modificato solo tramite l'operazione di aggiornamento.



| Voce | Valore |
|-------------------|---------------------------------------------|
| CN                | Voce TTL                                   |
| Ldap-Display-Name | entryTTL                                    |
| Dimensione              | 4 byte. Massimo = 1 anno, valore predefinito = 1 giorno. |
| Aggiorna privilegio  | \-                                          |
| Frequenza di aggiornamento  | \-                                          |
| Attribute-Id      | 1.3.6.1.4.1.1466.101.119.3                  |
| System-Id-Guid    | d213decc-d81a-4384-aac2-dcfcfd631cf8        |
| Sintassi            | [**Enumerazione**](s-enumeration.md)        |



## <a name="implementations"></a>Implementazioni

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adam**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|------------------------------------------------------|
| ID collegamento                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| Is-Single-Valued       | Vero                                                 |
| Indicizzato             | Falso                                                |
| Nel catalogo globale      | Falso                                                |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 31557600                                             |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000014                                           |
| Classi usate in        | [**Oggetto dinamico**](c-dynamicobject.md)<br/> |



## <a name="adam"></a>Adam



| Voce | Valore |
|------------------------|------------------------------------------------------|
| ID collegamento                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| Is-Single-Valued       | Vero                                                 |
| Indicizzato             | Falso                                                |
| Nel catalogo globale      | Falso                                                |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 31557600                                             |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000014                                           |
| Classi usate in        | [**Oggetto dinamico**](c-dynamicobject.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|------------------------------------------------------|
| ID collegamento                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| Is-Single-Valued       | Vero                                                 |
| Indicizzato             | Falso                                                |
| Nel catalogo globale      | Falso                                                |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 31557600                                             |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000014                                           |
| Classi usate in        | [**Oggetto dinamico**](c-dynamicobject.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|------------------------------------------------------|
| ID collegamento                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| Is-Single-Valued       | Vero                                                 |
| Indicizzato             | Falso                                                |
| Nel catalogo globale      | Falso                                                |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 31557600                                             |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000014                                           |
| Classi usate in        | [**Oggetto dinamico**](c-dynamicobject.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|------------------------------------------------------|
| ID collegamento                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| Is-Single-Valued       | Vero                                                 |
| Indicizzato             | Falso                                                |
| Nel catalogo globale      | Falso                                                |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 31557600                                             |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000014                                           |
| Classi usate in        | [**Oggetto dinamico**](c-dynamicobject.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|------------------------------------------------------|
| ID collegamento                | \-                                                   |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| Is-Single-Valued       | Vero                                                 |
| Indicizzato             | Falso                                                |
| Nel catalogo globale      | Falso                                                |
| NT-Security-Descriptor | O:BAG:BAD:S:                                         |
| Range-Lower            | 0                                                    |
| Range-Upper            | 31557600                                             |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000014                                           |
| Classi usate in        | [**Oggetto dinamico**](c-dynamicobject.md)<br/> |



 

 





