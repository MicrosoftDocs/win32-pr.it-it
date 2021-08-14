---
title: Attributo manager
description: Contiene il nome distinto dell'utente che è il responsabile dell'utente. L'oggetto utente del manager contiene una proprietà directReports che contiene riferimenti a tutti gli oggetti utente con le proprietà di gestione impostate su questo nome distinto.
ms.assetid: 40743784-a99c-4ec0-9140-9f865c073244
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo manager
- Schema AD dell'attributo manager
topic_type:
- apiref
api_name:
- Manager
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e87b17f3252963e03c86b5b25a3651606a004afe672f1c8ec07f419ddff3a826
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119301261"
---
# <a name="manager-attribute"></a>Attributo manager

Contiene il nome distinto dell'utente che è il responsabile dell'utente. L'oggetto utente del manager contiene una proprietà directReports che contiene riferimenti a tutti gli oggetti utente con le proprietà di gestione impostate su questo nome distinto.



| Voce | Valore |
|-------------------|-----------------------------------------------------------------------------|
| CN                | Manager                                                                     |
| Ldap-Display-Name | manager                                                                     |
| Dimensione              | \-                                                                          |
| Privilegio di aggiornamento  | Amministratore di dominio o proprietario dell'account.                                      |
| Frequenza di aggiornamento  | Quando viene creato il record dell'utente e ogni volta che il manager deve cambiare. |
| Attribute-Id      | 0.9.2342.19200300.100.1.10                                                  |
| System-Id-Guid    | bf9679b5-0de6-11d0-a285-00aa003049e2                                        |
| Sintassi            | [**Object(DS-DN)**](s-object-ds-dn.md)                                     |



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
| ID collegamento                | 42                                                                 |
| MAPI-Id                | 0x8005                                                             |
| System-Only            | Falso                                                              |
| Is-Single-Valued       | Vero                                                               |
| Indicizzato             | Falso                                                              |
| Nel catalogo globale      | Vero                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                       |
| Range-Lower            | \-                                                                 |
| Range-Upper            | \-                                                                 |
| Search-Flags           | 0x00000010                                                         |
| System-Flags           | 0x00000010                                                         |
| Classi usate in        | [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | 42                                                                                                                     |
| MAPI-Id                | 0x8005                                                                                                                 |
| System-Only            | Falso                                                                                                                  |
| Is-Single-Valued       | Vero                                                                                                                   |
| Indicizzato             | Falso                                                                                                                  |
| Nel catalogo globale      | Vero                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                           |
| Range-Lower            | \-                                                                                                                     |
| Range-Upper            | \-                                                                                                                     |
| Search-Flags           | 0x00000010                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Classi usate in        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | 42                                                                                                                     |
| MAPI-Id                | 0x8005                                                                                                                 |
| System-Only            | Falso                                                                                                                  |
| Is-Single-Valued       | Vero                                                                                                                   |
| Indicizzato             | Falso                                                                                                                  |
| Nel catalogo globale      | Vero                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                           |
| Range-Lower            | \-                                                                                                                     |
| Range-Upper            | \-                                                                                                                     |
| Search-Flags           | 0x00000010                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Classi usate in        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | 42                                                                                                                     |
| MAPI-Id                | 0x8005                                                                                                                 |
| System-Only            | Falso                                                                                                                  |
| A valore singolo       | Vero                                                                                                                   |
| Indicizzato             | Falso                                                                                                                  |
| Nel catalogo globale      | Vero                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                           |
| Range-Lower            | \-                                                                                                                     |
| Range-Upper            | \-                                                                                                                     |
| Search-Flags           | 0x00000010                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Classi usate in        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | 42                                                                                                                     |
| MAPI-Id                | 0x8005                                                                                                                 |
| System-Only            | Falso                                                                                                                  |
| A valore singolo       | Vero                                                                                                                   |
| Indicizzato             | Falso                                                                                                                  |
| Nel catalogo globale      | Vero                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                           |
| Range-Lower            | \-                                                                                                                     |
| Range-Upper            | \-                                                                                                                     |
| Search-Flags           | 0x00000010                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Classi usate in        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | 42                                                                                                                     |
| MAPI-Id                | 0x8005                                                                                                                 |
| System-Only            | Falso                                                                                                                  |
| A valore singolo       | Vero                                                                                                                   |
| Indicizzato             | Falso                                                                                                                  |
| Nel catalogo globale      | Vero                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                           |
| Range-Lower            | \-                                                                                                                     |
| Range-Upper            | \-                                                                                                                     |
| Search-Flags           | 0x00000010                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Classi usate in        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



 

 





