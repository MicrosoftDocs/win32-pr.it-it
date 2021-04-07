---
title: Attributo Tombstone-Lifetime
description: Il numero di giorni prima che un oggetto eliminato venga rimosso dai servizi directory.
ms.assetid: 58898097-912b-4fe6-b6ea-91f49aaa2b1b
ms.tgt_platform: multiple
keywords:
- Schema AD Tombstone-Lifetime attribute
- Schema AD dell'attributo tombstoneLifetime
topic_type:
- apiref
api_name:
- Tombstone-Lifetime
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb2bd0b7b970270c626437ee65288fd07bf48272
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103875506"
---
# <a name="tombstone-lifetime-attribute"></a>Attributo Tombstone-Lifetime

Il numero di giorni prima che un oggetto eliminato venga rimosso dai servizi directory. Questa operazione consente di rimuovere oggetti dai server replicati e di impedire che i ripristini riintroducano un oggetto eliminato. Questo valore si trova nell'oggetto servizio directory nella scheda di interfaccia di rete di configurazione.



| Voce | Valore |
|-------------------|-----------------------------------------------------------|
| CN                | Tombstone-Lifetime                                        |
| LDAP-Display-Name | tombstoneLifetime                                         |
| Dimensione              | 4 byte. Il valore predefinito è 60 giorni quando non viene immesso alcun valore. |
| Privilegio aggiornamento  | \-                                                        |
| Frequenza di aggiornamento  | \-                                                        |
| Attribute-Id      | 1.2.840.113556.1.2.54                                     |
| System-ID-GUID    | 16c3a860-1273-11d0-a060-00aa006c33ed                      |
| Sintassi            | [**Enumerazione**](s-enumeration.md)                      |



## <a name="implementations"></a>Implementazioni

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam)
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
| È a valore singolo       | Vero                                             |
| Indicizzato             | Falso                                            |
| Nel catalogo globale      | Falso                                            |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classi utilizzate in        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|--------------------------------------------------|
| ID collegamento                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | Falso                                            |
| È a valore singolo       | Vero                                             |
| Indicizzato             | Falso                                            |
| Nel catalogo globale      | Falso                                            |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classi utilizzate in        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



## <a name="adam"></a>ADAM



| Voce | Valore |
|------------------------|--------------------------------------------------|
| ID collegamento                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | Falso                                            |
| È a valore singolo       | Vero                                             |
| Indicizzato             | Falso                                            |
| Nel catalogo globale      | Falso                                            |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classi utilizzate in        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|--------------------------------------------------|
| ID collegamento                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | Falso                                            |
| È a valore singolo       | Vero                                             |
| Indicizzato             | Falso                                            |
| Nel catalogo globale      | Falso                                            |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classi utilizzate in        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|--------------------------------------------------|
| ID collegamento                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | Falso                                            |
| È a valore singolo       | Vero                                             |
| Indicizzato             | Falso                                            |
| Nel catalogo globale      | Falso                                            |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classi utilizzate in        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|--------------------------------------------------|
| ID collegamento                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | Falso                                            |
| È a valore singolo       | Vero                                             |
| Indicizzato             | Falso                                            |
| Nel catalogo globale      | Falso                                            |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classi utilizzate in        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|--------------------------------------------------|
| ID collegamento                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | Falso                                            |
| È a valore singolo       | Vero                                             |
| Indicizzato             | Falso                                            |
| Nel catalogo globale      | Falso                                            |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classi utilizzate in        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



 

 





