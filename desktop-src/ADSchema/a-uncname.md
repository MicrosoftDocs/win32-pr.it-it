---
title: Attributo UNC-Name
description: Nome della convenzione di denominazione universale per i volumi e le stampanti condivise.
ms.assetid: 967fd0dc-10af-4482-bc2c-1d1dc13dee39
ms.tgt_platform: multiple
keywords:
- Schema AD UNC-Name attribute
- Schema AD dell'attributo UNCName
topic_type:
- apiref
api_name:
- UNC-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e06bc54ebb035a491e2d93a1c372e2d46fc43f76
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303110"
---
# <a name="unc-name-attribute"></a>Attributo UNC-Name

Nome della convenzione di denominazione universale per i volumi e le stampanti condivise.



| Voce | Valore |
|-------------------|-----------------------------------------------|
| CN                | UNC-Name                                      |
| LDAP-Display-Name | uNCName                                       |
| Dimensione              | \-                                            |
| Privilegio aggiornamento  | Amministratore di dominio                          |
| Frequenza di aggiornamento  | Quando vengono creati nuovi volumi o code di stampa. |
| Attribute-Id      | 1.2.840.113556.1.4.137                        |
| System-ID-GUID    | bf967a64-0de6-11d0-a285-00aa003049e2          |
| Sintassi            | [**String(Unicode)**](s-string-unicode.md)   |



## <a name="implementations"></a>Implementazioni

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                |
| È a valore singolo       | Vero                                                                                                                                                 |
| Indicizzato             | Vero                                                                                                                                                 |
| Nel catalogo globale      | Vero                                                                                                                                                 |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                         |
| Range-Lower            | \-                                                                                                                                                   |
| Range-Upper            | \-                                                                                                                                                   |
| Search-Flags           | 0x00000001                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                           |
| Classi utilizzate in        | [**Index-Server-Catalog**](c-indexservercatalog.md)<br/> [**Coda di stampa**](c-printqueue.md)<br/> [**Volume**](c-volume.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                        |
| MAPI-Id                | \-                                                                                                                                                                                        |
| System-Only            | Falso                                                                                                                                                                                     |
| È a valore singolo       | Vero                                                                                                                                                                                      |
| Indicizzato             | Vero                                                                                                                                                                                      |
| Nel catalogo globale      | Vero                                                                                                                                                                                      |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                                                              |
| Range-Lower            | \-                                                                                                                                                                                        |
| Range-Upper            | \-                                                                                                                                                                                        |
| Search-Flags           | 0x00000001                                                                                                                                                                                |
| System-Flags           | 0x00000010                                                                                                                                                                                |
| Classi utilizzate in        | [**FT-DFS**](c-ftdfs.md)<br/> [**Index-Server-Catalog**](c-indexservercatalog.md)<br/> [**Coda di stampa**](c-printqueue.md)<br/> [**Volume**](c-volume.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                                                                                                                                |
| È a valore singolo       | Vero                                                                                                                                                                                                                                                                 |
| Indicizzato             | Vero                                                                                                                                                                                                                                                                 |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                                                                 |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                                                                                                                                         |
| Range-Lower            | \-                                                                                                                                                                                                                                                                   |
| Range-Upper            | \-                                                                                                                                                                                                                                                                   |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                           |
| Classi utilizzate in        | [**FT-DFS**](c-ftdfs.md)<br/> [**Index-Server-Catalog**](c-indexservercatalog.md)<br/> [**MS-Print-ConnectionPolicy**](c-msprint-connectionpolicy.md)<br/> [**Coda di stampa**](c-printqueue.md)<br/> [**Volume**](c-volume.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                                                                                                                                |
| È a valore singolo       | Vero                                                                                                                                                                                                                                                                 |
| Indicizzato             | Vero                                                                                                                                                                                                                                                                 |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                                                                 |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                                                                                                                                         |
| Range-Lower            | \-                                                                                                                                                                                                                                                                   |
| Range-Upper            | \-                                                                                                                                                                                                                                                                   |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                           |
| Classi utilizzate in        | [**FT-DFS**](c-ftdfs.md)<br/> [**Index-Server-Catalog**](c-indexservercatalog.md)<br/> [**MS-Print-ConnectionPolicy**](c-msprint-connectionpolicy.md)<br/> [**Coda di stampa**](c-printqueue.md)<br/> [**Volume**](c-volume.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                                                                                                                                |
| È a valore singolo       | Vero                                                                                                                                                                                                                                                                 |
| Indicizzato             | Vero                                                                                                                                                                                                                                                                 |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                                                                 |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                                                                                                                                         |
| Range-Lower            | \-                                                                                                                                                                                                                                                                   |
| Range-Upper            | \-                                                                                                                                                                                                                                                                   |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                           |
| Classi utilizzate in        | [**FT-DFS**](c-ftdfs.md)<br/> [**Index-Server-Catalog**](c-indexservercatalog.md)<br/> [**MS-Print-ConnectionPolicy**](c-msprint-connectionpolicy.md)<br/> [**Coda di stampa**](c-printqueue.md)<br/> [**Volume**](c-volume.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                                                                                                                                |
| È a valore singolo       | Vero                                                                                                                                                                                                                                                                 |
| Indicizzato             | Vero                                                                                                                                                                                                                                                                 |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                                                                 |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                                                                                                                                         |
| Range-Lower            | \-                                                                                                                                                                                                                                                                   |
| Range-Upper            | \-                                                                                                                                                                                                                                                                   |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                           |
| Classi utilizzate in        | [**FT-DFS**](c-ftdfs.md)<br/> [**Index-Server-Catalog**](c-indexservercatalog.md)<br/> [**MS-Print-ConnectionPolicy**](c-msprint-connectionpolicy.md)<br/> [**Coda di stampa**](c-printqueue.md)<br/> [**Volume**](c-volume.md)<br/> |



 

 





