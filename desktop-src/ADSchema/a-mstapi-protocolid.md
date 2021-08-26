---
title: Attributo ms-TAPI-Protocol-Id
description: Questo attributo indica il tipo di conferenza TAPI.
ms.assetid: 6114efc3-4201-4f20-81ca-4f90a9e44f60
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo ms-TAPI-Protocol-Id
- Schema AD dell'attributo msTAPI-ProtocolId
topic_type:
- apiref
api_name:
- ms-TAPI-Protocol-Id
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6fb09579ae7c97c9a44140cf634b9fab42f257401fb00091ac74209b0a4908b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120066181"
---
# <a name="ms-tapi-protocol-id-attribute"></a>Attributo ms-TAPI-Protocol-Id

Questo attributo indica il tipo di conferenza TAPI. Questo attributo viene usato per determinare come deve essere interpretato il BLOB binario nell'attributo [**ms-TAPI-Conference-BLOB.**](a-mstapi-conferenceblob.md) Questo attributo è una stringa arbitraria, in genere di lunghezza inferiore a 100 caratteri.



| Voce | Valore |
|-------------------|------------------------------------------------------------|
| CN                | ms-TAPI-Protocol-ID                                        |
| Ldap-Display-Name | msTAPI-ProtocolId                                          |
| Dimensione              | \-                                                         |
| Privilegio di aggiornamento  | Non sono necessari privilegi speciali.                            |
| Frequenza di aggiornamento  | Impostare una sola volta al momento della creazione dell'Rt-Conference oggetto . |
| Attribute-Id      | 1.2.840.113556.1.4.1699                                    |
| System-Id-Guid    | 89c1ebcf-7a5f-41fd-99ca-c900b32299ab                       |
| Sintassi            | [**String(Unicode)**](s-string-unicode.md)                |



## <a name="implementations"></a>Implementazioni

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|-------------------------------------------------------------------|
| ID collegamento                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | Falso                                                             |
| Is-Single-Valued       | Vero                                                              |
| Indicizzato             | Falso                                                             |
| Nel catalogo globale      | Falso                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000010                                                        |
| Classi usate in        | [**ms-TAPI-Rt-Conference**](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|-------------------------------------------------------------------|
| ID collegamento                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | Falso                                                             |
| Is-Single-Valued       | Vero                                                              |
| Indicizzato             | Falso                                                             |
| Nel catalogo globale      | Falso                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000010                                                        |
| Classi usate in        | [**ms-TAPI-Rt-Conference**](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|-------------------------------------------------------------------|
| ID collegamento                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | Falso                                                             |
| Is-Single-Valued       | Vero                                                              |
| Indicizzato             | Falso                                                             |
| Nel catalogo globale      | Falso                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000010                                                        |
| Classi usate in        | [**ms-TAPI-Rt-Conference**](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|-------------------------------------------------------------------|
| ID collegamento                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | Falso                                                             |
| Is-Single-Valued       | Vero                                                              |
| Indicizzato             | Falso                                                             |
| Nel catalogo globale      | Falso                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000010                                                        |
| Classi usate in        | [**ms-TAPI-Rt-Conference**](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|-------------------------------------------------------------------|
| ID collegamento                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | Falso                                                             |
| Is-Single-Valued       | Vero                                                              |
| Indicizzato             | Falso                                                             |
| Nel catalogo globale      | Falso                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000010                                                        |
| Classi usate in        | [**ms-TAPI-Rt-Conference**](c-mstapi-rtconference.md)<br/> |



 

 





