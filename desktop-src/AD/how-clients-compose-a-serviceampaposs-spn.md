---
title: Composizione del nome SPN di un servizio da parte dei client
description: Per autenticare un servizio, un'applicazione client compone un nome SPN per l'istanza del servizio a cui deve connettersi.
ms.assetid: cf6c491a-d84d-4c9c-bd69-1f2264f395b6
ms.tgt_platform: multiple
keywords:
- Composizione del nome SPN di un servizio da parte dei client
- nome dell'entità servizio AD, modo in cui i client costituiscono il nome SPN di un servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd8aa599b6d8238017897c9383bab188ce144e0d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955139"
---
# <a name="how-clients-compose-a-services-spn"></a><span data-ttu-id="00d17-105">Composizione del nome SPN di un servizio da parte dei client</span><span class="sxs-lookup"><span data-stu-id="00d17-105">How Clients Compose a Service's SPN</span></span>

<span data-ttu-id="00d17-106">Per autenticare un servizio, un'applicazione client compone un nome SPN per l'istanza del servizio a cui deve connettersi.</span><span class="sxs-lookup"><span data-stu-id="00d17-106">To authenticate a service, a client application composes an SPN for the service instance to which it must connect.</span></span> <span data-ttu-id="00d17-107">L'applicazione client può usare la funzione [**DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) per comporre un nome SPN.</span><span class="sxs-lookup"><span data-stu-id="00d17-107">The client application can use the [**DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) function to compose an SPN.</span></span> <span data-ttu-id="00d17-108">Il client specifica i componenti del nome SPN utilizzando dati noti o dati recuperati da origini diverse dal servizio stesso.</span><span class="sxs-lookup"><span data-stu-id="00d17-108">The client specifies the components of the SPN using known data or data retrieved from sources other than the service itself.</span></span>

<span data-ttu-id="00d17-109">Il formato di un nome SPN è come illustrato nel formato seguente:</span><span class="sxs-lookup"><span data-stu-id="00d17-109">The form of an SPN is as shown in the following form:</span></span>


```C++
<service class>/<host>:<port>/<service name>
```



<span data-ttu-id="00d17-110">In questo formato &lt; sono necessari "Service Class &gt; " e " &lt; host &gt; ".</span><span class="sxs-lookup"><span data-stu-id="00d17-110">In this form, "&lt;service class&gt;" and "&lt;host&gt;" are required.</span></span> <span data-ttu-id="00d17-111">" &lt; Port &gt; " e " &lt; Service Name &gt; " facoltativi.</span><span class="sxs-lookup"><span data-stu-id="00d17-111">"&lt;port&gt;" and "&lt;service name&gt;" optional.</span></span>

<span data-ttu-id="00d17-112">In genere, il client riconosce la &lt; parte "classe &gt; di servizio" del nome e riconosce quale dei componenti facoltativi includere nell'SPN.</span><span class="sxs-lookup"><span data-stu-id="00d17-112">Typically, the client recognizes the "&lt;service class&gt;" part of the name, and recognizes which of the optional components to include in the SPN.</span></span> <span data-ttu-id="00d17-113">Il client può recuperare i componenti del nome SPN dalle origini, ad esempio un punto di connessione del servizio (SCP) o l'input dell'utente.</span><span class="sxs-lookup"><span data-stu-id="00d17-113">The client can retrieve components of the SPN from sources such as a service connection point (SCP) or user input.</span></span> <span data-ttu-id="00d17-114">Ad esempio, il client può leggere l'attributo **serviceDNSName** del SCP di un servizio per ottenere il &lt; componente "host &gt; ".</span><span class="sxs-lookup"><span data-stu-id="00d17-114">For example, the client can read the **serviceDNSName** attribute of a service's SCP to get the "&lt;host&gt;" component.</span></span> <span data-ttu-id="00d17-115">L'attributo **serviceDNSName** contiene il nome DNS del server in cui è in esecuzione l'istanza del servizio o il nome DNS dei record SRV contenenti i dati host per le repliche del servizio.</span><span class="sxs-lookup"><span data-stu-id="00d17-115">The **serviceDNSName** attribute contains either the DNS name of the server on which the service instance is running or the DNS name of SRV records containing the host data for service replicas.</span></span> <span data-ttu-id="00d17-116">Il &lt; componente "nome servizio &gt; ", usato solo per i servizi replicabili, può essere il nome distinto del SCP del servizio, il nome DNS del dominio servito dal servizio o il nome DNS dei record SRV o MX.</span><span class="sxs-lookup"><span data-stu-id="00d17-116">The "&lt;service name&gt;" component, used only for replicable services, can be the distinguished name of the service's SCP, the DNS name of the domain served by the service, or the DNS name of SRV or MX records.</span></span>

<span data-ttu-id="00d17-117">Per ulteriori informazioni e un esempio di codice utilizzato per comporre un nome SPN per un servizio, vedere [come un client autentica un servizio Windows Sockets basato su SCP](how-a-client-authenticates-an-scp-based-windows-sockets-service.md).</span><span class="sxs-lookup"><span data-stu-id="00d17-117">For more information and a code example used to compose an SPN for a service, see [How a Client Authenticates an SCP-based Windows Sockets Service](how-a-client-authenticates-an-scp-based-windows-sockets-service.md).</span></span>

<span data-ttu-id="00d17-118">Per ulteriori informazioni e una descrizione dei componenti SPN, vedere [formati dei nomi per nomi SPN univoci](name-formats-for-unique-spns.md).</span><span class="sxs-lookup"><span data-stu-id="00d17-118">For more information and a description of the SPN components, see [Name Formats for Unique SPNs](name-formats-for-unique-spns.md).</span></span>

 

 




