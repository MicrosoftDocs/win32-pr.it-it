---
title: Impostazioni del canale di sicurezza
description: Le impostazioni del canale di sicurezza controllano il modo in cui la sicurezza viene applicata e verificata su un canale.
ms.assetid: ad964874-0bc7-4f03-8ceb-33627ff99f08
keywords:
- Servizi Web per le impostazioni del canale di sicurezza per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6fcd0b42b2d5581a5b7c489e9ada70f32abfefa
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104118682"
---
# <a name="security-channel-settings"></a>Impostazioni del canale di sicurezza

Le impostazioni del canale di sicurezza controllano il modo in cui la sicurezza viene applicata e verificata su un canale. Ogni impostazione del canale di sicurezza è rappresentata da una raccolta di coppie proprietà-valore, con le chiavi di proprietà definite dall' [**\_ ID della \_ proprietà \_ di sicurezza WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)di enumerazione. Ogni proprietà della raccolta ha un valore predefinito ragionevole. A causa di questi valori predefiniti, è possibile definire e utilizzare una descrizione di sicurezza senza specificare alcuna impostazione del canale di sicurezza.


[Le impostazioni di associazione di sicurezza](security-binding-settings.md) contengono raccolte simili di coppie proprietà-valore le cui chiavi sono definite dalla struttura della proprietà di [**\_ \_ associazione \_ di sicurezza WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property) . La differenza tra questi due tipi di impostazioni è che le impostazioni del canale di sicurezza hanno come ambito una descrizione della sicurezza (ovvero contengono proprietà di sicurezza a livello di canale), mentre le impostazioni di associazione di sicurezza hanno come ambito una delle associazioni di sicurezza e potrebbero esserci numerose associazioni di sicurezza. Di conseguenza, ad esempio, una descrizione di sicurezza personalizzata che contiene tre associazioni di sicurezza avrà un elenco di impostazioni del canale di sicurezza per l'intero canale e tre contenitori delle impostazioni di associazione di sicurezza, uno per ogni associazione di sicurezza.

Con le impostazioni del canale di sicurezza vengono utilizzate le enumerazioni seguenti:

-   [**\_livello di protezione WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level)
-   [**\_ID della \_ proprietà del token di sicurezza WS Request \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_request_security_token_property_id)
-   [**\_ \_ ID algoritmo di sicurezza WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_algorithm_id)
-   [**\_ID della \_ proprietà dell'algoritmo di sicurezza WS \_ \_**](/windows/win32/api/webservices/ne-webservices-ws_move_to)
-   [**\_layout dell' \_ intestazione di sicurezza WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_header_layout)
-   [**\_versione dell' \_ intestazione di sicurezza WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_header_version)
-   [**\_ID della \_ proprietà di sicurezza WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)
-   [**\_ \_ utilizzo timestamp di sicurezza WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage)
-   [**\_ID della \_ proprietà del token di sicurezza WS XML \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_security_token_property_id)

Con le impostazioni del canale di sicurezza vengono utilizzate le strutture seguenti:

-   [**\_proprietà del \_ token di sicurezza WS Request \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_request_security_token_property)
-   [**\_ \_ Proprietà algoritmo di sicurezza WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_algorithm_property)
-   [**\_suite di \_ algoritmi di sicurezza WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_algorithm_suite)
-   [**\_proprietà di sicurezza WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_property)
-   [**\_proprietà del \_ token di sicurezza WS XML \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_security_token_property)

 

 




