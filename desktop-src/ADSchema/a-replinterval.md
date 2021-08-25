---
title: Repl-Interval attributo
description: Attributo di Site-Link che definisce l'intervallo, in minuti, tra i cicli di replica tra i siti nell'elenco siti.
ms.assetid: ef4cbf75-7283-4930-9f98-1ffd6eb05669
ms.tgt_platform: multiple
keywords:
- Repl-Interval schema AD dell'attributo
- Schema AD dell'attributo replInterval
topic_type:
- apiref
api_name:
- Repl-Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb5cd02d3458684f6d70cff84435c7809fcd4c912befd65373a264f961cefd72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119837441"
---
# <a name="repl-interval-attribute"></a>Repl-Interval attributo

Attributo di Site-Link che definisce l'intervallo, in minuti, tra i cicli di replica tra i siti nell'elenco siti. Deve essere un multiplo di 15 minuti (la granularità della replica DS tra siti), un minimo di 15 minuti e un massimo di 10.080 minuti (una settimana).



| Voce | Valore |
|-------------------|------------------------------------------------|
| CN                | Repl-Interval                                  |
| Ldap-Display-Name | replInterval                                   |
| Dimensione              | 4 byte                                        |
| Privilegio di aggiornamento  | Amministratore dell'organizzazione                       |
| Frequenza di aggiornamento  | Quando l'intervallo di replica deve cambiare. |
| Attribute-Id      | 1.2.840.113556.1.4.1336                        |
| System-Id-Guid    | 45ba9d1a-56fa-11d2-90d0-00c04fd91ab1           |
| Sintassi            | [**Enumerazione**](s-enumeration.md)           |



## <a name="implementations"></a>Implementazioni

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adam**](#adam)
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
| Is-Single-Valued       | Vero                                                                                                       |
| Indicizzato             | Falso                                                                                                      |
| Nel catalogo globale      | Falso                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| Classi usate in        | [**Trasporto tra siti**](c-intersitetransport.md)<br/> [**Collegamento al sito**](c-sitelink.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | Falso                                                                                                      |
| Is-Single-Valued       | Vero                                                                                                       |
| Indicizzato             | Falso                                                                                                      |
| Nel catalogo globale      | Falso                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| Classi usate in        | [**Trasporto tra siti**](c-intersitetransport.md)<br/> [**Collegamento al sito**](c-sitelink.md)<br/> |



## <a name="adam"></a>Adam



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | Falso                                                                                                      |
| Is-Single-Valued       | Vero                                                                                                       |
| Indicizzato             | Falso                                                                                                      |
| Nel catalogo globale      | Falso                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| Classi usate in        | [**Trasporto tra siti**](c-intersitetransport.md)<br/> [**Collegamento di sito**](c-sitelink.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | Falso                                                                                                      |
| Is-Single-Valued       | Vero                                                                                                       |
| Indicizzato             | Falso                                                                                                      |
| Nel catalogo globale      | Falso                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| Classi usate in        | [**Trasporto tra siti**](c-intersitetransport.md)<br/> [**Collegamento di sito**](c-sitelink.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | Falso                                                                                                      |
| Is-Single-Valued       | Vero                                                                                                       |
| Indicizzato             | Falso                                                                                                      |
| Nel catalogo globale      | Falso                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| Classi usate in        | [**Trasporto tra siti**](c-intersitetransport.md)<br/> [**Collegamento di sito**](c-sitelink.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | Falso                                                                                                      |
| Is-Single-Valued       | Vero                                                                                                       |
| Indicizzato             | Falso                                                                                                      |
| Nel catalogo globale      | Falso                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| Classi usate in        | [**Trasporto tra siti**](c-intersitetransport.md)<br/> [**Collegamento di sito**](c-sitelink.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | Falso                                                                                                      |
| Is-Single-Valued       | Vero                                                                                                       |
| Indicizzato             | Falso                                                                                                      |
| Nel catalogo globale      | Falso                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| Classi usate in        | [**Trasporto tra siti**](c-intersitetransport.md)<br/> [**Collegamento di sito**](c-sitelink.md)<br/> |



 

 





