---
description: I componenti indicano il tipo di dati che rappresentano tramite un tipo.
ms.assetid: 19d785d5-09a7-48b9-a0a2-eca3049d67fe
title: Tipi di componenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1f89355b4b26090b7d43f9753c086b4ccc79df0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318904"
---
# <a name="component-types"></a><span data-ttu-id="839ac-103">Tipi di componenti</span><span class="sxs-lookup"><span data-stu-id="839ac-103">Component Types</span></span>

<span data-ttu-id="839ac-104">I componenti indicano il tipo di dati che rappresentano tramite un tipo.</span><span class="sxs-lookup"><span data-stu-id="839ac-104">Components indicate the sort of data they represent through a type.</span></span>

<span data-ttu-id="839ac-105">Attualmente, i tipi di componente (vedere il [**\_ \_ tipo di componente VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_type)) sono limitati agli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="839ac-105">Currently, component types (see [**VSS\_COMPONENT\_TYPE**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_type)) are limited to the following:</span></span>

-   <span data-ttu-id="839ac-106">Componenti database</span><span class="sxs-lookup"><span data-stu-id="839ac-106">Database components</span></span>
-   <span data-ttu-id="839ac-107">Filegroup</span><span class="sxs-lookup"><span data-stu-id="839ac-107">File groups</span></span>

<span data-ttu-id="839ac-108">Per informazioni sull'implementazione sull'impostazione dei tipi di componenti, vedere [definizione di componenti per Writer](definition-of-components-by-writers.md).</span><span class="sxs-lookup"><span data-stu-id="839ac-108">For implementation information about setting component types, see [Definition of Components by Writers](definition-of-components-by-writers.md).</span></span>

<span data-ttu-id="839ac-109">I writer hanno una digitazione dei dati che ne indica l'utilizzo (vedere il [**\_ \_ tipo di origine VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type)), che può essere il seguente:</span><span class="sxs-lookup"><span data-stu-id="839ac-109">Writers have a data typing that indicates their usage (see [**VSS\_SOURCE\_TYPE**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type)), which can be the following:</span></span>

-   <span data-ttu-id="839ac-110">Un database transazionale (ad esempio, SQL Server)</span><span class="sxs-lookup"><span data-stu-id="839ac-110">A transactional database (such as an SQL server)</span></span>
-   <span data-ttu-id="839ac-111">Un database non transazionale (ad esempio un client del foglio di calcolo)</span><span class="sxs-lookup"><span data-stu-id="839ac-111">A nontransactional database (such as a spreadsheet client)</span></span>
-   <span data-ttu-id="839ac-112">Filegroup (altro)</span><span class="sxs-lookup"><span data-stu-id="839ac-112">File group (other)</span></span>

<span data-ttu-id="839ac-113">La specifica di un tipo di componente come database consente un'identificazione più semplice del contenuto, consente la gestione separata dei file di log e di dati (vedere [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) e [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) per i dettagli) e impone un maggiore rigore nella selezione dei file non consentendo la selezione di file ricorsivi o usando un [*percorso alternativo*](vssgloss-a.md) (vedere [**IVssCreateWriterMetadata:: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles) e [**IVssCreateWriterMetadata:: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)).</span><span class="sxs-lookup"><span data-stu-id="839ac-113">Specifying a component type as database allows for easier identification of its content, allows for separate handling of log and data files (see [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) and [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) for details), and enforces greater rigor in file selection by not allowing either recursive file selection or using an [*alternate path*](vssgloss-a.md) (see [**IVssCreateWriterMetadata::AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles) and [**IVssCreateWriterMetadata::AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)).</span></span>

<span data-ttu-id="839ac-114">Con un componente del gruppo di file, d'altra parte, a meno che non si conoscano i dati in esso contenuti, si ha maggiore libertà di come vengono inseriti i file, perché è possibile usare la specifica ricorsiva e i percorsi alternativi.</span><span class="sxs-lookup"><span data-stu-id="839ac-114">With a file group component, on the other hand, at the price of not knowing what data it contains, you have greater freedom about how files are inserted, because you can use recursive specification and alternate paths.</span></span>

<span data-ttu-id="839ac-115">In futuro è possibile aggiungere altri tipi di componenti.</span><span class="sxs-lookup"><span data-stu-id="839ac-115">Additional component types may be added in the future.</span></span>

 

 



