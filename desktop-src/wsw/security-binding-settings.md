---
title: Impostazioni di associazione di sicurezza
description: Le impostazioni di associazione di sicurezza controllano il modo in cui un token di sicurezza viene ottenuto o utilizzato.
ms.assetid: 4bc03cb4-1ac2-4ad1-a45d-eae8f50f5355
keywords:
- Impostazioni di associazione di sicurezza servizi Web per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c5a3d27627c3360560a38ef9cb85e3fb5ece434
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103734826"
---
# <a name="security-binding-settings"></a>Impostazioni di associazione di sicurezza

Le impostazioni di associazione di sicurezza controllano il modo in cui un token di sicurezza viene ottenuto o utilizzato. Sono rappresentati come una raccolta di coppie proprietà-valore, con le chiavi di proprietà definite dalla [**proprietà di \_ \_ associazione di \_ sicurezza WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property)di enumerazione. Ogni proprietà della raccolta ha un valore predefinito ragionevole. Di conseguenza, è possibile definire e utilizzare una descrizione di sicurezza senza specificare le impostazioni di associazione di sicurezza.


Per informazioni sulle impostazioni di sicurezza a livello di canale, con le proprietà le cui chiavi sono definite dall'enumerazione dell' [**ID della proprietà di \_ sicurezza \_ \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id) , vedere [impostazioni del canale di sicurezza](security-channel-settings.md).

Gli elementi API seguenti vengono usati con le impostazioni di associazione di sicurezza.

| Enumerazione                                                                          | Descrizione                                                                                                                                                       |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_errore WS CERT \_**](/windows/win32/api/webservices/ne-webservices-ws_value_type)                                         | Definisce gli errori correlati alla convalida del certificato.                                                                                                               |
| [**\_schema di \_ autenticazione dell'intestazione WS http \_ \_**](https://technet.microsoft.com/windows/dd401907(v=vs.60))                 | Definisce le opzioni per l'esecuzione dell'autenticazione client usando le intestazioni di autenticazione HTTP.                                                                       |
| [**\_destinazione di \_ autenticazione dell'intestazione WS http \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_http_header_auth_target)                 | Definisce la destinazione per l'associazione di sicurezza per l'autenticazione dell'intestazione HTTP.                                                                                           |
| [**\_ \_ azione token di sicurezza WS Request \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_request_security_token_action)     | Definisce il set di azioni da utilizzare quando si negoziano i token di sicurezza utilizzando WS-Trust.                                                                              |
| [**\_nome della \_ suite di algoritmi di sicurezza WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_algorithm_suite_name)     | Una suite di algoritmi di sicurezza usati per attività come la firma e la encryting.                                                                                      |
| [**\_ \_ \_ ID Proprietà associazione di sicurezza WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_property_id)       | Identifica le proprietà utilizzate per specificare le impostazioni di associazione di sicurezza.                                                                                              |
| [**\_ \_ modalità entropia della chiave di sicurezza WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_entropy_mode)             | Definisce il modo in cui la casualità deve essere aggiunta alla chiave emessa durante una negoziazione del token di sicurezza eseguita con sicurezza in modalità mista e messaggi.                     |
| [**\_tipo di \_ chiave di sicurezza WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_type)                              | Tipo di chiave di un token di sicurezza.                                                                                                                                 |
| [**\_modalità di \_ riferimento del token di sicurezza WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_token_reference_mode)     | meccanismo da utilizzare per fare riferimento a un token di sicurezza da firme, elementi crittografati e token derivati nel contesto di associazioni di sicurezza in modalità mista e messaggi. |
| [**versione di WS \_ trust \_**](/windows/desktop/api/WebServices/ne-webservices-ws_trust_version)                                       | Definisce la versione della specifica WS-Trust da utilizzare con la sicurezza del messaggio e la sicurezza in modalità mista.                                                              |
| [**\_pacchetto di \_ \_ autenticazione integrata WS Windows \_**](/windows/desktop/api/WebServices/ne-webservices-ws_windows_integrated_auth_package) | Definisce il pacchetto SSP specifico da usare per l'autenticazione integrata di Windows.                                                                                |



 



| Struttura                                                               | Descrizione                                    |
|-------------------------------------------------------------------------|------------------------------------------------|
| [**\_proprietà di \_ associazione di sicurezza WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property) | Specifica un'impostazione specifica dell'associazione di sicurezza. |



 

 

 




