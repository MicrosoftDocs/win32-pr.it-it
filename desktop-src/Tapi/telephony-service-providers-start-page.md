---
description: Un provider di servizi di telefonia (TSP) è una libreria di collegamento dinamico (DLL) che supporta il controllo dei dispositivi di comunicazione tramite un set di funzioni del servizio esportate.
ms.assetid: 276c27ac-b6ee-42a7-8327-33dfd87e69bd
title: Provider di servizi di telefonia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40c3c8887723cc74a1bf0d77bcdcfd06c8468a4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884789"
---
# <a name="telephony-service-providers"></a><span data-ttu-id="46c67-103">Provider di servizi di telefonia</span><span class="sxs-lookup"><span data-stu-id="46c67-103">Telephony Service Providers</span></span>

## <a name="purpose"></a><span data-ttu-id="46c67-104">Scopo</span><span class="sxs-lookup"><span data-stu-id="46c67-104">Purpose</span></span>

<span data-ttu-id="46c67-105">Un provider di servizi di telefonia (TSP) è una libreria di collegamento dinamico (DLL) che supporta il controllo dei dispositivi di comunicazione tramite un set di funzioni del servizio esportate.</span><span class="sxs-lookup"><span data-stu-id="46c67-105">A telephony service provider (TSP) is a dynamic-link library (DLL) that supports communications device control through a set of exported service functions.</span></span> <span data-ttu-id="46c67-106">Un'applicazione TAPI utilizza comandi standardizzati, TAPI passa informazioni al provider del servizio di telefonia e il TSP gestisce i comandi specifici che devono essere scambiati con il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="46c67-106">A TAPI application uses standardized commands, TAPI passes information to the telephony service provider, and the TSP handles the specific commands that must be exchanged with the device.</span></span>

<span data-ttu-id="46c67-107">Un TSP deve essere conforme all'interfaccia del provider di servizi di telefonia (TSPI) per fungere da provider di servizi nell'ambiente di telefonia Microsoft.</span><span class="sxs-lookup"><span data-stu-id="46c67-107">A TSP must conform to the Telephony Service Provider Interface (TSPI) to function as a service provider within the Microsoft Telephony environment.</span></span> <span data-ttu-id="46c67-108">TSPI definisce le funzioni esterne esposte da un provider di servizi di telefonia fornito con apparecchiature per le comunicazioni.</span><span class="sxs-lookup"><span data-stu-id="46c67-108">TSPI defines the external functions exposed by a telephony service provider supplied with communications equipment.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="46c67-109">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="46c67-109">Developer audience</span></span>

<span data-ttu-id="46c67-110">È possibile scrivere applicazioni abilitate per TAPI in molti linguaggi, tra cui Java, Visual Basic e C/C++.</span><span class="sxs-lookup"><span data-stu-id="46c67-110">You can write TAPI-enabled applications in many languages, including Java, Visual Basic, and C/C++.</span></span> <span data-ttu-id="46c67-111">L'esperienza di sviluppo precedente con le telecomunicazioni o altre applicazioni di telefonia è utile ma non necessaria.</span><span class="sxs-lookup"><span data-stu-id="46c67-111">Previous development experience with telecommunications or other telephony applications is helpful but not necessary.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="46c67-112">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="46c67-112">Run-time requirements</span></span>

<span data-ttu-id="46c67-113">TSPI consente lo sviluppo di TSPs per tutte le versioni di Windows.</span><span class="sxs-lookup"><span data-stu-id="46c67-113">TSPI enables development of TSPs for all versions of Windows.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="46c67-114">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="46c67-114">In this section</span></span>



| <span data-ttu-id="46c67-115">Argomento</span><span class="sxs-lookup"><span data-stu-id="46c67-115">Topic</span></span>                                                                | <span data-ttu-id="46c67-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="46c67-116">Description</span></span>                                                              |
|----------------------------------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="46c67-117">Overview</span><span class="sxs-lookup"><span data-stu-id="46c67-117">Overview</span></span>](about-the-telephony-service-provider-tsp-.md)<br/> | <span data-ttu-id="46c67-118">Informazioni generali sull'architettura e i componenti di TSPI.</span><span class="sxs-lookup"><span data-stu-id="46c67-118">General information about TSPI's architecture and components.</span></span><br/> |
| [<span data-ttu-id="46c67-119">Riferimento</span><span class="sxs-lookup"><span data-stu-id="46c67-119">Reference</span></span>](tspi-reference.md)<br/>                           | <span data-ttu-id="46c67-120">Documentazione per le interfacce TSPI.</span><span class="sxs-lookup"><span data-stu-id="46c67-120">Documentation for the TSPI interfaces.</span></span><br/>                        |



 

## <a name="related-topics"></a><span data-ttu-id="46c67-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="46c67-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46c67-122">Panoramica della telefonia Microsoft</span><span class="sxs-lookup"><span data-stu-id="46c67-122">Microsoft Telephony Overview</span></span>](./microsoft-telephony-overview.md)
</dt> <dt>

[<span data-ttu-id="46c67-123">Provider di servizi multimediali</span><span class="sxs-lookup"><span data-stu-id="46c67-123">Media Service Providers</span></span>](./media-service-providers-start-page.md)
</dt> <dt>

[<span data-ttu-id="46c67-124">TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="46c67-124">TAPI 2.2</span></span>](./tapi-2-2-start-page.md)
</dt> <dt>

[<span data-ttu-id="46c67-125">TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="46c67-125">TAPI 3.1</span></span>](./tapi-3-1-start-page.md)
</dt> </dl>

 

