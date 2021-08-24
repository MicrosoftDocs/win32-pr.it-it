---
title: Code-Page attributo
description: Specifica la tabella codici per la lingua scelta dall'utente. Questo valore non viene usato da Windows 2000.
ms.assetid: f98e6fbe-0c9a-4ee0-8158-3eaaca359675
ms.tgt_platform: multiple
keywords:
- Code-Page schema AD dell'attributo
- Schema AD dell'attributo codePage
topic_type:
- apiref
api_name:
- Code-Page
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff90ba0413288ff09c5793cf582a64d88e1de32ac4a3eeaba3b6ae688bf6f8eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119442711"
---
# <a name="code-page-attribute"></a>Code-Page attributo

Specifica la tabella codici per la lingua scelta dall'utente. Questo valore non viene usato da Windows 2000.



| Voce | Valore |
|-------------------|-------------------------------------------------------|
| CN                | Code-Page                                             |
| Ldap-Display-Name | Codepage                                              |
| Dimensione              | 4 byte                                               |
| Privilegio di aggiornamento  | Amministratore di dominio                                  |
| Frequenza di aggiornamento  | Quando l'utente desidera modificare la lingua predefinita. |
| Attribute-Id      | 1.2.840.113556.1.4.16                                 |
| System-Id-Guid    | bf967938-0de6-11d0-a285-00aa003049e2                  |
| Sintassi            | [**Enumerazione**](s-enumeration.md)                  |



## <a name="implementations"></a>Implementazioni

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Voce | Valore |
|------------------------|-----------------------------------|
| ID collegamento                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| Is-Single-Valued       | Vero                              |
| Indicizzato             | Falso                             |
| Nel catalogo globale      | Falso                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| Classi usate in        | [**Utente**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|-----------------------------------|
| ID collegamento                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| Is-Single-Valued       | Vero                              |
| Indicizzato             | Falso                             |
| Nel catalogo globale      | Falso                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | 0                                 |
| Range-Upper            | 65535                             |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| Classi usate in        | [**Utente**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|-----------------------------------|
| ID collegamento                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| Is-Single-Valued       | Vero                              |
| Indicizzato             | Falso                             |
| Nel catalogo globale      | Falso                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | 0                                 |
| Range-Upper            | 65535                             |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| Classi usate in        | [**Utente**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|-----------------------------------|
| ID collegamento                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| Is-Single-Valued       | Vero                              |
| Indicizzato             | Falso                             |
| Nel catalogo globale      | Falso                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | 0                                 |
| Range-Upper            | 65535                             |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| Classi usate in        | [**Utente**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|-----------------------------------|
| ID collegamento                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| Is-Single-Valued       | Vero                              |
| Indicizzato             | Falso                             |
| Nel catalogo globale      | Falso                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | 0                                 |
| Range-Upper            | 65535                             |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| Classi usate in        | [**Utente**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|-----------------------------------|
| ID collegamento                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| Is-Single-Valued       | Vero                              |
| Indicizzato             | Falso                             |
| Nel catalogo globale      | Falso                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | 0                                 |
| Range-Upper            | 65535                             |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| Classi usate in        | [**Utente**](c-user.md)<br/> |



 

 





