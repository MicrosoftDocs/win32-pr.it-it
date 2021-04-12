---
description: Le operazioni di backup e ripristino VSS utilizzano ogni protocollo per l'interazione dei sistemi che utilizzano l'archiviazione di massa (writer) e quelli che eseguono il backup (richiedenti).
ms.assetid: c4dae5ce-0dfa-46ec-909f-8ae79d50a9cb
title: Uso della Servizio Copia Shadow del volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06a1c81d79de30085f783feb02b7a7d47d5dc765
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526304"
---
# <a name="using-the-volume-shadow-copy-service"></a><span data-ttu-id="e302f-103">Uso della Servizio Copia Shadow del volume</span><span class="sxs-lookup"><span data-stu-id="e302f-103">Using the Volume Shadow Copy Service</span></span>

<span data-ttu-id="e302f-104">Le operazioni di backup e ripristino VSS utilizzano ogni protocollo per l'interazione dei sistemi che utilizzano l'archiviazione di massa (writer) e quelli che eseguono il backup (richiedenti).</span><span class="sxs-lookup"><span data-stu-id="e302f-104">VSS backup and restore operations each use a protocol for the interaction of the systems that use mass storage (writers) and those that back it up (requesters).</span></span>

<span data-ttu-id="e302f-105">Le operazioni di backup e ripristino sono gestite principalmente dal richiedente, che controlla il comportamento del writer e del provider generando eventi COM a livello per l'elaborazione da parte del writer.</span><span class="sxs-lookup"><span data-stu-id="e302f-105">Both backup and restore operations are primarily driven by the requester, which controls writer and provider behavior by generating systemwide COM events for the writer to process.</span></span> <span data-ttu-id="e302f-106">Poiché i metodi per la generazione di eventi sono asincroni, i writer hanno un controllo limitato sullo stato del richiedente tramite i gestori asincroni disponibili per VSS (vedere [**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync)).</span><span class="sxs-lookup"><span data-stu-id="e302f-106">Because event-generating methods are asynchronous, writers do have limited control into the requester's state through the asynchronous handlers available to VSS (see [**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync)).</span></span>

<span data-ttu-id="e302f-107">Questa interazione richiede strutture di dati di base che descrivono file e gruppi di file ([*componenti*](vssgloss-c.md)), nonché un modello di metadati per consentire l'archiviazione delle informazioni di backup e consentire la comunicazione tra writer/richiedente.</span><span class="sxs-lookup"><span data-stu-id="e302f-107">This interaction requires basic data structures describing files and groups of files ([*components*](vssgloss-c.md)), as well as a metadata model to allow the storage of backup information and to permit writer/requester communication.</span></span>

-   [<span data-ttu-id="e302f-108">Compatibilità delle applicazioni VSS</span><span class="sxs-lookup"><span data-stu-id="e302f-108">VSS Application Compatibility</span></span>](usage-conventions.md)
-   [<span data-ttu-id="e302f-109">Configurazione di VSS</span><span class="sxs-lookup"><span data-stu-id="e302f-109">Configuring VSS</span></span>](configuring-vss.md)
-   [<span data-ttu-id="e302f-110">Metadati VSS</span><span class="sxs-lookup"><span data-stu-id="e302f-110">VSS Metadata</span></span>](vss-metadata.md)
-   [<span data-ttu-id="e302f-111">Uso della selezione e dei percorsi logici</span><span class="sxs-lookup"><span data-stu-id="e302f-111">Working with Selectability and Logical Paths</span></span>](working-with-selectability-and-logical-paths.md)
-   [<span data-ttu-id="e302f-112">Cenni preliminari sull'elaborazione di un backup in VSS</span><span class="sxs-lookup"><span data-stu-id="e302f-112">Overview of Processing a Backup Under VSS</span></span>](overview-of-processing-a-backup-under-vss.md)
-   [<span data-ttu-id="e302f-113">Panoramica dell'elaborazione di un ripristino in VSS</span><span class="sxs-lookup"><span data-stu-id="e302f-113">Overview of Processing a Restore Under VSS</span></span>](overview-of-processing-a-restore-under-vss.md)

 

 



