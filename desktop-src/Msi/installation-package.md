---
description: Un pacchetto di installazione di contiene tutte le informazioni richieste dal Windows Installer per installare o disinstallare un'applicazione o un prodotto e per eseguire l'interfaccia utente del programma di installazione.
ms.assetid: 532b3492-919f-4999-b86c-e3c210876141
title: Pacchetto di installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe5e5ff79d0c868036dd12ed533b1cd18f9f70d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313344"
---
# <a name="installation-package"></a><span data-ttu-id="72efa-103">Pacchetto di installazione</span><span class="sxs-lookup"><span data-stu-id="72efa-103">Installation Package</span></span>

<span data-ttu-id="72efa-104">Un pacchetto di installazione di contiene tutte le informazioni richieste dal Windows Installer per installare o disinstallare un'applicazione o un prodotto e per eseguire l'interfaccia utente del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="72efa-104">An installation package contains all of the information that the Windows Installer requires to install or uninstall an application or product and to run the setup user interface.</span></span> <span data-ttu-id="72efa-105">Ogni pacchetto di installazione include un file con estensione msi contenente un database di installazione, un flusso di informazioni di riepilogo e flussi di dati per varie parti dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="72efa-105">Each installation package includes an .msi file, containing an installation database, a summary information stream, and data streams for various parts of the installation.</span></span> <span data-ttu-id="72efa-106">Il file con estensione msi può inoltre contenere una o più trasformazioni, file di origine interni e file di origine esterni o file CAB richiesti dall'installazione.</span><span class="sxs-lookup"><span data-stu-id="72efa-106">The .msi file can also contain one or more transforms, internal source files, and external source files or cabinet files required by the installation.</span></span>

<span data-ttu-id="72efa-107">Gli sviluppatori di applicazioni devono creare un'installazione per l'utilizzo del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="72efa-107">Application developers must author an installation to use the installer.</span></span> <span data-ttu-id="72efa-108">Poiché il programma di installazione organizza le installazioni intorno al concetto di [componenti e funzionalità](components-and-features.md)e archivia tutte le informazioni sull'installazione in un database relazionale, il processo di creazione di un pacchetto di installazione comporta l'ampia gamma dei passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="72efa-108">Because the installer organizes installations around the concept of [components and features](components-and-features.md), and stores all information about the installation in a relational database, the process of authoring an installation package broadly entails the following steps:</span></span>

-   <span data-ttu-id="72efa-109">Identificare le funzionalità da presentare agli utenti.</span><span class="sxs-lookup"><span data-stu-id="72efa-109">Identify the features to be presented to users.</span></span>
-   <span data-ttu-id="72efa-110">Organizzare l'applicazione in componenti.</span><span class="sxs-lookup"><span data-stu-id="72efa-110">Organize the application into components.</span></span>
-   <span data-ttu-id="72efa-111">Inserire le informazioni nel database di installazione.</span><span class="sxs-lookup"><span data-stu-id="72efa-111">Populate the installation database with information.</span></span>
-   <span data-ttu-id="72efa-112">Convalidare il pacchetto di installazione.</span><span class="sxs-lookup"><span data-stu-id="72efa-112">Validate the installation package.</span></span>

<span data-ttu-id="72efa-113">Nella sezione successiva vengono descritti i componenti e le funzionalità del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="72efa-113">The next section discusses installer components and features.</span></span> <span data-ttu-id="72efa-114">Per ulteriori informazioni, vedere [componenti e funzionalità](components-and-features.md).</span><span class="sxs-lookup"><span data-stu-id="72efa-114">For more information, see [Components and Features](components-and-features.md).</span></span> <span data-ttu-id="72efa-115">La scelta delle funzionalità è generalmente determinata dalle funzionalità dell'applicazione dal punto di vista dell'utente.</span><span class="sxs-lookup"><span data-stu-id="72efa-115">The choice of features is commonly determined by the application's functionality from the user's perspective.</span></span>

<span data-ttu-id="72efa-116">È consigliabile che gli sviluppatori usino una procedura standard per la scelta dei componenti.</span><span class="sxs-lookup"><span data-stu-id="72efa-116">It is recommended that developers use a standard procedure for choosing components.</span></span> <span data-ttu-id="72efa-117">Per altre informazioni, vedere [organizzazione di applicazioni in componenti](organizing-applications-into-components.md).</span><span class="sxs-lookup"><span data-stu-id="72efa-117">For more information, see [Organizing Applications into Components](organizing-applications-into-components.md).</span></span>

<span data-ttu-id="72efa-118">Per popolare il database di installazione, gli autori di pacchetti possono utilizzare strumenti di creazione di pacchetti di terze parti o un editor tabelle e l'SDK Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="72efa-118">Package authors can use third-party package creation tools, or a table editor and the Windows Installer SDK, to populate the installation database.</span></span> <span data-ttu-id="72efa-119">Tutti i pacchetti di installazione devono essere convalidati per coerenza interna.</span><span class="sxs-lookup"><span data-stu-id="72efa-119">All installation packages need to be validated for internal consistency.</span></span> <span data-ttu-id="72efa-120">Per ulteriori informazioni, vedere [convalida dei pacchetti](package-validation.md).</span><span class="sxs-lookup"><span data-stu-id="72efa-120">For more information, see [Package Validation](package-validation.md).</span></span>

 

 



