---
title: Tipi di dati dell'API del server HTTP versione 1.0
description: L'API del server HTTP usa vari tipi di identificatore per scopi speciali dichiarati nel file di intestazione Http.h come interi senza segno a 64 bit.
ms.assetid: bec1d41e-0c80-49bc-84e1-b16c409cd0f3
keywords:
- HTTP_CONNECTION_ID tipo HTTP
- HTTP_RAW_CONNECTION_ID tipo HTTP
- HTTP_REQUEST_ID tipo HTTP
- HTTP_URL_CONTEXT tipo HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 151ef975470ca21c6e82e5bc7bd7bd8b99a70573385375e8552b6660ce78f631
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950800"
---
# <a name="http-server-api-version-10-data-types"></a>Tipi di dati dell'API del server HTTP versione 1.0

L'API del server HTTP usa vari tipi di identificatore per scopi speciali dichiarati nel file di intestazione Http.h come interi senza segno a 64 bit **(ULONGLONG):**

-   \_ID CONNESSIONE \_ HTTP
-   \_ID CONNESSIONE HTTP \_ RAW \_
-   \_ID RICHIESTA \_ HTTP
-   CONTESTO \_ URL \_ HTTP

Un'applicazione non deve tentare di generare o modificare alcun identificatore appartenente a uno di questi tipi.

 

 




