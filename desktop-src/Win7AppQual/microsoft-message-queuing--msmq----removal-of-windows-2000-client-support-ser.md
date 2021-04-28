---
description: Microsoft Message Queuing (MSMQ) - Rimozione del servizio di supporto client Windows 2000
ms.assetid: e29b477e-f7e9-413c-8eb9-2e764b7dd910
title: Microsoft Message Queuing (MSMQ) - Rimozione del servizio di supporto client Windows 2000
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4be68d40271153567bdaf6b04d73218aaf3d3977
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088149"
---
# <a name="microsoft-message-queuing-msmq---removal-of-windows-2000-client-support-service"></a><span data-ttu-id="769de-103">Microsoft Message Queuing (MSMQ) - Rimozione del servizio di supporto client Windows 2000</span><span class="sxs-lookup"><span data-stu-id="769de-103">Microsoft Message Queuing (MSMQ) - Removal of Windows 2000 Client Support Service</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="769de-104">Piattaforme interessate</span><span class="sxs-lookup"><span data-stu-id="769de-104">Affected Platforms</span></span>

<span data-ttu-id="769de-105">**Server** - Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="769de-105">**Servers** - Windows Server 2008 R2</span></span>  



## <a name="feature-impact"></a><span data-ttu-id="769de-106">Impatto sulle funzionalità</span><span class="sxs-lookup"><span data-stu-id="769de-106">Feature Impact</span></span>

 <span data-ttu-id="769de-107">**Gravità** - Alta</span><span class="sxs-lookup"><span data-stu-id="769de-107">**Severity** - High</span></span>  
<span data-ttu-id="769de-108">**Frequenza** - Bassa</span><span class="sxs-lookup"><span data-stu-id="769de-108">**Frequency** - Low</span></span>  

## <a name="description"></a><span data-ttu-id="769de-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="769de-109">Description</span></span>

<span data-ttu-id="769de-110">Il servizio di supporto client Windows 2000 è un componente facoltativo del server di Accodamento messaggi che è possibile installare in un computer controller di dominio Windows 2003 o Windows 2008.</span><span class="sxs-lookup"><span data-stu-id="769de-110">The Windows 2000 Client Support Service is an optional component of the Message Queuing Server that you can install on a Windows 2003 or Windows 2008 domain controller machine.</span></span> <span data-ttu-id="769de-111">Questo servizio consente ai client Windows 2000 di operare in modalità integrata di dominio con qualsiasi server di Accodamento messaggi installato nei computer Windows 2003/2008.</span><span class="sxs-lookup"><span data-stu-id="769de-111">This service allows Windows 2000 clients to operate in a domain-integrated mode with any Message Queuing server installed on Windows 2003/2008 machines.</span></span> <span data-ttu-id="769de-112">I client MSMQ che operano in Windows XP verso l'alto non necessitano di questo servizio.</span><span class="sxs-lookup"><span data-stu-id="769de-112">MSMQ Clients operating on Windows XP upwards do not need this service.</span></span>

### <a name="manifestation-of-impact"></a><span data-ttu-id="769de-113">Manifestazione di impatto</span><span class="sxs-lookup"><span data-stu-id="769de-113">Manifestation of Impact</span></span>

<span data-ttu-id="769de-114">Questa modifica influisce su Windows 2000 durante l'interoperabilità in un dominio di Windows 7 in cui tutti i controller di dominio sono Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="769de-114">This change impacts Windows 2000 when interoperating in a Windows 7 domain where all domain controllers are Windows Server 2008 R2.</span></span> <span data-ttu-id="769de-115">Se un cliente esegue l'aggiornamento al dominio Windows 7, le applicazioni MSMQ esistenti in qualsiasi computer Windows 2000 nel dominio non potranno operare in modalità integrata di dominio a meno che questi client non esercitino l'aggiornamento a una versione di Windows superiore.</span><span class="sxs-lookup"><span data-stu-id="769de-115">If a customer upgrades to the Windows 7 domain, the existing MSMQ applications on any Windows 2000 machines in the domain will not be able to operate in a domain-integrated mode unless these clients upgrade to a higher Windows version.</span></span>

### <a name="mitigation"></a><span data-ttu-id="769de-116">Mitigazione</span><span class="sxs-lookup"><span data-stu-id="769de-116">Mitigation</span></span>

<span data-ttu-id="769de-117">Gli utenti che dispongono di computer client Windows 2000 in un dominio Windows 7 possono configurare un controller di dominio Windows 2003/2008 nel dominio e installare il servizio di supporto client MSMQ Windows 2000 in questo controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="769de-117">Users who have Windows 2000 Client machines on a Windows 7 domain can configure a Windows 2003/2008 domain controller in the domain and install the MSMQ Windows 2000 Client Support Service on this domain controller.</span></span>

### <a name="leveraging-feature-capabilities"></a><span data-ttu-id="769de-118">Sfruttare le funzionalità delle funzionalità</span><span class="sxs-lookup"><span data-stu-id="769de-118">Leveraging Feature Capabilities</span></span>

<span data-ttu-id="769de-119">Gli utenti che dispongono di computer client Windows 2000 che eseguono MSMQ devono eseguire l'aggiornamento a una versione di Windows superiore per sfruttare l'implementazione basata su Active Directory del server MSMQ.</span><span class="sxs-lookup"><span data-stu-id="769de-119">Users who have Windows 2000 Client machines running MSMQ should upgrade to a higher Windows version in order to take advantage of the Active Directory-based implementation of the MSMQ Server.</span></span>

### <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="769de-120">Test di compatibilità, prestazioni, affidabilità e usabilità</span><span class="sxs-lookup"><span data-stu-id="769de-120">Compatibility, Performance, Reliability, and Usability Testing</span></span>

<span data-ttu-id="769de-121">Gli utenti che dispongono di computer client Windows 2000 che eseguono MSMQ in un dominio Windows 7 con uno o più controller di dominio di livello inferiore devono verificare che le applicazioni funzionino in questo dominio misto.</span><span class="sxs-lookup"><span data-stu-id="769de-121">Users who have Windows 2000 Client machines running MSMQ on a Windows 7 domain with one or more down-level domain controllers should verify that their applications are functional on this mixed domain.</span></span>

 

 



