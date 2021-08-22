---
title: X509-Cert attributo
description: Contiene i certificati X.509v3 con codifica DER rilasciati all'utente. Si noti che questa proprietà contiene i certificati a chiave pubblica rilasciati a questo utente dal Servizio certificati Microsoft.
ms.assetid: bdd6b9a4-c402-462c-be2c-8e7e582a899a
ms.tgt_platform: multiple
keywords:
- X509-Cert schema AD dell'attributo
- Attributo userCertificate Schema DI AD
topic_type:
- apiref
api_name:
- X509-Cert
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0d6d95ab05047c19ba978a02957dca3870c2f93cf26b323bd6aa55c2f35472a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644591"
---
# <a name="x509-cert-attribute"></a>X509-Cert attributo

Contiene i certificati X.509v3 con codifica DER rilasciati all'utente. Si noti che questa proprietà contiene i certificati a chiave pubblica rilasciati a questo utente dal Servizio certificati Microsoft.



| Voce | Valore |
|-------------------|-------------------------------------------------------------------------------------------------------------------------|
| CN                | X509-Cert                                                                                                               |
| Ldap-Display-Name | userCertificate                                                                                                         |
| Dimensione              | Questo attributo richiederà circa 4 KB per ogni certificato dell'agente di recupero chiavi emesso dalla CA usando l'istanza DI ENTERPRISE. |
| Aggiorna privilegio  | Amministratore di dominio                                                                                                    |
| Frequenza di aggiornamento  | Ogni volta che viene emesso un certificato.                                                                                      |
| Attribute-Id      | 2.5.4.36                                                                                                                |
| System-Id-Guid    | bf967a7f-0de6-11d0-a285-00aa003049e2                                                                                    |
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
| Is-Single-Valued       | Falso                                                                                  |
| Indicizzato             | Falso                                                                                  |
| Nel catalogo globale      | Vero                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                           |
| Range-Lower            | \-                                                                                     |
| Range-Upper            | \-                                                                                     |
| Search-Flags           | 0x00000000                                                                             |
| System-Flags           | 0x00000010                                                                             |
| Classi usate in        | [**Destinatario posta elettronica**](c-mailrecipient.md)<br/> [**Utente**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x8C6A                                                                                                                                                                                                                             |
| System-Only            | Falso                                                                                                                                                                                                                              |
| Is-Single-Valued       | Falso                                                                                                                                                                                                                              |
| Indicizzato             | Falso                                                                                                                                                                                                                              |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                       |
| Range-Lower            | \-                                                                                                                                                                                                                                 |
| Range-Upper            | \-                                                                                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                         |
| Classi usate in        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Destinatario posta elettronica**](c-mailrecipient.md)<br/> [**ms-PKI-Private-Key-Recovery-Agent**](c-mspki-privatekeyrecoveryagent.md)<br/> [**Utente**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x8C6A                                                                                                                                                                                                                             |
| System-Only            | Falso                                                                                                                                                                                                                              |
| Is-Single-Valued       | Falso                                                                                                                                                                                                                              |
| Indicizzato             | Falso                                                                                                                                                                                                                              |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                       |
| Range-Lower            | \-                                                                                                                                                                                                                                 |
| Range-Upper            | \-                                                                                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                         |
| Classi usate in        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/> [**ms-PKI-Private-Key-Recovery-Agent**](c-mspki-privatekeyrecoveryagent.md)<br/> [**Utente**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x8C6A                                                                                                                                                                                                                             |
| System-Only            | Falso                                                                                                                                                                                                                              |
| Is-Single-Valued       | Falso                                                                                                                                                                                                                              |
| Indicizzato             | Falso                                                                                                                                                                                                                              |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                       |
| Range-Lower            | \-                                                                                                                                                                                                                                 |
| Range-Upper            | \-                                                                                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                         |
| Classi usate in        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/> [**ms-PKI-Private-Key-Recovery-Agent**](c-mspki-privatekeyrecoveryagent.md)<br/> [**Utente**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x8C6A                                                                                                                                                                                                                             |
| System-Only            | Falso                                                                                                                                                                                                                              |
| Is-Single-Valued       | Falso                                                                                                                                                                                                                              |
| Indicizzato             | Falso                                                                                                                                                                                                                              |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                       |
| Range-Lower            | \-                                                                                                                                                                                                                                 |
| Range-Upper            | \-                                                                                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                         |
| Classi usate in        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/> [**ms-PKI-Private-Key-Recovery-Agent**](c-mspki-privatekeyrecoveryagent.md)<br/> [**Utente**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x8C6A                                                                                                                                                                                                                             |
| System-Only            | Falso                                                                                                                                                                                                                              |
| Is-Single-Valued       | Falso                                                                                                                                                                                                                              |
| Indicizzato             | Falso                                                                                                                                                                                                                              |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                       |
| Range-Lower            | \-                                                                                                                                                                                                                                 |
| Range-Upper            | \-                                                                                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                         |
| Classi usate in        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Destinatario di posta elettronica**](c-mailrecipient.md)<br/> [**ms-PKI-Private-Key-Recovery-Agent**](c-mspki-privatekeyrecoveryagent.md)<br/> [**Utente**](c-user.md)<br/> |



 

 





