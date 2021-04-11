---
title: Accesso remoto
description: Usare il servizio di accesso remoto (RAS) per creare applicazioni client.
ms.assetid: 4e6c04d4-f989-4248-901f-ec15f61582da
keywords:
- RAS del servizio di accesso remoto
- RAS RAS
- RAS del servizio di accesso remoto, pagina iniziale
- Ras RAS, vedere Accesso remoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95a4b1c06656b51395c8c4fc666e59d6115bd839
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104117407"
---
# <a name="remote-access"></a><span data-ttu-id="13bac-107">Accesso remoto</span><span class="sxs-lookup"><span data-stu-id="13bac-107">Remote Access</span></span>

## <a name="purpose"></a><span data-ttu-id="13bac-108">Scopo</span><span class="sxs-lookup"><span data-stu-id="13bac-108">Purpose</span></span>

<span data-ttu-id="13bac-109">Usare il servizio di accesso remoto (RAS) per creare applicazioni client.</span><span class="sxs-lookup"><span data-stu-id="13bac-109">Use Remote Access Service (RAS) to create client applications.</span></span> <span data-ttu-id="13bac-110">Queste applicazioni visualizzano finestre di dialogo comuni RAS, gestiscono le connessioni e i dispositivi di accesso remoto e modificano le voci del libro telefonico.</span><span class="sxs-lookup"><span data-stu-id="13bac-110">These applications display RAS common dialog boxes, manage remote access connections and devices, and manipulate phone-book entries.</span></span> <span data-ttu-id="13bac-111">RAS fornisce inoltre la nuova generazione di funzionalità server per il servizio di accesso remoto (RAS) per Windows.</span><span class="sxs-lookup"><span data-stu-id="13bac-111">RAS also provides the next generation of server functionality for the Remote Access Service (RAS) for Windows.</span></span> <span data-ttu-id="13bac-112">La funzionalità del server RRAS segue e si basa sul servizio di accesso remoto (RAS).</span><span class="sxs-lookup"><span data-stu-id="13bac-112">The RRAS server functionality follows and builds upon the Remote Access Service (RAS).</span></span>

## <a name="where-applicable"></a><span data-ttu-id="13bac-113">Se applicabile</span><span class="sxs-lookup"><span data-stu-id="13bac-113">Where applicable</span></span>

<span data-ttu-id="13bac-114">Il servizio di accesso remoto è applicabile in qualsiasi ambiente informatico che usa un collegamento WAN (Wide Area Network) o una rete privata virtuale (VPN).</span><span class="sxs-lookup"><span data-stu-id="13bac-114">The Remote Access Service is applicable in any computing environment that uses a Wide Area Network (WAN) link or a Virtual Private Network (VPN).</span></span> <span data-ttu-id="13bac-115">RAS rende possibile la connessione di un computer client remoto a un server di rete tramite un collegamento WAN o una VPN.</span><span class="sxs-lookup"><span data-stu-id="13bac-115">RAS makes it possible to connect a remote client computer to a network server over a WAN link or a VPN.</span></span> <span data-ttu-id="13bac-116">Il computer remoto funge quindi da rete LAN del server come se il computer remoto fosse connesso direttamente alla LAN.</span><span class="sxs-lookup"><span data-stu-id="13bac-116">The remote computer then functions on the server's LAN as though the remote computer was connected to the LAN directly.</span></span> <span data-ttu-id="13bac-117">L'API RAS consente ai programmatori di accedere alle funzionalità di RAS a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="13bac-117">The RAS API enables programmers to access the features of RAS programmatically.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="13bac-118">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="13bac-118">Developer audience</span></span>

<span data-ttu-id="13bac-119">L'API RAS è progettata per l'uso da parte dei programmatori C/C++.</span><span class="sxs-lookup"><span data-stu-id="13bac-119">The RAS API is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="13bac-120">I programmatori Microsoft Visual Basic possono anche trovare l'API utile.</span><span class="sxs-lookup"><span data-stu-id="13bac-120">Microsoft Visual Basic programmers may also find the API useful.</span></span> <span data-ttu-id="13bac-121">I programmatori devono acquisire familiarità con i concetti di rete.</span><span class="sxs-lookup"><span data-stu-id="13bac-121">Programmers should be familiar with networking concepts.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="13bac-122">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="13bac-122">Run-time requirements</span></span>

<span data-ttu-id="13bac-123">Alcune funzioni nell'API RAS sono supportate solo nei server di rete e altre funzioni sono supportate solo sui client di rete.</span><span class="sxs-lookup"><span data-stu-id="13bac-123">Some of the functions in the RAS API are supported only on network servers and other functions are supported only on network clients.</span></span> <span data-ttu-id="13bac-124">Per informazioni più specifiche sui sistemi operativi che supportano una particolare funzione, vedere le sezioni requisiti nella documentazione.</span><span class="sxs-lookup"><span data-stu-id="13bac-124">For more specific information about which operating systems support a particular function, refer to the Requirements sections in the documentation.</span></span>

<span data-ttu-id="13bac-125">La [funzionalità RAS avanzata](function-comparison-windows-2000-versus-rras-redistributable.md) di RRAS è disponibile per Windows NT Server 4,0 installando [RRAS Redistributable](https://www.microsoft.com/ntserver/nts/downloads/winfeatures/rras/rrasdown.asp).</span><span class="sxs-lookup"><span data-stu-id="13bac-125">The [enhanced RAS functionality](function-comparison-windows-2000-versus-rras-redistributable.md) of RRAS is available for Windows NT Server 4.0 by installing the [RRAS redistributable](https://www.microsoft.com/ntserver/nts/downloads/winfeatures/rras/rrasdown.asp).</span></span> <span data-ttu-id="13bac-126">Tutte le funzionalità di RRAS sono incorporate in Windows 2000 Server, Windows Server 2003 e Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="13bac-126">All the functionality of RRAS is incorporated into Windows 2000 Server, Windows Server 2003, and Windows Server 2008.</span></span> <span data-ttu-id="13bac-127">Le applicazioni RRAS non possono essere eseguite su workstation Windows NT 4,0 o sui sistemi operativi client, ad esempio Windows 95.</span><span class="sxs-lookup"><span data-stu-id="13bac-127">RRAS applications cannot run on Windows NT Workstation 4.0 or on client operating systems, such as Windows 95.</span></span> <span data-ttu-id="13bac-128">Per informazioni più specifiche sui sistemi operativi che supportano una particolare funzione, vedere le sezioni requisiti nella documentazione.</span><span class="sxs-lookup"><span data-stu-id="13bac-128">For more specific information about which operating systems support a particular function, refer to the Requirements sections in the documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="13bac-129">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="13bac-129">In this section</span></span>



| <span data-ttu-id="13bac-130">Argomento</span><span class="sxs-lookup"><span data-stu-id="13bac-130">Topic</span></span>                                                                                             | <span data-ttu-id="13bac-131">Descrizione</span><span class="sxs-lookup"><span data-stu-id="13bac-131">Description</span></span>                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="13bac-132">Servizio di accesso remoto</span><span class="sxs-lookup"><span data-stu-id="13bac-132">Remote Access Service</span></span>](about-remote-access-service.md)<br/>                               | <span data-ttu-id="13bac-133">Il servizio di accesso remoto (RAS) fornisce funzionalità di accesso remoto alle applicazioni client nei computer che eseguono Windows.</span><span class="sxs-lookup"><span data-stu-id="13bac-133">Remote Access Service (RAS) provides remote access capabilities to client applications on computers running Windows.</span></span><br/>                                                                                          |
| [<span data-ttu-id="13bac-134">Amministrazione del servizio di accesso remoto</span><span class="sxs-lookup"><span data-stu-id="13bac-134">Remote Access Service Administration</span></span>](about-remote-access-service-administration.md)<br/> | <span data-ttu-id="13bac-135">Amministrazione servizio di accesso remoto fornisce un set di funzioni per l'amministrazione delle autorizzazioni e delle porte utente nei server RAS.</span><span class="sxs-lookup"><span data-stu-id="13bac-135">Remote Access Service Administration provides a set of functions for administering user permissions and ports on RAS servers.</span></span> <span data-ttu-id="13bac-136">Utilizzando queste funzioni, è possibile sviluppare un'applicazione di amministrazione del server RAS.</span><span class="sxs-lookup"><span data-stu-id="13bac-136">Using these functions, you can develop a RAS server administration application.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="13bac-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="13bac-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13bac-138">Routing</span><span class="sxs-lookup"><span data-stu-id="13bac-138">Routing</span></span>](routing-start-page.md)
</dt> <dt>

[<span data-ttu-id="13bac-139">Protocolli di routing</span><span class="sxs-lookup"><span data-stu-id="13bac-139">Routing Protocols</span></span>](routing-protocols-start-page.md)
</dt> </dl>

 

 





