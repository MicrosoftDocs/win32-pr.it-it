---
title: Attributo Security-Identifier
description: Valore univoco di lunghezza variabile usato per identificare un account utente, un account di gruppo o una sessione di accesso a cui si applica una voce ACE.
ms.assetid: bb6a16f6-d2c1-48f1-af9a-40fe2a59f281
ms.tgt_platform: multiple
keywords:
- Schema AD Security-Identifier attribute
- Schema AD dell'attributo securityIdentifier
topic_type:
- apiref
api_name:
- Security-Identifier
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dd921d0bcba08c2174475007476add8e8787456
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744530"
---
# <a name="security-identifier-attribute"></a>Attributo Security-Identifier

Valore univoco di lunghezza variabile usato per identificare un account utente, un account di gruppo o una sessione di accesso a cui si applica una voce ACE.



| Voce | Valore |
|-------------------|--------------------------------------|
| CN                | Security-Identifier                  |
| LDAP-Display-Name | securityIdentifier                   |
| Dimensione              | \-                                   |
| Privilegio aggiornamento  | \-                                   |
| Frequenza di aggiornamento  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.121               |
| System-ID-GUID    | bf967a2f-0de6-11d0-a285-00aa003049e2 |
| Sintassi            | [**Stringa (SID)**](s-string-sid.md)  |



## <a name="implementations"></a>Implementazioni

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Voce | Valore |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | Falso                                                                                                             |
| È a valore singolo       | Vero                                                                                                              |
| Indicizzato             | Falso                                                                                                             |
| Nel catalogo globale      | Falso                                                                                                             |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                      |
| Range-Lower            | \-                                                                                                                |
| Range-Upper            | \-                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000010                                                                                                        |
| Classi utilizzate in        | [**Entità di sicurezza**](c-securityprincipal.md)<br/> [**Dominio trusted**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | Falso                                                                                                             |
| È a valore singolo       | Vero                                                                                                              |
| Indicizzato             | Falso                                                                                                             |
| Nel catalogo globale      | Vero                                                                                                              |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                      |
| Range-Lower            | \-                                                                                                                |
| Range-Upper            | \-                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000010                                                                                                        |
| Classi utilizzate in        | [**Entità di sicurezza**](c-securityprincipal.md)<br/> [**Dominio trusted**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | Falso                                                                                                             |
| È a valore singolo       | Vero                                                                                                              |
| Indicizzato             | Falso                                                                                                             |
| Nel catalogo globale      | Vero                                                                                                              |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                      |
| Range-Lower            | \-                                                                                                                |
| Range-Upper            | \-                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000010                                                                                                        |
| Classi utilizzate in        | [**Entità di sicurezza**](c-securityprincipal.md)<br/> [**Dominio trusted**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | Falso                                                                                                             |
| È a valore singolo       | Vero                                                                                                              |
| Indicizzato             | Falso                                                                                                             |
| Nel catalogo globale      | Vero                                                                                                              |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                      |
| Range-Lower            | \-                                                                                                                |
| Range-Upper            | \-                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000010                                                                                                        |
| Classi utilizzate in        | [**Entità di sicurezza**](c-securityprincipal.md)<br/> [**Dominio trusted**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | Falso                                                                                                             |
| È a valore singolo       | Vero                                                                                                              |
| Indicizzato             | Falso                                                                                                             |
| Nel catalogo globale      | Vero                                                                                                              |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                      |
| Range-Lower            | \-                                                                                                                |
| Range-Upper            | \-                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000010                                                                                                        |
| Classi utilizzate in        | [**Entità di sicurezza**](c-securityprincipal.md)<br/> [**Dominio trusted**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | Falso                                                                                                             |
| È a valore singolo       | Vero                                                                                                              |
| Indicizzato             | Falso                                                                                                             |
| Nel catalogo globale      | Vero                                                                                                              |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                      |
| Range-Lower            | \-                                                                                                                |
| Range-Upper            | \-                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000010                                                                                                        |
| Classi utilizzate in        | [**Entità di sicurezza**](c-securityprincipal.md)<br/> [**Dominio trusted**](c-trusteddomain.md)<br/> |



 

 





