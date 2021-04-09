---
title: Attributo Extra-Columns
description: Si tratta di un attributo multivalore i cui valori sono costituiti da un 5 Tuple (nome di attributo), (titolo della colonna), (visibilità predefinita (0, 1)), (larghezza della colonna (\ 8211; 1 per la larghezza automatica), 0 (riservato per un utilizzo futuro deve essere zero).
ms.assetid: aafe4657-0295-4af2-a7d0-8c7561516e17
ms.tgt_platform: multiple
keywords:
- Schema AD Extra-Columns attribute
- Schema AD dell'attributo di colonne di colonne
topic_type:
- apiref
api_name:
- Extra-Columns
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de0bc74532296c5e0f23da9635bb26df299ae60b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744378"
---
# <a name="extra-columns-attribute"></a>Attributo Extra-Columns

Si tratta di un attributo multivalore i cui valori sono costituiti da un 5 tuple: (nome attributo), (titolo colonna), (visibilità predefinita (0, 1)), (larghezza colonna (1 per larghezza automatica), 0 (riservato per uso futuro deve essere zero). Questo valore viene usato dalla console utenti e computer di Active Directory.



| Voce | Valore |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CN                | Extra-Columns                                                                                                                                                        |
| LDAP-Display-Name | extraColumns                                                                                                                                                         |
| Dimensione              | Ogni valore corrisponde alla dimensione della stringa della 5 tupla sopra. Per impostazione predefinita, nel contenitore DisplaySpecifier saranno presenti 22 valori nell'oggetto visualizzato per impostazione predefinita. |
| Privilegio aggiornamento  | Amministratore di dominio                                                                                                                                                 |
| Frequenza di aggiornamento  | Questa operazione verrà aggiornata solo se è installato un servizio come Exchange.                                                                                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1687                                                                                                                                              |
| System-ID-GUID    | d24e2846-1dd9-4bcf-99d7-a6227cc86da7                                                                                                                                 |
| Sintassi            | [**String(Unicode)**](s-string-unicode.md)                                                                                                                          |



## <a name="implementations"></a>Implementazioni

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|------------------------------------------------------------|
| ID collegamento                | \-                                                         |
| MAPI-Id                | \-                                                         |
| System-Only            | Falso                                                      |
| È a valore singolo       | Falso                                                      |
| Indicizzato             | Falso                                                      |
| Nel catalogo globale      | Falso                                                      |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                               |
| Range-Lower            | \-                                                         |
| Range-Upper            | \-                                                         |
| Search-Flags           | 0x00000000                                                 |
| System-Flags           | 0x00000010                                                 |
| Classi utilizzate in        | [**Display-specifier**](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|------------------------------------------------------------|
| ID collegamento                | \-                                                         |
| MAPI-Id                | \-                                                         |
| System-Only            | Falso                                                      |
| È a valore singolo       | Falso                                                      |
| Indicizzato             | Falso                                                      |
| Nel catalogo globale      | Falso                                                      |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                               |
| Range-Lower            | \-                                                         |
| Range-Upper            | \-                                                         |
| Search-Flags           | 0x00000000                                                 |
| System-Flags           | 0x00000010                                                 |
| Classi utilizzate in        | [**Display-specifier**](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|------------------------------------------------------------|
| ID collegamento                | \-                                                         |
| MAPI-Id                | \-                                                         |
| System-Only            | Falso                                                      |
| È a valore singolo       | Falso                                                      |
| Indicizzato             | Falso                                                      |
| Nel catalogo globale      | Falso                                                      |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                               |
| Range-Lower            | \-                                                         |
| Range-Upper            | \-                                                         |
| Search-Flags           | 0x00000000                                                 |
| System-Flags           | 0x00000010                                                 |
| Classi utilizzate in        | [**Display-specifier**](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|------------------------------------------------------------|
| ID collegamento                | \-                                                         |
| MAPI-Id                | \-                                                         |
| System-Only            | Falso                                                      |
| È a valore singolo       | Falso                                                      |
| Indicizzato             | Falso                                                      |
| Nel catalogo globale      | Falso                                                      |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                               |
| Range-Lower            | \-                                                         |
| Range-Upper            | \-                                                         |
| Search-Flags           | 0x00000000                                                 |
| System-Flags           | 0x00000010                                                 |
| Classi utilizzate in        | [**Display-specifier**](c-displayspecifier.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|------------------------------------------------------------|
| ID collegamento                | \-                                                         |
| MAPI-Id                | \-                                                         |
| System-Only            | Falso                                                      |
| È a valore singolo       | Falso                                                      |
| Indicizzato             | Falso                                                      |
| Nel catalogo globale      | Falso                                                      |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                               |
| Range-Lower            | \-                                                         |
| Range-Upper            | \-                                                         |
| Search-Flags           | 0x00000000                                                 |
| System-Flags           | 0x00000010                                                 |
| Classi utilizzate in        | [**Display-specifier**](c-displayspecifier.md)<br/> |



 

 





