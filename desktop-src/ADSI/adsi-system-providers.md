---
title: Provider di servizi ADSI
description: In questo argomento viene fornita una panoramica dei provider di servizi ADSI disponibili nel server.
ms.assetid: 419d7953-a879-4d6c-be74-173d76c3f932
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, provider di servizi
- ADSI provider di servizi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e44ba4ebc63338bfb38d2b9d5da1f46e51b31aa8
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300421"
---
# <a name="adsi-service-providers"></a><span data-ttu-id="33082-105">Provider di servizi ADSI</span><span class="sxs-lookup"><span data-stu-id="33082-105">ADSI Service Providers</span></span>

<span data-ttu-id="33082-106">ADSI include i provider di servizi elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="33082-106">ADSI includes the service providers listed in the following table.</span></span>



| <span data-ttu-id="33082-107">Provider di servizi</span><span class="sxs-lookup"><span data-stu-id="33082-107">Service provider</span></span> | <span data-ttu-id="33082-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="33082-108">Description</span></span>                                                                                | <span data-ttu-id="33082-109">Per ulteriori informazioni</span><span class="sxs-lookup"><span data-stu-id="33082-109">For more information</span></span>                                      |
|------------------|--------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span data-ttu-id="33082-110">LDAP</span><span class="sxs-lookup"><span data-stu-id="33082-110">LDAP</span></span><br/>  | <span data-ttu-id="33082-111">Implementazione dello spazio dei nomi compatibile con il protocollo Lightweight Directory Access.</span><span class="sxs-lookup"><span data-stu-id="33082-111">Namespace implementation compatible with Lightweight Directory Access Protocol.</span></span><br/> | [<span data-ttu-id="33082-112">Provider LDAP ADSI</span><span class="sxs-lookup"><span data-stu-id="33082-112">ADSI LDAP Provider</span></span>](adsi-ldap-provider.md)<br/>   |
| <span data-ttu-id="33082-113">WinNT</span><span class="sxs-lookup"><span data-stu-id="33082-113">WinNT</span></span><br/> | <span data-ttu-id="33082-114">Implementazione dello spazio dei nomi compatibile con Windows.</span><span class="sxs-lookup"><span data-stu-id="33082-114">Namespace implementation compatible with Windows.</span></span><br/>                               | [<span data-ttu-id="33082-115">Provider ADSI WinNT</span><span class="sxs-lookup"><span data-stu-id="33082-115">ADSI WinNT Provider</span></span>](adsi-winnt-provider.md)<br/> |



 

<span data-ttu-id="33082-116">Altri provider di servizi sono inclusi come parte di prodotti diversi da ADSI.</span><span class="sxs-lookup"><span data-stu-id="33082-116">Other service providers are included as part of products other than ADSI.</span></span> <span data-ttu-id="33082-117">Di seguito sono riportati i provider di servizi ADSI implementati da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="33082-117">The following are the ADSI service providers implemented by Microsoft.</span></span>



| <span data-ttu-id="33082-118">Provider di servizi</span><span class="sxs-lookup"><span data-stu-id="33082-118">Service provider</span></span> | <span data-ttu-id="33082-119">Per ulteriori informazioni</span><span class="sxs-lookup"><span data-stu-id="33082-119">For more information</span></span>                                                                        |
|------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="33082-120">IIS</span><span class="sxs-lookup"><span data-stu-id="33082-120">IIS</span></span><br/>   | <span data-ttu-id="33082-121">[Architettura del provider ADSI IIS](/previous-versions/iis/6.0-sdk/ms525929(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="33082-121">[IIS ADSI Provider Architecture](/previous-versions/iis/6.0-sdk/ms525929(v=vs.90))</span></span><br/> |



 

<span data-ttu-id="33082-122">I metodi e i metodi di proprietà esposti dalle interfacce ADSI non sono supportati da tutti i provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="33082-122">The methods and property methods exposed by ADSI interfaces are not supported by every service provider.</span></span> <span data-ttu-id="33082-123">Poiché i diversi servizi directory variano a seconda dei tipi di oggetti e proprietà archiviati, usano protocolli diversi e l'autenticazione, ADSI è progettato per funzionare senza interruzioni con i provider di servizi supportati.</span><span class="sxs-lookup"><span data-stu-id="33082-123">Because different directory services vary in the types of objects and properties stored, use different protocols, and authentication, ADSI is designed to work seamlessly with supported service providers.</span></span> <span data-ttu-id="33082-124">Sono pertanto disponibili interfacce, metodi e metodi di proprietà che funzionano con un provider di servizi, ad esempio LDAP, che potrebbero non funzionare in un altro, ad esempio WinNT.</span><span class="sxs-lookup"><span data-stu-id="33082-124">Thus, there are interfaces, methods, and property methods that work with one service provider, such as LDAP, that may not work on another, such as WinNT.</span></span>

<span data-ttu-id="33082-125">In questa sezione sono contenute informazioni specifiche del provider, ad esempio il formato ADsPath, un elenco di oggetti ADSI utilizzati per il provider di servizi e informazioni sul tipo di dati e sulla sintassi per i provider di servizi inclusi in ADSI.</span><span class="sxs-lookup"><span data-stu-id="33082-125">This section contains provider-specific information, such as the ADsPath format, a listing of ADSI objects used for that service provider, and data type and syntax information for the service providers included with ADSI.</span></span> <span data-ttu-id="33082-126">È inoltre disponibile una descrizione riepilogativa delle interfacce ADSI supportate da ogni provider incluso in ADSI.</span><span class="sxs-lookup"><span data-stu-id="33082-126">There is also a summary description of ADSI interfaces supported by each provider included with ADSI.</span></span>

<span data-ttu-id="33082-127">In ADSI i provider diversi sono associati a DLL diverse.</span><span class="sxs-lookup"><span data-stu-id="33082-127">In ADSI, different providers are associated with different DLLs.</span></span> <span data-ttu-id="33082-128">Il provider LDAP è associato a Adsldp.dll, Adsldpc.dll e Adsmsext.dll.</span><span class="sxs-lookup"><span data-stu-id="33082-128">The LDAP provider is associated with Adsldp.dll, Adsldpc.dll, and Adsmsext.dll.</span></span> <span data-ttu-id="33082-129">Il provider WinNT è associato a Adsnt.dll.</span><span class="sxs-lookup"><span data-stu-id="33082-129">The WinNT provider is associated with Adsnt.dll.</span></span> <span data-ttu-id="33082-130">Il provider del ROUTER è associato a Activeds.dll.</span><span class="sxs-lookup"><span data-stu-id="33082-130">The ROUTER provider is associated with Activeds.dll.</span></span>

> [!Note]  
> <span data-ttu-id="33082-131">Non presupporre che i provider ADSI predefiniti siano thread-safe.</span><span class="sxs-lookup"><span data-stu-id="33082-131">Do not assume that default ADSI providers are thread-safe.</span></span> <span data-ttu-id="33082-132">Gli sviluppatori di applicazioni multithreading devono coordinare l'accesso tra thread attraverso l'uso corretto di oggetti di sincronizzazione, ad esempio semafori, mutex, sezioni critiche e così via.</span><span class="sxs-lookup"><span data-stu-id="33082-132">Multithreaded application developers should coordinate access between threads through the proper use of synchronization objects such as semaphores, mutexes, critical sections, and so on.</span></span>

 

<span data-ttu-id="33082-133">Per ulteriori informazioni sui provider di servizi ADSI, vedere la pagina relativa al supporto del router e del provider [ADSI](adsi-router.md) per [le interfacce ADSI](provider-support-of-adsi-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="33082-133">For more information about ADSI service providers, see [ADSI Router](adsi-router.md) and [Provider Support of ADSI interfaces](provider-support-of-adsi-interfaces.md).</span></span>

 

