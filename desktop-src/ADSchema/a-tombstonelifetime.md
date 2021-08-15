---
title: Tombstone-Lifetime attributo
description: Numero di giorni prima che un oggetto eliminato venga rimosso dai servizi directory.
ms.assetid: 58898097-912b-4fe6-b6ea-91f49aaa2b1b
ms.tgt_platform: multiple
keywords:
- Tombstone-Lifetime schema AD dell'attributo
- Schema AD dell'attributo tombstoneLifetime
topic_type:
- apiref
api_name:
- Tombstone-Lifetime
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c96d440b82f488e7968f787ae52d9f431350bee6050bd50b385f5751f51e76a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644951"
---
# <a name="tombstone-lifetime-attribute"></a>Tombstone-Lifetime attributo

Numero di giorni prima che un oggetto eliminato venga rimosso dai servizi directory. Ciò consente di rimuovere oggetti dai server replicati e impedire ai ripristini di introdurre nuovamente un oggetto eliminato. Questo valore si trova nell'oggetto Servizio directory nella scheda di interfaccia di rete di configurazione.



| Voce | Valore |
|-------------------|-----------------------------------------------------------|
| CN                | Tombstone-Lifetime                                        |
| Ldap-Display-Name | tombstoneLifetime                                         |
| Dimensione              | 4 byte. Il valore predefinito è 60 giorni quando non viene immesso alcun valore. |
| Aggiorna privilegio  | \-                                                        |
| Frequenza di aggiornamento  | \-                                                        |
| Attribute-Id      | 1.2.840.113556.1.2.54                                     |
| System-Id-Guid    | 16c3a860-1273-11d0-a060-00aa006c33ed                      |
| Sintassi            | [**Enumerazione**](s-enumeration.md)                      |



## <a name="implementations"></a>Implementazioni

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adam**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Voce | Valore |
|------------------------|--------------------------------------------------|
| ID collegamento                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | Falso                                            |
| A valore singolo       | Vero                                             |
| Indicizzato             | Falso                                            |
| Nel catalogo globale      | Falso                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classi usate in        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|--------------------------------------------------|
| ID collegamento                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | Falso                                            |
| A valore singolo       | Vero                                             |
| Indicizzato             | Falso                                            |
| Nel catalogo globale      | Falso                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classi usate in        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



## <a name="adam"></a>Adam



| Voce | Valore |
|------------------------|--------------------------------------------------|
| ID collegamento                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | Falso                                            |
| A valore singolo       | Vero                                             |
| Indicizzato             | Falso                                            |
| Nel catalogo globale      | Falso                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classi usate in        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|--------------------------------------------------|
| ID collegamento                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | Falso                                            |
| Is-Single-Valued       | Vero                                             |
| Indicizzato             | Falso                                            |
| Nel catalogo globale      | Falso                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classi usate in        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|--------------------------------------------------|
| ID collegamento                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | Falso                                            |
| Is-Single-Valued       | Vero                                             |
| Indicizzato             | Falso                                            |
| Nel catalogo globale      | Falso                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classi usate in        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|--------------------------------------------------|
| ID collegamento                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | Falso                                            |
| Is-Single-Valued       | Vero                                             |
| Indicizzato             | Falso                                            |
| Nel catalogo globale      | Falso                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classi usate in        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|--------------------------------------------------|
| ID collegamento                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | Falso                                            |
| Is-Single-Valued       | Vero                                             |
| Indicizzato             | Falso                                            |
| Nel catalogo globale      | Falso                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classi usate in        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



 

 





