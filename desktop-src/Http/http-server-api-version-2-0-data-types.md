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
# <a name="http-server-api-version-20-data-types"></a><span data-ttu-id="805b4-103">Tipi di dati dell'API server HTTP versione 2,0</span><span class="sxs-lookup"><span data-stu-id="805b4-103">HTTP Server API Version 2.0 Data Types</span></span>

<span data-ttu-id="805b4-104">L'API server HTTP usa diversi tipi di identificatori per scopi specifici dichiarati nell'intestazione HTTP. h, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="805b4-104">The HTTP Server API uses various special purpose identifier types declared in the Http.h header as follows:</span></span>

-   <span data-ttu-id="805b4-105">**Ushort** \_ \_ parametro timeout configurazione servizio http \_ \_ , \* \_ \_ \_ parametro timeout configurazione servizio \_ PHTTP</span><span class="sxs-lookup"><span data-stu-id="805b4-105">**USHORT** HTTP\_SERVICE\_CONFIG\_TIMEOUT\_PARAM, \*PHTTP\_SERVICE\_CONFIG\_TIMEOUT\_PARAM</span></span>
-   <span data-ttu-id="805b4-106">**ULONGLONG** \_ID opaco http \_ , \* \_ ID opaco \_ PHTTP</span><span class="sxs-lookup"><span data-stu-id="805b4-106">**ULONGLONG** HTTP\_OPAQUE\_ID, \*PHTTP\_OPAQUE\_ID</span></span>
-   <span data-ttu-id="805b4-107">**Http \_ ID richiesta HTTP \_ ID opaco** \_ \_ , \* \_ ID richiesta \_ PHTTP</span><span class="sxs-lookup"><span data-stu-id="805b4-107">**HTTP\_OPAQUE\_ID** HTTP\_REQUEST\_ID, \*PHTTP\_REQUEST\_ID</span></span>
-   <span data-ttu-id="805b4-108">**Http \_ ID connessione HTTP \_ ID opaco** \_ \_ , \* \_ ID connessione \_ PHTTP</span><span class="sxs-lookup"><span data-stu-id="805b4-108">**HTTP\_OPAQUE\_ID** HTTP\_CONNECTION\_ID, \*PHTTP\_CONNECTION\_ID</span></span>
-   <span data-ttu-id="805b4-109">**Http \_ ID \_** di connessione non elaborata http ID opaco \_ \_ \_ , \* \_ \_ ID connessione non elaborata PHTTP \_</span><span class="sxs-lookup"><span data-stu-id="805b4-109">**HTTP\_OPAQUE\_ID** HTTP\_RAW\_CONNECTION\_ID, \*PHTTP\_RAW\_CONNECTION\_ID</span></span>
-   <span data-ttu-id="805b4-110">**Ushort** \_ \_ parametro timeout configurazione servizio http \_ \_ , \* \_ \_ \_ parametro timeout configurazione servizio \_ PHTTP</span><span class="sxs-lookup"><span data-stu-id="805b4-110">**USHORT** HTTP\_SERVICE\_CONFIG\_TIMEOUT\_PARAM, \*PHTTP\_SERVICE\_CONFIG\_TIMEOUT\_PARAM</span></span>

<span data-ttu-id="805b4-111">Un'applicazione non deve tentare di generare o modificare un identificatore che appartiene a uno di questi tipi.</span><span class="sxs-lookup"><span data-stu-id="805b4-111">An application should not attempt to generate or modify any identifier that belongs to one of these types.</span></span>

 

 




