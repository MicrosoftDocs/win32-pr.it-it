---
title: attributo ms-FRS-topologia-pref
description: L'attributo ms-FRS-topologia-pref viene usato per registrare le impostazioni di topologia NTFRS preferite.
ms.assetid: 2804ad8a-bec8-491b-84ea-bdff1c8635d0
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo ms-FRS-topologia-pref
- msFRS-topologia-schema AD dell'attributo pref
topic_type:
- apiref
api_name:
- ms-FRS-Topology-Pref
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de417b03385e51d6a97fd68097f81bcc0cb6b9db
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744666"
---
# <a name="ms-frs-topology-pref-attribute"></a>attributo ms-FRS-topologia-pref

L'attributo **MS-FRS-topologia-pref** viene usato per registrare le impostazioni di topologia NTFRS preferite. Quando un membro FRS viene aggiunto o eliminato al set di repliche, viene fatto riferimento a questi attributi e vengono apportate modifiche alle connessioni tra il resto dei membri FRS nel set di repliche.

I valori validi per questo attributo sono i seguenti.

| Valore | Descrizione                              |
|-------|------------------------------------------|
| 1     | \_anello RSTOPOLOGYPREF \_ FRS<br/>     |
| 2     | FRS \_ RSTOPOLOGYPREF \_ HUBSPOKE<br/> |
| 3     | FRS \_ RSTOPOLOGYPREF \_ FULLMESH<br/> |
| 4     | \_RSTOPOLOGYPREF \_ personalizzato FRS<br/>   |



 



| Voce | Valore |
|-------------------|--------------------------------------------------------------------|
| CN                | MS-FRS-topologia-pref                                               |
| LDAP-Display-Name | msFRS-topologia-pref                                                |
| Dimensione              | \-                                                                 |
| Privilegio aggiornamento  | Amministratore di dominio                                               |
| Frequenza di aggiornamento  | Quando viene creato il set di repliche o la topologia preferita viene modificata. |
| Attribute-Id      | 1.2.840.113556.1.4.1692                                            |
| System-ID-GUID    | 92aa27e0-5c50-402d-9ec1-ee847def9788                               |
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
| È a valore singolo       | Vero                                                      |
| Indicizzato             | Falso                                                     |
| Nel catalogo globale      | Falso                                                     |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Classi utilizzate in        | [**NTFRS-set di repliche**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|-----------------------------------------------------------|
| ID collegamento                | \-                                                        |
| MAPI-Id                | \-                                                        |
| System-Only            | Falso                                                     |
| È a valore singolo       | Vero                                                      |
| Indicizzato             | Falso                                                     |
| Nel catalogo globale      | Falso                                                     |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Classi utilizzate in        | [**NTFRS-set di repliche**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|-----------------------------------------------------------|
| ID collegamento                | \-                                                        |
| MAPI-Id                | \-                                                        |
| System-Only            | Falso                                                     |
| È a valore singolo       | Vero                                                      |
| Indicizzato             | Falso                                                     |
| Nel catalogo globale      | Falso                                                     |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Classi utilizzate in        | [**NTFRS-set di repliche**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|-----------------------------------------------------------|
| ID collegamento                | \-                                                        |
| MAPI-Id                | \-                                                        |
| System-Only            | Falso                                                     |
| È a valore singolo       | Vero                                                      |
| Indicizzato             | Falso                                                     |
| Nel catalogo globale      | Falso                                                     |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Classi utilizzate in        | [**NTFRS-set di repliche**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|-----------------------------------------------------------|
| ID collegamento                | \-                                                        |
| MAPI-Id                | \-                                                        |
| System-Only            | Falso                                                     |
| È a valore singolo       | Vero                                                      |
| Indicizzato             | Falso                                                     |
| Nel catalogo globale      | Falso                                                     |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Classi utilizzate in        | [**NTFRS-set di repliche**](c-ntfrsreplicaset.md)<br/> |



 

 





