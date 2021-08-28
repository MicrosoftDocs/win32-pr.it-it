---
title: Funzioni dell'API server HTTP versione 2.0
description: L'API server HTTP versione 2.0 fornisce le funzioni seguenti.
ms.assetid: 12daffca-b403-4f06-8037-206f90e33252
keywords:
- Funzioni dell'API server HTTP versione 2.0
- Funzioni HTTP, API server HTTP versione 2.0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b832a3f8fb1a97c48c49809d3e2f1975965becdc4c7bbf3942601d577d4702d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119981361"
---
# <a name="http-server-api-version-20-functions"></a>Funzioni dell'API server HTTP versione 2.0

L'API server HTTP versione 2.0 fornisce le funzioni seguenti.

| Funzione | Descrizione |
|-|-|
| [**HttpDelegateRequestEx**](/windows/win32/api/http/nf-http-httpdelegaterequestex) | Delega una richiesta dalla coda di richieste di origine alla coda di richieste di destinazione. |
| [**HttpFindUrlGroupId**](/windows/win32/api/http/nf-http-httpfindurlgroupid) | Recupera un ID gruppo DI URL per un URL e una coda di richieste. |
| [**HttpIsFeatureSupported**](/windows/win32/api/http/nf-http-httpisfeaturesupported) | Controlla se una particolare funzionalità è supportata. |

## <a name="server-session"></a>Sessione del server

| Funzione | Descrizione |
|-|-|
| [**HttpCloseServerSession**](/windows/desktop/api/Http/nf-http-httpcloseserversession) | |
| [**HttpCreateServerSession**](/windows/desktop/api/Http/nf-http-httpcreateserversession) | |
| [**HttpQueryServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty) | |
| [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) | |

## <a name="url-groups"></a>Gruppi di URL

| Funzione | Descrizione |
|-|-|
| [**HttpAddUrlToUrlGroup**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup) | |
| [**HttpCreateUrlGroup**](/windows/desktop/api/Http/nf-http-httpcreateurlgroup) | |
| [**HttpCloseUrlGroup**](/windows/desktop/api/Http/nf-http-httpcloseurlgroup) | |
| [**Proprietà HttpQueryUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty) | |
| [**HttpRemoveUrlFromUrlGroup**](/windows/desktop/api/Http/nf-http-httpremoveurlfromurlgroup) | |
| [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) | |

## <a name="request-queue"></a>Coda richiesta

| Funzione | Descrizione |
|-|-|
| [**HttpCloseRequestQueue**](/windows/desktop/api/Http/nf-http-httpcloserequestqueue) | |
| [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) | |
| [**HttpQueryRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpqueryrequestqueueproperty) | |
| [**HttpSetRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) | |
| [**HttpShutdownRequestQueue**](/windows/desktop/api/Http/nf-http-httpshutdownrequestqueue) | |
| [**HttpWaitForDemandStart**](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) | |

## <a name="related-topics"></a>Argomenti correlati

[Strutture dell'API server HTTP versione 2.0](http-server-api-version-2-0-structures.md)
