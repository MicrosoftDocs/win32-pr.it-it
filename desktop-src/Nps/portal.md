---
title: Server dei criteri di rete
description: Server dei criteri di rete è l'implementazione Microsoft di un server e un proxy RADIUS (Remote Authentication Dial-in User Service).
ms.assetid: d0eb41cb-e9c0-4a60-aeac-77d1dd90a75b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0d1dfc680c8a23ca1e80f52230736b3ab586cc8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337886"
---
# <a name="network-policy-server"></a><span data-ttu-id="d7f34-103">Server dei criteri di rete</span><span class="sxs-lookup"><span data-stu-id="d7f34-103">Network Policy Server</span></span>

## <a name="purpose"></a><span data-ttu-id="d7f34-104">Scopo</span><span class="sxs-lookup"><span data-stu-id="d7f34-104">Purpose</span></span>

<span data-ttu-id="d7f34-105">Server dei criteri di rete è l'implementazione Microsoft di un server e un proxy RADIUS (Remote Authentication Dial-in User Service).</span><span class="sxs-lookup"><span data-stu-id="d7f34-105">Network Policy Server (NPS) is the Microsoft implementation of a Remote Authentication Dial-in User Service (RADIUS) server and proxy.</span></span> <span data-ttu-id="d7f34-106">È il successore del servizio di autenticazione Internet (IAS).</span><span class="sxs-lookup"><span data-stu-id="d7f34-106">It is the successor of Internet Authentication Service (IAS).</span></span>

<span data-ttu-id="d7f34-107">Come server RADIUS, NPS esegue l'autenticazione, l'autorizzazione e l'accounting per le connessioni wireless, di autenticazione e di accesso remoto e VPN (Virtual Private Network).</span><span class="sxs-lookup"><span data-stu-id="d7f34-107">As a RADIUS server, NPS performs authentication, authorization, and accounting for wireless, authenticating switch, and remote access dial-up and virtual private network (VPN) connections.</span></span>

<span data-ttu-id="d7f34-108">Server dei criteri di rete è anche un server di valutazione dell'integrità per protezione accesso alla rete (NAP).</span><span class="sxs-lookup"><span data-stu-id="d7f34-108">NPS is also a health evaluator server for Network Access Protection (NAP).</span></span> <span data-ttu-id="d7f34-109">NPS esegue l'autenticazione e l'autorizzazione dei tentativi di connessione di rete e, in base ai criteri di integrità del sistema configurati, valuta la conformità dell'integrità del computer e determina come limitare l'accesso alla rete o la comunicazione di un computer non conforme.</span><span class="sxs-lookup"><span data-stu-id="d7f34-109">NPS performs authentication and authorization of network connection attempts and, based on configured system health policies, evaluates computer health compliance and determines how to limit a noncompliant computer's network access or communication.</span></span> <span data-ttu-id="d7f34-110">Si tratta di una nuova funzionalità specifica solo per NPS. Il servizio IAS non lo supporta.</span><span class="sxs-lookup"><span data-stu-id="d7f34-110">This is a new feature specific to NPS only; IAS does not support it.</span></span> <span data-ttu-id="d7f34-111">Per un elenco completo delle nuove funzionalità di server dei criteri di [rete, vedere servizio di autenticazione Internet e server dei criteri di rete](internet-authentication-service-vs-network-policy-server.md) .</span><span class="sxs-lookup"><span data-stu-id="d7f34-111">See [Internet Authentication Service and Network Policy Server](internet-authentication-service-vs-network-policy-server.md) for a complete list of features new to NPS.</span></span>

<span data-ttu-id="d7f34-112">Server dei criteri di server include due set di API: API per le estensioni NPS e API per oggetti dati server (SDO).</span><span class="sxs-lookup"><span data-stu-id="d7f34-112">NPS includes two API sets: NPS Extensions API and Server Data Objects (SDO) API.</span></span> <span data-ttu-id="d7f34-113">Sia l'API di NPS che l'API SDO sono supportate anche dal precursore di NPS, il servizio di autenticazione Internet.</span><span class="sxs-lookup"><span data-stu-id="d7f34-113">Both NPS Extensions API and SDO API are also supported by the precursor of NPS, the Internet Authentication Service.</span></span>

<span data-ttu-id="d7f34-114">L'API delle estensioni NPS può essere usata per estendere i metodi di autenticazione, autorizzazione e contabilità offerti da server dei criteri di servizio e precedenti da IAS.</span><span class="sxs-lookup"><span data-stu-id="d7f34-114">NPS Extensions API can be used to extend the authentication, authorization, and accounting methods offered by NPS and previously by IAS.</span></span>

<span data-ttu-id="d7f34-115">L'API oggetti dati server può essere utilizzata per modificare la configurazione dei criteri di rete in un computer che esegue NPS o IAS.</span><span class="sxs-lookup"><span data-stu-id="d7f34-115">Server Data Objects API can be used to manipulate the network policy configuration on a computer that runs NPS or IAS.</span></span>

> [!Note]  
> <span data-ttu-id="d7f34-116">I criteri di rete nel server dei criteri di rete sono equivalenti ai criteri di accesso remoto in IAS.</span><span class="sxs-lookup"><span data-stu-id="d7f34-116">Network policies in NPS are equivalent to remote access policies in IAS.</span></span>

 

## <a name="developer-audience"></a><span data-ttu-id="d7f34-117">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="d7f34-117">Developer audience</span></span>

<span data-ttu-id="d7f34-118">L'API delle estensioni NPS è progettata per l'uso da parte dei programmatori che usano il software di sviluppo C/C++.</span><span class="sxs-lookup"><span data-stu-id="d7f34-118">The NPS Extensions API is designed for use by programmers using C/C++ development software.</span></span> <span data-ttu-id="d7f34-119">I programmatori devono acquisire familiarità con i concetti di rete e il protocollo RADIUS.</span><span class="sxs-lookup"><span data-stu-id="d7f34-119">Programmers should be familiar with networking concepts and the RADIUS protocol.</span></span> <span data-ttu-id="d7f34-120">RADIUS è documentato in [rfc 2865](https://www.ietf.org/rfc/rfc2865.txt) e [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt).</span><span class="sxs-lookup"><span data-stu-id="d7f34-120">RADIUS is documented in [RFC 2865](https://www.ietf.org/rfc/rfc2865.txt) and [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt).</span></span>

<span data-ttu-id="d7f34-121">L'API oggetti dati server è progettata per l'uso da parte dei programmatori che usano C/C++ o software di sviluppo Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="d7f34-121">The Server Data Objects API is designed for use by programmers using C/C++ or Visual Basic development software.</span></span> <span data-ttu-id="d7f34-122">I programmatori devono avere familiarità con il [servizio di accesso remoto](/windows/desktop/RRAS/remote-access-request-for-comments) (RAS) e il protocollo RADIUS.</span><span class="sxs-lookup"><span data-stu-id="d7f34-122">Programmers should be familiar with [Remote Access Service](/windows/desktop/RRAS/remote-access-request-for-comments) (RAS) and the RADIUS protocol.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="d7f34-123">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="d7f34-123">Run-time requirements</span></span>

<span data-ttu-id="d7f34-124">L'API delle estensioni NPS è supportata in Windows Server 2008 con l'installazione di Microsoft Commercial Internet Service (MCIS).</span><span class="sxs-lookup"><span data-stu-id="d7f34-124">NPS Extensions API is supported on Windows Server 2008 with the installation of the Microsoft Commercial Internet Service (MCIS).</span></span>

<span data-ttu-id="d7f34-125">L'API oggetti dati server è supportata in Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="d7f34-125">Server Data Objects API is supported on Windows Server 2008.</span></span>

<span data-ttu-id="d7f34-126">Server dei criteri di rete è disponibile in Windows Server 2008 con l'installazione di Microsoft Commercial Internet Service (MCIS).</span><span class="sxs-lookup"><span data-stu-id="d7f34-126">NPS is available on Windows Server 2008 with the installation of the Microsoft Commercial Internet Service (MCIS).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d7f34-127">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="d7f34-127">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="d7f34-128">Overview</span><span class="sxs-lookup"><span data-stu-id="d7f34-128">Overview</span></span>](about-network-policy-server.md)
</dt> <dd>

<span data-ttu-id="d7f34-129">Informazioni generali su RADIUS, IAS e NPS.</span><span class="sxs-lookup"><span data-stu-id="d7f34-129">General information regarding RADIUS, IAS, and NPS.</span></span>

</dd> <dt>

[<span data-ttu-id="d7f34-130">API delle estensioni del server dei criteri di rete</span><span class="sxs-lookup"><span data-stu-id="d7f34-130">Network Policy Server Extensions API</span></span>](ias-extensions.md)
</dt> <dd>

<span data-ttu-id="d7f34-131">API per l'implementazione delle DLL di estensione usate per l'autenticazione, l'autorizzazione e l'accounting.</span><span class="sxs-lookup"><span data-stu-id="d7f34-131">API for implementing extension DLLs used for authentication, authorization, and accounting.</span></span>

</dd> <dt>

[<span data-ttu-id="d7f34-132">API oggetti dati server</span><span class="sxs-lookup"><span data-stu-id="d7f34-132">Server Data Objects API</span></span>](server-data-objects.md)
</dt> <dd>

<span data-ttu-id="d7f34-133">API per la gestione della configurazione dei criteri di rete.</span><span class="sxs-lookup"><span data-stu-id="d7f34-133">API for managing the network policy configuration.</span></span>

</dd> <dt>

[<span data-ttu-id="d7f34-134">Programmabilità SQL</span><span class="sxs-lookup"><span data-stu-id="d7f34-134">SQL Programmability</span></span>](sql-programmability.md)
</dt> <dd>

<span data-ttu-id="d7f34-135">Esempi di stored procedure utilizzate per la gestione della registrazione di NPS (IAS).</span><span class="sxs-lookup"><span data-stu-id="d7f34-135">Samples of stored procedures used for managing NPS (IAS) logging.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="d7f34-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d7f34-136">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="d7f34-137">[TechNet: Server dei criteri di rete](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="d7f34-137">[TechNet: Network Policy Server](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11))</span></span>
</dt> <dt>

<span data-ttu-id="d7f34-138">[TechNet: servizio di autenticazione Internet](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="d7f34-138">[TechNet: Internet Authentication Service](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11))</span></span>
</dt> <dt>

[<span data-ttu-id="d7f34-139">Protezione accesso alla rete</span><span class="sxs-lookup"><span data-stu-id="d7f34-139">Network Access Protection</span></span>](/windows/desktop/NAP/network-access-protection-start-page)
</dt> </dl>

 

 