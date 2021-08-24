---
title: Security-Identifier attributo
description: Valore univoco di lunghezza variabile utilizzato per identificare un account utente, un account di gruppo o una sessione di accesso a cui si applica una ACE.
ms.assetid: bb6a16f6-d2c1-48f1-af9a-40fe2a59f281
ms.tgt_platform: multiple
keywords:
- Security-Identifier schema AD dell'attributo
- Schema AD dell'attributo securityIdentifier
topic_type:
- apiref
api_name:
- Security-Identifier
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f15449127dd11e7e0ebfef9f63d8e79470ed662377cbdd1929ed072b2502dae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119836871"
---
# <a name="security-identifier-attribute"></a>Security-Identifier attributo

Valore univoco di lunghezza variabile utilizzato per identificare un account utente, un account di gruppo o una sessione di accesso a cui si applica una ACE.



| Voce | Valore |
|-------------------|--------------------------------------|
| CN                | Security-Identifier                  |
| Ldap-Display-Name | securityIdentifier                   |
| Dimensione              | \-                                   |
| Aggiorna privilegio  | \-                                   |
| Frequenza di aggiornamento  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.121               |
| System-Id-Guid    | bf967a2f-0de6-11d0-a285-00aa003049e2 |
| Sintassi            | [**String(Sid)**](s-string-sid.md)  |



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
| Is-Single-Valued       | Vero                                                                                                              |
| Indicizzato             | Falso                                                                                                             |
| Nel catalogo globale      | Falso                                                                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                      |
| Range-Lower            | \-                                                                                                                |
| Range-Upper            | \-                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000010                                                                                                        |
| Classi usate in        | [**Entità di sicurezza**](c-securityprincipal.md)<br/> [**Dominio trusted**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | Falso                                                                                                             |
| Is-Single-Valued       | Vero                                                                                                              |
| Indicizzato             | Falso                                                                                                             |
| Nel catalogo globale      | Vero                                                                                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                      |
| Range-Lower            | \-                                                                                                                |
| Range-Upper            | \-                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000010                                                                                                        |
| Classi usate in        | [**Entità di sicurezza**](c-securityprincipal.md)<br/> [**Dominio trusted**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | Falso                                                                                                             |
| Is-Single-Valued       | Vero                                                                                                              |
| Indicizzato             | Falso                                                                                                             |
| Nel catalogo globale      | Vero                                                                                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                      |
| Range-Lower            | \-                                                                                                                |
| Range-Upper            | \-                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000010                                                                                                        |
| Classi usate in        | [**Entità di sicurezza**](c-securityprincipal.md)<br/> [**Dominio trusted**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | Falso                                                                                                             |
| Is-Single-Valued       | Vero                                                                                                              |
| Indicizzato             | Falso                                                                                                             |
| Nel catalogo globale      | Vero                                                                                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                      |
| Range-Lower            | \-                                                                                                                |
| Range-Upper            | \-                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000010                                                                                                        |
| Classi usate in        | [**Entità di sicurezza**](c-securityprincipal.md)<br/> [**Dominio trusted**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | Falso                                                                                                             |
| Is-Single-Valued       | Vero                                                                                                              |
| Indicizzato             | Falso                                                                                                             |
| Nel catalogo globale      | Vero                                                                                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                      |
| Range-Lower            | \-                                                                                                                |
| Range-Upper            | \-                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000010                                                                                                        |
| Classi usate in        | [**Entità di sicurezza**](c-securityprincipal.md)<br/> [**Dominio trusted**](c-trusteddomain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                |
| MAPI-Id                | \-                                                                                                                |
| System-Only            | Falso                                                                                                             |
| Is-Single-Valued       | Vero                                                                                                              |
| Indicizzato             | Falso                                                                                                             |
| Nel catalogo globale      | Vero                                                                                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                      |
| Range-Lower            | \-                                                                                                                |
| Range-Upper            | \-                                                                                                                |
| Search-Flags           | 0x00000000                                                                                                        |
| System-Flags           | 0x00000010                                                                                                        |
| Classi usate in        | [**Entità di sicurezza**](c-securityprincipal.md)<br/> [**Dominio trusted**](c-trusteddomain.md)<br/> |



 

 





