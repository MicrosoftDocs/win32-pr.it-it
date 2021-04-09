---
description: In questo argomento vengono fornite le linee guida per l'installazione o la reinstallazione di un'installazione a più istanze di che utilizza le trasformazioni dell'istanza.
ms.assetid: cf9076b1-5674-4ba8-9890-e981221d7b03
title: Installazione di più istanze con le trasformazioni dell'istanza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bae8d73ad60567e1557257c1207558290ba29db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049647"
---
# <a name="installing-multiple-instances-with-instance-transforms"></a><span data-ttu-id="7332f-103">Installazione di più istanze con le trasformazioni dell'istanza</span><span class="sxs-lookup"><span data-stu-id="7332f-103">Installing Multiple Instances with Instance Transforms</span></span>

<span data-ttu-id="7332f-104">In questo argomento vengono fornite le linee guida per l'installazione o la reinstallazione di un'installazione a più istanze di che utilizza le trasformazioni dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="7332f-104">This topic provides guidelines for installing or reinstalling a multiple instance installation that uses instance transforms.</span></span>

-   <span data-ttu-id="7332f-105">Quando si installa una nuova istanza di con una trasformazione istanza, includere la proprietà **MSINEWINSTANCE** e impostare **MSINEWINSTANCE**= 1.</span><span class="sxs-lookup"><span data-stu-id="7332f-105">When installing a new instance with an instance transform, include the **MSINEWINSTANCE** property and set **MSINEWINSTANCE**=1.</span></span>
-   <span data-ttu-id="7332f-106">Quando si installa una nuova istanza di con una trasformazione istanza, includere la proprietà Transforms e impostare la prima trasformazione nell'elenco di trasformazioni nella trasformazione istanza che modifica il codice del prodotto.</span><span class="sxs-lookup"><span data-stu-id="7332f-106">When installing a new instance with an instance transform, include the TRANSFORMS property and set the first transform in the list of transforms to the instance transform that changes the product code.</span></span> <span data-ttu-id="7332f-107">Tutte le trasformazioni di personalizzazione devono seguire la trasformazione istanza all'inizio dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="7332f-107">Any customization transforms should follow the instance transform at the beginning of this list.</span></span>
-   <span data-ttu-id="7332f-108">Il modo più semplice per avviare un'installazione di manutenzione e reinstallare un'istanza di consiste nel fare riferimento al codice prodotto dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="7332f-108">The easiest way to initiate a maintenance installation, and reinstall an instance, is to reference the product code of the instance.</span></span> <span data-ttu-id="7332f-109">Se si avvia l'installazione di manutenzione utilizzando il percorso del pacchetto, è necessario specificare anche il codice prodotto dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="7332f-109">If you initiate the maintenance installation by using the package path, you must also specify the product code of the instance.</span></span> <span data-ttu-id="7332f-110">Dalla riga di comando, usare l'opzione/n {Product code}.</span><span class="sxs-lookup"><span data-stu-id="7332f-110">From the command line, use the /n {Product Code} option.</span></span> <span data-ttu-id="7332f-111">Dal codice o dallo script, usare la proprietà **MSIINSTANCEGUID** .</span><span class="sxs-lookup"><span data-stu-id="7332f-111">From code or script, use the **MSIINSTANCEGUID** property.</span></span>

<span data-ttu-id="7332f-112">Nell'esempio seguente viene illustrata l'installazione di una nuova istanza di da una riga di comando in cui la trasformazione dell'istanza è preceduta da due punti che specificano che la trasformazione è incorporata nel pacchetto.</span><span class="sxs-lookup"><span data-stu-id="7332f-112">The following example shows installing a new instance from a command line where the instance transform is prefixed by a colon which specifies that the transform is embedded in the package.</span></span>

<span data-ttu-id="7332f-113">**msiexec/I mypackage.msi Transforms =: instance. MST MSINEWINSTANCE = 1/QB**</span><span class="sxs-lookup"><span data-stu-id="7332f-113">**msiexec /I mypackage.msi TRANSFORMS=:instance.mst MSINEWINSTANCE=1 /qb**</span></span>

<span data-ttu-id="7332f-114">Nell'esempio seguente viene illustrata l'installazione di una nuova istanza di utilizzando [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta).</span><span class="sxs-lookup"><span data-stu-id="7332f-114">The following example shows installing a new instance using [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta).</span></span>

``` syntax
UINT uiStat = MsiInstallProduct(_T("path to mypackage.msi"), _T("TRANSFORMS=:instance.mst MSINEWINSTANCE=1"));
```

<span data-ttu-id="7332f-115">Nell'esempio seguente viene illustrata l'installazione della nuova istanza da script.</span><span class="sxs-lookup"><span data-stu-id="7332f-115">The following example shows installing the new instance from script.</span></span>

``` syntax
Dim Installer As Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "path to mypackage.msi", "TRANSFORMS=:instance.mst MSINEWINSTANCE=1"
```

<span data-ttu-id="7332f-116">Nell'esempio seguente viene reinstallata un'istanza senza inserire nuovamente il pacchetto nella cache.</span><span class="sxs-lookup"><span data-stu-id="7332f-116">The following example reinstalls an instance without re-caching the package.</span></span> <span data-ttu-id="7332f-117">All'istanza viene fatto riferimento dal codice del prodotto {00000001-0002-0000-0000-624474736554} .</span><span class="sxs-lookup"><span data-stu-id="7332f-117">The instance is referred to by its product code {00000001-0002-0000-0000-624474736554}.</span></span>

<span data-ttu-id="7332f-118">**msiexec/I {00000001-0002-0000-0000-624474736554} REINSTALL = ALL REINSTALLMODE = omus/QB**</span><span class="sxs-lookup"><span data-stu-id="7332f-118">**msiexec /I {00000001-0002-0000-0000-624474736554} REINSTALL=ALL REINSTALLMODE=omus /qb**</span></span>

<span data-ttu-id="7332f-119">Nell'esempio seguente viene reinstallata un'istanza di e il pacchetto viene nuovamente memorizzato nella cache dalla riga di comando.</span><span class="sxs-lookup"><span data-stu-id="7332f-119">The following example reinstalls an instance and re-caches the package from the command line.</span></span> <span data-ttu-id="7332f-120">Il percorso del pacchetto fa riferimento all'istanza.</span><span class="sxs-lookup"><span data-stu-id="7332f-120">The instance is referred to by the package path.</span></span> <span data-ttu-id="7332f-121">Se il prodotto è stato installato originariamente con una trasformazione istanza, è necessario includere l'opzione/n {Product code}.</span><span class="sxs-lookup"><span data-stu-id="7332f-121">You are only required to include the /n {Product Code} option if the product is originally installed with an instance transform.</span></span>

<span data-ttu-id="7332f-122">**msiexec/I c: \\ newpath \\mypackage.msi/N {00000001-0002-0000-0000-624474736554} REINSTALL = ALL REINSTALLMODE = vomus/qb**</span><span class="sxs-lookup"><span data-stu-id="7332f-122">**msiexec /I c:\\newpath\\mypackage.msi /n {00000001-0002-0000-0000-624474736554} REINSTALL=ALL REINSTALLMODE=vomus /qb**</span></span>

<span data-ttu-id="7332f-123">Nell'esempio seguente viene reinstallata un'istanza di e il pacchetto viene memorizzato nella cache utilizzando **MsiInstallProduct**.</span><span class="sxs-lookup"><span data-stu-id="7332f-123">The following example reinstalls an instance and caches the package using **MsiInstallProduct**.</span></span> <span data-ttu-id="7332f-124">Il percorso del pacchetto fa riferimento all'istanza.</span><span class="sxs-lookup"><span data-stu-id="7332f-124">The instance is referred to by the package path.</span></span> <span data-ttu-id="7332f-125">Utilizzare la proprietà **MSIINSTANCEGUID** per fornire il codice prodotto dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="7332f-125">Use the **MSIINSTANCEGUID** property to provide the product code of the instance.</span></span>

``` syntax
UINT uiStat = MsiInstallProduct(_T("path to mypackage.msi"), _T("MSIINSTANCEGUID={00000001-0002-0000-0000-624474736554}  REINSTALL=ALL REINSTALLMODE=vomus"));
```

<span data-ttu-id="7332f-126">Nell'esempio seguente viene reinstallata un'istanza di e il pacchetto viene memorizzato nella cache tramite script.</span><span class="sxs-lookup"><span data-stu-id="7332f-126">The following example reinstalls an instance and caches the package using script.</span></span> <span data-ttu-id="7332f-127">Utilizzare la proprietà **MSIINSTANCEGUID** per fornire il codice prodotto dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="7332f-127">Use the **MSIINSTANCEGUID** property to provide the product code of the instance.</span></span>

``` syntax
Dim Installer As Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "path to mypackage.msi", "MSIINSTANCEGUID={00000001-0002-0000-0000-624474736554}  REINSTALL=ALL REINSTALLMODE=vomus"
```

<span data-ttu-id="7332f-128">Nell'esempio seguente viene illustrato come annunciare un'istanza utilizzando la riga di comando.</span><span class="sxs-lookup"><span data-stu-id="7332f-128">The following example shows how to advertise an instance using the command line.</span></span>

<span data-ttu-id="7332f-129">**msiexec/JM mypackage.msi/t: instance. MST/c/QB**</span><span class="sxs-lookup"><span data-stu-id="7332f-129">**msiexec /jm mypackage.msi /t :instance.mst /c /qb**</span></span>

<span data-ttu-id="7332f-130">Nell'esempio seguente viene illustrato come installare per annunciare un'istanza di utilizzando **MsiAdvertiseProductEx**.</span><span class="sxs-lookup"><span data-stu-id="7332f-130">The following example shows how to install to advertise an instance using **MsiAdvertiseProductEx**.</span></span>

``` syntax
UINT uiStat = MsiAdvertiseProductEx(_T("path to mypackage.msi"), NULL, _T(":instance.mst"), 0, 0, MSIADVERTISEOPTIONS_INSTANCE);
```

<span data-ttu-id="7332f-131">Nell'esempio seguente viene illustrato come applicare una patch a un'istanza da una riga di comando.</span><span class="sxs-lookup"><span data-stu-id="7332f-131">The following example shows how to apply a patch to an instance from a command line.</span></span> <span data-ttu-id="7332f-132">Se il prodotto è stato originariamente installato con una trasformazione istanza, è necessario includere l'opzione/n {Product code}.</span><span class="sxs-lookup"><span data-stu-id="7332f-132">You are only required to include the /n {Product Code} option if the product was originally installed with an instance transform.</span></span>

<span data-ttu-id="7332f-133">**msiexec/p. msp/n {00000001-0002-0000-0000-624474736554} /qb**</span><span class="sxs-lookup"><span data-stu-id="7332f-133">**msiexec /p mypatch.msp /n {00000001-0002-0000-0000-624474736554} /qb**</span></span>

<span data-ttu-id="7332f-134">Nell'esempio seguente viene illustrato come applicare una patch a un'installazione di un'istanza utilizzando [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha).</span><span class="sxs-lookup"><span data-stu-id="7332f-134">The following example shows how to apply a patch to an instance installation using [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha).</span></span>

``` syntax
UINT uiStat = MsiApplyPatch(_T("path to mypatch.msp"), _T("{00000001-0002-0000-0000-624474736554}"), INSTALLTYPE_SINGLE_INSTANCE, _T("REINSTALL=ALL REINSTALLMODE=omus"));
```

<span data-ttu-id="7332f-135">Per ulteriori informazioni, vedere [installazione di più istanze di prodotti e patch](installing-multiple-instances-of-products-and-patches.md) e [creazione di più istanze con le trasformazioni dell'istanza](authoring-multiple-instances-with-instance-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="7332f-135">For more information, see [Installing Multiple Instances of Products and Patches](installing-multiple-instances-of-products-and-patches.md) and [Authoring Multiple Instances with Instance Transforms](authoring-multiple-instances-with-instance-transforms.md).</span></span>

 

 



