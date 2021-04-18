---
title: Tipi di dati dell'API server HTTP versione 1,0
description: L'API del server HTTP usa diversi tipi di identificatore per scopi specifici dichiarati nel file di intestazione HTTP. h come interi senza segno a 64 bit.
ms.assetid: bec1d41e-0c80-49bc-84e1-b16c409cd0f3
keywords:
- Tipo di HTTP_CONNECTION_ID HTTP
- Tipo di HTTP_RAW_CONNECTION_ID HTTP
- Tipo di HTTP_REQUEST_ID HTTP
- Tipo di HTTP_URL_CONTEXT HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 681e24c06334a9010287e2084d9d6a04428ca6a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298857"
---
# <a name="http-server-api-version-10-data-types"></a>Tipi di dati dell'API server HTTP versione 1,0

L'API del server HTTP usa diversi tipi di identificatore per scopi specifici dichiarati nel file di intestazione HTTP. h come interi senza segno a 64 bit (**ULONGLONGs**):

-   \_ID connessione \_ http
-   \_ \_ ID connessione RAW \_ http
-   \_ID richiesta \_ http
-   \_contesto URL \_ http

Un'applicazione non deve tentare di generare o modificare un identificatore che appartiene a uno di questi tipi.

 

 




