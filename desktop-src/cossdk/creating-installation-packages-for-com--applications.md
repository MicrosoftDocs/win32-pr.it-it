---
description: Creazione di pacchetti di installazione per applicazioni COM+
ms.assetid: 3ef7b280-b521-4cd2-9906-013c9dfe16ab
title: Creazione di pacchetti di installazione per applicazioni COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ec34852ab405d965fa1ad8f8fb5892616d1347
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304829"
---
# <a name="creating-installation-packages-for-com-applications"></a><span data-ttu-id="0806a-103">Creazione di pacchetti di installazione per applicazioni COM+</span><span class="sxs-lookup"><span data-stu-id="0806a-103">Creating Installation Packages for COM+ Applications</span></span>

<span data-ttu-id="0806a-104">È possibile utilizzare lo strumento di amministrazione Servizi componenti o la libreria di amministrazione COM+ per creare pacchetti di installazione per applicazioni COM+ e proxy di applicazione.</span><span class="sxs-lookup"><span data-stu-id="0806a-104">You can use the Component Services administrative tool or the COM+ Administration Library to create installation packages for COM+ applications and application proxies.</span></span>

<span data-ttu-id="0806a-105">COM+ genera Windows Installer pacchetti di installazione, che in un singolo file contengono tutti i componenti necessari per installare un'applicazione COM+ in un altro computer.</span><span class="sxs-lookup"><span data-stu-id="0806a-105">COM+ generates Windows Installer installation packages, which in a single file contain all the necessary pieces to install a COM+ application on another computer.</span></span>

<span data-ttu-id="0806a-106">Quando si esporta un'applicazione COM+, lo strumento di amministrazione Servizi componenti determina il set di classi, i componenti e gli attributi dell'applicazione, nonché gli attributi a livello di applicazione.</span><span class="sxs-lookup"><span data-stu-id="0806a-106">When exporting a COM+ application, the Component Services administrative tool determines the application's set of classes, components, and their attributes, as well as application-level attributes.</span></span> <span data-ttu-id="0806a-107">Da queste informazioni, lo strumento di amministrazione Servizi componenti genera un singolo file con estensione msi, che contiene quanto segue:</span><span class="sxs-lookup"><span data-stu-id="0806a-107">From this information, the Component Services administrative tool generates a single .msi file, which contains the following:</span></span>

-   <span data-ttu-id="0806a-108">Windows Installer tabelle con le informazioni di registrazione COM (vedere la documentazione Windows Installer per informazioni dettagliate).</span><span class="sxs-lookup"><span data-stu-id="0806a-108">Windows Installer tables with COM registration information (see the Windows Installer documentation for details).</span></span>
-   <span data-ttu-id="0806a-109">Un file con estensione APL contenente gli attributi dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0806a-109">An .apl file containing the application's attributes.</span></span> <span data-ttu-id="0806a-110">Si tratta di un file interno. il formato del file non è documentato.</span><span class="sxs-lookup"><span data-stu-id="0806a-110">(This is an internal file; the format of this file is not documented.)</span></span>
-   <span data-ttu-id="0806a-111">Dll e librerie dei tipi che descrivono le interfacce implementate dalle classi dell'applicazione COM+.</span><span class="sxs-lookup"><span data-stu-id="0806a-111">DLLs and type libraries that describe the interfaces implemented by the COM+ application's classes.</span></span>

<span data-ttu-id="0806a-112">Oltre al file con estensione msi, lo strumento di amministrazione Servizi componenti genera un file CAB.</span><span class="sxs-lookup"><span data-stu-id="0806a-112">In addition to the .msi file, the Component Services administrative tool generates a cabinet (.cab) file.</span></span> <span data-ttu-id="0806a-113">Questo file esegue il wrapping del file con estensione msi, consentendo allo sviluppatore di distribuire l'applicazione COM+ tramite Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="0806a-113">This file wraps the .msi file, allowing the developer to deploy the COM+ application through Microsoft Internet Explorer.</span></span>

> [!Note]  
> <span data-ttu-id="0806a-114">Quando si esporta un'applicazione COM+, lo strumento di amministrazione Servizi componenti esegue il pacchetto solo delle parti COM+ standard dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0806a-114">When exporting a COM+ application, the Component Services administrative tool packages only the standard COM+ parts of the application.</span></span> <span data-ttu-id="0806a-115">Non esegue il pacchetto, ad esempio, di eventuali file di dati o DLL dipendenti.</span><span class="sxs-lookup"><span data-stu-id="0806a-115">It does not package, for example, any dependent DLL or data files.</span></span> <span data-ttu-id="0806a-116">Prima di installare l'applicazione COM+, è necessario che i file DLL dipendenti siano installati in un computer.</span><span class="sxs-lookup"><span data-stu-id="0806a-116">The dependent DLL files must first be installed on a computer prior to installing the COM+ application.</span></span> <span data-ttu-id="0806a-117">In alternativa, è possibile utilizzare lo strumento di creazione Windows Installer per aggiungere questi file dipendenti al file con estensione msi generato dallo strumento di amministrazione Servizi componenti.</span><span class="sxs-lookup"><span data-stu-id="0806a-117">Alternatively, you can use the Windows Installer authoring tool to add these dependent files to the .msi file generated by the Component Services administrative tool.</span></span> <span data-ttu-id="0806a-118">Per informazioni dettagliate, vedere la documentazione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="0806a-118">(See the Windows Installer documentation for details.)</span></span>

 

## <a name="installing-com-applications-on-other-computers"></a><span data-ttu-id="0806a-119">Installazione di applicazioni COM+ in altri computer</span><span class="sxs-lookup"><span data-stu-id="0806a-119">Installing COM+ Applications on Other Computers</span></span>

<span data-ttu-id="0806a-120">Il file di Windows Installer (MSI) generato dallo strumento di amministrazione Servizi componenti può essere utilizzato per installare l'applicazione COM+ in un altro computer.</span><span class="sxs-lookup"><span data-stu-id="0806a-120">The Windows Installer (.msi) file generated by the Component Services administrative tool can be used to install the COM+ application on another computer.</span></span> <span data-ttu-id="0806a-121">Il file con estensione msi contenente un'applicazione COM+ può essere installato solo su computer che supportano servizi COM+.</span><span class="sxs-lookup"><span data-stu-id="0806a-121">The .msi file containing a COM+ application can be installed only on computers that support COM+ services.</span></span> <span data-ttu-id="0806a-122">Per le procedure dettagliate relative alla distribuzione di applicazioni COM+, vedere "installazione di applicazioni COM+" nella Guida all'amministrazione di Servizi componenti.</span><span class="sxs-lookup"><span data-stu-id="0806a-122">For detailed procedures on deploying COM+ applications, see "Installing COM+ Applications," in the Component Services Administration Help.</span></span>

<span data-ttu-id="0806a-123">A meno che il file con estensione msi non venga modificato utilizzando uno strumento di creazione Windows Installer, le applicazioni COM+ installate utilizzando il Windows Installer vengono visualizzate nel pannello di controllo Installazione applicazioni.</span><span class="sxs-lookup"><span data-stu-id="0806a-123">Unless the .msi file is modified using a Windows Installer authoring tool, COM+ applications installed by using the Windows Installer appear in the Add/Remove Programs control panel.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0806a-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0806a-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0806a-125">Distribuzione di proxy di applicazione</span><span class="sxs-lookup"><span data-stu-id="0806a-125">Deploying Application Proxies</span></span>](deploying-application-proxies.md)
</dt> <dt>

[<span data-ttu-id="0806a-126">Catalogo COM+</span><span class="sxs-lookup"><span data-stu-id="0806a-126">The COM+ Catalog</span></span>](the-com--catalog.md)
</dt> </dl>

 

 



