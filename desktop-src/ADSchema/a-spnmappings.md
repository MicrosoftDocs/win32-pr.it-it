---
title: SPN-Mappings attributo
description: Questo attributo a più valori contiene un elenco di nomi dell'entità servizio (SPN) per mostrare l'equivalenza dei tipi SPN.
ms.assetid: 6d37618d-426d-4e7b-8475-c912adb595ee
ms.tgt_platform: multiple
keywords:
- SPN-Mappings schema AD dell'attributo
- Schema AD dell'attributo sPNMappings
topic_type:
- apiref
api_name:
- SPN-Mappings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 451f8d3f98984f725915410e964e39a66905f29c1ccbcf9156b55d7ba51d3e5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118960050"
---
# <a name="spn-mappings-attribute"></a>SPN-Mappings attributo

Questo attributo a più valori contiene un elenco di nomi dell'entità servizio (SPN) per mostrare l'equivalenza dei tipi SPN. Il nome SPN è il nome utilizzato da un client per identificare in modo univoco un'istanza di un servizio. Se si installano più istanze di un servizio in computer distribuiti in una foresta, a ogni istanza deve essere associato un nome SPN distinto. Se i client possono usare più nomi per l'autenticazione, una determinata istanza di servizio può presentare più SPN. Ad esempio, "ldap/..." È possibile eseguire il mapping dei nomi SPN in modo che siano equivalenti a "host/..." Spn.



| Voce | Valore |
|-------------------|--------------------------------------------------------------------------------------------------------------------|
| CN                | SPN-Mappings                                                                                                       |
| Ldap-Display-Name | sPNMappings                                                                                                        |
| Dimensione              | \-                                                                                                                 |
| Aggiorna privilegio  | Questo valore viene impostato durante l'installazione del prodotto. Può essere modificato dall'amministratore di sistema in un secondo momento. |
| Frequenza di aggiornamento  | \-                                                                                                                 |
| Attribute-Id      | 1.2.840.113556.1.4.1347                                                                                            |
| System-Id-Guid    | 2ab0e76c-7041-11d2-9905-0000f87a57d4                                                                               |
| Sintassi            | [**String(Unicode)**](s-string-unicode.md)                                                                        |



## <a name="implementations"></a>Implementazioni

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Voce | Valore |
|------------------------|--------------------------------------------------|
| ID collegamento                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Falso                                            |
| Is-Single-Valued       | Falso                                            |
| Indicizzato             | Falso                                            |
| Nel catalogo globale      | Falso                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classi usate in        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|--------------------------------------------------|
| ID collegamento                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Falso                                            |
| Is-Single-Valued       | Falso                                            |
| Indicizzato             | Falso                                            |
| Nel catalogo globale      | Falso                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classi usate in        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|--------------------------------------------------|
| ID collegamento                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Falso                                            |
| Is-Single-Valued       | Falso                                            |
| Indicizzato             | Falso                                            |
| Nel catalogo globale      | Falso                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classi usate in        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|--------------------------------------------------|
| ID collegamento                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Falso                                            |
| Is-Single-Valued       | Falso                                            |
| Indicizzato             | Falso                                            |
| Nel catalogo globale      | Falso                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classi usate in        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|--------------------------------------------------|
| ID collegamento                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Falso                                            |
| Is-Single-Valued       | Falso                                            |
| Indicizzato             | Falso                                            |
| Nel catalogo globale      | Falso                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classi usate in        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|--------------------------------------------------|
| ID collegamento                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Falso                                            |
| Is-Single-Valued       | Falso                                            |
| Indicizzato             | Falso                                            |
| Nel catalogo globale      | Falso                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classi usate in        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



 

 





