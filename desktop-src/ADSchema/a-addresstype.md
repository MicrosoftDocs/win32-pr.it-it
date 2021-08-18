---
title: Address-Type attributo
description: Stringa di caratteri che descrive il formato dell'indirizzo dell'utente. I tipi di indirizzo vengono mappati ai formati di indirizzo. Ciò significa che esaminando il tipo di indirizzo di un destinatario, le applicazioni client possono determinare come formattare un indirizzo appropriato per il destinatario.
ms.assetid: ff39b1f5-1844-43e9-a4a5-2b5f7c396f34
ms.tgt_platform: multiple
keywords:
- Address-Type schema AD dell'attributo
- Attributo addressType Schema di ACTIVE Directory
topic_type:
- apiref
api_name:
- Address-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eec2ce0ff9651350803a05b3b3bf3dda663419c9948617b706688bf78057ad72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118688488"
---
# <a name="address-type-attribute"></a>Address-Type attributo

Stringa di caratteri che descrive il formato dell'indirizzo dell'utente. I tipi di indirizzo vengono mappati ai formati di indirizzo. Ciò significa che esaminando il tipo di indirizzo di un destinatario, le applicazioni client possono determinare come formattare un indirizzo appropriato per il destinatario.



| Voce | Valore |
|-------------------|---------------------------------------------------------------------------------------------------------------------------|
| CN                | Address-Type                                                                                                              |
| Ldap-Display-Name | addressType                                                                                                               |
| Dimensione              | Tipi di indirizzo: 3COM, ATT, CCMAIL, COMPUSERVE, EX, FAX, MSFAX, MCI, MHS, MS, MSA, MSN,PROFS,SMTP, SNADS, TELEX, X400, X500 |
| Aggiorna privilegio  | Questo valore viene impostato dal sistema.                                                                                          |
| Frequenza di aggiornamento  | Imposta quando viene creato l'oggetto.                                                                                           |
| Attribute-Id      | 1.2.840.113556.1.2.350                                                                                                    |
| System-Id-Guid    | 5fd42464-1262-11d0-a060-00aa006c33ed                                                                                      |
| Sintassi            | [**String(Teletex)**](s-string-teletex.md)                                                                               |



## <a name="implementations"></a>Implementazioni

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Voce | Valore |
|------------------------|----------------------------------------------------------|
| ID collegamento                | \-                                                       |
| MAPI-Id                | 0x8048                                                   |
| System-Only            | Falso                                                    |
| Is-Single-Valued       | Vero                                                     |
| Indicizzato             | Falso                                                    |
| Nel catalogo globale      | Falso                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                             |
| Range-Lower            | 1                                                        |
| Range-Upper            | 32                                                       |
| Search-Flags           | 0x00000000                                               |
| System-Flags           | 0x00000010                                               |
| Classi usate in        | [**Modello di indirizzo**](c-addresstemplate.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|----------------------------------------------------------|
| ID collegamento                | \-                                                       |
| MAPI-Id                | 0x8048                                                   |
| System-Only            | Falso                                                    |
| Is-Single-Valued       | Vero                                                     |
| Indicizzato             | Falso                                                    |
| Nel catalogo globale      | Falso                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                             |
| Range-Lower            | 1                                                        |
| Range-Upper            | 32                                                       |
| Search-Flags           | 0x00000000                                               |
| System-Flags           | 0x00000010                                               |
| Classi usate in        | [**Modello di indirizzo**](c-addresstemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|----------------------------------------------------------|
| ID collegamento                | \-                                                       |
| MAPI-Id                | 0x8048                                                   |
| System-Only            | Falso                                                    |
| Is-Single-Valued       | Vero                                                     |
| Indicizzato             | Falso                                                    |
| Nel catalogo globale      | Falso                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                             |
| Range-Lower            | 1                                                        |
| Range-Upper            | 32                                                       |
| Search-Flags           | 0x00000000                                               |
| System-Flags           | 0x00000010                                               |
| Classi usate in        | [**Modello di indirizzo**](c-addresstemplate.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|----------------------------------------------------------|
| ID collegamento                | \-                                                       |
| MAPI-Id                | 0x8048                                                   |
| System-Only            | Falso                                                    |
| Is-Single-Valued       | Vero                                                     |
| Indicizzato             | Falso                                                    |
| Nel catalogo globale      | Falso                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                             |
| Range-Lower            | 1                                                        |
| Range-Upper            | 32                                                       |
| Search-Flags           | 0x00000000                                               |
| System-Flags           | 0x00000010                                               |
| Classi usate in        | [**Modello di indirizzo**](c-addresstemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|----------------------------------------------------------|
| ID collegamento                | \-                                                       |
| MAPI-Id                | 0x8048                                                   |
| System-Only            | Falso                                                    |
| Is-Single-Valued       | Vero                                                     |
| Indicizzato             | Falso                                                    |
| Nel catalogo globale      | Falso                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                             |
| Range-Lower            | 1                                                        |
| Range-Upper            | 32                                                       |
| Search-Flags           | 0x00000000                                               |
| System-Flags           | 0x00000010                                               |
| Classi usate in        | [**Modello di indirizzo**](c-addresstemplate.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|----------------------------------------------------------|
| ID collegamento                | \-                                                       |
| MAPI-Id                | 0x8048                                                   |
| System-Only            | Falso                                                    |
| Is-Single-Valued       | Vero                                                     |
| Indicizzato             | Falso                                                    |
| Nel catalogo globale      | Falso                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                             |
| Range-Lower            | 1                                                        |
| Range-Upper            | 32                                                       |
| Search-Flags           | 0x00000000                                               |
| System-Flags           | 0x00000010                                               |
| Classi usate in        | [**Modello di indirizzo**](c-addresstemplate.md)<br/> |



 

 





