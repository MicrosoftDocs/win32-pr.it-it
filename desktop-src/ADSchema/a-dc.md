---
title: Domain-Component attributo
description: Attributo di denominazione per gli oggetti Domain e DNS. In genere visualizzato come dc DomainName.
ms.assetid: 1d674af1-ed2f-4266-9704-8c6ed5a9bdd8
ms.tgt_platform: multiple
keywords:
- Domain-Component schema AD dell'attributo
- Attributo dc Schema di ACTIVE Directory
topic_type:
- apiref
api_name:
- Domain-Component
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe93b6629ac176452edbe5cdf13bf35afa955890cde369273f87990034bcd3e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118177772"
---
# <a name="domain-component-attribute"></a>Domain-Component attributo

Attributo di denominazione per gli oggetti Domain e DNS. In genere viene visualizzato come dc=DomainName.



| Voce | Valore |
|-------------------|---------------------------------------------|
| CN                | Domain-Component                            |
| Ldap-Display-Name | dc                                          |
| Dimensione              | \-                                          |
| Aggiorna privilegio  | Amministratore di dominio                        |
| Frequenza di aggiornamento  | Quando viene creato il dominio.                 |
| Attribute-Id      | 0.9.2342.19200300.100.1.25                  |
| System-Id-Guid    | 19195a55-6da0-11d0-afd3-00c04fd930c9        |
| Sintassi            | [**String(Unicode)**](s-string-unicode.md) |



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
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | Falso                                                                                                                   |
| A valore singolo       | Vero                                                                                                                    |
| Indicizzato             | Falso                                                                                                                   |
| Nel catalogo globale      | Vero                                                                                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| Classi usate in        | [**Nodo DNS**](c-dnsnode.md)<br/> [**Zona DNS**](c-dnszone.md)<br/> [**Dominio**](c-domain.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | Falso                                                                                                                   |
| A valore singolo       | Vero                                                                                                                    |
| Indicizzato             | Falso                                                                                                                   |
| Nel catalogo globale      | Vero                                                                                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| Classi usate in        | [**Nodo DNS**](c-dnsnode.md)<br/> [**Zona DNS**](c-dnszone.md)<br/> [**Dominio**](c-domain.md)<br/> |



## <a name="adam"></a>Adam



| Voce | Valore |
|------------------------|---------------------------------------|
| ID collegamento                | \-                                    |
| MAPI-Id                | \-                                    |
| System-Only            | Falso                                 |
| A valore singolo       | Vero                                  |
| Indicizzato             | Falso                                 |
| Nel catalogo globale      | Vero                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                          |
| Range-Lower            | 1                                     |
| Range-Upper            | 255                                   |
| Search-Flags           | 0x00000000                            |
| System-Flags           | 0x00000012                            |
| Classi usate in        | [**Dominio**](c-domain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | Falso                                                                                                                   |
| A valore singolo       | Vero                                                                                                                    |
| Indicizzato             | Falso                                                                                                                   |
| Nel catalogo globale      | Vero                                                                                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| Classi usate in        | [**Nodo DNS**](c-dnsnode.md)<br/> [**Zona DNS**](c-dnszone.md)<br/> [**Dominio**](c-domain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | Falso                                                                                                                   |
| A valore singolo       | Vero                                                                                                                    |
| Indicizzato             | Falso                                                                                                                   |
| Nel catalogo globale      | Vero                                                                                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| Classi usate in        | [**Nodo DNS**](c-dnsnode.md)<br/> [**Zona DNS**](c-dnszone.md)<br/> [**Dominio**](c-domain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | Falso                                                                                                                   |
| A valore singolo       | Vero                                                                                                                    |
| Indicizzato             | Falso                                                                                                                   |
| Nel catalogo globale      | Vero                                                                                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| Classi usate in        | [**Nodo DNS**](c-dnsnode.md)<br/> [**Zona DNS**](c-dnszone.md)<br/> [**Dominio**](c-domain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | Falso                                                                                                                   |
| A valore singolo       | Vero                                                                                                                    |
| Indicizzato             | Falso                                                                                                                   |
| Nel catalogo globale      | Vero                                                                                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| Classi usate in        | [**Nodo DNS**](c-dnsnode.md)<br/> [**Zona DNS**](c-dnszone.md)<br/> [**Dominio**](c-domain.md)<br/> |



 

 





