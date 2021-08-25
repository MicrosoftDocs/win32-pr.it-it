---
title: Attributo Keywords
description: Elenco di parole chiave che possono essere usate per individuare un punto di connessione specificato.
ms.assetid: 24297ebf-8d32-4b22-9dd9-b26bce675118
ms.tgt_platform: multiple
keywords:
- Attributo Keywords Schema DI AD
- Attributo keywords Schema DI AD
topic_type:
- apiref
api_name:
- Keywords
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f2efa6f3b24aae32cdd0501a5474133981f2c9e582997663480814c6d1167e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119924821"
---
# <a name="keywords-attribute"></a>Attributo Keywords

Elenco di parole chiave che possono essere usate per individuare un punto di connessione specificato.



| Voce | Valore |
|-------------------|---------------------------------------------|
| CN                | Parole chiave                                    |
| Ldap-Display-Name | keywords                                    |
| Dimensione              | \-                                          |
| Privilegio di aggiornamento  | \-                                          |
| Frequenza di aggiornamento  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.48                       |
| System-Id-Guid    | bf967993-0de6-11d0-a285-00aa003049e2        |
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
|------------------------|----------------------------------------------------------|
| ID collegamento                | \-                                                       |
| MAPI-Id                | \-                                                       |
| System-Only            | Falso                                                    |
| Is-Single-Valued       | Falso                                                    |
| Indicizzato             | Vero                                                     |
| Nel catalogo globale      | Vero                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                             |
| Range-Lower            | 1                                                        |
| Range-Upper            | 256                                                      |
| Search-Flags           | 0x00000001                                               |
| System-Flags           | 0x00000010                                               |
| Classi usate in        | [**Punto di connessione**](c-connectionpoint.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                      |
| System-Only            | Falso                                                                                                                                                                                                                                                                                   |
| Is-Single-Valued       | Falso                                                                                                                                                                                                                                                                                   |
| Indicizzato             | Vero                                                                                                                                                                                                                                                                                    |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                                                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                              |
| Classi usate in        | [**Versione dell'applicazione**](c-applicationversion.md)<br/> [**Punto di connessione**](c-connectionpoint.md)<br/> [**FT-Dfs**](c-ftdfs.md)<br/> [**ms-DS-App-Configuration**](c-msds-app-configuration.md)<br/> [**ms-DS-App-Data**](c-msds-appdata.md)<br/> |



## <a name="adam"></a>Adam



| Voce | Valore |
|------------------------|--------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                       |
| MAPI-Id                | \-                                                                                                                       |
| System-Only            | Falso                                                                                                                    |
| Is-Single-Valued       | Falso                                                                                                                    |
| Indicizzato             | Vero                                                                                                                     |
| Nel catalogo globale      | Vero                                                                                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                             |
| Range-Lower            | 1                                                                                                                        |
| Range-Upper            | 256                                                                                                                      |
| Search-Flags           | 0x00000001                                                                                                               |
| System-Flags           | 0x00000010                                                                                                               |
| Classi usate in        | [**ms-DS-Service-Connection-Point-Publication-Service**](c-msds-serviceconnectionpointpublicationservice.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                      |
| System-Only            | Falso                                                                                                                                                                                                                                                                                   |
| Is-Single-Valued       | Falso                                                                                                                                                                                                                                                                                   |
| Indicizzato             | Vero                                                                                                                                                                                                                                                                                    |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                                                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                              |
| Classi usate in        | [**Versione dell'applicazione**](c-applicationversion.md)<br/> [**Punto di connessione**](c-connectionpoint.md)<br/> [**FT-Dfs**](c-ftdfs.md)<br/> [**ms-DS-App-Configuration**](c-msds-app-configuration.md)<br/> [**ms-DS-App-Data**](c-msds-appdata.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                      |
| System-Only            | Falso                                                                                                                                                                                                                                                                                   |
| Is-Single-Valued       | Falso                                                                                                                                                                                                                                                                                   |
| Indicizzato             | Vero                                                                                                                                                                                                                                                                                    |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                                                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                              |
| Classi usate in        | [**Versione dell'applicazione**](c-applicationversion.md)<br/> [**Punto di connessione**](c-connectionpoint.md)<br/> [**FT-Dfs**](c-ftdfs.md)<br/> [**ms-DS-App-Configuration**](c-msds-app-configuration.md)<br/> [**ms-DS-App-Data**](c-msds-appdata.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                      |
| System-Only            | Falso                                                                                                                                                                                                                                                                                   |
| Is-Single-Valued       | Falso                                                                                                                                                                                                                                                                                   |
| Indicizzato             | Vero                                                                                                                                                                                                                                                                                    |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                                                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                              |
| Classi usate in        | [**Versione dell'applicazione**](c-applicationversion.md)<br/> [**Punto di connessione**](c-connectionpoint.md)<br/> [**FT-Dfs**](c-ftdfs.md)<br/> [**ms-DS-App-Configuration**](c-msds-app-configuration.md)<br/> [**ms-DS-App-Data**](c-msds-appdata.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                      |
| System-Only            | Falso                                                                                                                                                                                                                                                                                   |
| Is-Single-Valued       | Falso                                                                                                                                                                                                                                                                                   |
| Indicizzato             | Vero                                                                                                                                                                                                                                                                                    |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                                                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                              |
| Classi usate in        | [**Versione applicazione**](c-applicationversion.md)<br/> [**Punto di connessione**](c-connectionpoint.md)<br/> [**FT-Dfs**](c-ftdfs.md)<br/> [**ms-DS-App-Configuration**](c-msds-app-configuration.md)<br/> [**ms-DS-App-Data**](c-msds-appdata.md)<br/> |



 

 





