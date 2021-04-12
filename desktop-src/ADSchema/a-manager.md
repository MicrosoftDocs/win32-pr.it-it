---
title: Gestore (attributo)
description: Contiene il nome distinto dell'utente che corrisponde al responsabile dell'utente. L'oggetto utente del Manager contiene una proprietà directReports che contiene riferimenti a tutti gli oggetti utente che hanno le proprietà Manager impostate su questo nome distinto.
ms.assetid: 40743784-a99c-4ec0-9140-9f865c073244
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo Manager
- Schema AD dell'attributo Manager
topic_type:
- apiref
api_name:
- Manager
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f42c659a436f9798861f5c37df19f8d10db91127
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104401000"
---
# <a name="manager-attribute"></a>Gestore (attributo)

Contiene il nome distinto dell'utente che corrisponde al responsabile dell'utente. L'oggetto utente del Manager contiene una proprietà directReports che contiene riferimenti a tutti gli oggetti utente che hanno le proprietà Manager impostate su questo nome distinto.



| Voce | Valore |
|-------------------|-----------------------------------------------------------------------------|
| CN                | Manager                                                                     |
| LDAP-Display-Name | manager                                                                     |
| Dimensione              | \-                                                                          |
| Privilegio aggiornamento  | Amministratore di dominio o proprietario dell'account.                                      |
| Frequenza di aggiornamento  | Quando il record dell'utente viene creato e ogni volta che il responsabile deve cambiare. |
| Attribute-Id      | 0.9.2342.19200300.100.1.10                                                  |
| System-ID-GUID    | bf9679b5-0de6-11d0-a285-00aa003049e2                                        |
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
| È a valore singolo       | Vero                                                               |
| Indicizzato             | Falso                                                              |
| Nel catalogo globale      | Vero                                                               |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                       |
| Range-Lower            | \-                                                                 |
| Range-Upper            | \-                                                                 |
| Search-Flags           | 0x00000010                                                         |
| System-Flags           | 0x00000010                                                         |
| Classi utilizzate in        | [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | 42                                                                                                                     |
| MAPI-Id                | 0x8005                                                                                                                 |
| System-Only            | Falso                                                                                                                  |
| È a valore singolo       | Vero                                                                                                                   |
| Indicizzato             | Falso                                                                                                                  |
| Nel catalogo globale      | Vero                                                                                                                   |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                           |
| Range-Lower            | \-                                                                                                                     |
| Range-Upper            | \-                                                                                                                     |
| Search-Flags           | 0x00000010                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Classi utilizzate in        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | 42                                                                                                                     |
| MAPI-Id                | 0x8005                                                                                                                 |
| System-Only            | Falso                                                                                                                  |
| È a valore singolo       | Vero                                                                                                                   |
| Indicizzato             | Falso                                                                                                                  |
| Nel catalogo globale      | Vero                                                                                                                   |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                           |
| Range-Lower            | \-                                                                                                                     |
| Range-Upper            | \-                                                                                                                     |
| Search-Flags           | 0x00000010                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Classi utilizzate in        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | 42                                                                                                                     |
| MAPI-Id                | 0x8005                                                                                                                 |
| System-Only            | Falso                                                                                                                  |
| È a valore singolo       | Vero                                                                                                                   |
| Indicizzato             | Falso                                                                                                                  |
| Nel catalogo globale      | Vero                                                                                                                   |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                           |
| Range-Lower            | \-                                                                                                                     |
| Range-Upper            | \-                                                                                                                     |
| Search-Flags           | 0x00000010                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Classi utilizzate in        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | 42                                                                                                                     |
| MAPI-Id                | 0x8005                                                                                                                 |
| System-Only            | Falso                                                                                                                  |
| È a valore singolo       | Vero                                                                                                                   |
| Indicizzato             | Falso                                                                                                                  |
| Nel catalogo globale      | Vero                                                                                                                   |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                           |
| Range-Lower            | \-                                                                                                                     |
| Range-Upper            | \-                                                                                                                     |
| Search-Flags           | 0x00000010                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Classi utilizzate in        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | 42                                                                                                                     |
| MAPI-Id                | 0x8005                                                                                                                 |
| System-Only            | Falso                                                                                                                  |
| È a valore singolo       | Vero                                                                                                                   |
| Indicizzato             | Falso                                                                                                                  |
| Nel catalogo globale      | Vero                                                                                                                   |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                           |
| Range-Lower            | \-                                                                                                                     |
| Range-Upper            | \-                                                                                                                     |
| Search-Flags           | 0x00000010                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| Classi utilizzate in        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Organizational-Person**](c-organizationalperson.md)<br/> |



 

 





