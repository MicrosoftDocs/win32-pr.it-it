---
title: Attributo User-Workstations
description: Contiene i nomi NetBIOS o DNS dei computer che eseguono Windows NT Workstation o Windows 2000 Professional da cui l'utente può effettuare l'accesso.
ms.assetid: 92af070b-dadd-404d-8305-d85974639958
ms.tgt_platform: multiple
keywords:
- Schema AD User-Workstations attribute
- Schema AD dell'attributo userWorkstations
topic_type:
- apiref
api_name:
- User-Workstations
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cad59905dbf24c8baa13969d9a2ce5452767163
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103875118"
---
# <a name="user-workstations-attribute"></a>Attributo User-Workstations

Contiene i nomi NetBIOS o DNS dei computer che eseguono Windows NT Workstation o Windows 2000 Professional da cui l'utente può effettuare l'accesso. Ogni nome NetBIOS è separato da una virgola. Più nomi devono essere separati da virgole.

>[!Note]
>Questo attributo utente non deve più essere utilizzato. Per gestire gli account in grado di accedere alle workstation, è consigliabile utilizzare l'opzione "Consenti accesso locale" e "Nega accesso locale" o "Consenti accesso tramite Servizi Desktop remoto" e "Nega accesso tramite Servizi Desktop remoto".

| Voce | Valore |
|-------------------|--------------------------------------------------------------------------------------------|
| CN                | User-Workstations                                                                          |
| LDAP-Display-Name | userWorkstations                                                                           |
| Dimensione              | \-                                                                                         |
| Privilegio aggiornamento  | Amministratore di dominio o proprietario dell'account.                                                     |
| Frequenza di aggiornamento  | Quando il record dell'utente viene creato e ogni volta che è necessario modificare il privilegio di accesso dell'utente. |
| Attribute-Id      | 1.2.840.113556.1.4.86                                                                      |
| System-ID-GUID    | bf9679d7-0de6-11d0-a285-00aa003049e2                                                       |
| Sintassi            | [**String(Unicode)**](s-string-unicode.md)                                                |



## <a name="implementations"></a>Implementazioni

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Voce | Valore |
|------------------------|-----------------------------------|
| ID collegamento                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| È a valore singolo       | Vero                              |
| Indicizzato             | Falso                             |
| Nel catalogo globale      | Falso                             |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                      |
| Range-Lower            | 0                                 |
| Range-Upper            | 1024                              |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| Classi utilizzate in        | [**Utente**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|-----------------------------------|
| ID collegamento                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| È a valore singolo       | Vero                              |
| Indicizzato             | Falso                             |
| Nel catalogo globale      | Falso                             |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                      |
| Range-Lower            | 0                                 |
| Range-Upper            | 1024                              |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| Classi utilizzate in        | [**Utente**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|-----------------------------------|
| ID collegamento                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| È a valore singolo       | Vero                              |
| Indicizzato             | Falso                             |
| Nel catalogo globale      | Falso                             |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                      |
| Range-Lower            | 0                                 |
| Range-Upper            | 1024                              |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| Classi utilizzate in        | [**Utente**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|-----------------------------------|
| ID collegamento                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| È a valore singolo       | Vero                              |
| Indicizzato             | Falso                             |
| Nel catalogo globale      | Falso                             |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                      |
| Range-Lower            | 0                                 |
| Range-Upper            | 1024                              |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| Classi utilizzate in        | [**Utente**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|-----------------------------------|
| ID collegamento                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| È a valore singolo       | Vero                              |
| Indicizzato             | Falso                             |
| Nel catalogo globale      | Falso                             |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                      |
| Range-Lower            | 0                                 |
| Range-Upper            | 1024                              |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| Classi utilizzate in        | [**Utente**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|-----------------------------------|
| ID collegamento                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| È a valore singolo       | Vero                              |
| Indicizzato             | Falso                             |
| Nel catalogo globale      | Falso                             |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                      |
| Range-Lower            | 0                                 |
| Range-Upper            | 1024                              |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| Classi utilizzate in        | [**Utente**](c-user.md)<br/> |



 

 





