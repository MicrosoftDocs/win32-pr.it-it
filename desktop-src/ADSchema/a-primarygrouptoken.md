---
title: Attributo Primary-Group-Token
description: Attributo calcolato utilizzato nel recupero dell'elenco di appartenenze di un gruppo, ad esempio Domain Users. L'appartenenza completa di tali gruppi non viene archiviata in modo esplicito per motivi di ridimensionamento.
ms.assetid: b23d3b7f-074b-4f1b-bc06-b22738a8a79e
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo Primary-Group-Token
- Schema AD dell'attributo primaryGroupToken
topic_type:
- apiref
api_name:
- Primary-Group-Token
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd83e89a25a81f6d62207e48053fff5cafd279e29b482a9b80cb02de580ad3fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120065921"
---
# <a name="primary-group-token-attribute"></a>Attributo Primary-Group-Token

Attributo calcolato utilizzato nel recupero dell'elenco di appartenenze di un gruppo, ad esempio Domain Users. L'appartenenza completa di tali gruppi non viene archiviata in modo esplicito per motivi di ridimensionamento.



| Voce | Valore |
|-------------------|--------------------------------------------|
| CN                | Primary-Group-Token                        |
| Ldap-Display-Name | primaryGroupToken                          |
| Dimensione              | 4 byte                                    |
| Aggiorna privilegio  | Questo valore viene impostato dal sistema.           |
| Frequenza di aggiornamento  | Ogni volta che un gruppo primario di oggetti viene modificato. |
| Attribute-Id      | 1.2.840.113556.1.4.1412                    |
| System-Id-Guid    | c0ed8738-7efd-4481-84d9-66d2db8be369       |
| Sintassi            | [**Enumerazione**](s-enumeration.md)       |



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
|------------------------|-------------------------------------|
| ID collegamento                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | Vero                                |
| Is-Single-Valued       | Vero                                |
| Indicizzato             | Falso                               |
| Nel catalogo globale      | Falso                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| Classi usate in        | [**Group**](c-group.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|-------------------------------------|
| ID collegamento                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | Vero                                |
| Is-Single-Valued       | Vero                                |
| Indicizzato             | Falso                               |
| Nel catalogo globale      | Falso                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| Classi usate in        | [**Group**](c-group.md)<br/> |



## <a name="adam"></a>Adam



| Voce | Valore |
|------------------------|-------------------------------------|
| ID collegamento                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | Vero                                |
| Is-Single-Valued       | Vero                                |
| Indicizzato             | Falso                               |
| Nel catalogo globale      | Falso                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| Classi usate in        | [**Group**](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|-------------------------------------|
| ID collegamento                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | Vero                                |
| Is-Single-Valued       | Vero                                |
| Indicizzato             | Falso                               |
| Nel catalogo globale      | Falso                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| Classi usate in        | [**Group**](c-group.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|-------------------------------------|
| ID collegamento                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | Vero                                |
| Is-Single-Valued       | Vero                                |
| Indicizzato             | Falso                               |
| Nel catalogo globale      | Falso                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| Classi usate in        | [**Group**](c-group.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|-------------------------------------|
| ID collegamento                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | Vero                                |
| Is-Single-Valued       | Vero                                |
| Indicizzato             | Falso                               |
| Nel catalogo globale      | Falso                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| Classi usate in        | [**Group**](c-group.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|-------------------------------------|
| ID collegamento                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | Vero                                |
| Is-Single-Valued       | Vero                                |
| Indicizzato             | Falso                               |
| Nel catalogo globale      | Falso                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| Classi usate in        | [**Group**](c-group.md)<br/> |



 

 





