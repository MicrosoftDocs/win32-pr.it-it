---
title: Product-Code attributo
description: Questo attributo contiene un identificatore univoco per un'applicazione per una determinata versione del prodotto, rappresentato come GUID stringa, ad esempio \ 0034; 12345678-1234-1234-1234-123456789012 \ 0034;.
ms.assetid: 1fb50a4c-1a6a-4231-a6b2-92f6bc4a1ead
ms.tgt_platform: multiple
keywords:
- Product-Code schema AD dell'attributo
- Schema AD dell'attributo productCode
topic_type:
- apiref
api_name:
- Product-Code
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d527263787b68fbe7ab328fa5d1e91a0b7b9dd2385b29d5e6b0bb4a9fedc0400
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118681749"
---
# <a name="product-code-attribute"></a>Product-Code attributo

Questo attributo contiene un identificatore univoco per un'applicazione per una determinata versione del prodotto, rappresentato come GUID di stringa, ad esempio " {12345678-1234-1234-1234-123456789012} ". Le lettere usate in questo GUID devono essere maiuscole. Questo ID deve variare per versioni e lingue diverse.



| Voce | Valore |
|-------------------|-------------------------------------------------------|
| CN                | Product-Code                                          |
| Ldap-Display-Name | productCode                                           |
| Dimensione              | \-                                                    |
| Privilegio di aggiornamento  | \-                                                    |
| Frequenza di aggiornamento  | \-                                                    |
| Attribute-Id      | 1.2.840.113556.1.4.818                                |
| System-Id-Guid    | d9e18317-8939-11d1-aebc-0000f80367c1                  |
| Sintassi            | [**Object(Replica-Link)**](s-object-replica-link.md) |



## <a name="implementations"></a>Implementazioni

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Voce | Valore |
|------------------------|------------------------------------------------------------------|
| ID collegamento                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | Falso                                                            |
| Is-Single-Valued       | Vero                                                             |
| Indicizzato             | Falso                                                            |
| Nel catalogo globale      | Falso                                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                     |
| Range-Lower            | 0                                                                |
| Range-Upper            | 16                                                               |
| Search-Flags           | 0x00000000                                                       |
| System-Flags           | 0x00000010                                                       |
| Classi usate in        | [**Registrazione pacchetto**](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|------------------------------------------------------------------|
| ID collegamento                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | Falso                                                            |
| Is-Single-Valued       | Vero                                                             |
| Indicizzato             | Falso                                                            |
| Nel catalogo globale      | Falso                                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                     |
| Range-Lower            | 0                                                                |
| Range-Upper            | 16                                                               |
| Search-Flags           | 0x00000000                                                       |
| System-Flags           | 0x00000010                                                       |
| Classi usate in        | [**Registrazione pacchetto**](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|------------------------------------------------------------------|
| ID collegamento                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | Falso                                                            |
| Is-Single-Valued       | Vero                                                             |
| Indicizzato             | Falso                                                            |
| Nel catalogo globale      | Falso                                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                     |
| Range-Lower            | 0                                                                |
| Range-Upper            | 16                                                               |
| Search-Flags           | 0x00000000                                                       |
| System-Flags           | 0x00000010                                                       |
| Classi usate in        | [**Registrazione del pacchetto**](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|------------------------------------------------------------------|
| ID collegamento                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | Falso                                                            |
| A valore singolo       | Vero                                                             |
| Indicizzato             | Falso                                                            |
| Nel catalogo globale      | Falso                                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                     |
| Range-Lower            | 0                                                                |
| Range-Upper            | 16                                                               |
| Search-Flags           | 0x00000000                                                       |
| System-Flags           | 0x00000010                                                       |
| Classi usate in        | [**Registrazione del pacchetto**](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|------------------------------------------------------------------|
| ID collegamento                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | Falso                                                            |
| A valore singolo       | Vero                                                             |
| Indicizzato             | Falso                                                            |
| Nel catalogo globale      | Falso                                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                     |
| Range-Lower            | 0                                                                |
| Range-Upper            | 16                                                               |
| Search-Flags           | 0x00000000                                                       |
| System-Flags           | 0x00000010                                                       |
| Classi usate in        | [**Registrazione del pacchetto**](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|------------------------------------------------------------------|
| ID collegamento                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | Falso                                                            |
| A valore singolo       | Vero                                                             |
| Indicizzato             | Falso                                                            |
| Nel catalogo globale      | Falso                                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                     |
| Range-Lower            | 0                                                                |
| Range-Upper            | 16                                                               |
| Search-Flags           | 0x00000000                                                       |
| System-Flags           | 0x00000010                                                       |
| Classi usate in        | [**Registrazione del pacchetto**](c-packageregistration.md)<br/> |



 

 





