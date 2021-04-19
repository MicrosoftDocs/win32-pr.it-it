---
description: .
ms.assetid: 5ebc8c4c-acee-4658-8d36-30fbb17b1ef1
title: Rimozione dei servizi UDDI dal sistema operativo server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7681167177b850ba44ac0fc26e019c7393008b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317618"
---
# <a name="removal-of-uddi-services-from-server-operating-system"></a><span data-ttu-id="466e0-103">Rimozione dei servizi UDDI dal sistema operativo server</span><span class="sxs-lookup"><span data-stu-id="466e0-103">Removal of UDDI Services from Server Operating System</span></span>

## <a name="affected-platform"></a><span data-ttu-id="466e0-104">Piattaforma interessata</span><span class="sxs-lookup"><span data-stu-id="466e0-104">Affected Platform</span></span>

<span data-ttu-id="466e0-105">**Server** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="466e0-105">**Servers** - Windows Server 2008 R2</span></span>  



## <a name="feature-impact"></a><span data-ttu-id="466e0-106">Effetto sulle funzionalità</span><span class="sxs-lookup"><span data-stu-id="466e0-106">Feature Impact</span></span>

<span data-ttu-id="466e0-107">**Gravità** -medio</span><span class="sxs-lookup"><span data-stu-id="466e0-107">**Severity** - Medium</span></span>  
<span data-ttu-id="466e0-108">**Frequenza** -bassa</span><span class="sxs-lookup"><span data-stu-id="466e0-108">**Frequency** - Low</span></span>  

## <a name="description"></a><span data-ttu-id="466e0-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="466e0-109">Description</span></span>

<span data-ttu-id="466e0-110">Microsoft ha rimosso il ruolo del server Servizi UDDI (Universal Description, Discovery, and Integration) da Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="466e0-110">Microsoft has removed the UDDI (Universal Description, Discovery, and Integration) Services server role from Windows Server 2008 R2.</span></span> <span data-ttu-id="466e0-111">Le versioni future dei servizi UDDI faranno parte del prodotto Microsoft BizTalk.</span><span class="sxs-lookup"><span data-stu-id="466e0-111">Future releases of UDDI Services will be part of the Microsoft BizTalk product.</span></span> <span data-ttu-id="466e0-112">Il riallineamento e il consolidamento del prodotto consentono a Microsoft di gestire al meglio il mercato SOA (Service-Oriented Architecture).</span><span class="sxs-lookup"><span data-stu-id="466e0-112">This product realignment and consolidation positions Microsoft to better serve the services-oriented architecture (SOA) market.</span></span>

<span data-ttu-id="466e0-113">La prima versione Post-Windows Server 2008 dei servizi UDDI sarà conforme agli standard UDDI v 3.0.</span><span class="sxs-lookup"><span data-stu-id="466e0-113">The first post-Windows Server 2008 release of UDDI Services will be UDDI v3.0 standards compliant.</span></span> <span data-ttu-id="466e0-114">Verrà fornito come parte della versione di BizTalk Server 2009.</span><span class="sxs-lookup"><span data-stu-id="466e0-114">It will ship as part of the BizTalk Server 2009 release.</span></span> <span data-ttu-id="466e0-115">Per soddisfare il nostro impegno a offrire un'esperienza utente soddisfacente, offriamo un pacchetto di installazione di servizi UDDI V3 per Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="466e0-115">To meet our commitment to provide a satisfactory user experience, we will offer a UDDI Services v3 installation package for Windows Server 2008 R2.</span></span>

## <a name="manifestation"></a><span data-ttu-id="466e0-116">Manifestazione</span><span class="sxs-lookup"><span data-stu-id="466e0-116">Manifestation</span></span>

<span data-ttu-id="466e0-117">La presenza di versioni precedenti dei componenti dei servizi UDDI nel sistema blocca l'aggiornamento a Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="466e0-117">The presence of previous versions of UDDI Services components on the system blocks an upgrade to Windows Server 2008 R2.</span></span>

## <a name="mitigation-of-impact"></a><span data-ttu-id="466e0-118">Attenuazione dell'effetto</span><span class="sxs-lookup"><span data-stu-id="466e0-118">Mitigation of Impact</span></span>

<span data-ttu-id="466e0-119">Gli utenti che hanno distribuito un sito di servizi UDDI da Windows Server 2003 o Windows Server 2008 possono scegliere di non aggiornare i server che eseguono i servizi UDDI a Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="466e0-119">Users who have deployed a UDDI Services site from Windows Server 2003 or Windows Server 2008 can choose not to upgrade the servers running the UDDI Services to Windows Server 2008 R2.</span></span> <span data-ttu-id="466e0-120">Possono inoltre spostare i servizi UDDI in caselle dedicate di Windows Server 2003 o Windows Server 2008 se è necessario aggiornare le caselle attuali dei servizi UDDI.</span><span class="sxs-lookup"><span data-stu-id="466e0-120">They can also move the UDDI Services to dedicated Windows Server 2003 or Windows Server 2008 boxes if they have to upgrade the current UDDI Services boxes.</span></span>

## <a name="solution"></a><span data-ttu-id="466e0-121">Soluzione</span><span class="sxs-lookup"><span data-stu-id="466e0-121">Solution</span></span>

<span data-ttu-id="466e0-122">La soluzione consigliata consiste nel distribuire i servizi UDDI v 3.0 da BizTalk Server 2009 in un computer Windows Server 2008 R2 e quindi eseguire la migrazione del sito precedente al nuovo sito.</span><span class="sxs-lookup"><span data-stu-id="466e0-122">The recommended solution is to deploy UDDI Services v3.0 from BizTalk Server 2009 onto a Windows Server 2008 R2 machine, and then to migrate the old site to the new site.</span></span> <span data-ttu-id="466e0-123">UDDI Services v 3.0 fornisce la compatibilità con le versioni precedenti dei servizi UDDI 2,0, pertanto tutte le applicazioni che utilizzano servizi UDDI non saranno interessate.</span><span class="sxs-lookup"><span data-stu-id="466e0-123">UDDI Services v3.0 provides backward compatibility with UDDI Services 2.0, so any applications that are using UDDI Services will be unaffected.</span></span>

<span data-ttu-id="466e0-124">A questo scopo, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="466e0-124">To do this, follow these steps:</span></span>

1.  <span data-ttu-id="466e0-125">Configurare un nuovo sito dei servizi UDDI v 3.0 in un computer già caricato con Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="466e0-125">Set up a new UDDI Services v3.0 site on a machine already loaded with Windows Server 2008 R2.</span></span> <span data-ttu-id="466e0-126">Nota: in una configurazione distribuita, un sito UDDI v 3.0 può essere costituito da più di un computer Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="466e0-126">(Note: In a distributed setup, a UDDI v3.0 site can consist of more than one Windows Server 2008 R2 machines.)</span></span>
2.  <span data-ttu-id="466e0-127">Utilizzare l'utilità di migrazione dati UDDI per eseguire la migrazione dei dati dal database dei servizi UDDI precedente al nuovo database.</span><span class="sxs-lookup"><span data-stu-id="466e0-127">Use the UDDI data migration tool to migrate the data from the old UDDI Services database to the new database.</span></span>
3.  <span data-ttu-id="466e0-128">Eseguire il backup del database dei servizi UDDI precedente per garantire la funzionalità di rollback.</span><span class="sxs-lookup"><span data-stu-id="466e0-128">Back up the old UDDI Services database to ensure rollback capability.</span></span>
4.  <span data-ttu-id="466e0-129">Disinstallare il software dei servizi UDDI precedente, quindi aggiornare le caselle a Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="466e0-129">Uninstall the old UDDI Services software and then upgrade those boxes to Windows Server 2008 R2.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="466e0-130">Collegamenti ad altre risorse</span><span class="sxs-lookup"><span data-stu-id="466e0-130">Links to Other Resources</span></span>

-   [<span data-ttu-id="466e0-131">Sito Web dei servizi UDDI Microsoft</span><span class="sxs-lookup"><span data-stu-id="466e0-131">Microsoft UDDI Services website</span></span>](https://msdn.microsoft.com/biztalk/dd789428.aspx)
-   [<span data-ttu-id="466e0-132">Specifiche UDDI</span><span class="sxs-lookup"><span data-stu-id="466e0-132">UDDI specifications</span></span>](http://uddi.xml.org/specification)
-   [<span data-ttu-id="466e0-133">Download di servizi UDDI v 3.0 per Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="466e0-133">UDDI Services v3.0 download for Windows Server 2008 R2</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=e4761835-70f0-4e8d-96c5-64818d54e06e)

 

 



