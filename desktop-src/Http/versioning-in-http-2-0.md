---
title: Controllo delle versioni (API server HTTP)
description: L'API http server versione 2.0 applica il controllo delle versioni con ambito di oggetto per determinare la versione dell'API.
ms.assetid: 2c2d7501-85e0-44ec-aa42-01372b29266e
keywords:
- Controllo delle versioni nell'API http server versione 2.0
- API http server versione 2.0, controllo delle versioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc7a84af7de439cdd13cc1e9ff66fff367370fa963882077904ad656b856511
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829691"
---
# <a name="versioning-http-server-api"></a>Controllo delle versioni (API server HTTP)

L'API server HTTP versione 2.0 rende obsolete le code di richiesta versione 1.0 e le associazioni URL con la coda di richiesta. Il controllo delle versioni con ambito di oggetto consente alle applicazioni di fornire informazioni sulla versione specifiche dell'applicazione. Un'applicazione può chiamare automaticamente la versione corretta delle strutture per il sistema operativo in cui è in esecuzione.

## <a name="request-queues"></a>Code di richieste

A partire dall'API http server versione 2.0, le code di richiesta vengono create con [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) rendendo obsoleta la funzione [**HttpCreateHttpHandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle) versione 1.0. I gruppi di URL sono stati introdotti nella versione 2.0 con la [**funzione HttpCreateUrlGroup.**](/windows/desktop/api/Http/nf-http-httpcreateurlgroup) Gli URL vengono aggiunti al gruppo usando [**HttpAddUrlToUrlGroup,**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup) che rende obsoleta la funzione [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl) versione 1.0. I gruppi di URL versione 2.0 non devono essere usati con le code di richiesta della versione 1.0.

A partire dalla versione 2.0, le funzioni della versione 1.0 seguenti sono obsolete e non possono essere usate con le code di richiesta della versione 2.0:

-   [**HttpCreateHttpHandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle)
-   [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl)
-   [**HttpRemoveUrl**](/windows/desktop/api/Http/nf-http-httpremoveurl)

Per altre informazioni sulla configurazione dei gruppi di URL, vedere [l'argomento Configurazione del gruppo di URL.](configuring-the-url-group.md) Per altre informazioni sulle code di richiesta della versione 2.0, vedere [l'argomento Coda di richieste](named-request-queue.md) denominate.

## <a name="object-scoped-versioning"></a>Object-Scoped controllo delle versioni

Nella versione 1.0 l'applicazione fornisce la versione dell'API server HTTP nella chiamata a [**HttpInitialize.**](/windows/desktop/api/Http/nf-http-httpinitialize) Le informazioni sulla versione vengono accettate solo dalla prima applicazione che ha chiamato **HttpInitialize** e vengono applicate a tutte le applicazioni API del server HTTP nello stesso processo. A partire dall'API versione 2.0, le informazioni sulla versione globale fornite nella chiamata a **HttpInitialize** non vengono usate. Per le applicazioni versione 2.0, la versione dell'API server HTTP viene passata nel parametro Version quando la coda di richieste o la sessione del server viene creata da [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) o [**HttpCreateServerSession**](/windows/desktop/api/Http/nf-http-httpcreateserversession). Quando la coda di richieste viene creata con la versione 1.0 [**HttpCreateHttpHandle,**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle)viene contrassegnata automaticamente come versione 1.0. Entrambe le applicazioni versione 1.0 e 2.0 possono essere eseguite nello stesso processo.

Le [**strutture \_ HTTP REQUEST**](/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)) e HTTP [**\_ RESPONSE**](http-response.md) vengono aggiornate per includere le informazioni di autenticazione nell'API del server HTTP versione 2.0. [**HTTP \_ REQUEST \_ V1**](/windows/desktop/api/Http/ns-http-http_request_v1) [**e HTTP REQUEST \_ \_ V2**](/windows/desktop/api/Http/ns-http-http_request_v2) sono specifici della versione dell'API usata dall'applicazione. Tuttavia, le applicazioni non devono usare queste strutture direttamente nel codice. devono invece usare **HTTP \_ REQUEST** per ottenere la versione corretta in base alla versione della coda di richieste in cui è stata ricevuta la richiesta. Tenere inoltre presente che le dimensioni della struttura **HTTP \_ REQUEST** si basano sulla versione del sistema operativo in cui viene compilato il codice.

 

 
