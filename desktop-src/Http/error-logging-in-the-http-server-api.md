---
title: Registrazione degli errori in HTTP Server API
description: Alcuni tipi di errori vengono gestiti dall'API del server HTTP anziché essere passati a un'applicazione per la gestione, perché la frequenza di tali errori potrebbe altrimenti inondare un registro eventi o un gestore dell'applicazione.
ms.assetid: b919a718-e20b-4f34-a02e-bc028f8c32c7
keywords:
- API server HTTP, registrazione degli errori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c92c071929b61020b456d8ecabc81ebc0f05503c2f385b235afc323cf8dea33
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130681"
---
# <a name="error-logging-in-the-http-server-api"></a>Registrazione degli errori in HTTP Server API

Alcuni tipi di errori vengono gestiti dall'API del server HTTP anziché essere passati a un'applicazione per la gestione, perché la frequenza di tali errori potrebbe altrimenti inondare un registro eventi o un gestore dell'applicazione.

I tre argomenti seguenti descrivono i diversi aspetti della registrazione degli errori dell'API server HTTP:

-   [Configurazione](configuring-http-server-api-error-logging.md) Le impostazioni del Registro di sistema controllano se l'API server HTTP registra gli errori, le dimensioni massime consentite dei file di log e la posizione in cui vengono salvati i file di log.
-   [Formato del file di log](format-of-the-http-server-api-error-logs.md) L'API server HTTP crea file di log conformi alle convenzioni del file di log World Wide Web Consortium (W3C) e può essere analizzato tramite strumenti standard. A differenza dei file di log W3C, tuttavia, i file di log dell'API del server HTTP non contengono nomi delle colonne.
-   [Tipi di errori registrati](types-of-errors-logged-by-the-http-server-api.md) L'API del server HTTP registra un'ampia gamma di errori comuni.

 

 




