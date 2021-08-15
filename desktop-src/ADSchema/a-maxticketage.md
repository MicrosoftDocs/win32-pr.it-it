---
title: Attributo Max-Ticket-Age
description: Questo attributo determina la quantità massima di tempo, in ore, in cui il ticket di concessione ticket (TGT) di un utente può essere usato ai fini dell'autenticazione Kerberos.
ms.assetid: 54ab0f2b-31eb-45d7-9a43-e70dc78136b5
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo Max-Ticket-Age
- Schema AD dell'attributo maxTicketAge
topic_type:
- apiref
api_name:
- Max-Ticket-Age
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9c876bbab2b60d655464129d0a59aeda110f78d8e2514866a3bcf28a859cb3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119301011"
---
# <a name="max-ticket-age-attribute"></a>Attributo Max-Ticket-Age

Questo attributo determina la quantità massima di tempo, in ore, in cui il ticket di concessione ticket (TGT) di un utente può essere usato ai fini dell'autenticazione Kerberos. Quando il TGT di un utente scade, ne deve essere richiesto uno nuovo o quello esistente deve essere rinnovato. Per impostazione predefinita, questa impostazione è impostata su 10 ore nell'oggetto Criteri di gruppo Criteri di gruppo dominio predefinito.



| Voce | Valore |
|-------------------|--------------------------------------|
| CN                | Max-Ticket-Age                       |
| Ldap-Display-Name | maxTicketAge                         |
| Dimensione              | \-                                   |
| Aggiorna privilegio  | \-                                   |
| Frequenza di aggiornamento  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.77                |
| System-Id-Guid    | bf9679be-0de6-11d0-a285-00aa003049e2 |
| Sintassi            | [**Intervallo**](s-interval.md)       |



## <a name="implementations"></a>Implementazioni

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Voce | Valore |
|------------------------|----------------------------------------------------|
| ID collegamento                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | Falso                                              |
| A valore singolo       | Vero                                               |
| Indicizzato             | Falso                                              |
| Nel catalogo globale      | Falso                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| Classi usate in        | [**Criteri di dominio**](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|----------------------------------------------------|
| ID collegamento                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | Falso                                              |
| A valore singolo       | Vero                                               |
| Indicizzato             | Falso                                              |
| Nel catalogo globale      | Falso                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| Classi usate in        | [**Criteri di dominio**](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|----------------------------------------------------|
| ID collegamento                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | Falso                                              |
| A valore singolo       | Vero                                               |
| Indicizzato             | Falso                                              |
| Nel catalogo globale      | Falso                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| Classi usate in        | [**Criteri di dominio**](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|----------------------------------------------------|
| ID collegamento                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | Falso                                              |
| Is-Single-Valued       | Vero                                               |
| Indicizzato             | Falso                                              |
| Nel catalogo globale      | Falso                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| Classi usate in        | [**Criteri di dominio**](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|----------------------------------------------------|
| ID collegamento                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | Falso                                              |
| Is-Single-Valued       | Vero                                               |
| Indicizzato             | Falso                                              |
| Nel catalogo globale      | Falso                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| Classi usate in        | [**Criteri di dominio**](c-domainpolicy.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|----------------------------------------------------|
| ID collegamento                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | Falso                                              |
| Is-Single-Valued       | Vero                                               |
| Indicizzato             | Falso                                              |
| Nel catalogo globale      | Falso                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| Classi usate in        | [**Criteri di dominio**](c-domainpolicy.md)<br/> |



 

 





