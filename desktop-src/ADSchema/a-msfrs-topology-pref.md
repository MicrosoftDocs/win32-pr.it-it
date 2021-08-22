---
title: Attributo ms-FRS-Topology-Pref
description: L'attributo ms-FRS-Topology-Pref viene usato per registrare le impostazioni della topologia NTFRS preferite.
ms.assetid: 2804ad8a-bec8-491b-84ea-bdff1c8635d0
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo ms-FRS-Topology-Pref
- Schema AD dell'attributo msFRS-Topology-Pref
topic_type:
- apiref
api_name:
- ms-FRS-Topology-Pref
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8467a038db4f5c263253d31c33cb7dc01bb548712918d654b27b7778079d5c20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118960530"
---
# <a name="ms-frs-topology-pref-attribute"></a>Attributo ms-FRS-Topology-Pref

**L'attributo ms-FRS-Topology-Pref** viene usato per registrare le impostazioni della topologia NTFRS preferite. Quando un membro FRS viene aggiunto o eliminato al set di repliche, viene fatto riferimento a questi attributi e vengono apportate modifiche alle connessioni tra gli altri membri frs nel set di repliche.

I valori validi per questo attributo sono i seguenti.

| Valore | Descrizione                              |
|-------|------------------------------------------|
| 1     | FRS \_ RSTOPOLOGYPREF \_ RING<br/>     |
| 2     | FRS \_ RSTOPOLOGYPREF \_ HUBSPOKE<br/> |
| 3     | FRS \_ RSTOPOLOGYPREF \_ FULLMESH<br/> |
| 4     | FRS \_ RSTOPOLOGYPREF \_ CUSTOM<br/>   |



 



| Voce | Valore |
|-------------------|--------------------------------------------------------------------|
| CN                | ms-FRS-Topology-Pref                                               |
| Ldap-Display-Name | msFRS-Topology-Pref                                                |
| Dimensione              | \-                                                                 |
| Privilegio di aggiornamento  | Amministratore di dominio                                               |
| Frequenza di aggiornamento  | Quando viene creato il set di repliche o viene modificata la topologia preferita. |
| Attribute-Id      | 1.2.840.113556.1.4.1692                                            |
| System-Id-Guid    | 92aa27e0-5c50-402d-9ec1-ee847def9788                               |
| Sintassi            | [**String(Unicode)**](s-string-unicode.md)                        |



## <a name="implementations"></a>Implementazioni

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|-----------------------------------------------------------|
| ID collegamento                | \-                                                        |
| MAPI-Id                | \-                                                        |
| System-Only            | Falso                                                     |
| Is-Single-Valued       | Vero                                                      |
| Indicizzato             | Falso                                                     |
| Nel catalogo globale      | Falso                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Classi usate in        | [**NTFRS-Replica-Set**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|-----------------------------------------------------------|
| ID collegamento                | \-                                                        |
| MAPI-Id                | \-                                                        |
| System-Only            | Falso                                                     |
| Is-Single-Valued       | Vero                                                      |
| Indicizzato             | Falso                                                     |
| Nel catalogo globale      | Falso                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Classi usate in        | [**NTFRS-Replica-Set**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|-----------------------------------------------------------|
| ID collegamento                | \-                                                        |
| MAPI-Id                | \-                                                        |
| System-Only            | Falso                                                     |
| Is-Single-Valued       | Vero                                                      |
| Indicizzato             | Falso                                                     |
| Nel catalogo globale      | Falso                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Classi usate in        | [**Set di repliche NTFRS**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|-----------------------------------------------------------|
| ID collegamento                | \-                                                        |
| MAPI-Id                | \-                                                        |
| System-Only            | Falso                                                     |
| Is-Single-Valued       | Vero                                                      |
| Indicizzato             | Falso                                                     |
| Nel catalogo globale      | Falso                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Classi usate in        | [**Set di repliche NTFRS**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|-----------------------------------------------------------|
| ID collegamento                | \-                                                        |
| MAPI-Id                | \-                                                        |
| System-Only            | Falso                                                     |
| Is-Single-Valued       | Vero                                                      |
| Indicizzato             | Falso                                                     |
| Nel catalogo globale      | Falso                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Classi usate in        | [**Set di repliche NTFRS**](c-ntfrsreplicaset.md)<br/> |



 

 





