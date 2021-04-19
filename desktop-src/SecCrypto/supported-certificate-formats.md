---
description: Elenca i formati di certificato supportati da Servizi certificati.
ms.assetid: e6a324d0-9b62-4625-a604-cb1eeca22aae
title: Formati di certificato supportati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 912f37f3e4c29ae765f68484aecf0bf9d9b8aea9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312786"
---
# <a name="supported-certificate-formats"></a>Formati di certificato supportati

I servizi certificati possono emettere i seguenti tipi di certificati.



| Termine                                                                                                                                                                                                                                                                                                                                                                                             | Descrizione                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="X.509_version_3_SSL-compatible_client_authentication_certificate"></span><span id="x.509_version_3_ssl-compatible_client_authentication_certificate"></span><span id="X.509_VERSION_3_SSL-COMPATIBLE_CLIENT_AUTHENTICATION_CERTIFICATE"></span>Certificato di autenticazione client compatibile con SSL [*X. 509*](../secgloss/x-gly.md) versione 3<br/> | Questo certificato di autenticazione client identifica un client e viene utilizzato dai server per autenticare un client che richiede l'accesso al server.<br/>     |
| <span id="X.509_v3_SSL-compatible_server_authentication_certificate"></span><span id="x.509_v3_ssl-compatible_server_authentication_certificate"></span><span id="X.509_V3_SSL-COMPATIBLE_SERVER_AUTHENTICATION_CERTIFICATE"></span>Certificato di autenticazione server compatibile con SSL X. 509 v3<br/>                                                                                         | Questo certificato di autenticazione server identifica un server e viene usato dai client per autenticare un server a cui il client vuole accedere.<br/> |
| <span id="S_MIME_certificate"></span><span id="s_mime_certificate"></span><span id="S_MIME_CERTIFICATE"></span>Certificato [*S/MIME*](../secgloss/s-gly.md)<br/>                                                                                                           | Questo certificato viene usato dai client per la posta elettronica sicura sotto il protocollo S/MIME (Secure/Multipurpose Internet Mail Extensions).<br/>              |



 

Oltre a questi certificati, i servizi certificati possono essere usati anche per emettere altri certificati X. 509 scrivendo un modulo criteri personalizzato.

> [!Note]  
> "Certificato di autenticazione server" e "certificato server", oltre a "certificato di autenticazione client" e "certificato client" sono termini intercambiabili.

 

Inoltre, i servizi certificati includono modelli di certificato nella configurazione dell'autorità di certificazione aziendale Microsoft. Consultare la documentazione della Guida di Windows per i modelli di certificato per comprendere come definiscono gli scopi del certificato.

 

 
