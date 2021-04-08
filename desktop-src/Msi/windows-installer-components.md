---
description: Un componente è una parte dell'applicazione o del prodotto da installare.
ms.assetid: f1c9696d-3267-44be-a904-ab26250fae2e
title: Componenti Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ad90f2fb576d0333a26fc92f9cf951e4da06bab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967783"
---
# <a name="windows-installer-components"></a><span data-ttu-id="0f1d6-103">Componenti Windows Installer</span><span class="sxs-lookup"><span data-stu-id="0f1d6-103">Windows Installer Components</span></span>

<span data-ttu-id="0f1d6-104">Un componente è una parte dell'applicazione o del prodotto da installare.</span><span class="sxs-lookup"><span data-stu-id="0f1d6-104">A component is a piece of the application or product to be installed.</span></span> <span data-ttu-id="0f1d6-105">Esempi di componenti includono singoli file, un gruppo di file correlati, oggetti COM, registrazione, chiavi del registro di sistema, scelte rapide, risorse, librerie raggruppate in una directory o parti condivise di codice, ad esempio MFC o DAO.</span><span class="sxs-lookup"><span data-stu-id="0f1d6-105">Examples of components include single files, a group of related files, COM objects, registration, registry keys, shortcuts, resources, libraries grouped into a directory, or shared pieces of code such as MFC or DAO.</span></span>

<span data-ttu-id="0f1d6-106">Il servizio del programma di installazione installa o rimuove un componente come singolo elemento coerente.</span><span class="sxs-lookup"><span data-stu-id="0f1d6-106">The installer service installs or removes a component as a single coherent piece.</span></span> <span data-ttu-id="0f1d6-107">Tiene traccia di ogni componente in base al rispettivo GUID ID componente specificato nella colonna ComponentId della [tabella Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="0f1d6-107">It tracks every component by the respective component ID GUID specified in the ComponentId column of the [Component table](component-table.md).</span></span>

> [!Note]  
> <span data-ttu-id="0f1d6-108">Due componenti che condividono lo stesso ID componente vengono considerati come più istanze dello stesso componente indipendentemente dal contenuto effettivo.</span><span class="sxs-lookup"><span data-stu-id="0f1d6-108">Two components that share the same component ID are treated as multiple instances of the same component regardless of their actual content.</span></span> <span data-ttu-id="0f1d6-109">Nel computer di un utente viene installata una sola istanza di un componente.</span><span class="sxs-lookup"><span data-stu-id="0f1d6-109">Only a single instance of any component is installed on a user's computer.</span></span> <span data-ttu-id="0f1d6-110">Diverse funzionalità o applicazioni possono pertanto condividere alcuni componenti.</span><span class="sxs-lookup"><span data-stu-id="0f1d6-110">Several features or applications may therefore share some components.</span></span>

 

<span data-ttu-id="0f1d6-111">Poiché i componenti sono comunemente condivisi, l'autore di un pacchetto di installazione deve seguire regole rigide quando si specificano i componenti di una funzionalità o di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0f1d6-111">Because components are commonly shared, the author of an installation package must follow strict rules when specifying the components of a feature or application.</span></span> <span data-ttu-id="0f1d6-112">Questo è essenziale per il corretto funzionamento del Windows Installer meccanismo di conteggio dei riferimenti.</span><span class="sxs-lookup"><span data-stu-id="0f1d6-112">This is essential for the correct operation of the Windows Installer reference-counting mechanism.</span></span> <span data-ttu-id="0f1d6-113">Per altre informazioni, vedere [organizzazione di applicazioni in componenti](organizing-applications-into-components.md).</span><span class="sxs-lookup"><span data-stu-id="0f1d6-113">For more information, see [Organizing Applications into Components](organizing-applications-into-components.md).</span></span>

<span data-ttu-id="0f1d6-114">In breve, queste regole sono:</span><span class="sxs-lookup"><span data-stu-id="0f1d6-114">In brief, these rules are:</span></span>

-   <span data-ttu-id="0f1d6-115">Ogni componente deve essere archiviato in un'unica cartella.</span><span class="sxs-lookup"><span data-stu-id="0f1d6-115">Each component must be stored in a single folder.</span></span>
-   <span data-ttu-id="0f1d6-116">Nessun file, voce del registro di sistema, collegamento o altre risorse devono essere spediti come membro di più di un componente.</span><span class="sxs-lookup"><span data-stu-id="0f1d6-116">No file, registry entry, shortcut, or other resources should ever be shipped as a member of more than one component.</span></span> <span data-ttu-id="0f1d6-117">Questo vale per i prodotti, le versioni dei prodotti e le società.</span><span class="sxs-lookup"><span data-stu-id="0f1d6-117">This applies across products, product versions, and companies.</span></span>

<span data-ttu-id="0f1d6-118">Per ulteriori informazioni sull'utilizzo dei componenti di, vedere.</span><span class="sxs-lookup"><span data-stu-id="0f1d6-118">For more information about using components, see</span></span>

-   [<span data-ttu-id="0f1d6-119">Installazione di un componente mancante</span><span class="sxs-lookup"><span data-stu-id="0f1d6-119">Installing a Missing Component</span></span>](installing-a-missing-component.md)
-   [<span data-ttu-id="0f1d6-120">Installazione di componenti permanenti, file, tipi di carattere, chiavi del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="0f1d6-120">Installing Permanent Components, Files, Fonts, Registry Keys</span></span>](installing-permanent-components-files-fonts-registry-keys.md)
-   [<span data-ttu-id="0f1d6-121">Utilizzo di componenti qualificati</span><span class="sxs-lookup"><span data-stu-id="0f1d6-121">Using Qualified Components</span></span>](using-qualified-components.md)
-   [<span data-ttu-id="0f1d6-122">Utilizzo di componenti transitivi</span><span class="sxs-lookup"><span data-stu-id="0f1d6-122">Using Transitive Components</span></span>](using-transitive-components.md)
-   [<span data-ttu-id="0f1d6-123">Utilizzo delle funzionalità e dei componenti</span><span class="sxs-lookup"><span data-stu-id="0f1d6-123">Working with Features and Components</span></span>](working-with-features-and-components.md)
-   [<span data-ttu-id="0f1d6-124">Creazione di un pacchetto di grandi dimensioni</span><span class="sxs-lookup"><span data-stu-id="0f1d6-124">Authoring a Large Package</span></span>](authoring-a-large-package.md)
-   [<span data-ttu-id="0f1d6-125">Verifica dell'installazione di funzionalità, componenti, file</span><span class="sxs-lookup"><span data-stu-id="0f1d6-125">Checking the Installation of Features, Components, Files</span></span>](checking-the-installation-of-features-components-files.md)
-   [<span data-ttu-id="0f1d6-126">Ricerca di una funzionalità o di un componente danneggiato</span><span class="sxs-lookup"><span data-stu-id="0f1d6-126">Searching for a Broken Feature or Component</span></span>](searching-for-a-broken-feature-or-component.md)
-   [<span data-ttu-id="0f1d6-127">Pubblicazione di prodotti, funzionalità e componenti</span><span class="sxs-lookup"><span data-stu-id="0f1d6-127">Publishing Products, Features, and Components</span></span>](publishing-products-features-and-components.md)

 

 



