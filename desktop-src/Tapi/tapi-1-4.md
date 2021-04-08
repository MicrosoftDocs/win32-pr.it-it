---
description: TAPI 1,4 ha aggiunto una serie di API, messaggi, costanti ed elementi della struttura alla specifica 1,3.
ms.assetid: 293f732f-0288-46d1-b542-d948c6179158
title: TAPI 1,4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c32f4320043ada2e2ae5477a698bde63f28d2f25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967461"
---
# <a name="tapi-14"></a><span data-ttu-id="d72dd-103">TAPI 1,4</span><span class="sxs-lookup"><span data-stu-id="d72dd-103">TAPI 1.4</span></span>

<span data-ttu-id="d72dd-104">TAPI 1,4 ha aggiunto una serie di API, messaggi, costanti ed elementi della struttura alla specifica 1,3.</span><span class="sxs-lookup"><span data-stu-id="d72dd-104">TAPI 1.4 added a number of APIs, messages, constants, and structure elements to the 1.3 specification.</span></span> <span data-ttu-id="d72dd-105">TAPI 1,4 supporta solo TSPs a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="d72dd-105">TAPI 1.4 supports only 16-bit TSPs.</span></span> <span data-ttu-id="d72dd-106">Tuttavia, consente di sviluppare applicazioni a 32 bit senza doversi preoccupare delle limitazioni di Windows a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="d72dd-106">However, it does allow 32-bit applications to be developed without having to worry about the limitations of 16-bit Windows.</span></span>

<span data-ttu-id="d72dd-107">I file di intestazione TAPI e TSPI vengono usati per sviluppare entrambe le applicazioni sia per TAPI 1,4 che per TAPI 2. x.</span><span class="sxs-lookup"><span data-stu-id="d72dd-107">The TAPI and TSPI header files are used to develop both applications for both TAPI 1.4 and TAPI 2.x.</span></span> <span data-ttu-id="d72dd-108">Sebbene non siano state apportate numerose modifiche alle strutture tra queste due specifiche, sono state apportate modifiche all'API, in particolare al supporto Unicode, che rendono molto importante notare che le intestazioni vengono compilate in modo diverso, a seconda della \_ costante della versione corrente di TAPI \_ .</span><span class="sxs-lookup"><span data-stu-id="d72dd-108">While there were not many changes to the structures between these two specifications, there were changes to the API (specifically, Unicode support) that make it very important to note that the headers compile differently, depending on the TAPI\_CURRENT\_VERSION constant.</span></span> <span data-ttu-id="d72dd-109">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="d72dd-109">For example:</span></span>

``` syntax
#define TAPI_CURRENT_VERSION 0x00010004
#include <tapi.h>
```

> [!Note]  
> <span data-ttu-id="d72dd-110">\_ \_ Per tutte le applicazioni TAPI è necessario definire la versione corrente di TAPI.</span><span class="sxs-lookup"><span data-stu-id="d72dd-110">TAPI\_CURRENT\_VERSION should be defined for all TAPI applications.</span></span> <span data-ttu-id="d72dd-111">Sebbene non sia strettamente necessario per lo sviluppo di TAPI 2. x, potrebbero verificarsi modifiche future per richiederlo.</span><span class="sxs-lookup"><span data-stu-id="d72dd-111">While it is not strictly necessary for TAPI 2.x development, future changes could occur to require this.</span></span>

 

 

 



