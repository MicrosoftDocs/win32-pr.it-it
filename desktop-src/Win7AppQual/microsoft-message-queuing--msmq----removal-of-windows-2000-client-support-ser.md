---
description: .
ms.assetid: e29b477e-f7e9-413c-8eb9-2e764b7dd910
title: Microsoft Message Queuing (MSMQ)-rimozione del servizio di supporto client di Windows 2000
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54688ee4ad24eb691c95e4d70ce0acb881e212eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058058"
---
# <a name="microsoft-message-queuing-msmq---removal-of-windows-2000-client-support-service"></a><span data-ttu-id="047d2-103">Microsoft Message Queuing (MSMQ)-rimozione del servizio di supporto client di Windows 2000</span><span class="sxs-lookup"><span data-stu-id="047d2-103">Microsoft Message Queuing (MSMQ) - Removal of Windows 2000 Client Support Service</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="047d2-104">Piattaforme interessate</span><span class="sxs-lookup"><span data-stu-id="047d2-104">Affected Platforms</span></span>

<span data-ttu-id="047d2-105">**Server** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="047d2-105">**Servers** - Windows Server 2008 R2</span></span>  



## <a name="feature-impact"></a><span data-ttu-id="047d2-106">Effetto sulle funzionalità</span><span class="sxs-lookup"><span data-stu-id="047d2-106">Feature Impact</span></span>

 <span data-ttu-id="047d2-107">**Gravità** -alta</span><span class="sxs-lookup"><span data-stu-id="047d2-107">**Severity** - High</span></span>  
<span data-ttu-id="047d2-108">**Frequenza** -bassa</span><span class="sxs-lookup"><span data-stu-id="047d2-108">**Frequency** - Low</span></span>  

## <a name="description"></a><span data-ttu-id="047d2-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="047d2-109">Description</span></span>

<span data-ttu-id="047d2-110">Il servizio di supporto client di Windows 2000 è un componente facoltativo del server di Accodamento messaggi che è possibile installare in un computer con controller di dominio Windows 2003 o Windows 2008.</span><span class="sxs-lookup"><span data-stu-id="047d2-110">The Windows 2000 Client Support Service is an optional component of the Message Queuing Server that you can install on a Windows 2003 or Windows 2008 domain controller machine.</span></span> <span data-ttu-id="047d2-111">Questo servizio consente ai client Windows 2000 di operare in una modalità integrata del dominio con qualsiasi server di Accodamento messaggi installato nei computer Windows 2003/2008.</span><span class="sxs-lookup"><span data-stu-id="047d2-111">This service allows Windows 2000 clients to operate in a domain-integrated mode with any Message Queuing server installed on Windows 2003/2008 machines.</span></span> <span data-ttu-id="047d2-112">I client MSMQ che operano su Windows XP verso l'alto non necessitano di questo servizio.</span><span class="sxs-lookup"><span data-stu-id="047d2-112">MSMQ Clients operating on Windows XP upwards do not need this service.</span></span>

### <a name="manifestation-of-impact"></a><span data-ttu-id="047d2-113">Manifesto di effetto</span><span class="sxs-lookup"><span data-stu-id="047d2-113">Manifestation of Impact</span></span>

<span data-ttu-id="047d2-114">Questa modifica ha effetto su Windows 2000 quando si interopera in un dominio di Windows 7 in cui tutti i controller di dominio sono Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="047d2-114">This change impacts Windows 2000 when interoperating in a Windows 7 domain where all domain controllers are Windows Server 2008 R2.</span></span> <span data-ttu-id="047d2-115">Se un cliente si aggiorna al dominio di Windows 7, le applicazioni MSMQ esistenti in qualsiasi computer Windows 2000 nel dominio non saranno in grado di funzionare in una modalità integrata a livello di dominio, a meno che questi client non eseguano l'aggiornamento a una versione di Windows più recente.</span><span class="sxs-lookup"><span data-stu-id="047d2-115">If a customer upgrades to the Windows 7 domain, the existing MSMQ applications on any Windows 2000 machines in the domain will not be able to operate in a domain-integrated mode unless these clients upgrade to a higher Windows version.</span></span>

### <a name="mitigation"></a><span data-ttu-id="047d2-116">Strategia di riduzione del rischio</span><span class="sxs-lookup"><span data-stu-id="047d2-116">Mitigation</span></span>

<span data-ttu-id="047d2-117">Gli utenti che dispongono di computer client Windows 2000 in un dominio Windows 7 possono configurare un controller di dominio Windows 2003/2008 nel dominio e installare il servizio di supporto client Windows 2000 MSMQ in questo controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="047d2-117">Users who have Windows 2000 Client machines on a Windows 7 domain can configure a Windows 2003/2008 domain controller in the domain and install the MSMQ Windows 2000 Client Support Service on this domain controller.</span></span>

### <a name="leveraging-feature-capabilities"></a><span data-ttu-id="047d2-118">Sfruttando le funzionalità</span><span class="sxs-lookup"><span data-stu-id="047d2-118">Leveraging Feature Capabilities</span></span>

<span data-ttu-id="047d2-119">Gli utenti con computer client Windows 2000 che eseguono MSMQ dovranno eseguire l'aggiornamento a una versione di Windows superiore per sfruttare i vantaggi dell'implementazione basata su Active Directory del server MSMQ.</span><span class="sxs-lookup"><span data-stu-id="047d2-119">Users who have Windows 2000 Client machines running MSMQ should upgrade to a higher Windows version in order to take advantage of the Active Directory-based implementation of the MSMQ Server.</span></span>

### <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="047d2-120">Compatibilità, prestazioni, affidabilità e test di usabilità</span><span class="sxs-lookup"><span data-stu-id="047d2-120">Compatibility, Performance, Reliability, and Usability Testing</span></span>

<span data-ttu-id="047d2-121">Gli utenti con computer client Windows 2000 che eseguono MSMQ in un dominio Windows 7 con uno o più controller di dominio di livello inferiore devono verificare che le applicazioni siano funzionali in questo dominio misto.</span><span class="sxs-lookup"><span data-stu-id="047d2-121">Users who have Windows 2000 Client machines running MSMQ on a Windows 7 domain with one or more down-level domain controllers should verify that their applications are functional on this mixed domain.</span></span>

 

 



