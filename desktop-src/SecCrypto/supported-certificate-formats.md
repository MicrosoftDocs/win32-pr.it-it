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
# <a name="supported-certificate-formats"></a><span data-ttu-id="abb22-103">Formati di certificato supportati</span><span class="sxs-lookup"><span data-stu-id="abb22-103">Supported Certificate Formats</span></span>

<span data-ttu-id="abb22-104">I servizi certificati possono emettere i seguenti tipi di certificati.</span><span class="sxs-lookup"><span data-stu-id="abb22-104">Certificate Services can issue the following types of certificates.</span></span>



| <span data-ttu-id="abb22-105">Termine</span><span class="sxs-lookup"><span data-stu-id="abb22-105">Term</span></span>                                                                                                                                                                                                                                                                                                                                                                                             | <span data-ttu-id="abb22-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="abb22-106">Description</span></span>                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abb22-107"><span id="X.509_version_3_SSL-compatible_client_authentication_certificate"></span><span id="x.509_version_3_ssl-compatible_client_authentication_certificate"></span><span id="X.509_VERSION_3_SSL-COMPATIBLE_CLIENT_AUTHENTICATION_CERTIFICATE"></span>Certificato di autenticazione client compatibile con SSL [*X. 509*](../secgloss/x-gly.md) versione 3</span><span class="sxs-lookup"><span data-stu-id="abb22-107"><span id="X.509_version_3_SSL-compatible_client_authentication_certificate"></span><span id="x.509_version_3_ssl-compatible_client_authentication_certificate"></span><span id="X.509_VERSION_3_SSL-COMPATIBLE_CLIENT_AUTHENTICATION_CERTIFICATE"></span>[*X.509*](../secgloss/x-gly.md) version 3 SSL-compatible client authentication certificate</span></span><br/> | <span data-ttu-id="abb22-108">Questo certificato di autenticazione client identifica un client e viene utilizzato dai server per autenticare un client che richiede l'accesso al server.</span><span class="sxs-lookup"><span data-stu-id="abb22-108">This client authentication certificate identifies a client and is used by servers to authenticate a client that requests server access.</span></span><br/>     |
| <span data-ttu-id="abb22-109"><span id="X.509_v3_SSL-compatible_server_authentication_certificate"></span><span id="x.509_v3_ssl-compatible_server_authentication_certificate"></span><span id="X.509_V3_SSL-COMPATIBLE_SERVER_AUTHENTICATION_CERTIFICATE"></span>Certificato di autenticazione server compatibile con SSL X. 509 v3</span><span class="sxs-lookup"><span data-stu-id="abb22-109"><span id="X.509_v3_SSL-compatible_server_authentication_certificate"></span><span id="x.509_v3_ssl-compatible_server_authentication_certificate"></span><span id="X.509_V3_SSL-COMPATIBLE_SERVER_AUTHENTICATION_CERTIFICATE"></span>X.509 v3 SSL-compatible server authentication certificate</span></span><br/>                                                                                         | <span data-ttu-id="abb22-110">Questo certificato di autenticazione server identifica un server e viene usato dai client per autenticare un server a cui il client vuole accedere.</span><span class="sxs-lookup"><span data-stu-id="abb22-110">This server authentication certificate identifies a server and is used by clients to authenticate a server that the client wants to access.</span></span><br/> |
| <span data-ttu-id="abb22-111"><span id="S_MIME_certificate"></span><span id="s_mime_certificate"></span><span id="S_MIME_CERTIFICATE"></span>Certificato [*S/MIME*](../secgloss/s-gly.md)</span><span class="sxs-lookup"><span data-stu-id="abb22-111"><span id="S_MIME_certificate"></span><span id="s_mime_certificate"></span><span id="S_MIME_CERTIFICATE"></span>[*S/MIME*](../secgloss/s-gly.md) certificate</span></span><br/>                                                                                                           | <span data-ttu-id="abb22-112">Questo certificato viene usato dai client per la posta elettronica sicura sotto il protocollo S/MIME (Secure/Multipurpose Internet Mail Extensions).</span><span class="sxs-lookup"><span data-stu-id="abb22-112">This certificate is used by clients for secure email under the S/MIME (Secure/Multipurpose Internet Mail Extensions) protocol.</span></span><br/>              |



 

<span data-ttu-id="abb22-113">Oltre a questi certificati, i servizi certificati possono essere usati anche per emettere altri certificati X. 509 scrivendo un modulo criteri personalizzato.</span><span class="sxs-lookup"><span data-stu-id="abb22-113">In addition to these certificates, Certificate Services can also be used to issue other X.509 certificates by writing a custom policy module.</span></span>

> [!Note]  
> <span data-ttu-id="abb22-114">"Certificato di autenticazione server" e "certificato server", oltre a "certificato di autenticazione client" e "certificato client" sono termini intercambiabili.</span><span class="sxs-lookup"><span data-stu-id="abb22-114">"Server authentication certificate" and "server certificate" as well as "client authentication certificate" and "client certificate" are interchangeable terms.</span></span>

 

<span data-ttu-id="abb22-115">Inoltre, i servizi certificati includono modelli di certificato nella configurazione dell'autorità di certificazione aziendale Microsoft.</span><span class="sxs-lookup"><span data-stu-id="abb22-115">Additionally, Certificate Services includes certificate templates in the Microsoft enterprise certification authority configuration.</span></span> <span data-ttu-id="abb22-116">Consultare la documentazione della Guida di Windows per i modelli di certificato per comprendere come definiscono gli scopi del certificato.</span><span class="sxs-lookup"><span data-stu-id="abb22-116">Consult the Windows Help documentation for certificate templates to understand how they define certificate purposes.</span></span>

 

 
