---
description: I controlli TAPI 3 Rendezvous forniscono i meccanismi per annunciare e individuare le conferenze dell'IP multimediale a più parti. Di seguito viene descritto un set di componenti e interfacce di Component Object Model (COM) per implementare la conferenza.
ms.assetid: 0ca2edac-b507-497e-9e63-78a10466e2eb
title: Informazioni sulle conferenze telefoniche IP Rendezvous
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4bd06fb848088a42e34bd7b176358a7507e3d2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104558982"
---
# <a name="about-rendezvous-ip-telephony-conferencing"></a><span data-ttu-id="58dc6-104">Informazioni sulle conferenze telefoniche IP Rendezvous</span><span class="sxs-lookup"><span data-stu-id="58dc6-104">About Rendezvous IP Telephony Conferencing</span></span>

<span data-ttu-id="58dc6-105">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="58dc6-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="58dc6-106">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="58dc6-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="58dc6-107">I controlli TAPI 3 Rendezvous forniscono i meccanismi per annunciare e individuare le conferenze dell'IP multimediale a più parti.</span><span class="sxs-lookup"><span data-stu-id="58dc6-107">The TAPI 3 Rendezvous controls provide mechanisms to advertise and discover multiparty multimedia IP conferences.</span></span> <span data-ttu-id="58dc6-108">Di seguito viene descritto un set di componenti e interfacce di Component Object Model (COM) per implementare la conferenza.</span><span class="sxs-lookup"><span data-stu-id="58dc6-108">The following describes a set of Component Object Model (COM) components and interfaces to implement conferencing.</span></span>

<span data-ttu-id="58dc6-109">COM è il modello di codifica di base per TAPI 3 e la loro familiarità si presuppone in questo documento.</span><span class="sxs-lookup"><span data-stu-id="58dc6-109">COM is the basic coding model for TAPI 3, and familiarity with it is assumed throughout this document.</span></span> <span data-ttu-id="58dc6-110">Per informazioni su COM, cercare Platform Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="58dc6-110">For information on COM, search the Platform Software Development Kit (SDK).</span></span>

## <a name="features"></a><span data-ttu-id="58dc6-111">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="58dc6-111">Features</span></span>

-   <span data-ttu-id="58dc6-112">Fornisce l'astrazione di una directory di conferenza per la modifica degli annunci di conferenze multimediali</span><span class="sxs-lookup"><span data-stu-id="58dc6-112">Provides the abstraction of a conference directory for manipulating announcements of multimedia conferences</span></span>
-   <span data-ttu-id="58dc6-113">Fornisce sicurezza tramite autenticazione, crittografia e un livello di controllo di accesso (ACL) per annuncio</span><span class="sxs-lookup"><span data-stu-id="58dc6-113">Provides security through authentication, encryption, and a per-announcement access control layer (ACL)</span></span>
-   <span data-ttu-id="58dc6-114">Fornisce uno schema comune per un annuncio della conferenza, abilitando le ricerche in base ai valori di attributo</span><span class="sxs-lookup"><span data-stu-id="58dc6-114">Provides a common schema for a conference announcement, enabling searches by attribute values</span></span>
-   <span data-ttu-id="58dc6-115">Consente le estensioni tramite un attributo gestito dal provider (BLOB della conferenza) nello schema</span><span class="sxs-lookup"><span data-stu-id="58dc6-115">Allows extensions through a provider-maintained attribute (conference blob) in the schema</span></span>
-   <span data-ttu-id="58dc6-116">Fornisce un wrapper COM per l'API di allocazione di indirizzi multicast (MADCAP)</span><span class="sxs-lookup"><span data-stu-id="58dc6-116">Provides a COM wrapper for the multicast address allocation (MADCAP) API</span></span>

## <a name="architecture"></a><span data-ttu-id="58dc6-117">Architettura</span><span class="sxs-lookup"><span data-stu-id="58dc6-117">Architecture</span></span>

<span data-ttu-id="58dc6-118">Le descrizioni e i diagrammi seguenti illustrano gli aspetti chiave dell'architettura del sistema.</span><span class="sxs-lookup"><span data-stu-id="58dc6-118">The following descriptions and diagram illustrate key aspects of the system architecture.</span></span>

-   <span data-ttu-id="58dc6-119">Il client può modificare le conferenze archiviate in una directory dinamica ILS o nel server NTDS usando i controlli Rendezvous.</span><span class="sxs-lookup"><span data-stu-id="58dc6-119">The client can manipulate conferences stored on an ILS dynamic directory or NTDS server using Rendezvous controls.</span></span> <span data-ttu-id="58dc6-120">Il protocollo LDAP (Lightweight Directory Access Protocol) viene utilizzato per comunicare con un server ILS.</span><span class="sxs-lookup"><span data-stu-id="58dc6-120">The Lightweight Directory Access Protocol (LDAP) is used to communicate with an ILS server.</span></span>
-   <span data-ttu-id="58dc6-121">I controlli Rendezvous forniscono interfacce COM doppie per lo script e la programmazione.</span><span class="sxs-lookup"><span data-stu-id="58dc6-121">The Rendezvous controls provide dual COM interfaces for scripting and programming.</span></span>
-   <span data-ttu-id="58dc6-122">Un server SAP (Session annuncio Protocol) con accesso diretto a Internet è in ascolto degli annunci di conferenze su Internet e popola i server dinamici ILS con le informazioni sulla conferenza.</span><span class="sxs-lookup"><span data-stu-id="58dc6-122">A Session Announcement Protocol (SAP) server with direct access to the Internet listens to conference announcements on the Internet and populates ILS dynamic servers with the conference information.</span></span> <span data-ttu-id="58dc6-123">Analogamente, annuncia anche le conferenze create localmente il cui ambito include Internet.</span><span class="sxs-lookup"><span data-stu-id="58dc6-123">Similarly, it also announces the locally created conferences whose scope includes the Internet.</span></span> <span data-ttu-id="58dc6-124">Il server SAP non è pianificato per Microsoft Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="58dc6-124">(The SAP server is not planned for Microsoft Windows 2000.)</span></span>

![architettura del sistema Rendezvous](images/rend1.png)

 

 



