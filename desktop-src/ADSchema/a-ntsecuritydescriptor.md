---
title: NT-Security-Descriptor-attributo
description: Descrittore di sicurezza di Windows NT per l'oggetto dello schema. Un descrittore di sicurezza è una struttura di dati che contiene informazioni sulla sicurezza relative a un oggetto, ad esempio la proprietà e le autorizzazioni dell'oggetto.
ms.assetid: 3a17b584-97ea-441c-846e-3031aea171b2
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo NT-Security-descrittore
- Schema AD dell'attributo nTSecurityDescriptor
topic_type:
- apiref
api_name:
- NT-Security-Descriptor
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e951e28ce97b04380609774baf57e4c6bf8c545
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519710"
---
# <a name="nt-security-descriptor-attribute"></a>NT-Security-Descriptor-attributo

Descrittore di sicurezza di Windows NT per l'oggetto dello schema. Un descrittore di sicurezza è una struttura di dati che contiene informazioni sulla sicurezza relative a un oggetto, ad esempio la proprietà e le autorizzazioni dell'oggetto.

Per informazioni sul formato di questo valore, vedere il [formato della stringa del descrittore di sicurezza (Windows)](https://msdn.microsoft.com/library(d=robot)/aa379570(d=robot,l=en-us,v=vs.85).aspx).



| Voce | Valore |
|-------------------|-----------------------------------------------------|
| CN                | NT-Security-descrittore                              |
| LDAP-Display-Name | nTSecurityDescriptor                                |
| Dimensione              | \-                                                  |
| Privilegio aggiornamento  | \-                                                  |
| Frequenza di aggiornamento  | \-                                                  |
| Attribute-Id      | 1.2.840.113556.1.2.281                              |
| System-ID-GUID    | bf9679e3-0de6-11d0-a285-00aa003049e2                |
| Sintassi            | [**String(NT-Sec-Desc)**](s-string-nt-sec-desc.md) |



## <a name="implementations"></a>Implementazioni

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | Falso                                                                                                                                              |
| È a valore singolo       | Vero                                                                                                                                               |
| Indicizzato             | Falso                                                                                                                                              |
| Nel catalogo globale      | Vero                                                                                                                                               |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x00000012                                                                                                                                         |
| Classi utilizzate in        | [**Sam-dominio-base**](c-samdomainbase.md)<br/> [**Entità di sicurezza**](c-securityprincipal.md)<br/> [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | Falso                                                                                                                                              |
| È a valore singolo       | Vero                                                                                                                                               |
| Indicizzato             | Falso                                                                                                                                              |
| Nel catalogo globale      | Vero                                                                                                                                               |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x0000001A                                                                                                                                         |
| Classi utilizzate in        | [**Sam-dominio-base**](c-samdomainbase.md)<br/> [**Entità di sicurezza**](c-securityprincipal.md)<br/> [**In alto**](c-top.md)<br/> |



## <a name="adam"></a>ADAM



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                           |
| MAPI-Id                | 0x8013                                                                                       |
| System-Only            | Falso                                                                                        |
| È a valore singolo       | Vero                                                                                         |
| Indicizzato             | Falso                                                                                        |
| Nel catalogo globale      | Vero                                                                                         |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                 |
| Range-Lower            | 0                                                                                            |
| Range-Upper            | 132096                                                                                       |
| Search-Flags           | 0x00000008                                                                                   |
| System-Flags           | 0x0000001A                                                                                   |
| Classi utilizzate in        | [**Entità di sicurezza**](c-securityprincipal.md)<br/> [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | Falso                                                                                                                                              |
| È a valore singolo       | Vero                                                                                                                                               |
| Indicizzato             | Falso                                                                                                                                              |
| Nel catalogo globale      | Vero                                                                                                                                               |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x0000001A                                                                                                                                         |
| Classi utilizzate in        | [**Sam-dominio-base**](c-samdomainbase.md)<br/> [**Entità di sicurezza**](c-securityprincipal.md)<br/> [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | Falso                                                                                                                                              |
| È a valore singolo       | Vero                                                                                                                                               |
| Indicizzato             | Falso                                                                                                                                              |
| Nel catalogo globale      | Vero                                                                                                                                               |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x0000001A                                                                                                                                         |
| Classi utilizzate in        | [**Sam-dominio-base**](c-samdomainbase.md)<br/> [**Entità di sicurezza**](c-securityprincipal.md)<br/> [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | Falso                                                                                                                                              |
| È a valore singolo       | Vero                                                                                                                                               |
| Indicizzato             | Falso                                                                                                                                              |
| Nel catalogo globale      | Vero                                                                                                                                               |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x0000001A                                                                                                                                         |
| Classi utilizzate in        | [**Sam-dominio-base**](c-samdomainbase.md)<br/> [**Entità di sicurezza**](c-securityprincipal.md)<br/> [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | Falso                                                                                                                                              |
| È a valore singolo       | Vero                                                                                                                                               |
| Indicizzato             | Falso                                                                                                                                              |
| Nel catalogo globale      | Vero                                                                                                                                               |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x0000001A                                                                                                                                         |
| Classi utilizzate in        | [**Sam-dominio-base**](c-samdomainbase.md)<br/> [**Entità di sicurezza**](c-securityprincipal.md)<br/> [**In alto**](c-top.md)<br/> |



 

 





