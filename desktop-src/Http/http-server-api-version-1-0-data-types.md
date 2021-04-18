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
# <a name="http-server-api-version-10-data-types"></a><span data-ttu-id="f48d4-107">Tipi di dati dell'API server HTTP versione 1,0</span><span class="sxs-lookup"><span data-stu-id="f48d4-107">HTTP Server API Version 1.0 Data Types</span></span>

<span data-ttu-id="f48d4-108">L'API del server HTTP usa diversi tipi di identificatore per scopi specifici dichiarati nel file di intestazione HTTP. h come interi senza segno a 64 bit (**ULONGLONGs**):</span><span class="sxs-lookup"><span data-stu-id="f48d4-108">The HTTP Server API uses various special purpose identifier types declared in the Http.h header file as 64-bit unsigned integers (**ULONGLONGs**):</span></span>

-   <span data-ttu-id="f48d4-109">\_ID connessione \_ http</span><span class="sxs-lookup"><span data-stu-id="f48d4-109">HTTP\_CONNECTION\_ID</span></span>
-   <span data-ttu-id="f48d4-110">\_ \_ ID connessione RAW \_ http</span><span class="sxs-lookup"><span data-stu-id="f48d4-110">HTTP\_RAW\_CONNECTION\_ID</span></span>
-   <span data-ttu-id="f48d4-111">\_ID richiesta \_ http</span><span class="sxs-lookup"><span data-stu-id="f48d4-111">HTTP\_REQUEST\_ID</span></span>
-   <span data-ttu-id="f48d4-112">\_contesto URL \_ http</span><span class="sxs-lookup"><span data-stu-id="f48d4-112">HTTP\_URL\_CONTEXT</span></span>

<span data-ttu-id="f48d4-113">Un'applicazione non deve tentare di generare o modificare un identificatore che appartiene a uno di questi tipi.</span><span class="sxs-lookup"><span data-stu-id="f48d4-113">An application should not attempt to generate or modify any identifier that belongs to one of these types.</span></span>

 

 




