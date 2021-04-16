---
description: Il sistema utilizza le informazioni di configurazione per determinare come avviare il servizio.
ms.assetid: fc8c631e-076c-4745-8db0-90f46a202e6a
title: Service Configuration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5019469e17fdd0807aa101c7d1e4d6f6019da783
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525824"
---
# <a name="service-configuration"></a><span data-ttu-id="1a1ff-103">Service Configuration</span><span class="sxs-lookup"><span data-stu-id="1a1ff-103">Service Configuration</span></span>

<span data-ttu-id="1a1ff-104">Il sistema utilizza le informazioni di configurazione per determinare come avviare il servizio.</span><span class="sxs-lookup"><span data-stu-id="1a1ff-104">The system uses the configuration information to determine how to start the service.</span></span> <span data-ttu-id="1a1ff-105">Le informazioni di configurazione includono anche il nome visualizzato del servizio e la relativa descrizione.</span><span class="sxs-lookup"><span data-stu-id="1a1ff-105">The configuration information also includes the service display name and its description.</span></span> <span data-ttu-id="1a1ff-106">Per il servizio DHCP, ad esempio, è possibile usare il nome visualizzato "servizio Dynamic Host Configuration Protocol" e la descrizione "fornisce indirizzi Internet per il computer nella rete".</span><span class="sxs-lookup"><span data-stu-id="1a1ff-106">For example, for the DHCP service, you could use the display name "Dynamic Host Configuration Protocol Service" and the description "Provides internet addresses for computer on your network."</span></span>

<span data-ttu-id="1a1ff-107">Per modificare le informazioni di configurazione per un oggetto servizio, un programma di configurazione utilizza la funzione [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) o [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) .</span><span class="sxs-lookup"><span data-stu-id="1a1ff-107">To modify the configuration information for a service object, a configuration program uses the [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) or [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) function.</span></span> <span data-ttu-id="1a1ff-108">Per un esempio, vedere [modifica di una configurazione del servizio](changing-a-service-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="1a1ff-108">For an example, see [Changing a Service Configuration](changing-a-service-configuration.md).</span></span>

<span data-ttu-id="1a1ff-109">Per recuperare le informazioni di configurazione per un oggetto servizio, il programma di configurazione utilizza la funzione [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) o [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) .</span><span class="sxs-lookup"><span data-stu-id="1a1ff-109">To retrieve the configuration information for a service object, the configuration program uses the [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) or [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) function.</span></span> <span data-ttu-id="1a1ff-110">Per un esempio, vedere [esecuzione di query sulla configurazione di un servizio](querying-a-service-s-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="1a1ff-110">For an example, see [Querying a Service's Configuration](querying-a-service-s-configuration.md).</span></span>

<span data-ttu-id="1a1ff-111">Le funzioni di configurazione del servizio [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) e [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) supportano l'utilizzo di trigger per controllare l'avvio del servizio.</span><span class="sxs-lookup"><span data-stu-id="1a1ff-111">The [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) and [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) service configuration functions support the use of triggers to control service start.</span></span>

<span data-ttu-id="1a1ff-112">Per modificare il descrittore di sicurezza per un oggetto SCManager o un oggetto servizio, un programma di configurazione utilizza la funzione [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) .</span><span class="sxs-lookup"><span data-stu-id="1a1ff-112">To modify the security descriptor for either an SCManager object or a service object, a configuration program uses the [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) function.</span></span> <span data-ttu-id="1a1ff-113">Per recuperare una copia del descrittore di sicurezza, il programma di configurazione utilizza la funzione [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) .</span><span class="sxs-lookup"><span data-stu-id="1a1ff-113">To retrieve a copy of the security descriptor, the configuration program uses the [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1a1ff-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1a1ff-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a1ff-115">Configurazione di un servizio con SC</span><span class="sxs-lookup"><span data-stu-id="1a1ff-115">Configuring a Service Using SC</span></span>](configuring-a-service-using-sc.md)
</dt> </dl>

 

 
