---
title: Attributo X509-Cert
description: Contiene i certificati X. 509v3 con codifica DER rilasciati all'utente. Si noti che questa proprietà contiene i certificati di chiave pubblica rilasciati all'utente dal servizio certificati Microsoft.
ms.assetid: bdd6b9a4-c402-462c-be2c-8e7e582a899a
ms.tgt_platform: multiple
keywords:
- Schema AD X509-Cert attribute
- Schema AD dell'attributo userCertificate
topic_type:
- apiref
api_name:
- X509-Cert
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faa6f0dfb5acc25890361a124e52b8b24958915f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480208"
---
# <a name="x509-cert-attribute"></a>Attributo X509-Cert

Contiene i certificati X. 509v3 con codifica DER rilasciati all'utente. Si noti che questa proprietà contiene i certificati di chiave pubblica rilasciati all'utente dal servizio certificati Microsoft.



| Voce | Valore |
|-------------------|-------------------------------------------------------------------------------------------------------------------------|
| CN                | X509-Cert                                                                                                               |
| LDAP-Display-Name | userCertificate                                                                                                         |
| Dimensione              | Questo attributo richiede circa 4 KB per ogni certificato dell'agente di recupero chiavi emesso dalla CA utilizzando l'istanza di KRA. |
| Privilegio aggiornamento  | Amministratore di dominio                                                                                                    |
| Frequenza di aggiornamento  | Ogni volta che viene emesso un certificato.                                                                                      |
| Attribute-Id      | 2.5.4.36                                                                                                                |
| System-ID-GUID    | bf967a7f-0de6-11d0-a285-00aa003049e2                                                                                    |
| Sintassi            | [**Object(Replica-Link)**](s-object-replica-link.md)                                                                   |



## <a name="implementations"></a>Implementazioni

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Voce | Valore |
|------------------------|----------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                     |
| MAPI-Id                | 0x8C6A                                                                                 |
| System-Only            | Falso                                                                                  |
| È a valore singolo       | Falso                                                                                  |
| Indicizzato             | Falso                                                                                  |
| Nel catalogo globale      | Vero                                                                                   |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                           |
| Range-Lower            | \-                                                                                     |
| Range-Upper            | \-                                                                                     |
| Search-Flags           | 0x00000000                                                                             |
| System-Flags           | 0x00000010                                                                             |
| Classi utilizzate in        | [**Destinatario posta**](c-mailrecipient.md)<br/> [**Utente**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x8C6A                                                                                                                                                                                                                             |
| System-Only            | Falso                                                                                                                                                                                                                              |
| È a valore singolo       | Falso                                                                                                                                                                                                                              |
| Indicizzato             | Falso                                                                                                                                                                                                                              |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                               |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                                                                                                       |
| Range-Lower            | \-                                                                                                                                                                                                                                 |
| Range-Upper            | \-                                                                                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                         |
| Classi utilizzate in        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Destinatario posta**](c-mailrecipient.md)<br/> [**ms-PKI-Private-Key-Recovery-Agent**](c-mspki-privatekeyrecoveryagent.md)<br/> [**Utente**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x8C6A                                                                                                                                                                                                                             |
| System-Only            | Falso                                                                                                                                                                                                                              |
| È a valore singolo       | Falso                                                                                                                                                                                                                              |
| Indicizzato             | Falso                                                                                                                                                                                                                              |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                               |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                                                                                                       |
| Range-Lower            | \-                                                                                                                                                                                                                                 |
| Range-Upper            | \-                                                                                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                         |
| Classi utilizzate in        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Destinatario posta**](c-mailrecipient.md)<br/> [**ms-PKI-Private-Key-Recovery-Agent**](c-mspki-privatekeyrecoveryagent.md)<br/> [**Utente**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x8C6A                                                                                                                                                                                                                             |
| System-Only            | Falso                                                                                                                                                                                                                              |
| È a valore singolo       | Falso                                                                                                                                                                                                                              |
| Indicizzato             | Falso                                                                                                                                                                                                                              |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                               |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                                                                                                       |
| Range-Lower            | \-                                                                                                                                                                                                                                 |
| Range-Upper            | \-                                                                                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                         |
| Classi utilizzate in        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Destinatario posta**](c-mailrecipient.md)<br/> [**ms-PKI-Private-Key-Recovery-Agent**](c-mspki-privatekeyrecoveryagent.md)<br/> [**Utente**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x8C6A                                                                                                                                                                                                                             |
| System-Only            | Falso                                                                                                                                                                                                                              |
| È a valore singolo       | Falso                                                                                                                                                                                                                              |
| Indicizzato             | Falso                                                                                                                                                                                                                              |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                               |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                                                                                                       |
| Range-Lower            | \-                                                                                                                                                                                                                                 |
| Range-Upper            | \-                                                                                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                         |
| Classi utilizzate in        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Destinatario posta**](c-mailrecipient.md)<br/> [**ms-PKI-Private-Key-Recovery-Agent**](c-mspki-privatekeyrecoveryagent.md)<br/> [**Utente**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x8C6A                                                                                                                                                                                                                             |
| System-Only            | Falso                                                                                                                                                                                                                              |
| È a valore singolo       | Falso                                                                                                                                                                                                                              |
| Indicizzato             | Falso                                                                                                                                                                                                                              |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                               |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                                                                                                       |
| Range-Lower            | \-                                                                                                                                                                                                                                 |
| Range-Upper            | \-                                                                                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                         |
| Classi utilizzate in        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Destinatario posta**](c-mailrecipient.md)<br/> [**ms-PKI-Private-Key-Recovery-Agent**](c-mspki-privatekeyrecoveryagent.md)<br/> [**Utente**](c-user.md)<br/> |



 

 





