---
description: Il database Windows Installer è costituito da molte tabelle intercorrelate che insieme costituiscono un database relazionale delle informazioni necessarie per installare un gruppo di applicazioni.
ms.assetid: 3352dd8f-c082-4c4b-98be-5823c8b28f07
title: Informazioni sul database del programma di installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7f0ee2cc326f85d964ac3d845b97751a48fbb91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881178"
---
# <a name="about-the-installer-database"></a><span data-ttu-id="23cb2-103">Informazioni sul database del programma di installazione</span><span class="sxs-lookup"><span data-stu-id="23cb2-103">About the Installer Database</span></span>

<span data-ttu-id="23cb2-104">Il database Windows Installer è costituito da molte tabelle intercorrelate che insieme costituiscono un database relazionale delle informazioni necessarie per installare un gruppo di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="23cb2-104">The Windows Installer database consists of many interrelated tables that together comprise a relational database of the information necessary to install a group of applications.</span></span> <span data-ttu-id="23cb2-105">Poiché il database è relazionale, le tabelle vengono collegate tramite i dati nei valori di chiave primaria ed esterna.</span><span class="sxs-lookup"><span data-stu-id="23cb2-105">Because the database is relational, the tables are linked through the data in the primary and foreign key values.</span></span> <span data-ttu-id="23cb2-106">Questo fornisce un metodo efficiente per modificare il processo di installazione e significa che gli utenti possono personalizzare più facilmente un'applicazione o un gruppo di applicazioni di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="23cb2-106">This provides an efficient method for changing the installation process and means that users can more easily customize a large application or group of applications.</span></span> <span data-ttu-id="23cb2-107">Le tabelle di database riflettono il layout generale dell'intero gruppo di applicazioni, tra cui:</span><span class="sxs-lookup"><span data-stu-id="23cb2-107">The database tables reflect the general layout of the entire group of applications, including:</span></span>

-   <span data-ttu-id="23cb2-108">Funzionalità disponibili</span><span class="sxs-lookup"><span data-stu-id="23cb2-108">Available features</span></span>
-   <span data-ttu-id="23cb2-109">Componenti</span><span class="sxs-lookup"><span data-stu-id="23cb2-109">Components</span></span>
-   <span data-ttu-id="23cb2-110">Relazione tra funzionalità e componenti</span><span class="sxs-lookup"><span data-stu-id="23cb2-110">Relationship between features and components</span></span>
-   <span data-ttu-id="23cb2-111">Impostazioni del registro di sistema necessarie</span><span class="sxs-lookup"><span data-stu-id="23cb2-111">Necessary registry settings</span></span>
-   <span data-ttu-id="23cb2-112">Interfaccia utente per l'applicazione</span><span class="sxs-lookup"><span data-stu-id="23cb2-112">User interface for the application</span></span>

<span data-ttu-id="23cb2-113">Per creare un database di installazione, è necessario compilare le tabelle con tutte le informazioni sulle applicazioni e il processo di installazione.</span><span class="sxs-lookup"><span data-stu-id="23cb2-113">To create an installation database, you must populate the tables with all the information about the applications and the installation process.</span></span> <span data-ttu-id="23cb2-114">La creazione manuale di tutte queste tabelle diventa un'attività di grandi dimensioni anche per un'installazione con dimensioni moderate; di conseguenza, alcuni strumenti di terze parti sono disponibili per facilitare la compilazione del database del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="23cb2-114">Manually authoring all these tables becomes a large task even for a moderate size installation; therefore some third-party tools are available to assist with building the installer database.</span></span> <span data-ttu-id="23cb2-115">Nelle sezioni seguenti vengono descritti i gruppi di tabelle di database correlate.</span><span class="sxs-lookup"><span data-stu-id="23cb2-115">The following sections describe groups of related database tables.</span></span>

[<span data-ttu-id="23cb2-116">Gruppo di tabelle Core</span><span class="sxs-lookup"><span data-stu-id="23cb2-116">Core Tables Group</span></span>](core-tables-group.md)

[<span data-ttu-id="23cb2-117">Gruppo di tabelle file</span><span class="sxs-lookup"><span data-stu-id="23cb2-117">File Tables Group</span></span>](file-tables-group.md)

[<span data-ttu-id="23cb2-118">Gruppo di tabelle del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="23cb2-118">Registry Tables Group</span></span>](registry-tables-group.md)

[<span data-ttu-id="23cb2-119">Gruppo tabelle di sistema</span><span class="sxs-lookup"><span data-stu-id="23cb2-119">System Tables Group</span></span>](system-tables-group.md)

[<span data-ttu-id="23cb2-120">Gruppo di tabelle Locator</span><span class="sxs-lookup"><span data-stu-id="23cb2-120">Locator Tables Group</span></span>](locator-tables-group.md)

[<span data-ttu-id="23cb2-121">Gruppo tabelle informazioni sul programma</span><span class="sxs-lookup"><span data-stu-id="23cb2-121">Program Information Tables Group</span></span>](program-information-tables-group.md)

[<span data-ttu-id="23cb2-122">Gruppo tabelle procedure di installazione</span><span class="sxs-lookup"><span data-stu-id="23cb2-122">Installation Procedure Tables Group</span></span>](installation-procedure-tables-group.md)

[<span data-ttu-id="23cb2-123">Legenda diagramma delle relazioni tra entità</span><span class="sxs-lookup"><span data-stu-id="23cb2-123">Entity Relationship Diagram Legend</span></span>](entity-relationship-diagram-legend.md)

[<span data-ttu-id="23cb2-124">File di archivio di testo</span><span class="sxs-lookup"><span data-stu-id="23cb2-124">Text Archive Files</span></span>](text-archive-files.md)

<span data-ttu-id="23cb2-125">Per un elenco completo di tutte le tabelle in un database di installazione, vedere [tabelle di database](database-tables.md).</span><span class="sxs-lookup"><span data-stu-id="23cb2-125">For a complete list of all tables in an installation database, see [Database Tables](database-tables.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="23cb2-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="23cb2-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23cb2-127">Versioni rilasciate, strumenti e ridistribuibili</span><span class="sxs-lookup"><span data-stu-id="23cb2-127">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



