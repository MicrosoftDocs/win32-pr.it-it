---
description: WSDAPI (Web Services on Devices) fornisce il supporto per il profilo dei dispositivi per i servizi Web (DPWS) in Windows Vista, che consente la comunicazione dei servizi Web (WS) tra i PC basati su Windows e i dispositivi connessi alla rete.
ms.assetid: 61fceca3-a33e-40f7-9370-97605a81eb06
title: Conformità della specifica WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d915a8f963ff346ad8a8fee8a2188aa69cecb8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231658"
---
# <a name="wsdapi-specification-compliance"></a><span data-ttu-id="377de-103">Conformità della specifica WSDAPI</span><span class="sxs-lookup"><span data-stu-id="377de-103">WSDAPI Specification Compliance</span></span>

<span data-ttu-id="377de-104">WSDAPI (Web Services on Devices) fornisce il supporto per il [profilo dei dispositivi per i servizi Web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) in Windows Vista, che consente la comunicazione dei servizi Web (WS) tra i PC basati su Windows e i dispositivi connessi alla rete.</span><span class="sxs-lookup"><span data-stu-id="377de-104">Web Services on Devices API (WSDAPI) provides support for the [Devices Profile for Web Services](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) on Windows Vista, which enables Web Services (WS) communication between Windows-based PCs and network connected devices.</span></span> <span data-ttu-id="377de-105">DPWS assembla le specifiche WS di base, ad esempio [WS-Eventing](https://schemas.xmlsoap.org/ws/2004/08/eventing/), [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf)e [WS-MetadataExchange](https://schemas.xmlsoap.org/ws/2004/09/mex/), e migliora o vincola le specifiche per fornire un set di base di funzionalità per i dispositivi con vincoli di risorse.</span><span class="sxs-lookup"><span data-stu-id="377de-105">DPWS assembles basic WS specifications, such as [WS-Eventing](https://schemas.xmlsoap.org/ws/2004/08/eventing/), [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf), and [WS-MetadataExchange](https://schemas.xmlsoap.org/ws/2004/09/mex/), and enhances or constrains them to provide a baseline set of capabilities for resource-constrained devices.</span></span> <span data-ttu-id="377de-106">Questa specifica di base contiene le funzionalità necessarie, ad esempio la possibilità di descrivere le proprietà del dispositivo tramite metadati e la funzionalità facoltativa, ad esempio la possibilità di rifiutare messaggi specifici per motivi di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="377de-106">This baseline specification contains required functionality, such as the ability to describe properties of the device through metadata, and optional functionality, such as the ability to reject specific messages for security reasons.</span></span>

<span data-ttu-id="377de-107">L'implementazione di WSDAPI in Windows Vista è la prima versione del supporto esplicito per DPWS e è un'implementazione non gestita di DPWS che è separata e distinta dalle altre implementazioni di servizi Web, ad esempio [Windows Communication Foundation](/previous-versions/dotnet/netframework-3.0/ms735119(v=vs.85)) o [WS-Management](https://schemas.xmlsoap.org/ws/2005/06/management/).</span><span class="sxs-lookup"><span data-stu-id="377de-107">The WSDAPI implementation in Windows Vista is the first release of explicit support for the DPWS, and is an unmanaged implementation of DPWS that is separate and distinct from other Web Services implementations (such as the [Windows Communication Foundation](/previous-versions/dotnet/netframework-3.0/ms735119(v=vs.85)) or [WS-Management](https://schemas.xmlsoap.org/ws/2005/06/management/)).</span></span>

<span data-ttu-id="377de-108">Gli argomenti seguenti sono di particolare interesse per i produttori di dispositivi e altri implementatori di dispositivi che creano dispositivi che interagiscono con client e host WSDAPI basati su Windows senza usare WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="377de-108">The following topics are of interest to device manufacturers and other device implementers that create devices that interoperate with Windows-based WSDAPI clients and hosts without using WSDAPI.</span></span> <span data-ttu-id="377de-109">In questi argomenti viene descritta l'implementazione di WSDAPI rispetto alle specifiche sottostanti.</span><span class="sxs-lookup"><span data-stu-id="377de-109">These topics describe the implementation of WSDAPI relative to the underlying specifications.</span></span> <span data-ttu-id="377de-110">Esse coprono l'implementazione di funzionalità necessarie, funzionalità facoltative e funzionalità aggiuntive non definite nella specifica.</span><span class="sxs-lookup"><span data-stu-id="377de-110">They cover the implementation of required functionality, optional functionality, and additional functionality not defined in the specification.</span></span>

-   [<span data-ttu-id="377de-111">Conformità della specifica DPWS</span><span class="sxs-lookup"><span data-stu-id="377de-111">DPWS Specification Compliance</span></span>](dpws-specification-compliance.md)
-   [<span data-ttu-id="377de-112">Conformità specifica WS-Discovery</span><span class="sxs-lookup"><span data-stu-id="377de-112">WS-Discovery Specification Compliance</span></span>](ws-discovery-specification-compliance.md)
-   [<span data-ttu-id="377de-113">Conformità alla specifica WS-MetadataExchange e WS-Transfer</span><span class="sxs-lookup"><span data-stu-id="377de-113">WS-MetadataExchange and WS-Transfer Specification Compliance</span></span>](ws-metadataexchange-and-ws-transfer-specification-compliance.md)
-   [<span data-ttu-id="377de-114">Funzionalità di WS-Discovery aggiuntive</span><span class="sxs-lookup"><span data-stu-id="377de-114">Additional WS-Discovery Functionality</span></span>](additional-ws-discovery-functionality.md)

## <a name="related-topics"></a><span data-ttu-id="377de-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="377de-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="377de-116">Sviluppo di dispositivi WSD</span><span class="sxs-lookup"><span data-stu-id="377de-116">WSD Device Development</span></span>](wsd-device-development.md)
</dt> <dt>

[<span data-ttu-id="377de-117">Indicazioni sull'implementazione di dispositivi WSD</span><span class="sxs-lookup"><span data-stu-id="377de-117">WSD Device Implementation Recommendations</span></span>](wsd-device-implementation-recommendations.md)
</dt> </dl>

 

 
