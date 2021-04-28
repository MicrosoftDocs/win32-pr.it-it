---
description: Rimozione di Servizi UDDI dal sistema operativo del server
ms.assetid: 5ebc8c4c-acee-4658-8d36-30fbb17b1ef1
title: Rimozione di Servizi UDDI dal sistema operativo del server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 960a4063d990a3b2cdac45cd933a1e7dfef41f88
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116329"
---
# <a name="removal-of-uddi-services-from-server-operating-system"></a><span data-ttu-id="068c4-103">Rimozione di Servizi UDDI dal sistema operativo del server</span><span class="sxs-lookup"><span data-stu-id="068c4-103">Removal of UDDI Services from Server Operating System</span></span>

## <a name="affected-platform"></a><span data-ttu-id="068c4-104">Piattaforma interessata</span><span class="sxs-lookup"><span data-stu-id="068c4-104">Affected Platform</span></span>

<span data-ttu-id="068c4-105">**Server** - Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="068c4-105">**Servers** - Windows Server 2008 R2</span></span>  



## <a name="feature-impact"></a><span data-ttu-id="068c4-106">Impatto sulle funzionalità</span><span class="sxs-lookup"><span data-stu-id="068c4-106">Feature Impact</span></span>

<span data-ttu-id="068c4-107">**Gravità** - Media</span><span class="sxs-lookup"><span data-stu-id="068c4-107">**Severity** - Medium</span></span>  
<span data-ttu-id="068c4-108">**Frequenza** - Bassa</span><span class="sxs-lookup"><span data-stu-id="068c4-108">**Frequency** - Low</span></span>  

## <a name="description"></a><span data-ttu-id="068c4-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="068c4-109">Description</span></span>

<span data-ttu-id="068c4-110">Microsoft ha rimosso il ruolo del server Servizi UDDI (Universal Description, Discovery, and Integration) da Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="068c4-110">Microsoft has removed the UDDI (Universal Description, Discovery, and Integration) Services server role from Windows Server 2008 R2.</span></span> <span data-ttu-id="068c4-111">Le versioni future di Servizi UDDI saranno parte del prodotto Microsoft BizTalk.</span><span class="sxs-lookup"><span data-stu-id="068c4-111">Future releases of UDDI Services will be part of the Microsoft BizTalk product.</span></span> <span data-ttu-id="068c4-112">Questo riallineamento e consolidamento del prodotto posiziona Microsoft per gestire meglio il mercato dell'architettura orientata ai servizi (SOA).</span><span class="sxs-lookup"><span data-stu-id="068c4-112">This product realignment and consolidation positions Microsoft to better serve the services-oriented architecture (SOA) market.</span></span>

<span data-ttu-id="068c4-113">La prima versione successiva a Windows Server 2008 di Servizi UDDI sarà conforme agli standard UDDI v3.0.</span><span class="sxs-lookup"><span data-stu-id="068c4-113">The first post-Windows Server 2008 release of UDDI Services will be UDDI v3.0 standards compliant.</span></span> <span data-ttu-id="068c4-114">Verrà rilasciato come parte della versione BizTalk Server 2009.</span><span class="sxs-lookup"><span data-stu-id="068c4-114">It will ship as part of the BizTalk Server 2009 release.</span></span> <span data-ttu-id="068c4-115">Per soddisfare il nostro impegno a offrire un'esperienza utente soddisfacente, verrà offerto un pacchetto di installazione di Servizi UDDI v3 per Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="068c4-115">To meet our commitment to provide a satisfactory user experience, we will offer a UDDI Services v3 installation package for Windows Server 2008 R2.</span></span>

## <a name="manifestation"></a><span data-ttu-id="068c4-116">Manifestazione</span><span class="sxs-lookup"><span data-stu-id="068c4-116">Manifestation</span></span>

<span data-ttu-id="068c4-117">La presenza di versioni precedenti dei componenti di Servizi UDDI nel sistema blocca un aggiornamento a Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="068c4-117">The presence of previous versions of UDDI Services components on the system blocks an upgrade to Windows Server 2008 R2.</span></span>

## <a name="mitigation-of-impact"></a><span data-ttu-id="068c4-118">Mitigazione dell'impatto</span><span class="sxs-lookup"><span data-stu-id="068c4-118">Mitigation of Impact</span></span>

<span data-ttu-id="068c4-119">Gli utenti che hanno distribuito un sito di Servizi UDDI da Windows Server 2003 o Windows Server 2008 possono scegliere di non aggiornare i server che eseguono i servizi UDDI a Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="068c4-119">Users who have deployed a UDDI Services site from Windows Server 2003 or Windows Server 2008 can choose not to upgrade the servers running the UDDI Services to Windows Server 2008 R2.</span></span> <span data-ttu-id="068c4-120">Possono anche spostare i servizi UDDI in caselle dedicate di Windows Server 2003 o Windows Server 2008 se è necessario aggiornare le caselle di Servizi UDDI correnti.</span><span class="sxs-lookup"><span data-stu-id="068c4-120">They can also move the UDDI Services to dedicated Windows Server 2003 or Windows Server 2008 boxes if they have to upgrade the current UDDI Services boxes.</span></span>

## <a name="solution"></a><span data-ttu-id="068c4-121">Soluzione</span><span class="sxs-lookup"><span data-stu-id="068c4-121">Solution</span></span>

<span data-ttu-id="068c4-122">La soluzione consigliata consiste nel distribuire Servizi UDDI v3.0 da BizTalk Server 2009 in un computer Windows Server 2008 R2 e quindi eseguire la migrazione del sito precedente al nuovo sito.</span><span class="sxs-lookup"><span data-stu-id="068c4-122">The recommended solution is to deploy UDDI Services v3.0 from BizTalk Server 2009 onto a Windows Server 2008 R2 machine, and then to migrate the old site to the new site.</span></span> <span data-ttu-id="068c4-123">Servizi UDDI v3.0 garantisce la compatibilità con le versioni precedenti di Servizi UDDI 2.0, pertanto tutte le applicazioni che usano Servizi UDDI non saranno interessate.</span><span class="sxs-lookup"><span data-stu-id="068c4-123">UDDI Services v3.0 provides backward compatibility with UDDI Services 2.0, so any applications that are using UDDI Services will be unaffected.</span></span>

<span data-ttu-id="068c4-124">A questo scopo, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="068c4-124">To do this, follow these steps:</span></span>

1.  <span data-ttu-id="068c4-125">Configurare un nuovo sito di Servizi UDDI v3.0 in un computer già caricato con Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="068c4-125">Set up a new UDDI Services v3.0 site on a machine already loaded with Windows Server 2008 R2.</span></span> <span data-ttu-id="068c4-126">Nota: in un'installazione distribuita un sito UDDI v3.0 può essere costituito da più computer Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="068c4-126">(Note: In a distributed setup, a UDDI v3.0 site can consist of more than one Windows Server 2008 R2 machines.)</span></span>
2.  <span data-ttu-id="068c4-127">Usare lo strumento di migrazione dei dati UDDI per eseguire la migrazione dei dati dal database di Servizi UDDI precedente al nuovo database.</span><span class="sxs-lookup"><span data-stu-id="068c4-127">Use the UDDI data migration tool to migrate the data from the old UDDI Services database to the new database.</span></span>
3.  <span data-ttu-id="068c4-128">Eseguire il backup del database di Servizi UDDI precedente per garantire la funzionalità di rollback.</span><span class="sxs-lookup"><span data-stu-id="068c4-128">Back up the old UDDI Services database to ensure rollback capability.</span></span>
4.  <span data-ttu-id="068c4-129">Disinstallare il software di Servizi UDDI precedente e quindi aggiornare tali caselle a Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="068c4-129">Uninstall the old UDDI Services software and then upgrade those boxes to Windows Server 2008 R2.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="068c4-130">Collegamenti ad altre risorse</span><span class="sxs-lookup"><span data-stu-id="068c4-130">Links to Other Resources</span></span>

-   [<span data-ttu-id="068c4-131">Sito Web di Servizi UDDI Microsoft</span><span class="sxs-lookup"><span data-stu-id="068c4-131">Microsoft UDDI Services website</span></span>](https://msdn.microsoft.com/biztalk/dd789428.aspx)
-   [<span data-ttu-id="068c4-132">Specifiche UDDI</span><span class="sxs-lookup"><span data-stu-id="068c4-132">UDDI specifications</span></span>](http://uddi.xml.org/specification)
-   [<span data-ttu-id="068c4-133">Download di Servizi UDDI v3.0 per Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="068c4-133">UDDI Services v3.0 download for Windows Server 2008 R2</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=e4761835-70f0-4e8d-96c5-64818d54e06e)

 

 



