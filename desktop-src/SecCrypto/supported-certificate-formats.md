---
description: Elenca i formati di certificato supportati da Servizi certificati.
ms.assetid: e6a324d0-9b62-4625-a604-cb1eeca22aae
title: Formati di certificato supportati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85ae0c4d638e957df5ddcf251ca64578a67a58b98890401c68593dd7a12c3952
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897632"
---
# <a name="supported-certificate-formats"></a>Formati di certificato supportati

Servizi certificati può rilasciare i tipi di certificati seguenti.



| Termine                                                                                                                                                                                                                                                                                                                                                                                             | Descrizione                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="X.509_version_3_SSL-compatible_client_authentication_certificate"></span><span id="x.509_version_3_ssl-compatible_client_authentication_certificate"></span><span id="X.509_VERSION_3_SSL-COMPATIBLE_CLIENT_AUTHENTICATION_CERTIFICATE"></span>Certificato di autenticazione client compatibile con SSL [*X.509*](../secgloss/x-gly.md) versione 3<br/> | Questo certificato di autenticazione client identifica un client e viene utilizzato dai server per autenticare un client che richiede l'accesso al server.<br/>     |
| <span id="X.509_v3_SSL-compatible_server_authentication_certificate"></span><span id="x.509_v3_ssl-compatible_server_authentication_certificate"></span><span id="X.509_V3_SSL-COMPATIBLE_SERVER_AUTHENTICATION_CERTIFICATE"></span>Certificato di autenticazione server compatibile con SSL X.509 v3<br/>                                                                                         | Questo certificato di autenticazione server identifica un server e viene utilizzato dai client per autenticare un server a cui il client desidera accedere.<br/> |
| <span id="S_MIME_certificate"></span><span id="s_mime_certificate"></span><span id="S_MIME_CERTIFICATE"></span>[*Certificato S/MIME*](../secgloss/s-gly.md)<br/>                                                                                                           | Questo certificato viene usato dai client per la posta elettronica sicura con il protocollo S/MIME (Secure/Multipurpose Internet Mail Extensions).<br/>              |



 

Oltre a questi certificati, Servizi certificati può essere usato anche per rilasciare altri certificati X.509 scrivendo un modulo criteri personalizzato.

> [!Note]  
> "Certificato di autenticazione server" e "Certificato server", nonché "certificato di autenticazione client" e "certificato client" sono termini intercambiabili.

 

Servizi certificati include inoltre modelli di certificato nella configurazione dell'autorità di certificazione dell'organizzazione (enterprise) Microsoft. Consultare la Windows della Guida per i modelli di certificato per comprendere come definiscono gli scopi dei certificati.

 

 
