---
description: A partire da provider di servizi di telefonia Windows 2000 che negoziano una versione di 3,0 o successiva deve avere un provider di servizi multimediali corrispondente.
ms.assetid: 9235c631-77bc-42c6-8139-9208c9c254b4
title: Comunicazione del provider di servizi multimediali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a50ec6a4fb96a86ceab3a302b138ee72d6c61b9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351476"
---
# <a name="media-service-provider-communication"></a><span data-ttu-id="04cca-103">Comunicazione del provider di servizi multimediali</span><span class="sxs-lookup"><span data-stu-id="04cca-103">Media Service Provider Communication</span></span>

<span data-ttu-id="04cca-104">A partire da provider di servizi di telefonia Windows 2000 che negoziano una versione di 3,0 o successiva deve avere un provider di servizi multimediali corrispondente.</span><span class="sxs-lookup"><span data-stu-id="04cca-104">Starting with Windows 2000 telephony service providers that negotiate a version of 3.0 or later must have a matching media service provider.</span></span> <span data-ttu-id="04cca-105">La divisione precisa delle responsabilità operative è dipendente dall'implementazione.</span><span class="sxs-lookup"><span data-stu-id="04cca-105">The precise division of operational responsibilities is implementation dependent.</span></span> <span data-ttu-id="04cca-106">Un TSP potrebbe, ad esempio, utilizzare l'MSP corrispondente per eseguire la determinazione del tipo di supporto in una sessione in ingresso.</span><span class="sxs-lookup"><span data-stu-id="04cca-106">For example, a TSP might use the matching MSP to perform media type determination on an incoming session.</span></span> <span data-ttu-id="04cca-107">Tuttavia, il TSP deve essere conforme al TSPI, il che significa ottenere tale determinazione dal MSP e segnalarlo a TAPI.</span><span class="sxs-lookup"><span data-stu-id="04cca-107">However, the TSP must conform to the TSPI, which means getting that determination from the MSP and reporting it to TAPI.</span></span>

<span data-ttu-id="04cca-108">TSPI fornisce le funzioni e i messaggi seguenti per consentire una connessione virtuale tra un TSP e un MSP:</span><span class="sxs-lookup"><span data-stu-id="04cca-108">TSPI provides the following functions and messages to allow a virtual connection between a TSP and an MSP:</span></span>

-   [<span data-ttu-id="04cca-109">**\_LINECLOSEMSPINSTANCE TSPI**</span><span class="sxs-lookup"><span data-stu-id="04cca-109">**TSPI\_lineCloseMSPInstance**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineclosemspinstance)
-   [<span data-ttu-id="04cca-110">**\_LINECREATEMSPINSTANCE TSPI**</span><span class="sxs-lookup"><span data-stu-id="04cca-110">**TSPI\_lineCreateMSPInstance**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance)
-   [<span data-ttu-id="04cca-111">**\_LINEMSPIDENTIFY TSPI**</span><span class="sxs-lookup"><span data-stu-id="04cca-111">**TSPI\_lineMSPIdentify**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linemspidentify)
-   [<span data-ttu-id="04cca-112">**\_LINERECEIVEMSPDATA TSPI**</span><span class="sxs-lookup"><span data-stu-id="04cca-112">**TSPI\_lineReceiveMSPData**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata)
-   [<span data-ttu-id="04cca-113">**LINEA \_ QOSINFO**</span><span class="sxs-lookup"><span data-stu-id="04cca-113">**LINE\_QOSINFO**</span></span>](line-qosinfo.md)
-   [<span data-ttu-id="04cca-114">**LINEA \_ SENDMSPDATA**</span><span class="sxs-lookup"><span data-stu-id="04cca-114">**LINE\_SENDMSPDATA**</span></span>](line-sendmspdata.md)

 

 
