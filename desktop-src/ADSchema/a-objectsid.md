---
title: Attributo Object-Sid
description: Valore binario che specifica l'ID di sicurezza (SID) dell'utente. Il SID è un valore univoco utilizzato per identificare l'utente come entità di sicurezza.
ms.assetid: 78ef0158-f59e-43df-b3fc-fb0f709936f6
ms.tgt_platform: multiple
keywords:
- Schema AD Object-Sid attribute
- Schema AD dell'attributo objectSid
topic_type:
- apiref
api_name:
- Object-Sid
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b536650177f873cbbc349096e84c3de274b8d376
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104122410"
---
# <a name="object-sid-attribute"></a>Attributo Object-Sid

Valore binario che specifica l'ID di sicurezza (SID) dell'utente. Il SID è un valore univoco utilizzato per identificare l'utente come entità di sicurezza.



| Voce | Valore |
|-------------------|--------------------------------------------------------------|
| CN                | Object-Sid                                                   |
| LDAP-Display-Name | objectSid                                                    |
| Dimensione              | \-                                                           |
| Privilegio aggiornamento  | Questo valore viene impostato dal sistema.                             |
| Frequenza di aggiornamento  | Questo valore viene impostato dal sistema quando viene creato l'account. |
| Attribute-Id      | 1.2.840.113556.1.4.146                                       |
| System-ID-GUID    | bf9679e8-0de6-11d0-a285-00aa003049e2                         |
| Sintassi            | [**Stringa (SID)**](s-string-sid.md)                          |



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
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x8027                                                                                                                                                                                                                                                     |
| System-Only            | Falso                                                                                                                                                                                                                                                      |
| È a valore singolo       | Vero                                                                                                                                                                                                                                                       |
| Indicizzato             | Vero                                                                                                                                                                                                                                                       |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                                                       |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                                                          |
| Range-Upper            | 28                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000009                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                 |
| Classi utilizzate in        | [**Entità di sicurezza esterna**](c-foreignsecurityprincipal.md)<br/> [**MSMQ-migrated-utente**](c-msmqmigrateduser.md)<br/> [**Sam-dominio-base**](c-samdomainbase.md)<br/> [**Entità di sicurezza**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x8027                                                                                                                                                                                                                                                     |
| System-Only            | Vero                                                                                                                                                                                                                                                       |
| È a valore singolo       | Vero                                                                                                                                                                                                                                                       |
| Indicizzato             | Vero                                                                                                                                                                                                                                                       |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                                                       |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                                                          |
| Range-Upper            | 28                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000009                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                 |
| Classi utilizzate in        | [**Entità di sicurezza esterna**](c-foreignsecurityprincipal.md)<br/> [**MSMQ-migrated-utente**](c-msmqmigrateduser.md)<br/> [**Sam-dominio-base**](c-samdomainbase.md)<br/> [**Entità di sicurezza**](c-securityprincipal.md)<br/> |



## <a name="adam"></a>ADAM



| Voce | Valore |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                               |
| MAPI-Id                | 0x8027                                                                                                                                                                                           |
| System-Only            | Vero                                                                                                                                                                                             |
| È a valore singolo       | Vero                                                                                                                                                                                             |
| Indicizzato             | Vero                                                                                                                                                                                             |
| Nel catalogo globale      | Vero                                                                                                                                                                                             |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                                                                     |
| Range-Lower            | 0                                                                                                                                                                                                |
| Range-Upper            | 28                                                                                                                                                                                               |
| Search-Flags           | 0x00000009                                                                                                                                                                                       |
| System-Flags           | 0x00000012                                                                                                                                                                                       |
| Classi utilizzate in        | [**Entità di sicurezza esterna**](c-foreignsecurityprincipal.md)<br/> [**ms-DS-bind-proxy**](c-msds-bindproxy.md)<br/> [**Entità di sicurezza**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x8027                                                                                                                                                                                                                                                     |
| System-Only            | Vero                                                                                                                                                                                                                                                       |
| È a valore singolo       | Vero                                                                                                                                                                                                                                                       |
| Indicizzato             | Vero                                                                                                                                                                                                                                                       |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                                                       |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                                                          |
| Range-Upper            | 28                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000009                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                 |
| Classi utilizzate in        | [**Entità di sicurezza esterna**](c-foreignsecurityprincipal.md)<br/> [**MSMQ-migrated-utente**](c-msmqmigrateduser.md)<br/> [**Sam-dominio-base**](c-samdomainbase.md)<br/> [**Entità di sicurezza**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x8027                                                                                                                                                                                                                                                     |
| System-Only            | Vero                                                                                                                                                                                                                                                       |
| È a valore singolo       | Vero                                                                                                                                                                                                                                                       |
| Indicizzato             | Vero                                                                                                                                                                                                                                                       |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                                                       |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                                                          |
| Range-Upper            | 28                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000009                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                 |
| Classi utilizzate in        | [**Entità di sicurezza esterna**](c-foreignsecurityprincipal.md)<br/> [**MSMQ-migrated-utente**](c-msmqmigrateduser.md)<br/> [**Sam-dominio-base**](c-samdomainbase.md)<br/> [**Entità di sicurezza**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x8027                                                                                                                                                                                                                                                     |
| System-Only            | Vero                                                                                                                                                                                                                                                       |
| È a valore singolo       | Vero                                                                                                                                                                                                                                                       |
| Indicizzato             | Vero                                                                                                                                                                                                                                                       |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                                                       |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                                                          |
| Range-Upper            | 28                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000009                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                 |
| Classi utilizzate in        | [**Entità di sicurezza esterna**](c-foreignsecurityprincipal.md)<br/> [**MSMQ-migrated-utente**](c-msmqmigrateduser.md)<br/> [**Sam-dominio-base**](c-samdomainbase.md)<br/> [**Entità di sicurezza**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x8027                                                                                                                                                                                                                                                     |
| System-Only            | Vero                                                                                                                                                                                                                                                       |
| È a valore singolo       | Vero                                                                                                                                                                                                                                                       |
| Indicizzato             | Vero                                                                                                                                                                                                                                                       |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                                                       |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                                                                                                                               |
| Range-Lower            | 0                                                                                                                                                                                                                                                          |
| Range-Upper            | 28                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000009                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                 |
| Classi utilizzate in        | [**Entità di sicurezza esterna**](c-foreignsecurityprincipal.md)<br/> [**MSMQ-migrated-utente**](c-msmqmigrateduser.md)<br/> [**Sam-dominio-base**](c-samdomainbase.md)<br/> [**Entità di sicurezza**](c-securityprincipal.md)<br/> |



 

 





