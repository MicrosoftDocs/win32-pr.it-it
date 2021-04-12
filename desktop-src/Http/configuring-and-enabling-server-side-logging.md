---
title: Configurazione e abilitazione della registrazione lato server
description: Configurazione e abilitazione della registrazione lato server
ms.assetid: d67d8f9a-6d8a-43f2-a1ef-75f69c04b1ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61e56247ee306d5a8804663e00162224df1d3f3e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395935"
---
# <a name="configuring-and-enabling-server-side-logging"></a>Configurazione e abilitazione della registrazione lato server

L'applicazione consente di registrare la sessione del server o il gruppo di URL prima di inviare la risposta con [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse). Nell'esempio seguente viene illustrato come configurare e abilitare la registrazione lato server di tipo W3C:

1.  L'applicazione Inizializza la struttura di [**\_ \_ informazioni di registrazione http**](/windows/desktop/api/Http/ns-http-http_logging_info) con **HttpLoggingTypeW3C** specificato nel membro del **formato** e una maschera di maschera delle costanti dei campi del [**\_ log \_ http**](http-log-field--constants.md) nel membro **Fields** .
2.  L'applicazione chiama [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) o [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) con **HttpServerLoggingProperty** specificato nel parametro *Property* e un puntatore alla struttura di [**\_ \_ informazioni di registrazione http**](/windows/desktop/api/Http/ns-http-http_logging_info) nel parametro *pPropertyInformation* .

La maschera di maschera delle costanti dei [**\_ \_ campi di log http**](http-log-field--constants.md) contiene i campi che possono essere registrati nel file di log W3C. Si noti che l'impostazione della proprietà **HttpServerLoggingProperty** in una sessione del server o un gruppo di URL non significa che le risposte http verranno registrate. La registrazione viene eseguita in base alle singole richieste quando W3C è abilitato nella chiamata a [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) o [**HttpSendResponseEntityBody**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody).

Per abilitare la registrazione delle risposte W3C per ogni richiesta, l'applicazione esegue i passaggi seguenti:

1.  L'applicazione Inizializza i membri dei [**dati dei \_ \_ campi del \_ log http**](/windows/desktop/api/Http/ns-http-http_log_fields_data) con le informazioni sul campo che verranno registrate per la risposta.
2.  Il membro **base. Type** della struttura [**dei \_ \_ \_ dati dei campi del log http**](/windows/desktop/api/Http/ns-http-http_log_fields_data) deve essere inizializzato su **HttpLogDataTypeFields**. Il campo **base. Type** garantisce l'estendibilità futura della struttura e dell'API.
3.  L'applicazione chiama [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) o [**HttpSendResponseEntityBody**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody) con un puntatore alla struttura [**\_ \_ \_ dei dati dei campi di log http**](/windows/desktop/api/Http/ns-http-http_log_fields_data) nel parametro *pLogData* . Il tipo di applicazione deve eseguire il cast del puntatore ai [**\_ \_ dati di log PHTTP**](/windows/desktop/api/Http/ns-http-http_log_data).

 

 




