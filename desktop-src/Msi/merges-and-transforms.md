---
description: Il Windows Installer conserva tutte le informazioni sull'installazione di in un database relazionale. È possibile modificare il database e, di conseguenza, l'installazione utilizzando le trasformazioni e le unioni.
ms.assetid: 32163e06-d03d-4b65-b744-62f306f2100d
title: Unioni e trasformazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aec6314e81afb5afa9d74346b64fe3129ba5ed30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318659"
---
# <a name="merges-and-transforms"></a><span data-ttu-id="6adb7-104">Unioni e trasformazioni</span><span class="sxs-lookup"><span data-stu-id="6adb7-104">Merges and Transforms</span></span>

<span data-ttu-id="6adb7-105">Il Windows Installer conserva tutte le informazioni sull'installazione di in un database relazionale.</span><span class="sxs-lookup"><span data-stu-id="6adb7-105">The Windows Installer keeps all information about the installation in a relational database.</span></span> <span data-ttu-id="6adb7-106">È possibile modificare il database e, di conseguenza, l'installazione utilizzando le trasformazioni e le unioni.</span><span class="sxs-lookup"><span data-stu-id="6adb7-106">You can modify this database, and therefore the installation, by using transforms and merges.</span></span>

## <a name="transforms"></a><span data-ttu-id="6adb7-107">Trasformazioni</span><span class="sxs-lookup"><span data-stu-id="6adb7-107">Transforms</span></span>

<span data-ttu-id="6adb7-108">Una [trasformazione del database](database-transforms.md) aggiunge o sostituisce gli elementi nel database originale.</span><span class="sxs-lookup"><span data-stu-id="6adb7-108">A [database transform](database-transforms.md) adds or replaces elements in the original database.</span></span> <span data-ttu-id="6adb7-109">Una trasformazione, ad esempio, può modificare tutto il testo dell'interfaccia utente di un'applicazione da Francese a inglese.</span><span class="sxs-lookup"><span data-stu-id="6adb7-109">For example, a transform can change all of the text in an application's user interface from French to English.</span></span>

<span data-ttu-id="6adb7-110">Gli utilizzi primari per le trasformazioni includono:</span><span class="sxs-lookup"><span data-stu-id="6adb7-110">Primary uses for transforms include:</span></span>

-   <span data-ttu-id="6adb7-111">Personalizzazione dei pacchetti di installazione di base per determinati gruppi di utenti.</span><span class="sxs-lookup"><span data-stu-id="6adb7-111">Customization of base installation packages for particular groups of users.</span></span>

    <span data-ttu-id="6adb7-112">Le trasformazioni possono essere utilizzate per incapsulare le varie personalizzazioni di un singolo pacchetto di base richieste da gruppi di utenti diversi.</span><span class="sxs-lookup"><span data-stu-id="6adb7-112">Transforms can be used to encapsulate the various customizations of a single base package that are required by different groups of users.</span></span> <span data-ttu-id="6adb7-113">Ad esempio, questa operazione è utile nelle organizzazioni in cui i reparti del supporto Finance e del personale richiedono installazioni diverse di un determinato prodotto.</span><span class="sxs-lookup"><span data-stu-id="6adb7-113">For example, this is useful in organizations where the finance and staff support departments require different installations of a particular product.</span></span> <span data-ttu-id="6adb7-114">Il pacchetto di base di un prodotto può essere disponibile per tutti gli utenti in un punto di installazione amministrativa con personalizzazioni appropriate distribuite a ogni gruppo di utenti separatamente.</span><span class="sxs-lookup"><span data-stu-id="6adb7-114">A product's base package can be available to everyone at one administrative installation point with appropriate customizations distributed to each group of users separately.</span></span>

-   <span data-ttu-id="6adb7-115">Sincronizzazione di applicazioni in più lingue.</span><span class="sxs-lookup"><span data-stu-id="6adb7-115">Synchronization of applications across languages.</span></span>

    <span data-ttu-id="6adb7-116">Le trasformazioni sono utili per mantenere i pacchetti creati in posizioni ampiamente separate sincronizzate durante la creazione.</span><span class="sxs-lookup"><span data-stu-id="6adb7-116">Transforms are useful for keeping packages authored at widely separated locations synchronized during authoring.</span></span> <span data-ttu-id="6adb7-117">Se, ad esempio, un aggiornamento viene sviluppato per la prima volta in una versione in lingua inglese di un'applicazione presente in inglese e francese, è possibile applicare una trasformazione alla versione in lingua inglese aggiornata che la converte in una versione francese aggiornata.</span><span class="sxs-lookup"><span data-stu-id="6adb7-117">For example, if an upgrade is first developed for an English version of an application that exists in English and French, a transform can be applied to the upgraded English version that converts it into an upgraded French version.</span></span>

    <span data-ttu-id="6adb7-118">È possibile applicare più trasformazioni a un pacchetto di base e quindi applicarle in tempo reale durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="6adb7-118">Multiple transforms can be applied to a base package and then applied on-the-fly during installation.</span></span> <span data-ttu-id="6adb7-119">Questo consente di estendere le funzionalità del programma di installazione per creare pacchetti personalizzati e fornisce un meccanismo per assegnare in modo efficiente le installazioni più appropriate a diversi gruppi di utenti.</span><span class="sxs-lookup"><span data-stu-id="6adb7-119">This extends the capabilities of the installer to create custom packages and provides a mechanism for efficiently assigning the most appropriate installations to different groups of users.</span></span>

-   <span data-ttu-id="6adb7-120">Applicazione di patch.</span><span class="sxs-lookup"><span data-stu-id="6adb7-120">Patching applications.</span></span>

    <span data-ttu-id="6adb7-121">Le trasformazioni possono essere utilizzate per applicare una correzione secondaria a un'applicazione che non richiede un aggiornamento importante.</span><span class="sxs-lookup"><span data-stu-id="6adb7-121">Transforms can be used to apply a minor fix to an application that does not warrant a major upgrade.</span></span> <span data-ttu-id="6adb7-122">Per ulteriori informazioni sulle patch, vedere la pagina relativa ai [pacchetti di patch](patch-packages.md).</span><span class="sxs-lookup"><span data-stu-id="6adb7-122">For more information about patches, see [Patch Packages](patch-packages.md).</span></span>

## <a name="merges"></a><span data-ttu-id="6adb7-123">Unioni</span><span class="sxs-lookup"><span data-stu-id="6adb7-123">Merges</span></span>

<span data-ttu-id="6adb7-124">Un'Unione combina due database in un unico database e aggiunge, anziché sostituire, le informazioni.</span><span class="sxs-lookup"><span data-stu-id="6adb7-124">A merge combines two databases into one database, and adds, rather than replaces, information.</span></span> <span data-ttu-id="6adb7-125">Se le stesse informazioni sono presenti in entrambi i database, si verifica un conflitto di merge.</span><span class="sxs-lookup"><span data-stu-id="6adb7-125">If the same information exists in both databases, a merge conflict occurs.</span></span> <span data-ttu-id="6adb7-126">Le unioni sono utili per i team di sviluppo perché consentono a un'applicazione di grandi dimensioni di essere divisa in parti che possono essere ricombinate in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="6adb7-126">Merges are useful to development teams because they allow a large application to be divided into parts that can be recombined later.</span></span> <span data-ttu-id="6adb7-127">Ad esempio, gli elementi del database per l'installazione di un nuovo componente possono essere sviluppati separatamente e successivamente Uniti nel database di installazione principale.</span><span class="sxs-lookup"><span data-stu-id="6adb7-127">For example, the database elements for the installation of a new component can be developed separately and later merged into the main installation database.</span></span> <span data-ttu-id="6adb7-128">Per altre informazioni, vedere [merge modules](merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="6adb7-128">For more information, see [Merge Modules](merge-modules.md).</span></span>

<span data-ttu-id="6adb7-129">Un team di sviluppo può applicare un'operazione di Unione nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="6adb7-129">A development team might apply a merge operation in the following way:</span></span>

1.  <span data-ttu-id="6adb7-130">Separa i gruppi e lavora simultaneamente su componenti diversi di un'applicazione di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="6adb7-130">Separate into groups and work simultaneously on different components of a large application.</span></span>
2.  <span data-ttu-id="6adb7-131">Ogni gruppo di sviluppo compila quindi un database con le informazioni di installazione per il proprio componente, senza preoccuparsi degli altri componenti dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6adb7-131">Each development group then populates a database with installation information for its own component, without being concerned with the other components of the application.</span></span>
3.  <span data-ttu-id="6adb7-132">Una volta completato lo sviluppo di un componente, il database del componente può essere Unito nel database di installazione principale per l'intera applicazione.</span><span class="sxs-lookup"><span data-stu-id="6adb7-132">After the development of a component is complete, that component's database can be merged into the main installation database for the entire application.</span></span>

 

 



