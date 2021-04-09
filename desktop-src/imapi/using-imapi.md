---
title: Uso di IMAPi
description: Negli argomenti seguenti viene illustrato l'utilizzo dell'API per la creazione di immagini master.
ms.assetid: c42043db-612f-488f-a6ae-a8caea8ac42b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccd44d01e925d07d251e93a29c5268cc7e9c5076
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856949"
---
# <a name="using-imapi"></a><span data-ttu-id="0ca20-103">Uso di IMAPi</span><span class="sxs-lookup"><span data-stu-id="0ca20-103">Using IMAPI</span></span>

<span data-ttu-id="0ca20-104">Negli argomenti seguenti viene illustrato l'utilizzo dell'API per la creazione di immagini master.</span><span class="sxs-lookup"><span data-stu-id="0ca20-104">The following topics demonstrate the use of the image mastering API.</span></span>

## <a name="usage-scenarios"></a><span data-ttu-id="0ca20-105">Scenari di utilizzo</span><span class="sxs-lookup"><span data-stu-id="0ca20-105">Usage Scenarios</span></span>

<span data-ttu-id="0ca20-106">La documentazione seguente fornisce indicazioni dettagliate per gli scenari IMAP comuni.</span><span class="sxs-lookup"><span data-stu-id="0ca20-106">The following documentation provides detailed guidance for common IMAPI scenarios.</span></span>



| <span data-ttu-id="0ca20-107">Scenario</span><span class="sxs-lookup"><span data-stu-id="0ca20-107">Scenario</span></span>                                                                                                         | <span data-ttu-id="0ca20-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0ca20-108">Description</span></span>                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0ca20-109">Verifica del supporto delle unità</span><span class="sxs-lookup"><span data-stu-id="0ca20-109">Checking Drive Support</span></span>](checking-drive-support.md)                                                             | <span data-ttu-id="0ca20-110">Viene illustrato il rilevamento del supporto per un'unità multimediale.</span><span class="sxs-lookup"><span data-stu-id="0ca20-110">Demonstrates the detection of support for a media drive.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="0ca20-111">Verifica del supporto multimediale</span><span class="sxs-lookup"><span data-stu-id="0ca20-111">Checking Media Support</span></span>](checking-media-support.md)                                                             | <span data-ttu-id="0ca20-112">Viene illustrato il rilevamento del supporto per i supporti.</span><span class="sxs-lookup"><span data-stu-id="0ca20-112">Demonstrates the detection of support for media.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="0ca20-113">Masterizzazione di un'immagine del disco</span><span class="sxs-lookup"><span data-stu-id="0ca20-113">Burning a Disc Image</span></span>](burning-a-disc.md)                                                                       | <span data-ttu-id="0ca20-114">Viene illustrata la masterizzazione di un disco utilizzando IMAPi.</span><span class="sxs-lookup"><span data-stu-id="0ca20-114">Demonstrates mastering (burning a disc) using IMAPI.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="0ca20-115">Aggiunta di un'immagine di avvio</span><span class="sxs-lookup"><span data-stu-id="0ca20-115">Adding a Boot Image</span></span>](adding-a-boot-image.md)                                                                   | <span data-ttu-id="0ca20-116">Si basa sull'esempio di [masterizzazione di un'immagine del disco](burning-a-disc.md) aggiungendo codice per includere un'immagine di avvio nella sezione di avvio del disco.</span><span class="sxs-lookup"><span data-stu-id="0ca20-116">Builds on the [Burning a Disc Image](burning-a-disc.md) example by adding code to include a bootable image in the boot section of the disc.</span></span><br/>               |
| [<span data-ttu-id="0ca20-117">Creazione di un disco multisessione</span><span class="sxs-lookup"><span data-stu-id="0ca20-117">Creating a Multisession Disc</span></span>](creating-a-multisession-disc.md)                                                 | <span data-ttu-id="0ca20-118">Viene illustrata la creazione di un disco multisessione con IMAPi.</span><span class="sxs-lookup"><span data-stu-id="0ca20-118">Demonstrates the creation of a multisession disc using IMAPI.</span></span><br/>                                                                                              |
| [<span data-ttu-id="0ca20-119">Monitoraggio dello stato di avanzamento con gli eventi</span><span class="sxs-lookup"><span data-stu-id="0ca20-119">Monitoring Progress With Events</span></span>](monitoring-progress-with-events.md)                                           | <span data-ttu-id="0ca20-120">Viene illustrato l'utilizzo di interfacce specifiche per consentire l'implementazione di un gestore eventi in modo che sia possibile ricevere informazioni sullo stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="0ca20-120">Demonstrates the use of specific interfaces in order to allow the implementation of an event handler so that progress information may be received.</span></span> <br/>        |
| [<span data-ttu-id="0ca20-121">Prevenzione della disconnessione o della sospensione durante un'ustione</span><span class="sxs-lookup"><span data-stu-id="0ca20-121">Preventing Logoff or Suspend During a Burn</span></span>](preventing-logoff-or-suspend-during-a-burn.md)                     | <span data-ttu-id="0ca20-122">Contiene informazioni che descrivono in dettaglio le considerazioni relative allo sviluppo di applicazioni per quanto riguarda gli scenari che coinvolgono l'utente ' disconnessione ' è suspend ' in Windows.</span><span class="sxs-lookup"><span data-stu-id="0ca20-122">Contains information detailing application development considerations to be made in regards to scenarios involving user 'Logoff' and 'Suspend' in Windows.</span></span><br/> |
| [<span data-ttu-id="0ca20-123">Fornire le autorizzazioni utente per i dispositivi con masterizzazione multimediale</span><span class="sxs-lookup"><span data-stu-id="0ca20-123">Providing User Permissions for Media Burning Devices</span></span>](providing-user-permissions-for-media-burning-devices.md) | <span data-ttu-id="0ca20-124">Descrive il processo necessario per verificare che un utente disponga di autorizzazioni adeguate per l'utilizzo di dispositivi con masterizzazione multimediale in Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="0ca20-124">Details the process required to ensure a user has adequate permissions to utilize media burning devices on Windows XP and Windows Server 2003.</span></span><br/>             |



 

## <a name="application-compatibility"></a><span data-ttu-id="0ca20-125">Compatibilità delle applicazioni</span><span class="sxs-lookup"><span data-stu-id="0ca20-125">Application Compatibility</span></span>

<span data-ttu-id="0ca20-126">La documentazione seguente contiene informazioni importanti da tenere in considerazione durante lo sviluppo di un'applicazione che usa IMAPi.</span><span class="sxs-lookup"><span data-stu-id="0ca20-126">The following documentation contains important information to take consideration while developing an application that utilizes IMAPI.</span></span>



| <span data-ttu-id="0ca20-127">Informazioni aggiuntive</span><span class="sxs-lookup"><span data-stu-id="0ca20-127">Guidance</span></span>                                                   | <span data-ttu-id="0ca20-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0ca20-128">Description</span></span>                                                                                                                                                                                                                                                 |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0ca20-129">Layout multisessione IMAPi</span><span class="sxs-lookup"><span data-stu-id="0ca20-129">IMAPI Multisession Layout</span></span>](imapi-multisession-layout.md) | <span data-ttu-id="0ca20-130">Descrive il layout del disco usato da IMAPi per implementare la multisessione.</span><span class="sxs-lookup"><span data-stu-id="0ca20-130">Details the disc layout that IMAPI utilizes to implement multisession.</span></span> <span data-ttu-id="0ca20-131">Queste informazioni vengono utilizzate per garantire l'interoperabilità tra IMAPi e altri software di masterizzazione, oltre a consentire la creazione di immagini di dischi multisessione compatibili con IMAP.</span><span class="sxs-lookup"><span data-stu-id="0ca20-131">This information is used to ensure interoperability between IMAPI and other burning software, as well as allow the creation of IMAPI-compatible multisession disc images.</span></span><br/> |



 

 

 





