---
description: Un provider di servizi di telefonia TAPI (TSP) è una libreria di collegamento dinamico (DLL) che supporta il controllo dei dispositivi di comunicazione tramite un set di funzioni del servizio esportate.
ms.assetid: 6e4fb295-940e-4f76-ad43-fad7da90094a
title: Informazioni sul provider di servizi di telefonia (TSP)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5200a4291bdd91aba9f93a5552fecf4b52d24ee3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750791"
---
# <a name="about-the-telephony-service-provider-tsp"></a><span data-ttu-id="e7b3d-103">Informazioni sul provider di servizi di telefonia (TSP)</span><span class="sxs-lookup"><span data-stu-id="e7b3d-103">About the Telephony Service Provider (TSP)</span></span>

<span data-ttu-id="e7b3d-104">\[ H323 e IPConf TSPs non sono disponibili per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e7b3d-104">\[ The H323 and IPConf TSPs are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e7b3d-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="e7b3d-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="e7b3d-106">Un provider di servizi di telefonia TAPI (TSP) è una libreria di collegamento dinamico (DLL) che supporta il controllo dei dispositivi di comunicazione tramite un set di funzioni del servizio esportate.</span><span class="sxs-lookup"><span data-stu-id="e7b3d-106">A TAPI telephony service provider (TSP) is a dynamic-link library (DLL) that supports communications device control through a set of exported service functions.</span></span> <span data-ttu-id="e7b3d-107">Un'applicazione TAPI USA comandi standardizzati, TAPI passa alla formazione per il provider di servizi di telefonia e il TSP gestisce i comandi specifici che devono essere scambiati con il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e7b3d-107">A TAPI application uses standardized commands, TAPI passes in formation to the telephony service provider, and the TSP handles the specific commands that must be exchanged with the device.</span></span>

<span data-ttu-id="e7b3d-108">Le sezioni seguenti descrivono brevemente le TSPs fornite con Microsoft Windows:</span><span class="sxs-lookup"><span data-stu-id="e7b3d-108">The following sections briefly describe the TSPs provided with Microsoft Windows:</span></span>

-   [<span data-ttu-id="e7b3d-109">H323 TSP</span><span class="sxs-lookup"><span data-stu-id="e7b3d-109">H323 TSP</span></span>](h323-tsp.md)
-   [<span data-ttu-id="e7b3d-110">IPConf TSP</span><span class="sxs-lookup"><span data-stu-id="e7b3d-110">IPConf TSP</span></span>](ipconf-tsp.md)
-   [<span data-ttu-id="e7b3d-111">Driver di dispositivo in modalità kernel (TSP)</span><span class="sxs-lookup"><span data-stu-id="e7b3d-111">Kernel-Mode Device Driver TSP</span></span>](kernel-mode-device-driver-tsp.md)
-   [<span data-ttu-id="e7b3d-112">TSP proxy NDIS</span><span class="sxs-lookup"><span data-stu-id="e7b3d-112">NDIS Proxy TSP</span></span>](ndis-proxy-tsp.md)
-   [<span data-ttu-id="e7b3d-113">TSP remoto</span><span class="sxs-lookup"><span data-stu-id="e7b3d-113">Remote TSP</span></span>](remote-tsp.md)
-   [<span data-ttu-id="e7b3d-114">TSP di terze parti</span><span class="sxs-lookup"><span data-stu-id="e7b3d-114">Third-Party TSP</span></span>](third-party-tsp.md)
-   [<span data-ttu-id="e7b3d-115">TSP Unimodem</span><span class="sxs-lookup"><span data-stu-id="e7b3d-115">Unimodem TSP</span></span>](unimodem-tsp.md)

<span data-ttu-id="e7b3d-116">Per informazioni dettagliate, vedere il Resource Kit per il sistema operativo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e7b3d-116">For detailed information, please see the Resource Kit for the target operating system.</span></span> <span data-ttu-id="e7b3d-117">TSPs di terze parti per i dispositivi di comunicazione specializzati verranno in genere forniti dal produttore e verranno installati con il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e7b3d-117">Third-party TSPs for specialized communications devices will typically be provided by the manufacturer and will be installed with the device.</span></span>

<span data-ttu-id="e7b3d-118">Negli argomenti seguenti viene descritto come creare un TSP che funzionerà correttamente nell'ambiente di telefonia Microsoft e come creare una coppia TSP/MSP:</span><span class="sxs-lookup"><span data-stu-id="e7b3d-118">The following topics describe how to create a TSP that will function properly within the Microsoft Telephony environment, and how to create a TSP/MSP pair:</span></span>

-   [<span data-ttu-id="e7b3d-119">Interfaccia del provider di servizi di telefonia (TSPI)</span><span class="sxs-lookup"><span data-stu-id="e7b3d-119">Telephony Service Provider Interface (TSPI)</span></span>](telephony-service-provider-interface-tspi-.md)
-   [<span data-ttu-id="e7b3d-120">Riferimento a TSPI</span><span class="sxs-lookup"><span data-stu-id="e7b3d-120">TSPI Reference</span></span>](tspi-reference.md)
-   [<span data-ttu-id="e7b3d-121">Provider di servizi multimediali</span><span class="sxs-lookup"><span data-stu-id="e7b3d-121">Media Service Providers</span></span>](./media-service-providers-start-page.md)

> [!Note]  
> <span data-ttu-id="e7b3d-122">Un TSP è una DLL creata dall'utente.</span><span class="sxs-lookup"><span data-stu-id="e7b3d-122">A TSP is a user-created DLL.</span></span> <span data-ttu-id="e7b3d-123">Se si sta creando un TSP per una piattaforma Windows a 64 bit, è necessario compilarlo come DLL o DLL a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="e7b3d-123">If you are creating a TSP for a 64-bit Windows platform, you must compile it as a 64-bit DLL or DLLs.</span></span>

 

 

 
