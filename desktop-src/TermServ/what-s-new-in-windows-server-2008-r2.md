---
title: Novità di Windows Server 2008 R2
description: Windows Server 2008 R2 introduce i nuovi elementi di programmazione seguenti per Servizi Desktop remoto.
ms.assetid: 605a9a34-11fa-433a-9ccd-8368c75b10f0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fec9c29a142d8c97a17d4a73ee1015f84702851
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/11/2020
ms.locfileid: "103956144"
---
# <a name="whats-new-in-windows-server-2008-r2"></a><span data-ttu-id="0ec87-103">Novità di Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0ec87-103">What's New in Windows Server 2008 R2</span></span>

<span data-ttu-id="0ec87-104">Windows Server 2008 R2 introduce i nuovi elementi di programmazione seguenti per Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="0ec87-104">Windows Server 2008 R2 introduces the following new programming elements for Remote Desktop Services.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0ec87-105">Servizi terminal è ora Servizi Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="0ec87-105">Terminal Services Is Now Remote Desktop Services</span></span><br/></td>
<td><span data-ttu-id="0ec87-106">Servizi terminal è stato rinominato Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="0ec87-106">Terminal Services has been renamed Remote Desktop Services.</span></span> <span data-ttu-id="0ec87-107">Un server in cui è installato il servizio ruolo host sessione Desktop remoto (host sessione Desktop remoto) viene ora definito server Host sessione Desktop remoto anziché server terminal.</span><span class="sxs-lookup"><span data-stu-id="0ec87-107">A server that has the Remote Desktop Session Host (RD Session Host) role service installed is now called an RD Session Host server, instead of a terminal server.</span></span><br/>
<ul>
<li><span data-ttu-id="0ec87-108"><a href="terminal-services-is-now-remote-desktop-services.md">Servizi terminal è ora Servizi Desktop remoto</a></span><span class="sxs-lookup"><span data-stu-id="0ec87-108"><a href="terminal-services-is-now-remote-desktop-services.md">Terminal Services Is Now Remote Desktop Services</a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0ec87-109">API di virtualizzazione Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="0ec87-109">Remote Desktop Virtualization API</span></span><br/></td>
<td><span data-ttu-id="0ec87-110">L'API di virtualizzazione Desktop remoto fornisce enumerazioni, interfacce e strutture che è possibile utilizzare per creare plug-in personalizzati che eseguono l'override della logica di reindirizzamento standard di Connessione Desktop remoto broker (gestore connessione Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="0ec87-110">The Remote Desktop Virtualization API provides enumerations, interfaces, and structures that you can use to create custom plug-ins that override the standard redirection logic of Remote Desktop Connection Broker (RD Connection Broker).</span></span> <span data-ttu-id="0ec87-111">Gestore connessione Desktop remoto (in precedenza noto come broker di sessione di servizi Terminal) è stato espanso per supportare le connessioni alle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="0ec87-111">RD Connection Broker (formerly known as TS Session Broker) was expanded to support connections to virtual machines.</span></span><br/>
<ul>
<li><span data-ttu-id="0ec87-112"><a href="using-the-remote-desktop-virtualization-api.md">Uso dell'API di virtualizzazione Desktop remoto</a></span><span class="sxs-lookup"><span data-stu-id="0ec87-112"><a href="using-the-remote-desktop-virtualization-api.md">Using the Remote Desktop Virtualization API</a></span></span></li>
<li><span data-ttu-id="0ec87-113"><a href="terminal-services-virtualization-api-reference.md">Informazioni di riferimento sulle API di virtualizzazione Desktop remoto</a></span><span class="sxs-lookup"><span data-stu-id="0ec87-113"><a href="terminal-services-virtualization-api-reference.md">Remote Desktop Virtualization API Reference</a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0ec87-114">Provider di Remote Desktop Protocol</span><span class="sxs-lookup"><span data-stu-id="0ec87-114">Remote Desktop Protocol Provider</span></span><br/></td>
<td><span data-ttu-id="0ec87-115">L'API del provider Remote Desktop Protocol può essere usata per creare un protocollo che Personalizza l'interazione tra il servizio Servizi Desktop remoto e i client desktop.</span><span class="sxs-lookup"><span data-stu-id="0ec87-115">The Remote Desktop Protocol Provider API can be used to create a protocol that customizes the interaction between the Remote Desktop Services service and desktop clients.</span></span><br/>
<ul>
<li><span data-ttu-id="0ec87-116"><a href="creating-a-custom-remote-protocol.md">Creazione di un provider di Remote Desktop Protocol</a></span><span class="sxs-lookup"><span data-stu-id="0ec87-116"><a href="creating-a-custom-remote-protocol.md">Creating a Remote Desktop Protocol Provider</a></span></span></li>
<li><span data-ttu-id="0ec87-117"><a href="custom-remote-protocol-reference.md">Riferimento al provider Remote Desktop Protocol</a></span><span class="sxs-lookup"><span data-stu-id="0ec87-117"><a href="custom-remote-protocol-reference.md">Remote Desktop Protocol Provider Reference</a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0ec87-118">API Servizi Desktop remoto AudioEndpoint</span><span class="sxs-lookup"><span data-stu-id="0ec87-118">Remote Desktop Services AudioEndpoint API</span></span><br/></td>
<td><span data-ttu-id="0ec87-119">L'API Servizi Desktop remoto AudioEndpoint supporta l'enumerazione, le interfacce e le strutture per la registrazione dell'endpoint audio e il trasporto di dati.</span><span class="sxs-lookup"><span data-stu-id="0ec87-119">The Remote Desktop Services AudioEndpoint API supports enumeration, interfaces, and structures for audio endpoint registration and data transport.</span></span><br/>
<ul>
<li><span data-ttu-id="0ec87-120"><a href="terminal-services-audioendpoint-api-reference.md">Informazioni di riferimento sull'API Servizi Desktop remoto AudioEndpoint</a></span><span class="sxs-lookup"><span data-stu-id="0ec87-120"><a href="terminal-services-audioendpoint-api-reference.md">Remote Desktop Services AudioEndpoint API Reference</a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0ec87-121">API del servizio Servizio di gestione Connessione RemoteApp e desktop</span><span class="sxs-lookup"><span data-stu-id="0ec87-121">RemoteApp and Desktop Connection Management Service API</span></span><br/></td>
<td><span data-ttu-id="0ec87-122">L'API del servizio Servizio di gestione Connessione RemoteApp e desktop supporta le interfacce e le strutture che è possibile usare per eseguire il filtro personalizzato delle risorse e fornire supporto per i tipi di file che non sono supportati in modo nativo in Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="0ec87-122">The RemoteApp and Desktop Connection Management Service API supports interfaces and structures that you can use to perform custom filtering of resources and provide support for file types that are not natively supported in Windows Server 2008 R2.</span></span><br/>
<ul>
<li><span data-ttu-id="0ec87-123"><a href="centralized-publishing-api-reference.md">Riferimento all'API del servizio Servizio di gestione Connessione RemoteApp e desktop</a></span><span class="sxs-lookup"><span data-stu-id="0ec87-123"><a href="centralized-publishing-api-reference.md">RemoteApp and Desktop Connection Management Service API Reference</a></span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

 

 





