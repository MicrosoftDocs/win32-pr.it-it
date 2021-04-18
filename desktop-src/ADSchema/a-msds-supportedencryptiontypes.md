---
title: attributi ms-DS-supported-Encryption-Types
description: Algoritmi di crittografia supportati da account utente, computer o attendibilità. Si noti che il KDC usa queste informazioni durante la generazione di un ticket di servizio per l'account.
ms.assetid: 6f9055a9-531e-4f4b-8703-aca5531a3bcb
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo di tipo crittografia-supportato da MS-DS
- attributo msDS-SupportedEncryptionTypes-schema AD
topic_type:
- apiref
api_name:
- ms-DS-Supported-Encryption-Types
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7ab16959d1f1cd4405cb661a6026f3734a134f8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303491"
---
# <a name="ms-ds-supported-encryption-types-attribute"></a>attributi ms-DS-supported-Encryption-Types

Algoritmi di crittografia supportati da account utente, computer o attendibilità.

> [!Note]  
> Il KDC usa queste informazioni durante la generazione di un ticket di servizio per l'account. I servizi e i computer possono aggiornare automaticamente questo attributo sui rispettivi account in Active Directory e pertanto necessitano dell'accesso in scrittura a questo attributo.

 



| Voce | Valore |
|-------------------|--------------------------------------|
| CN                | Tipi di crittografia supportati da MS-DS     |
| LDAP-Display-Name | msDS-SupportedEncryptionTypes        |
| Dimensione              | \-                                   |
| Privilegio aggiornamento  | \-                                   |
| Frequenza di aggiornamento  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1963              |
| System-ID-GUID    | 20119867-1d04-4ab7-9371-cfc3d5df0afd |
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
| È a valore singolo       | Vero                                                                                   |
| Indicizzato             | Falso                                                                                  |
| Nel catalogo globale      | Falso                                                                                  |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                           |
| Range-Lower            | \-                                                                                     |
| Range-Upper            | \-                                                                                     |
| Search-Flags           | 0x00000000                                                                             |
| System-Flags           | 0x00000010                                                                             |
| Classi utilizzate in        | [**Dominio trusted**](c-trusteddomain.md)<br/> [**Utente**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                     |
| MAPI-Id                | \-                                                                                     |
| System-Only            | Falso                                                                                  |
| È a valore singolo       | Vero                                                                                   |
| Indicizzato             | Falso                                                                                  |
| Nel catalogo globale      | Falso                                                                                  |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                           |
| Range-Lower            | \-                                                                                     |
| Range-Upper            | \-                                                                                     |
| Search-Flags           | 0x00000000                                                                             |
| System-Flags           | 0x00000010                                                                             |
| Classi utilizzate in        | [**Dominio trusted**](c-trusteddomain.md)<br/> [**Utente**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                     |
| MAPI-Id                | \-                                                                                     |
| System-Only            | Falso                                                                                  |
| È a valore singolo       | Vero                                                                                   |
| Indicizzato             | Falso                                                                                  |
| Nel catalogo globale      | Falso                                                                                  |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                           |
| Range-Lower            | \-                                                                                     |
| Range-Upper            | \-                                                                                     |
| Search-Flags           | 0x00000000                                                                             |
| System-Flags           | 0x00000010                                                                             |
| Classi utilizzate in        | [**Dominio trusted**](c-trusteddomain.md)<br/> [**Utente**](c-user.md)<br/> |



 

 





