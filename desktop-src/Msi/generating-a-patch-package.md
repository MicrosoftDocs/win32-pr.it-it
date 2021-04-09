---
description: Il metodo consigliato per la generazione di un pacchetto di patch consiste nell'usare uno strumento per la creazione di patch, ad esempio Msimsp.exe per chiamare UiCreatePatchPackage in Patchwiz.dll. In Windows Installer SDK sono disponibili Msimsp.exe e PatchWiz.dll.
ms.assetid: 7fa661aa-d52c-4b08-961f-90ec778f02ff
title: Generazione di un pacchetto di patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ef64ac66cd0201ae99080ec86e32230bc88407b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967801"
---
# <a name="generating-a-patch-package"></a><span data-ttu-id="7c3e1-104">Generazione di un pacchetto di patch</span><span class="sxs-lookup"><span data-stu-id="7c3e1-104">Generating a Patch Package</span></span>

<span data-ttu-id="7c3e1-105">Il metodo consigliato per la generazione di un pacchetto di patch consiste nell'usare uno strumento per la creazione di patch, ad esempio [Msimsp.exe](msimsp-exe.md) per chiamare [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) in [Patchwiz.dll](patchwiz-dll.md).</span><span class="sxs-lookup"><span data-stu-id="7c3e1-105">The recommended method for generating a patch package is to use a patch creation tool such as [Msimsp.exe](msimsp-exe.md) to call [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) in [Patchwiz.dll](patchwiz-dll.md).</span></span> <span data-ttu-id="7c3e1-106">In Windows Installer SDK sono disponibili Msimsp.exe e PatchWiz.dll.</span><span class="sxs-lookup"><span data-stu-id="7c3e1-106">Msimsp.exe and PatchWiz.dll are provided in the Windows Installer SDK.</span></span>

<span data-ttu-id="7c3e1-107">La riga di comando di esempio seguente usa Msimsp.exe e il file con estensione PCP creato in [creazione di un file delle proprietà di creazione patch](creating-a-patch-creation-properties-file.md) per generare il pacchetto di patch di esempio MNP2000. msp.</span><span class="sxs-lookup"><span data-stu-id="7c3e1-107">The following example command line uses Msimsp.exe and the .pcp file created in [Creating a Patch Creation Properties File](creating-a-patch-creation-properties-file.md) to generate the sample patch package MNP2000.msp.</span></span>

<span data-ttu-id="7c3e1-108">**Msimsp.exe-s C: \\ Nota \_ patch del programma di installazione \\ \\ MNP2000. PCP-p C: \\ Nota \_ patch di installazione \\ \\ MNP2000. msp**</span><span class="sxs-lookup"><span data-stu-id="7c3e1-108">**Msimsp.exe -s C:\\Note\_Installer\\Patch\\MNP2000.pcp -p C:\\Note\_Installer\\Patch\\MNP2000.msp**</span></span>

<span data-ttu-id="7c3e1-109">Uno strumento di creazione patch creato può generare il pacchetto di patch chiamando [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="7c3e1-109">An authored patch creation tool may generate the patch package by calling [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) as follows.</span></span>

``` syntax
UiCreatePatchPackage ("C:\\Note_Installer\\Patch\\MNP2000.pcp", "C:\\Note_Installer\\Patch\\MNP2000.msp", NULL, NULL, "", TRUE)
```

[<span data-ttu-id="7c3e1-110">Continua</span><span class="sxs-lookup"><span data-stu-id="7c3e1-110">Continue</span></span>](applying-a-patch-package-to-a-local-installation.md)

 

 



