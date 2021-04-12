---
description: Il Servizio Copia Shadow del volume (VSS) è un set di API COM e C++ che consentono di eseguire i backup del volume mentre le applicazioni nel sistema (denominate writer) continuano a scrivere nei volumi.
ms.assetid: 94d9504b-2838-4516-8031-daa7bd9d2fec
title: Informazioni di riferimento sull'API copia shadow del volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea8651c987c01ce67f1383f2ab1a24ca3fea8bbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526293"
---
# <a name="volume-shadow-copy-api-reference"></a><span data-ttu-id="50bde-103">Informazioni di riferimento sull'API copia shadow del volume</span><span class="sxs-lookup"><span data-stu-id="50bde-103">Volume Shadow Copy API Reference</span></span>

<span data-ttu-id="50bde-104">Il Servizio Copia Shadow del volume (VSS) è un set di API COM e C++ che consentono di eseguire i backup del volume mentre le applicazioni nel sistema (denominate writer) continuano a scrivere nei volumi.</span><span class="sxs-lookup"><span data-stu-id="50bde-104">The Volume Shadow Copy Service (VSS) is a set of COM and C++ APIs that enable volume backups to be performed while applications on the system (called writers) continue to write to the volumes.</span></span>

<span data-ttu-id="50bde-105">VSS supporta questi backup tramite la creazione di copie shadow, un duplicato del volume originale in un determinato momento.</span><span class="sxs-lookup"><span data-stu-id="50bde-105">VSS supports these backups through the creation of shadow copies, a duplicate of the original volume at a given point in time.</span></span>

<span data-ttu-id="50bde-106">Gli sviluppatori di terze parti possono utilizzare l'API VSS per creare richiedenti, ad esempio un'applicazione di backup, per creare e gestire copie shadow.</span><span class="sxs-lookup"><span data-stu-id="50bde-106">Third-party developers can use the VSS API to create requesters (such as a backup application) to create and manage shadow copies.</span></span>

<span data-ttu-id="50bde-107">Il lavoro effettivo di creazione e rappresentazione delle copie shadow viene eseguito dalle applicazioni a livello di sistema note come provider.</span><span class="sxs-lookup"><span data-stu-id="50bde-107">The actual work of creating and representing shadow copies is conducted by system-level applications known as providers.</span></span>

<span data-ttu-id="50bde-108">Gli sviluppatori possono anche usare l'API per costruire Writer: applicazioni compatibili con VSS in grado di coordinare le operazioni di I/O con la creazione e la manipolazione delle copie shadow.</span><span class="sxs-lookup"><span data-stu-id="50bde-108">Developers can also use the API to construct writers: VSS-aware applications that are able to coordinate I/O operations with the creation and manipulation of shadow copies.</span></span>

-   [<span data-ttu-id="50bde-109">Classi API copia shadow del volume</span><span class="sxs-lookup"><span data-stu-id="50bde-109">Volume Shadow Copy API Classes</span></span>](volume-shadow-copy-api-classes.md)
-   [<span data-ttu-id="50bde-110">Tipi di dati dell'API copia shadow del volume</span><span class="sxs-lookup"><span data-stu-id="50bde-110">Volume Shadow Copy API Data Types</span></span>](volume-shadow-copy-api-data-types.md)
-   [<span data-ttu-id="50bde-111">Enumerazioni API copia shadow del volume</span><span class="sxs-lookup"><span data-stu-id="50bde-111">Volume Shadow Copy API Enumerations</span></span>](volume-shadow-copy-api-enumeration-types.md)
-   [<span data-ttu-id="50bde-112">Funzioni API copia shadow del volume</span><span class="sxs-lookup"><span data-stu-id="50bde-112">Volume Shadow Copy API Functions</span></span>](volume-shadow-copy-api-functions.md)
-   [<span data-ttu-id="50bde-113">Interfacce API copia shadow del volume</span><span class="sxs-lookup"><span data-stu-id="50bde-113">Volume Shadow Copy API Interfaces</span></span>](volume-shadow-copy-api-interfaces.md)
-   [<span data-ttu-id="50bde-114">Strutture API copia shadow del volume</span><span class="sxs-lookup"><span data-stu-id="50bde-114">Volume Shadow Copy API Structures</span></span>](volume-shadow-copy-api-structures.md)
-   [<span data-ttu-id="50bde-115">Glossario copia shadow del volume</span><span class="sxs-lookup"><span data-stu-id="50bde-115">Volume Shadow Copy Glossary</span></span>](volume-shadow-copy-glossary.md)

<span data-ttu-id="50bde-116">Per ulteriori informazioni sulla scrittura di richiedenti e writer, vedere [utilizzo del servizio Copia Shadow del volume](using-the-volume-shadow-copy-service.md).</span><span class="sxs-lookup"><span data-stu-id="50bde-116">For more information on writing requesters and writers, see [Using the Volume Shadow Copy Service](using-the-volume-shadow-copy-service.md).</span></span>

 

 



