---
title: Tipi di dati dell'API server HTTP versione 2,0
description: Tipi di dati dell'API server HTTP versione 2,0
ms.assetid: 13a0cac9-9e75-4350-a523-5ad9a57caad7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 670099f3303682f52fdc78397dc7f229577b94d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298629"
---
# <a name="http-server-api-version-20-data-types"></a>Tipi di dati dell'API server HTTP versione 2,0

L'API server HTTP usa diversi tipi di identificatori per scopi specifici dichiarati nell'intestazione HTTP. h, come indicato di seguito:

-   **Ushort** \_ \_ parametro timeout configurazione servizio http \_ \_ , \* \_ \_ \_ parametro timeout configurazione servizio \_ PHTTP
-   **ULONGLONG** \_ID opaco http \_ , \* \_ ID opaco \_ PHTTP
-   **Http \_ ID richiesta HTTP \_ ID opaco** \_ \_ , \* \_ ID richiesta \_ PHTTP
-   **Http \_ ID connessione HTTP \_ ID opaco** \_ \_ , \* \_ ID connessione \_ PHTTP
-   **Http \_ ID \_** di connessione non elaborata http ID opaco \_ \_ \_ , \* \_ \_ ID connessione non elaborata PHTTP \_
-   **Ushort** \_ \_ parametro timeout configurazione servizio http \_ \_ , \* \_ \_ \_ parametro timeout configurazione servizio \_ PHTTP

Un'applicazione non deve tentare di generare o modificare un identificatore che appartiene a uno di questi tipi.

 

 




