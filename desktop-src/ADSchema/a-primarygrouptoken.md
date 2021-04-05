---
title: Primary-Group-token-attributo
description: Attributo calcolato utilizzato per recuperare l'elenco di appartenenze di un gruppo, ad esempio gli utenti di dominio. L'appartenenza completa di tali gruppi non viene archiviata in modo esplicito per motivi di scalabilità.
ms.assetid: b23d3b7f-074b-4f1b-bc06-b22738a8a79e
ms.tgt_platform: multiple
keywords:
- Primary-Group-token attributo AD schema
- Schema AD dell'attributo primaryGroupToken
topic_type:
- apiref
api_name:
- Primary-Group-Token
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b237ab5998ca3f38f2d07128b36d9337c96935d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104122390"
---
# <a name="primary-group-token-attribute"></a>Primary-Group-token-attributo

Attributo calcolato utilizzato per recuperare l'elenco di appartenenze di un gruppo, ad esempio gli utenti di dominio. L'appartenenza completa di tali gruppi non viene archiviata in modo esplicito per motivi di scalabilità.



| Voce | Valore |
|-------------------|--------------------------------------------|
| CN                | Primary-Group-token                        |
| LDAP-Display-Name | primaryGroupToken                          |
| Dimensione              | 4 byte                                    |
| Privilegio aggiornamento  | Questo valore viene impostato dal sistema.           |
| Frequenza di aggiornamento  | Quando viene modificato un gruppo primario di oggetti. |
| Attribute-Id      | 1.2.840.113556.1.4.1412                    |
| System-ID-GUID    | c0ed8738-7efd-4481-84d9-66d2db8be369       |
| Sintassi            | [**Enumerazione**](s-enumeration.md)       |



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
|------------------------|-------------------------------------|
| ID collegamento                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | Vero                                |
| È a valore singolo       | Vero                                |
| Indicizzato             | Falso                               |
| Nel catalogo globale      | Falso                               |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| Classi utilizzate in        | [**Group**](c-group.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|-------------------------------------|
| ID collegamento                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | Vero                                |
| È a valore singolo       | Vero                                |
| Indicizzato             | Falso                               |
| Nel catalogo globale      | Falso                               |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| Classi utilizzate in        | [**Group**](c-group.md)<br/> |



## <a name="adam"></a>ADAM



| Voce | Valore |
|------------------------|-------------------------------------|
| ID collegamento                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | Vero                                |
| È a valore singolo       | Vero                                |
| Indicizzato             | Falso                               |
| Nel catalogo globale      | Falso                               |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| Classi utilizzate in        | [**Group**](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|-------------------------------------|
| ID collegamento                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | Vero                                |
| È a valore singolo       | Vero                                |
| Indicizzato             | Falso                               |
| Nel catalogo globale      | Falso                               |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| Classi utilizzate in        | [**Group**](c-group.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|-------------------------------------|
| ID collegamento                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | Vero                                |
| È a valore singolo       | Vero                                |
| Indicizzato             | Falso                               |
| Nel catalogo globale      | Falso                               |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| Classi utilizzate in        | [**Group**](c-group.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|-------------------------------------|
| ID collegamento                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | Vero                                |
| È a valore singolo       | Vero                                |
| Indicizzato             | Falso                               |
| Nel catalogo globale      | Falso                               |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| Classi utilizzate in        | [**Group**](c-group.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|-------------------------------------|
| ID collegamento                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | Vero                                |
| È a valore singolo       | Vero                                |
| Indicizzato             | Falso                               |
| Nel catalogo globale      | Falso                               |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| Classi utilizzate in        | [**Group**](c-group.md)<br/> |



 

 





