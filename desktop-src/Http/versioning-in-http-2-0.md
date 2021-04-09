---
title: Controllo delle versioni (API server HTTP)
description: L'API server HTTP versione 2,0 applica il controllo delle versioni con ambito oggetto per determinare la versione dell'API.
ms.assetid: 2c2d7501-85e0-44ec-aa42-01372b29266e
keywords:
- Controllo delle versioni in HTTP Server versione 2,0 API
- Server HTTP versione 2,0 API, controllo delle versioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5221ff7a93bb24e7e0b8a1b9f7c2399012cdbe95
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104118790"
---
# <a name="versioning-http-server-api"></a>Controllo delle versioni (API server HTTP)

L'API server HTTP versione 2,0 rende obsolete le code di richieste e le associazioni URL della versione 1,0 con la coda delle richieste. Il controllo delle versioni con ambito di oggetto consente alle applicazioni di fornire informazioni sulla versione specifiche dell'applicazione. Le applicazioni possono chiamare automaticamente la versione corretta delle strutture per il sistema operativo in cui è in esecuzione.

## <a name="request-queues"></a>Code di richieste

A partire dall'API server HTTP versione 2,0, le code di richiesta vengono create con [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) rendendo obsoleta la funzione [**HttpCreateHttpHandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle) della versione 1,0. I gruppi di URL sono introdotti nella versione 2,0 con la funzione [**HttpCreateUrlGroup**](/windows/desktop/api/Http/nf-http-httpcreateurlgroup) . Gli URL vengono aggiunti al gruppo usando [**HttpAddUrlToUrlGroup**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup) , che rende obsoleta la funzione [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl) della versione 1,0. I gruppi di URL versione 2,0 non devono essere usati con le code di richieste della versione 1,0.

A partire dalla versione 2,0, le funzioni di versione 1,0 seguenti sono obsolete e non possono essere usate con le code di richieste della versione 2,0:

-   [**HttpCreateHttpHandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle)
-   [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl)
-   [**HttpRemoveUrl**](/windows/desktop/api/Http/nf-http-httpremoveurl)

Per ulteriori informazioni sulla configurazione dei gruppi di URL, vedere l'argomento [configurazione del gruppo di URL](configuring-the-url-group.md) . Per ulteriori informazioni sulle code di richieste della versione 2,0, vedere l'argomento relativo alla [coda di richieste denominata](named-request-queue.md) .

## <a name="object-scoped-versioning"></a>Controllo delle versioni di Object-Scoped

Nella versione 1,0, l'applicazione fornisce la versione dell'API del server HTTP nella chiamata a [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize). Le informazioni sulla versione vengono accettate solo dalla prima applicazione che ha chiamato **HttpInitialize** e viene applicata a tutte le applicazioni API del server http nello stesso processo. A partire dall'API versione 2,0, le informazioni sulla versione globale fornite nella chiamata a **HttpInitialize** non vengono usate. Per le applicazioni della versione 2,0, la versione dell'API del server HTTP viene passata nel parametro della versione quando la coda di richieste o la sessione del server viene creata da [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) o [**HttpCreateServerSession**](/windows/desktop/api/Http/nf-http-httpcreateserversession). Quando la coda di richieste viene creata con la versione 1,0 [**HttpCreateHttpHandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle), viene contrassegnata automaticamente come versione 1,0. Entrambe le applicazioni versione 1,0 e versione 2,0 possono essere eseguite nello stesso processo.

La [**\_ richiesta http**](/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)) e le strutture di [**\_ risposta http**](http-response.md) vengono aggiornate per includere le informazioni di autenticazione nell'API server http versione 2,0. [**Http \_ La richiesta \_ V1**](/windows/desktop/api/Http/ns-http-http_request_v1) e la [**\_ richiesta HTTP \_ v2**](/windows/desktop/api/Http/ns-http-http_request_v2) sono specifiche per la versione dell'API usata dall'applicazione. Tuttavia, le applicazioni non devono utilizzare queste strutture direttamente nel codice. usare invece la **\_ richiesta http** per ottenere la versione corretta in base alla versione della coda di richieste in cui è stata ricevuta la richiesta. Tenere inoltre presente che le dimensioni della struttura **di \_ richiesta http** sono basate sulla versione del sistema operativo in cui viene compilato il codice.

 

 
