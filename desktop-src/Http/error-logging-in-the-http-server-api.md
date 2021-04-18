---
title: Registrazione degli errori in HTTP Server API
description: Alcuni tipi di errori vengono gestiti dall'API del server HTTP anziché essere passati di nuovo a un'applicazione per la gestione, perché la frequenza di tali errori potrebbe altrimenti comportare un registro eventi o un gestore dell'applicazione.
ms.assetid: b919a718-e20b-4f34-a02e-bc028f8c32c7
keywords:
- API del server HTTP, registrazione degli errori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d988d87a65c914625623c3f55d33a7f8cc9a4f94
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297897"
---
# <a name="error-logging-in-the-http-server-api"></a>Registrazione degli errori in HTTP Server API

Alcuni tipi di errori vengono gestiti dall'API del server HTTP anziché essere passati di nuovo a un'applicazione per la gestione, perché la frequenza di tali errori potrebbe altrimenti comportare un registro eventi o un gestore dell'applicazione.

I tre argomenti seguenti descrivono i diversi aspetti della registrazione degli errori dell'API del server HTTP:

-   [Configurazione](configuring-http-server-api-error-logging.md) di Le impostazioni del registro di sistema controllano se l'API del server HTTP registra gli errori, le dimensioni massime consentite dei file di log e i file di log salvati.
-   [Formato del file di log](format-of-the-http-server-api-error-logs.md) L'API server HTTP crea file di log conformi alle convenzioni dei file di log di World Wide Web Consortium (W3C) e può essere analizzato utilizzando gli strumenti standard. Tuttavia, a differenza dei file di log W3C, i file di log dell'API del server HTTP non contengono i nomi delle colonne.
-   [Tipi di errori registrati](types-of-errors-logged-by-the-http-server-api.md) L'API server HTTP registra una serie di errori comuni.

 

 




