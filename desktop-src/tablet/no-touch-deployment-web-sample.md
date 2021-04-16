---
description: In questo esempio viene illustrato come distribuire un'applicazione Tablet PC gestita sul Web utilizzando la distribuzione senza tocco.
ms.assetid: d226bd67-e20d-431b-b0c3-9361b00a9340
title: Esempio di Web Deployment No-Touch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a0742deef8ea9b418fba6de4724975ee27693f8
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104530444"
---
# <a name="no-touch-deployment-web-sample"></a><span data-ttu-id="2c489-103">Esempio di Web Deployment No-Touch</span><span class="sxs-lookup"><span data-stu-id="2c489-103">No-Touch Deployment Web Sample</span></span>

<span data-ttu-id="2c489-104">In questo esempio viene illustrato come distribuire un'applicazione Tablet PC gestita sul Web utilizzando la distribuzione senza tocco.</span><span class="sxs-lookup"><span data-stu-id="2c489-104">This sample shows how to deploy a managed Tablet PC application over the Web by using no-touch deployment.</span></span> <span data-ttu-id="2c489-105">È necessario avere familiarità con i concetti illustrati nella [distribuzione senza tocco nella .NET Framework](/documentation/?url=%2flibrary%2fdv_vstechart%2fhtml%2fvbtchno-touchdeploymentinnetframework.asp).</span><span class="sxs-lookup"><span data-stu-id="2c489-105">You should be familiar with the concepts discussed in [No-Touch Deployment in the .NET Framework](/documentation/?url=%2flibrary%2fdv_vstechart%2fhtml%2fvbtchno-touchdeploymentinnetframework.asp).</span></span> <span data-ttu-id="2c489-106">Per eseguire l'esempio, è necessario che nel computer sia installato Microsoft Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="2c489-106">Your computer must have Microsoft Internet Information Services (IIS) installed to run this sample.</span></span>

## <a name="overview"></a><span data-ttu-id="2c489-107">Panoramica</span><span class="sxs-lookup"><span data-stu-id="2c489-107">Overview</span></span>

<span data-ttu-id="2c489-108">Con la distribuzione senza tocco, le applicazioni tablet PCWindows Forms-applicazioni desktop compilate usando le classi nello spazio dei nomi System. Windows. Forms di Microsoft .NET Framework e Microsoft Windows XP Tablet PC Edition Development Kit 1,7-possono essere scaricate, installate ed eseguite direttamente sui computer degli utenti senza alcuna modifica del registro di sistema o dei componenti di sistema condivisi.</span><span class="sxs-lookup"><span data-stu-id="2c489-108">With no-touch deployment, Tablet PCWindows Forms applications-desktop applications built by using the classes in the System.Windows.Forms namespace of the Microsoft .NET Framework and the Microsoft Windows XP Tablet PC Edition Development Kit 1.7-can be downloaded, installed, and run directly on users' computers without any alteration of the registry or shared system components.</span></span>

<span data-ttu-id="2c489-109">Questo esempio accetta il progetto originale per l' [esempio di modulo delle attestazioni automatiche](auto-claims-form-sample.md), autoclaims e fornisce un progetto di programma di installazione, autoclaims \_ NoTouchWeb.</span><span class="sxs-lookup"><span data-stu-id="2c489-109">This sample takes the original project for [Auto Claims Form Sample](auto-claims-form-sample.md), AutoClaims, and provides an installer project, AutoClaims\_NoTouchWeb.</span></span> <span data-ttu-id="2c489-110">Una volta compilata ed eseguita, il progetto di installazione crea una nuova radice virtuale, denominata anche autoclaims \_ NoTouchWeb.</span><span class="sxs-lookup"><span data-stu-id="2c489-110">Once compiled and run, the installer project creates a new virtual root, also called AutoClaims\_NoTouchWeb.</span></span> <span data-ttu-id="2c489-111">Il programma di installazione copia un file, default.htm, che include un collegamento all'assembly AutoClaims.exe.</span><span class="sxs-lookup"><span data-stu-id="2c489-111">The installer copies a file, default.htm, that includes a link to the AutoClaims.exe assembly.</span></span> <span data-ttu-id="2c489-112">Per avviare l'applicazione rich client, passare alla radice virtuale con Microsoft Internet Explorer, quindi fare clic sul collegamento nella pagina default.htm.</span><span class="sxs-lookup"><span data-stu-id="2c489-112">To launch the rich client application, navigate to the virtual root with Microsoft Internet Explorer, and then click the link in the default.htm page.</span></span>

> [!Note]  
> <span data-ttu-id="2c489-113">È necessario passare alla radice virtuale tramite IIS (ad esempio, https://localhost/AutoClaims\_NoTouchWeb/default.htm) e non direttamente tramite il file System per consentire l'uso dell'applicazione nel dominio applicazione di Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="2c489-113">You must navigate to the virtual root by way of IIS (for example, https://localhost/AutoClaims\_NoTouchWeb/default.htm) and not directly through the file system in order for the application to work in the Internet Explorer application domain.</span></span>

 


```C++
<html>
    <head>
        <title>AutoClaims (No Touch Web)</title>
      </head>
      <body>
          <a href="AutoClaims.exe">Launch AutoClaims Sample</a>
      </body>
</html>
```



## <a name="no-touch-deployment-requirements"></a><span data-ttu-id="2c489-114">Requisiti per la distribuzione di No-Touch</span><span class="sxs-lookup"><span data-stu-id="2c489-114">No-Touch Deployment Requirements</span></span>

<span data-ttu-id="2c489-115">Tutti gli assembly dipendenti devono trovarsi nel percorso di ricerca dell'assembly o nella radice della directory virtuale del sito Web.</span><span class="sxs-lookup"><span data-stu-id="2c489-115">All dependent assemblies must be located either in the assembly search path or the root of the virtual directory of the Web site.</span></span> <span data-ttu-id="2c489-116">Il progetto di distribuzione autoclaims \_ NoTouchWeb installa l'assembly e la pagina di riferimento, default.htm, nella stessa radice virtuale (Autoclaims \_ NoTouchWeb).</span><span class="sxs-lookup"><span data-stu-id="2c489-116">The AutoClaims\_NoTouchWeb deployment project installs the assembly and the referring page, default.htm, into the same virtual root (AutoClaims\_NoTouchWeb).</span></span>

> [!Note]  
> <span data-ttu-id="2c489-117">Gli esempi Web compilati non vengono installati tramite l'opzione di installazione predefinita per l'SDK.</span><span class="sxs-lookup"><span data-stu-id="2c489-117">The compiled web samples are not installed by the default installation option for the SDK.</span></span> <span data-ttu-id="2c489-118">È necessario completare un'installazione personalizzata e selezionare l'opzione secondaria "esempi Web precompilati" per installarli.</span><span class="sxs-lookup"><span data-stu-id="2c489-118">You must complete a custom installation and select the "Pre-compiled Web Samples" sub-option to install them.</span></span>

 

<span data-ttu-id="2c489-119">Per ulteriori informazioni sull'utilizzo di input penna sul Web, vedere [input penna sul Web](ink-on-the-web.md).</span><span class="sxs-lookup"><span data-stu-id="2c489-119">For more information about using ink on the Web, see [Ink on the Web](ink-on-the-web.md).</span></span>

 

 