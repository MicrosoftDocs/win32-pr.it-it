---
title: Phone-Home-attributo primario
description: Il numero di telefono dell'abitazione principale dell'utente.
ms.assetid: 624d89fd-942c-448d-bd51-7d93954370b1
ms.tgt_platform: multiple
keywords:
- Phone-Home-schema AD dell'attributo primario
- Schema AD dell'attributo homePhone
topic_type:
- apiref
api_name:
- Phone-Home-Primary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c2d2e68116a15dcbf4431d33bb56b4ffed8ee2e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303344"
---
# <a name="phone-home-primary-attribute"></a>Phone-Home-attributo primario

Il numero di telefono dell'abitazione principale dell'utente.



| Voce | Valore |
|-------------------|----------------------------------------------------------------------------------|
| CN                | Telefono-Home-primario                                                               |
| LDAP-Display-Name | homePhone                                                                        |
| Dimensione              | \-                                                                               |
| Privilegio aggiornamento  | Amministratore di dominio o proprietario dell'account.                                           |
| Frequenza di aggiornamento  | Quando viene creato il record dell'utente e ogni volta che il numero di telefono deve essere modificato. |
| Attribute-Id      | 0.9.2342.19200300.100.1.20                                                       |
| System-ID-GUID    | f0f8ffa1-1191-11d0-a060-00aa006c33ed                                             |
| Sintassi            | [**String(Unicode)**](s-string-unicode.md)                                      |



## <a name="implementations"></a>Implementazioni

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Voce | Valore |
|------------------------|--------------------------------------------------------------------|
| ID collegamento                | \-                                                                 |
| MAPI-Id                | 0x3A09                                                             |
| System-Only            | Falso                                                              |
| È a valore singolo       | Vero                                                               |
| Indicizzato             | Falso                                                              |
| Nel catalogo globale      | Vero                                                               |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                       |
| Range-Lower            | 1                                                                  |
| Range-Upper            | 64                                                                 |
| Search-Flags           | 0x00000000                                                         |
| System-Flags           | 0x00000010                                                         |
| Classi utilizzate in        | [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                       |
| MAPI-Id                | 0x3A09                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                    |
| È a valore singolo       | Vero                                                                                                                                                     |
| Indicizzato             | Falso                                                                                                                                                    |
| Nel catalogo globale      | Vero                                                                                                                                                     |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                             |
| Range-Lower            | 1                                                                                                                                                        |
| Range-Upper            | 64                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                               |
| System-Flags           | 0x00000010                                                                                                                                               |
| Classi utilizzate in        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Utente**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                       |
| MAPI-Id                | 0x3A09                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                    |
| È a valore singolo       | Vero                                                                                                                                                     |
| Indicizzato             | Falso                                                                                                                                                    |
| Nel catalogo globale      | Vero                                                                                                                                                     |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                             |
| Range-Lower            | 1                                                                                                                                                        |
| Range-Upper            | 64                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                               |
| System-Flags           | 0x00000010                                                                                                                                               |
| Classi utilizzate in        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Utente**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                       |
| MAPI-Id                | 0x3A09                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                    |
| È a valore singolo       | Vero                                                                                                                                                     |
| Indicizzato             | Falso                                                                                                                                                    |
| Nel catalogo globale      | Vero                                                                                                                                                     |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                             |
| Range-Lower            | 1                                                                                                                                                        |
| Range-Upper            | 64                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                               |
| System-Flags           | 0x00000010                                                                                                                                               |
| Classi utilizzate in        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Utente**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                       |
| MAPI-Id                | 0x3A09                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                    |
| È a valore singolo       | Vero                                                                                                                                                     |
| Indicizzato             | Falso                                                                                                                                                    |
| Nel catalogo globale      | Vero                                                                                                                                                     |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                             |
| Range-Lower            | 1                                                                                                                                                        |
| Range-Upper            | 64                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                               |
| System-Flags           | 0x00000010                                                                                                                                               |
| Classi utilizzate in        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Utente**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                       |
| MAPI-Id                | 0x3A09                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                    |
| È a valore singolo       | Vero                                                                                                                                                     |
| Indicizzato             | Falso                                                                                                                                                    |
| Nel catalogo globale      | Vero                                                                                                                                                     |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                             |
| Range-Lower            | 1                                                                                                                                                        |
| Range-Upper            | 64                                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                               |
| System-Flags           | 0x00000010                                                                                                                                               |
| Classi utilizzate in        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> [**Utente**](c-user.md)<br/> |



 

 





