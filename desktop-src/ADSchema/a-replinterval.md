---
title: Attributo Repl-Interval
description: Attributo di Site-Link oggetti che definiscono l'intervallo, in minuti, tra i cicli di replica tra i siti nell'elenco di siti.
ms.assetid: ef4cbf75-7283-4930-9f98-1ffd6eb05669
ms.tgt_platform: multiple
keywords:
- Schema AD Repl-Interval attribute
- Schema AD dell'attributo replInterval
topic_type:
- apiref
api_name:
- Repl-Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e681b01fbc60b775b0cb947007056dc1d3d3adbb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104122378"
---
# <a name="repl-interval-attribute"></a>Attributo Repl-Interval

Attributo di Site-Link oggetti che definiscono l'intervallo, in minuti, tra i cicli di replica tra i siti nell'elenco di siti. Deve essere un multiplo di 15 minuti (la granularità della replica DS tra siti), un minimo di 15 minuti e un massimo di 10.080 minuti (una settimana).



| Voce | Valore |
|-------------------|------------------------------------------------|
| CN                | Repl-Interval                                  |
| LDAP-Display-Name | replInterval                                   |
| Dimensione              | 4 byte                                        |
| Privilegio aggiornamento  | Amministratore dell'organizzazione                       |
| Frequenza di aggiornamento  | Quando l'intervallo di replica deve essere modificato. |
| Attribute-Id      | 1.2.840.113556.1.4.1336                        |
| System-ID-GUID    | 45ba9d1a-56fa-11d2-90d0-00c04fd91ab1           |
| Sintassi            | [**Enumerazione**](s-enumeration.md)           |



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
|------------------------|------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | Falso                                                                                                      |
| È a valore singolo       | Vero                                                                                                       |
| Indicizzato             | Falso                                                                                                      |
| Nel catalogo globale      | Falso                                                                                                      |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| Classi utilizzate in        | [**Trasporto tra siti**](c-intersitetransport.md)<br/> [**Sito-collegamento**](c-sitelink.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | Falso                                                                                                      |
| È a valore singolo       | Vero                                                                                                       |
| Indicizzato             | Falso                                                                                                      |
| Nel catalogo globale      | Falso                                                                                                      |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| Classi utilizzate in        | [**Trasporto tra siti**](c-intersitetransport.md)<br/> [**Sito-collegamento**](c-sitelink.md)<br/> |



## <a name="adam"></a>ADAM



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | Falso                                                                                                      |
| È a valore singolo       | Vero                                                                                                       |
| Indicizzato             | Falso                                                                                                      |
| Nel catalogo globale      | Falso                                                                                                      |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| Classi utilizzate in        | [**Trasporto tra siti**](c-intersitetransport.md)<br/> [**Sito-collegamento**](c-sitelink.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | Falso                                                                                                      |
| È a valore singolo       | Vero                                                                                                       |
| Indicizzato             | Falso                                                                                                      |
| Nel catalogo globale      | Falso                                                                                                      |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| Classi utilizzate in        | [**Trasporto tra siti**](c-intersitetransport.md)<br/> [**Sito-collegamento**](c-sitelink.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | Falso                                                                                                      |
| È a valore singolo       | Vero                                                                                                       |
| Indicizzato             | Falso                                                                                                      |
| Nel catalogo globale      | Falso                                                                                                      |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| Classi utilizzate in        | [**Trasporto tra siti**](c-intersitetransport.md)<br/> [**Sito-collegamento**](c-sitelink.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | Falso                                                                                                      |
| È a valore singolo       | Vero                                                                                                       |
| Indicizzato             | Falso                                                                                                      |
| Nel catalogo globale      | Falso                                                                                                      |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| Classi utilizzate in        | [**Trasporto tra siti**](c-intersitetransport.md)<br/> [**Sito-collegamento**](c-sitelink.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | Falso                                                                                                      |
| È a valore singolo       | Vero                                                                                                       |
| Indicizzato             | Falso                                                                                                      |
| Nel catalogo globale      | Falso                                                                                                      |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| Classi utilizzate in        | [**Trasporto tra siti**](c-intersitetransport.md)<br/> [**Sito-collegamento**](c-sitelink.md)<br/> |



 

 





