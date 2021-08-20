---
title: Attributo ACS-Identity-Name
description: Questo attributo contiene il DN di un utente o di un'unità organizzativa ed è l'identità di un utente o di un gruppo di utenti a cui si applicano i criteri QoS.
ms.assetid: 00e6e2bd-aec8-426f-b89e-0661c15cfd46
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo ACS-Identity-Name
- Attributo aCSIdentityName Schema AD
topic_type:
- apiref
api_name:
- ACS-Identity-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7f623f15510d38243822420925f628d427d2adc975f2b140b78dc191a91200a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838401"
---
# <a name="acs-identity-name-attribute"></a>Attributo ACS-Identity-Name

Questo attributo contiene il DN di un utente o di un'unità organizzativa ed è l'identità di un utente o di un gruppo di utenti a cui si applicano i criteri QoS.



| Voce | Valore |
|-------------------|---------------------------------------------|
| CN                | ACS-Identity-Name                           |
| Ldap-Display-Name | aCSIdentityName                             |
| Dimensione              | \-                                          |
| Aggiorna privilegio  | Amministratore di dominio                        |
| Frequenza di aggiornamento  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.784                      |
| System-Id-Guid    | dab029b6-ddf7-11d1-90a5-00c04fd91ab1        |
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
|------------------------|----------------------------------------------|
| ID collegamento                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| A valore singolo       | Falso                                        |
| Indicizzato             | Falso                                        |
| Nel catalogo globale      | Falso                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classi usate in        | [**Criteri ACS**](c-acspolicy.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|----------------------------------------------|
| ID collegamento                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| A valore singolo       | Falso                                        |
| Indicizzato             | Falso                                        |
| Nel catalogo globale      | Falso                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classi usate in        | [**Criteri ACS**](c-acspolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|----------------------------------------------|
| ID collegamento                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| A valore singolo       | Falso                                        |
| Indicizzato             | Falso                                        |
| Nel catalogo globale      | Falso                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classi usate in        | [**Criteri ACS**](c-acspolicy.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|----------------------------------------------|
| ID collegamento                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| Is-Single-Valued       | Falso                                        |
| Indicizzato             | Falso                                        |
| Nel catalogo globale      | Falso                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classi usate in        | [**ACS-Policy**](c-acspolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|----------------------------------------------|
| ID collegamento                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| Is-Single-Valued       | Falso                                        |
| Indicizzato             | Falso                                        |
| Nel catalogo globale      | Falso                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classi usate in        | [**ACS-Policy**](c-acspolicy.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|----------------------------------------------|
| ID collegamento                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falso                                        |
| Is-Single-Valued       | Falso                                        |
| Indicizzato             | Falso                                        |
| Nel catalogo globale      | Falso                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| Classi usate in        | [**ACS-Policy**](c-acspolicy.md)<br/> |



 

 





