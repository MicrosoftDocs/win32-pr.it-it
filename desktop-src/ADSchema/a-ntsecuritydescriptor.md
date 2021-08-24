---
title: Attributo NT-Security-Descriptor
description: Descrittore Windows NT di sicurezza per l'oggetto schema. Un descrittore di sicurezza è una struttura di dati che contiene informazioni di sicurezza su un oggetto, ad esempio la proprietà e le autorizzazioni dell'oggetto.
ms.assetid: 3a17b584-97ea-441c-846e-3031aea171b2
ms.tgt_platform: multiple
keywords:
- Schema AD dell'attributo NT-Security-Descriptor
- Schema AD dell'attributo nTSecurityDescriptor
topic_type:
- apiref
api_name:
- NT-Security-Descriptor
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d33b5753429b63638f1f1c9a3103aa8d78bd8590b77ceebec4fff05b82e10dd6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119703011"
---
# <a name="nt-security-descriptor-attribute"></a>Attributo NT-Security-Descriptor

Descrittore Windows NT di sicurezza per l'oggetto schema. Un descrittore di sicurezza è una struttura di dati che contiene informazioni di sicurezza su un oggetto, ad esempio la proprietà e le autorizzazioni dell'oggetto.

Per informazioni sul formato di questo valore, vedere [Security Descriptor String Format (Windows)](https://msdn.microsoft.com/library(d=robot)/aa379570(d=robot,l=en-us,v=vs.85).aspx).



| Voce | Valore |
|-------------------|-----------------------------------------------------|
| CN                | NT-Security-Descriptor                              |
| Ldap-Display-Name | Ntsecuritydescriptor                                |
| Dimensione              | \-                                                  |
| Privilegio di aggiornamento  | \-                                                  |
| Frequenza di aggiornamento  | \-                                                  |
| Attribute-Id      | 1.2.840.113556.1.2.281                              |
| System-Id-Guid    | bf9679e3-0de6-11d0-a285-00aa003049e2                |
| Sintassi            | [**String(NT-Sec-Desc)**](s-string-nt-sec-desc.md) |



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
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | Falso                                                                                                                                              |
| Is-Single-Valued       | Vero                                                                                                                                               |
| Indicizzato             | Falso                                                                                                                                              |
| Nel catalogo globale      | Vero                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x00000012                                                                                                                                         |
| Classi usate in        | [**Sam-Domain-Base**](c-samdomainbase.md)<br/> [**Entità di sicurezza**](c-securityprincipal.md)<br/> [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | Falso                                                                                                                                              |
| Is-Single-Valued       | Vero                                                                                                                                               |
| Indicizzato             | Falso                                                                                                                                              |
| Nel catalogo globale      | Vero                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x0000001A                                                                                                                                         |
| Classi usate in        | [**Sam-Domain-Base**](c-samdomainbase.md)<br/> [**Entità di sicurezza**](c-securityprincipal.md)<br/> [**In alto**](c-top.md)<br/> |



## <a name="adam"></a>Adam



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                           |
| MAPI-Id                | 0x8013                                                                                       |
| System-Only            | Falso                                                                                        |
| Is-Single-Valued       | Vero                                                                                         |
| Indicizzato             | Falso                                                                                        |
| Nel catalogo globale      | Vero                                                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                 |
| Range-Lower            | 0                                                                                            |
| Range-Upper            | 132096                                                                                       |
| Search-Flags           | 0x00000008                                                                                   |
| System-Flags           | 0x0000001A                                                                                   |
| Classi usate in        | [**Entità di sicurezza**](c-securityprincipal.md)<br/> [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | Falso                                                                                                                                              |
| Is-Single-Valued       | Vero                                                                                                                                               |
| Indicizzato             | Falso                                                                                                                                              |
| Nel catalogo globale      | Vero                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x0000001A                                                                                                                                         |
| Classi usate in        | [**Sam-Domain-Base**](c-samdomainbase.md)<br/> [**Entità di sicurezza**](c-securityprincipal.md)<br/> [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | Falso                                                                                                                                              |
| Is-Single-Valued       | Vero                                                                                                                                               |
| Indicizzato             | Falso                                                                                                                                              |
| Nel catalogo globale      | Vero                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x0000001A                                                                                                                                         |
| Classi usate in        | [**Sam-Domain-Base**](c-samdomainbase.md)<br/> [**Entità di sicurezza**](c-securityprincipal.md)<br/> [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | Falso                                                                                                                                              |
| Is-Single-Valued       | Vero                                                                                                                                               |
| Indicizzato             | Falso                                                                                                                                              |
| Nel catalogo globale      | Vero                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x0000001A                                                                                                                                         |
| Classi usate in        | [**Sam-Domain-Base**](c-samdomainbase.md)<br/> [**Entità di sicurezza**](c-securityprincipal.md)<br/> [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | Falso                                                                                                                                              |
| Is-Single-Valued       | Vero                                                                                                                                               |
| Indicizzato             | Falso                                                                                                                                              |
| Nel catalogo globale      | Vero                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x0000001A                                                                                                                                         |
| Classi usate in        | [**Sam-Domain-Base**](c-samdomainbase.md)<br/> [**Entità di sicurezza**](c-securityprincipal.md)<br/> [**In alto**](c-top.md)<br/> |



 

 





