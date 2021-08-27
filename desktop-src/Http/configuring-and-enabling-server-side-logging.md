---
title: Configurazione e abilitazione della registrazione lato server
description: Configurazione e abilitazione della registrazione lato server
ms.assetid: d67d8f9a-6d8a-43f2-a1ef-75f69c04b1ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c95856cf72379de44211f05bb78fb4c6839f77b2fd6c42b91b26068bc9c5d0d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050811"
---
# <a name="configuring-and-enabling-server-side-logging"></a>Configurazione e abilitazione della registrazione lato server

L'applicazione abilita la registrazione nella sessione del server o nel gruppo di URL prima di inviare la risposta [**con HttpSendHttpResponse.**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) Nell'esempio seguente viene illustrato come configurare e abilitare la registrazione lato server di tipo W3C:

1.  L'applicazione inizializza la struttura [**HTTP \_ LOGGING \_ INFO**](/windows/desktop/api/Http/ns-http-http_logging_info) con **HttpLoggingTypeW3C** specificato nel membro **Format** e una maschera di bit delle costanti HTTP [**LOG \_ \_ FIELD**](http-log-field--constants.md) nel membro **Fields.**
2.  L'applicazione chiama [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) o [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) con **HttpServerLoggingProperty** specificato nel parametro *Property* e un puntatore alla struttura [**HTTP LOGGING \_ \_ INFO**](/windows/desktop/api/Http/ns-http-http_logging_info) nel *parametro pPropertyInformation.*

La maschera di bit delle [**costanti HTTP \_ LOG \_ FIELD**](http-log-field--constants.md) contiene i campi che possono essere registrati nel file di log W3C. Si noti che **l'impostazione della proprietà HttpServerLoggingProperty** in una sessione del server o in un gruppo di URL non significa che le risposte HTTP verranno registrate. La registrazione viene eseguita per ogni richiesta quando W3C è abilitato nella chiamata a [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) o [**HttpSendResponseEntityBody.**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody)

Per abilitare la registrazione delle risposte W3C per ogni richiesta, l'applicazione esegue i passaggi seguenti:

1.  L'applicazione inizializza i membri di [**HTTP \_ LOG FIELDS \_ \_ DATA**](/windows/desktop/api/Http/ns-http-http_log_fields_data) con le informazioni sul campo che verranno registrate per la risposta.
2.  Il **membro Base.Type** della struttura [**HTTP LOG FIELDS \_ \_ \_ DATA**](/windows/desktop/api/Http/ns-http-http_log_fields_data) deve essere inizializzato su **HttpLogDataTypeFields.** Il **campo Base.Type** garantisce l'estendibilità futura della struttura e dell'API.
3.  L'applicazione [**chiama HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) o [**HttpSendResponseEntityBody**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody) con un puntatore alla struttura [**HTTP LOG FIELDS \_ \_ \_ DATA**](/windows/desktop/api/Http/ns-http-http_log_fields_data) nel *parametro pLogData.* L'applicazione deve eseguire il cast del puntatore a [**PHTTP \_ LOG \_ DATA**](/windows/desktop/api/Http/ns-http-http_log_data).

 

 




