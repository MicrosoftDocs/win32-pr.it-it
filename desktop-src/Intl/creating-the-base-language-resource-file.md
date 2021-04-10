---
description: Creazione del file di risorse della lingua di base
ms.assetid: 770e1f4b-5258-4b6b-afa4-5c19743daaaa
title: Creazione del file di risorse della lingua di base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b96d566625025c105e123e0e2edf9f4f20721274
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058146"
---
# <a name="creating-the-base-language-resource-file"></a><span data-ttu-id="23d1b-103">Creazione del file di risorse della lingua di base</span><span class="sxs-lookup"><span data-stu-id="23d1b-103">Creating the Base Language Resource File</span></span>

<span data-ttu-id="23d1b-104">Le risorse per gli elementi dell'interfaccia utente sono definite per il linguaggio di base supportato dall'applicazione, ad esempio inglese (Stati Uniti).</span><span class="sxs-lookup"><span data-stu-id="23d1b-104">Resources for user interface elements are defined for the basic language that the application supports, for example, English (United States).</span></span> <span data-ttu-id="23d1b-105">Un esempio di file di risorse PE Win32 è un file RC, creato con il compilatore RC.</span><span class="sxs-lookup"><span data-stu-id="23d1b-105">An example of a Win32 PE resource file is an .rc file, created using RC Compiler.</span></span> <span data-ttu-id="23d1b-106">Per informazioni dettagliate sulla creazione di file RC, vedere [informazioni sui file di risorse](../menurc/about-resource-files.md).</span><span class="sxs-lookup"><span data-stu-id="23d1b-106">For details of .rc file creation, see [About Resource Files](../menurc/about-resource-files.md).</span></span>

<span data-ttu-id="23d1b-107">Se si usa un file RC per le risorse della lingua di base, è possibile usare un file di configurazione delle risorse per una rappresentazione XML dei dati di configurazione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="23d1b-107">If using an .rc file for the base language resources, you have the option of using a resource configuration file for an XML representation of resource configuration data.</span></span> <span data-ttu-id="23d1b-108">Per creare questo file, vedere [preparazione di un file di configurazione delle risorse](preparing-a-resource-configuration-file.md).</span><span class="sxs-lookup"><span data-stu-id="23d1b-108">To create this file, see [Preparing a Resource Configuration File](preparing-a-resource-configuration-file.md).</span></span>

<span data-ttu-id="23d1b-109">È anche possibile usare un file PE non Win32 per definire le risorse della lingua di base.</span><span class="sxs-lookup"><span data-stu-id="23d1b-109">You can also use a non-Win32 PE file to define base language resources.</span></span> <span data-ttu-id="23d1b-110">È ad esempio possibile utilizzare un file con estensione XML o txt a questo scopo.</span><span class="sxs-lookup"><span data-stu-id="23d1b-110">For example, you might use an .xml file or .txt file for this purpose.</span></span>

> [!Note]  
> <span data-ttu-id="23d1b-111">Quando si definiscono le risorse della lingua di base usando un file PE non Win32, non è possibile usare il compilatore RC per la definizione di risorsa.</span><span class="sxs-lookup"><span data-stu-id="23d1b-111">When you define base language resources using a non-Win32 PE file, you cannot use RC Compiler for resource definition.</span></span> <span data-ttu-id="23d1b-112">Si definisce invece il proprio formato di risorsa e l'applicazione deve fornire le proprie funzionalità per individuare e caricare le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="23d1b-112">Instead, you define your own resource format, and your application must provide its own functionality to find and load the required resources.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="23d1b-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="23d1b-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23d1b-114">Preparazione delle risorse</span><span class="sxs-lookup"><span data-stu-id="23d1b-114">Preparing Resources</span></span>](preparing-resources.md)
</dt> <dt>

[<span data-ttu-id="23d1b-115">Preparazione di un file di configurazione delle risorse</span><span class="sxs-lookup"><span data-stu-id="23d1b-115">Preparing a Resource Configuration File</span></span>](preparing-a-resource-configuration-file.md)
</dt> </dl>

 

 
