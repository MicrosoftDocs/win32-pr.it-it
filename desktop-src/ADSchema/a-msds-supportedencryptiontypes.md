---
title: Attributo ms-DS-Supported-Encryption-Types
description: Algoritmi di crittografia supportati da account utente, computer o attendibilità. Nota Il KDC usa queste informazioni durante la generazione di un ticket di servizio per questo account.
ms.assetid: 6f9055a9-531e-4f4b-8703-aca5531a3bcb
ms.tgt_platform: multiple
keywords:
- Attributo ms-DS-Supported-Encryption-Types schema DI AD
- Schema AD dell'attributo msDS-SupportedEncryptionTypes
topic_type:
- apiref
api_name:
- ms-DS-Supported-Encryption-Types
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1d092061dfebcea8e9a0e4f4a060010e16102108d1e2e74f05e6df2db706141
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544341"
---
# <a name="ms-ds-supported-encryption-types-attribute"></a>Attributo ms-DS-Supported-Encryption-Types

Algoritmi di crittografia supportati da account utente, computer o attendibilità.

> [!Note]  
> Il KDC usa queste informazioni durante la generazione di un ticket di servizio per questo account. Servizi e computer possono aggiornare automaticamente questo attributo nei rispettivi account in Active Directory e pertanto devono accedere in scrittura a questo attributo.

 



| Voce | Valore |
|-------------------|--------------------------------------|
| CN                | ms-DS-Supported-Encryption-Types     |
| Ldap-Display-Name | msDS-SupportedEncryptionTypes        |
| Dimensione              | \-                                   |
| Privilegio di aggiornamento  | \-                                   |
| Frequenza di aggiornamento  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1963              |
| System-Id-Guid    | 20119867-1d04-4ab7-9371-cfc3d5df0afd |
| Sintassi            | [**Enumerazione**](s-enumeration.md) |



## <a name="implementations"></a>Implementazioni

-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                     |
| MAPI-Id                | \-                                                                                     |
| System-Only            | Falso                                                                                  |
| Is-Single-Valued       | Vero                                                                                   |
| Indicizzato             | Falso                                                                                  |
| Nel catalogo globale      | Falso                                                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                           |
| Range-Lower            | \-                                                                                     |
| Range-Upper            | \-                                                                                     |
| Search-Flags           | 0x00000000                                                                             |
| System-Flags           | 0x00000010                                                                             |
| Classi usate in        | [**Dominio trusted**](c-trusteddomain.md)<br/> [**Utente**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                     |
| MAPI-Id                | \-                                                                                     |
| System-Only            | Falso                                                                                  |
| Is-Single-Valued       | Vero                                                                                   |
| Indicizzato             | Falso                                                                                  |
| Nel catalogo globale      | Falso                                                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                           |
| Range-Lower            | \-                                                                                     |
| Range-Upper            | \-                                                                                     |
| Search-Flags           | 0x00000000                                                                             |
| System-Flags           | 0x00000010                                                                             |
| Classi usate in        | [**Dominio trusted**](c-trusteddomain.md)<br/> [**Utente**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                     |
| MAPI-Id                | \-                                                                                     |
| System-Only            | Falso                                                                                  |
| Is-Single-Valued       | Vero                                                                                   |
| Indicizzato             | Falso                                                                                  |
| Nel catalogo globale      | Falso                                                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                           |
| Range-Lower            | \-                                                                                     |
| Range-Upper            | \-                                                                                     |
| Search-Flags           | 0x00000000                                                                             |
| System-Flags           | 0x00000010                                                                             |
| Classi usate in        | [**Dominio trusted**](c-trusteddomain.md)<br/> [**Utente**](c-user.md)<br/> |



 

 





