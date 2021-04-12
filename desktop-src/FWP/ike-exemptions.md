---
title: Esenzioni IKE/AuthIP
description: Protocollo IKE (IKE) e Authenticated Internet Protocol (AuthIP), per funzionare, è necessario esentare il traffico di rete dal filtro IPsec.
ms.assetid: 365bfebc-250a-440f-8056-ff9601daa030
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d58a6d00ddd337d56c3c00a34b6949213be6ee26
ms.sourcegitcommit: 60ad94096619da5476f9bbcd4cc231b40b6f5358
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104398636"
---
# <a name="ikeauthip-exemptions"></a><span data-ttu-id="725ad-103">Esenzioni IKE/AuthIP</span><span class="sxs-lookup"><span data-stu-id="725ad-103">IKE/AuthIP Exemptions</span></span>

<span data-ttu-id="725ad-104">I moduli di chiave Internet Protocol Security (IPsec), protocollo IKE (IKE) e Authenticated Internet Protocol (AuthIP), per funzionare, devono esentare il traffico di rete dal filtro IPsec.</span><span class="sxs-lookup"><span data-stu-id="725ad-104">The Internet Protocol security (IPsec) keying modules, Internet Key Exchange (IKE) and Authenticated Internet Protocol (AuthIP), in order to function, need to exempt their network traffic from the IPsec filtering.</span></span>

<span data-ttu-id="725ad-105">In Windows Filtering Platform (WFP) il motore di filtro di base (BFE) aggiunge automaticamente i filtri di esenzione IKE e AuthIP quando viene aggiunto il primo filtro dei criteri della modalità principale IKE o AuthIP e li elimina quando viene eliminato l'ultimo filtro dei criteri IKE o AuthIP MM.</span><span class="sxs-lookup"><span data-stu-id="725ad-105">In Windows Filtering Platform (WFP) the Base Filtering Engine (BFE) automatically adds IKE and AuthIP exemption filters when the first IKE or AuthIP main mode (MM) policy filter is added and deletes them when the last IKE or AuthIP MM policy filter is deleted.</span></span> <span data-ttu-id="725ad-106">In questo modo, i provider di criteri non devono gestire singolarmente le esenzioni di filtro IKE e AuthIP.</span><span class="sxs-lookup"><span data-stu-id="725ad-106">This way, the policy providers do not have to manage IKE and AuthIP filtering exemptions individually.</span></span>

<span data-ttu-id="725ad-107">Un filtro dei criteri IKE MM è un filtro nel livello [**FWPM \_ livello motore \_ IKEEXT \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) che fa riferimento a un contesto del provider di tipo [**FWPM \_ IPSec \_ IKE \_ mm \_ context**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type).</span><span class="sxs-lookup"><span data-stu-id="725ad-107">An IKE MM policy filter is a filter in the engine layer [**FWPM\_LAYER\_IKEEXT\_V{4\|6}**](management-filtering-layer-identifiers-.md) that references a provider context of type [**FWPM\_IPSEC\_IKE\_MM\_CONTEXT**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type).</span></span>

<span data-ttu-id="725ad-108">Un filtro dei criteri AuthIP MM è un filtro nel livello del motore [**FWPM \_ livello \_ IKEEXT \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) che fa riferimento a un contesto del provider di tipo FWPM il [**\_ \_ \_ \_ contesto di AuthIP mm di IPSec**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type).</span><span class="sxs-lookup"><span data-stu-id="725ad-108">An AuthIP MM policy filter is a filter in the engine layer [**FWPM\_LAYER\_IKEEXT\_V{4\|6}**](management-filtering-layer-identifiers-.md) that references a provider context of type [**FWPM\_IPSEC\_AUTHIP\_MM\_CONTEXT**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type).</span></span>

<span data-ttu-id="725ad-109">Un filtro di esenzione IKE o AuthIP è un filtro nel livello motore [**FWPM \_ del \_ trasporto in \_ ingresso \_ v {4 \| 6}**](management-filtering-layer-identifiers-.md) o **FWPM \_ Layer in \_ uscita del \_ trasporto \_ v {4 \| 6}** ponderato in modo automatico nell'intervallo di ponderazione del FWPM di [**\_ ponderazione \_ \_ IKE \_**](filter-weight-identifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="725ad-109">An IKE or AuthIP exemption filter is a filter in the engine layer [**FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6}**](management-filtering-layer-identifiers-.md) or **FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6}** auto-weighted in the [**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**](filter-weight-identifiers.md) weight range.</span></span>

<span data-ttu-id="725ad-110">Di seguito sono riportate le esenzioni IKE e AuthIP implementate da BFE.</span><span class="sxs-lookup"><span data-stu-id="725ad-110">The IKE and AuthIP exemptions implemented by BFE are as follows.</span></span>

| <span data-ttu-id="725ad-111">Versione IP</span><span class="sxs-lookup"><span data-stu-id="725ad-111">IP version</span></span>      | <span data-ttu-id="725ad-112">Porta</span><span class="sxs-lookup"><span data-stu-id="725ad-112">Port</span></span>                        | <span data-ttu-id="725ad-113">Esenzione</span><span class="sxs-lookup"><span data-stu-id="725ad-113">Exemption</span></span>                                                                                                                                                                                                                             |
|-----------------|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="725ad-114">IPv4</span><span class="sxs-lookup"><span data-stu-id="725ad-114">IPv4</span></span><br/> | <span data-ttu-id="725ad-115">UDP: 500 UDP: 4500</span><span class="sxs-lookup"><span data-stu-id="725ad-115">UDP:500 UDP:4500</span></span><br/> | <span data-ttu-id="725ad-116">Consentire il traffico IKE e AuthIP al livello di trasporto in ingresso e al livello di trasporto in uscita.</span><span class="sxs-lookup"><span data-stu-id="725ad-116">Permit IKE and AuthIP traffic at the inbound transport layer and at the outbound transport layer.</span></span> <br/> <span data-ttu-id="725ad-117">Consentire il traffico IKE e AuthIP ai livelli di ricezione/accettazione e connessione di ALE, ma limitarlo al sistema locale.</span><span class="sxs-lookup"><span data-stu-id="725ad-117">Permit IKE and AuthIP traffic at the ALE receive/accept and connect layers, but restrict it to local system.</span></span><br/> |
| <span data-ttu-id="725ad-118">IPv6</span><span class="sxs-lookup"><span data-stu-id="725ad-118">IPv6</span></span><br/> | <span data-ttu-id="725ad-119">UDP: 500</span><span class="sxs-lookup"><span data-stu-id="725ad-119">UDP:500</span></span><br/>          | <span data-ttu-id="725ad-120">Consentire il traffico IKE e AuthIP al livello di trasporto in ingresso e al livello di trasporto in uscita.</span><span class="sxs-lookup"><span data-stu-id="725ad-120">Permit IKE and AuthIP traffic at the inbound transport layer and at the outbound transport layer.</span></span> <br/> <span data-ttu-id="725ad-121">Consentire il traffico IKE e AuthIP ai livelli di ricezione/accettazione e connessione di ALE, ma limitarlo al sistema locale.</span><span class="sxs-lookup"><span data-stu-id="725ad-121">Permit IKE and AuthIP traffic at the ALE receive/accept and connect layers, but restrict it to local system.</span></span><br/> |



 

<span data-ttu-id="725ad-122">I filtri di esenzione IKE e AuthIP sono aperti a tutti gli indirizzi.</span><span class="sxs-lookup"><span data-stu-id="725ad-122">The IKE and AuthIP exemption filters are open to all addresses.</span></span> <span data-ttu-id="725ad-123">Per implementare un firewall con un controllo più granulare, i provider di criteri devono aggiungere filtri in un intervallo di ponderazione superiore alle [**\_ \_ \_ \_ esenzioni IKE dell'intervallo di FWPM ponderato**](filter-weight-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="725ad-123">To implement a firewall with more granular control, policy providers should add filters in a weight range higher than [**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**](filter-weight-identifiers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="725ad-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="725ad-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="725ad-125">Configurazione IPsec</span><span class="sxs-lookup"><span data-stu-id="725ad-125">IPsec Configuration</span></span>](ipsec-configuration.md)
</dt> <dt>

[<span data-ttu-id="725ad-126">Assegnazione di pesi dei filtri</span><span class="sxs-lookup"><span data-stu-id="725ad-126">Filter Weight Assignment</span></span>](filter-weight-assignment.md)
</dt> </dl>

 

 





