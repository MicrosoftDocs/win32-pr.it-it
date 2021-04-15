---
title: Attributo SPN-Mappings
description: Questo attributo a più valori contiene un elenco di nomi dell'entità servizio (SPN) per mostrare l'equivalenza dei tipi SPN.
ms.assetid: 6d37618d-426d-4e7b-8475-c912adb595ee
ms.tgt_platform: multiple
keywords:
- Schema AD SPN-Mappings attribute
- Schema AD dell'attributo sPNMappings
topic_type:
- apiref
api_name:
- SPN-Mappings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3ccb07e068a22d0a85928832890f0b66ebda016
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519982"
---
# <a name="spn-mappings-attribute"></a>Attributo SPN-Mappings

Questo attributo a più valori contiene un elenco di nomi dell'entità servizio (SPN) per mostrare l'equivalenza dei tipi SPN. SPN è il nome usato da un client per identificare in modo univoco un'istanza di un servizio. Se si installano più istanze di un servizio in computer distribuiti in una foresta, a ogni istanza deve essere associato un nome SPN distinto. Se i client possono usare più nomi per l'autenticazione, una determinata istanza di servizio può presentare più SPN. Ad esempio, "LDAP/..." È possibile eseguire il mapping degli SPN in modo che siano equivalenti a "host/..." SPN.



| Voce | Valore |
|-------------------|--------------------------------------------------------------------------------------------------------------------|
| CN                | SPN-Mappings                                                                                                       |
| LDAP-Display-Name | sPNMappings                                                                                                        |
| Dimensione              | \-                                                                                                                 |
| Privilegio aggiornamento  | Questo valore viene impostato durante l'installazione del prodotto. Può essere modificato dall'amministratore di sistema in un secondo momento. |
| Frequenza di aggiornamento  | \-                                                                                                                 |
| Attribute-Id      | 1.2.840.113556.1.4.1347                                                                                            |
| System-ID-GUID    | 2ab0e76c-7041-11d2-9905-0000f87a57d4                                                                               |
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
| È a valore singolo       | Falso                                            |
| Indicizzato             | Falso                                            |
| Nel catalogo globale      | Falso                                            |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classi utilizzate in        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|--------------------------------------------------|
| ID collegamento                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Falso                                            |
| È a valore singolo       | Falso                                            |
| Indicizzato             | Falso                                            |
| Nel catalogo globale      | Falso                                            |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classi utilizzate in        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|--------------------------------------------------|
| ID collegamento                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Falso                                            |
| È a valore singolo       | Falso                                            |
| Indicizzato             | Falso                                            |
| Nel catalogo globale      | Falso                                            |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classi utilizzate in        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|--------------------------------------------------|
| ID collegamento                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Falso                                            |
| È a valore singolo       | Falso                                            |
| Indicizzato             | Falso                                            |
| Nel catalogo globale      | Falso                                            |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classi utilizzate in        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|--------------------------------------------------|
| ID collegamento                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Falso                                            |
| È a valore singolo       | Falso                                            |
| Indicizzato             | Falso                                            |
| Nel catalogo globale      | Falso                                            |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classi utilizzate in        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|--------------------------------------------------|
| ID collegamento                | \-                                               |
| MAPI-Id                | \-                                               |
| System-Only            | Falso                                            |
| È a valore singolo       | Falso                                            |
| Indicizzato             | Falso                                            |
| Nel catalogo globale      | Falso                                            |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Classi utilizzate in        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



 

 





