---
title: Attributo ms-FRS-Hub-Member
description: L'attributo ms-FRS-Hub-Member viene usato per registrare le impostazioni della topologia NTFRS preferite.
ms.assetid: df8623e0-745a-46f8-a696-8f6e7014fd2b
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo ms-FRS-Hub-Member
- Schema AD dell'attributo msFRS-Hub-Member
topic_type:
- apiref
api_name:
- ms-FRS-Hub-Member
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2f2cc1014b081ac13183144fca34c2087539de0
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885709"
---
# <a name="ms-frs-hub-member-attribute"></a>Attributo ms-FRS-Hub-Member

**L'attributo ms-FRS-Hub-Member** viene usato per registrare le impostazioni della topologia NTFRS preferite. Quando un membro frs viene aggiunto o eliminato a un set di repliche, viene fatto riferimento a questi attributi e vengono apportate le modifiche appropriate alle connessioni tra gli altri membri del servizio Replica file nel set di repliche.



| Voce | Valore |
|-------------------|--------------------------------------------------------------------|
| CN                | ms-FRS-Hub-Member                                                  |
| Ldap-Display-Name | msFRS-Hub-Member                                                   |
| Dimensione              | \-                                                                 |
| Aggiorna privilegio  | Amministratore di dominio                                               |
| Frequenza di aggiornamento  | Quando viene creato il set di repliche o viene modificata la topologia preferita. |
| Attribute-Id      | 1.2.840.113556.1.4.1693                                            |
| System-Id-Guid    | 5643ff81-35b6-4ca9-9512-baf0bd0a2772                               |
| Sintassi            | [**Object(DS-DN)**](s-object-ds-dn.md)                            |



## <a name="implementations"></a>Implementazioni

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|-----------------------------------------------------------|
| ID collegamento                | 1046                                                      |
| MAPI-Id                | \-                                                        |
| System-Only            | Falso                                                     |
| A valore singolo       | Vero                                                      |
| Indicizzato             | Falso                                                     |
| Nel catalogo globale      | Falso                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Classi usate in        | [**Set di repliche NTFRS**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|-----------------------------------------------------------|
| ID collegamento                | 1046                                                      |
| MAPI-Id                | \-                                                        |
| System-Only            | Falso                                                     |
| A valore singolo       | Vero                                                      |
| Indicizzato             | Falso                                                     |
| Nel catalogo globale      | Falso                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Classi usate in        | [**Set di repliche NTFRS**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|-----------------------------------------------------------|
| ID collegamento                | 1046                                                      |
| MAPI-Id                | \-                                                        |
| System-Only            | Falso                                                     |
| A valore singolo       | Vero                                                      |
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
| ID collegamento                | 1046                                                      |
| MAPI-Id                | \-                                                        |
| System-Only            | Falso                                                     |
| A valore singolo       | Vero                                                      |
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
| ID collegamento                | 1046                                                      |
| MAPI-Id                | \-                                                        |
| System-Only            | Falso                                                     |
| A valore singolo       | Vero                                                      |
| Indicizzato             | Falso                                                     |
| Nel catalogo globale      | Falso                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Classi usate in        | [**Set di repliche NTFRS**](c-ntfrsreplicaset.md)<br/> |



## <a name="remarks"></a>Commenti

Si tratta del nome distinto completo di un [**oggetto NTFRS-Member.**](c-ntfrsmember.md) Il nome distinto è nel formato "CN=*&lt; &gt; computerGuid*, CN= *<Dfs Link Name>* , CN= , *<Dfs Root name>* CN=DFS Volumes, CN=File Replication Service,CN=System, DC=..."

 

 





