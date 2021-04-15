---
title: Identità endpoint
description: I tipi definiti in questa sezione vengono utilizzati per definire l'identità di sicurezza di un indirizzo endpoint.
ms.assetid: 39639b9a-32e2-44d2-9bda-a2ad23850de8
keywords:
- Endpoint Identity Web Services per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a7a3f7b95d5fc1b926d8bafb49b06f96c7d68fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395370"
---
# <a name="endpoint-identity"></a>Identità endpoint

I tipi definiti in questa sezione vengono utilizzati per definire l'identità di sicurezza di un indirizzo endpoint.

Gli elementi API seguenti fanno parte del rientro dell'endpoint:



| Enumerazione                                                       | Descrizione                                                                                                                   |
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ tipo identità endpoint \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_endpoint_identity_type) | Tipo di identità dell'endpoint, utilizzato come selettore per sottotipi di [**identità WS \_ endpoint \_**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_identity). |



 



| Struttura                                                               | Descrizione                                                                                  |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**\_ \_ identità endpoint WS \_ CERT**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_endpoint_identity)       | Tipo per l'identità dell'endpoint del certificato.                                                 |
| [**\_ \_ identità endpoint DNS \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_dns_endpoint_identity)         | Tipo per specificare un'identità dell'endpoint rappresentata da un nome DNS.                      |
| [**\_identità endpoint \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_identity)                  | Tipo di base per tutte le identità dell'endpoint.                                                   |
| [**\_ \_ identità endpoint WS \_ RSA**](/windows/desktop/api/WebServices/ns-webservices-ws_rsa_endpoint_identity)         | Digitare per l'identità dell'endpoint RSA.                                                              |
| [**\_identità dell' \_ endpoint WS SPN \_**](/windows/desktop/api/WebServices/ns-webservices-ws_spn_endpoint_identity)         | Tipo per specificare un'identità dell'endpoint rappresentata da un SPN (nome dell'entità servizio). |
| [**\_ \_ identità endpoint sconosciuta \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_unknown_endpoint_identity) | Tipo per un'identità dell'endpoint sconosciuta.                                                   |
| [**identità dell'endpoint di WS \_ UPN \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_upn_endpoint_identity)         | Tipo per specificare un'identità dell'endpoint rappresentata da un UPN (nome dell'entità utente).     |



 

 

 




