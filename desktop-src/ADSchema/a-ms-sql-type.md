---
title: Attributo di tipo MS-SQL
description: Tipo di replica utilizzato da SQL Server.
ms.assetid: 8e7fa9ab-9a25-4ee3-9134-68af698a5fb8
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo di tipo MS-SQL
- Schema AD dell'attributo di tipo mS-SQL
topic_type:
- apiref
api_name:
- MS-SQL-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 057b85b0c522a891cc31cde699fd062897c54818
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103875773"
---
# <a name="ms-sql-type-attribute"></a>Attributo di tipo MS-SQL

Tipo di replica utilizzato da SQL Server. Di seguito sono riportati i valori possibili per questo attributo.



| Valore        | Descrizione                           |
|--------------|---------------------------------------|
| 0<br/> | Replica transazionale.<br/> |
| 1<br/> | Replica snapshot.<br/>      |
| 2<br/> | Replica di tipo merge.<br/>         |



 



| Voce | Valore |
|-------------------|---------------------------------------------|
| CN                | Tipo MS-SQL                                 |
| LDAP-Display-Name | Tipo mS-SQL                                 |
| Dimensione              | \-                                          |
| Privilegio aggiornamento  | Amministratore di dominio                        |
| Frequenza di aggiornamento  | Quando la replica è configurata.                 |
| Attribute-Id      | 1.2.840.113556.1.4.1391                     |
| System-ID-GUID    | ca48eba8-ccee-11d2-9993-0000f87a57d4        |
| Sintassi            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementazioni

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Voce | Valore |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                  |
| MAPI-Id                | \-                                                                                                                                  |
| System-Only            | Falso                                                                                                                               |
| È a valore singolo       | Vero                                                                                                                                |
| Indicizzato             | Falso                                                                                                                               |
| Nel catalogo globale      | Falso                                                                                                                               |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                        |
| Range-Lower            | \-                                                                                                                                  |
| Range-Upper            | \-                                                                                                                                  |
| Search-Flags           | 0x00000000                                                                                                                          |
| System-Flags           | 0x00000010                                                                                                                          |
| Classi utilizzate in        | [**MS-SQL-SQLPublication**](c-ms-sql-sqlpublication.md)<br/> [**MS-SQL-OLAPDatabase**](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                  |
| MAPI-Id                | \-                                                                                                                                  |
| System-Only            | Falso                                                                                                                               |
| È a valore singolo       | Vero                                                                                                                                |
| Indicizzato             | Falso                                                                                                                               |
| Nel catalogo globale      | Falso                                                                                                                               |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                        |
| Range-Lower            | \-                                                                                                                                  |
| Range-Upper            | \-                                                                                                                                  |
| Search-Flags           | 0x00000000                                                                                                                          |
| System-Flags           | 0x00000010                                                                                                                          |
| Classi utilizzate in        | [**MS-SQL-SQLPublication**](c-ms-sql-sqlpublication.md)<br/> [**MS-SQL-OLAPDatabase**](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                  |
| MAPI-Id                | \-                                                                                                                                  |
| System-Only            | Falso                                                                                                                               |
| È a valore singolo       | Vero                                                                                                                                |
| Indicizzato             | Falso                                                                                                                               |
| Nel catalogo globale      | Falso                                                                                                                               |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                        |
| Range-Lower            | \-                                                                                                                                  |
| Range-Upper            | \-                                                                                                                                  |
| Search-Flags           | 0x00000000                                                                                                                          |
| System-Flags           | 0x00000010                                                                                                                          |
| Classi utilizzate in        | [**MS-SQL-SQLPublication**](c-ms-sql-sqlpublication.md)<br/> [**MS-SQL-OLAPDatabase**](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                  |
| MAPI-Id                | \-                                                                                                                                  |
| System-Only            | Falso                                                                                                                               |
| È a valore singolo       | Vero                                                                                                                                |
| Indicizzato             | Falso                                                                                                                               |
| Nel catalogo globale      | Falso                                                                                                                               |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                        |
| Range-Lower            | \-                                                                                                                                  |
| Range-Upper            | \-                                                                                                                                  |
| Search-Flags           | 0x00000000                                                                                                                          |
| System-Flags           | 0x00000010                                                                                                                          |
| Classi utilizzate in        | [**MS-SQL-SQLPublication**](c-ms-sql-sqlpublication.md)<br/> [**MS-SQL-OLAPDatabase**](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                  |
| MAPI-Id                | \-                                                                                                                                  |
| System-Only            | Falso                                                                                                                               |
| È a valore singolo       | Vero                                                                                                                                |
| Indicizzato             | Falso                                                                                                                               |
| Nel catalogo globale      | Falso                                                                                                                               |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                        |
| Range-Lower            | \-                                                                                                                                  |
| Range-Upper            | \-                                                                                                                                  |
| Search-Flags           | 0x00000000                                                                                                                          |
| System-Flags           | 0x00000010                                                                                                                          |
| Classi utilizzate in        | [**MS-SQL-SQLPublication**](c-ms-sql-sqlpublication.md)<br/> [**MS-SQL-OLAPDatabase**](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                  |
| MAPI-Id                | \-                                                                                                                                  |
| System-Only            | Falso                                                                                                                               |
| È a valore singolo       | Vero                                                                                                                                |
| Indicizzato             | Falso                                                                                                                               |
| Nel catalogo globale      | Falso                                                                                                                               |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                        |
| Range-Lower            | \-                                                                                                                                  |
| Range-Upper            | \-                                                                                                                                  |
| Search-Flags           | 0x00000000                                                                                                                          |
| System-Flags           | 0x00000010                                                                                                                          |
| Classi utilizzate in        | [**MS-SQL-SQLPublication**](c-ms-sql-sqlpublication.md)<br/> [**MS-SQL-OLAPDatabase**](c-ms-sql-olapdatabase.md)<br/> |



 

 





