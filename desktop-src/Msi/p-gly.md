---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ms.assetid: 868f5ed3-b179-404b-9462-1d3a179103f8
title: P (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a4e6b8f1343fdd68f4a6ce042852cff1e28e05c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131475"
---
# <a name="p-windows-installer"></a><span data-ttu-id="18ebf-103">P (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="18ebf-103">P (Windows Installer)</span></span>

<span data-ttu-id="18ebf-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [d](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [i](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) P [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="18ebf-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) P [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="18ebf-105"><span id="_msi_package_using_windows_installer_gly"></span><span id="_MSI_PACKAGE_USING_WINDOWS_INSTALLER_GLY"></span>**pacchetto**</span><span class="sxs-lookup"><span data-stu-id="18ebf-105"><span id="_msi_package_using_windows_installer_gly"></span><span id="_MSI_PACKAGE_USING_WINDOWS_INSTALLER_GLY"></span>**package**</span></span>
</dt> <dd>

<span data-ttu-id="18ebf-106">[*file con estensione msi*](m-gly.md) ed eventuali [*file di origine esterni*](e-gly.md) a cui il file può fare riferimento.</span><span class="sxs-lookup"><span data-stu-id="18ebf-106">[*.msi file*](m-gly.md) and any [*external source files*](e-gly.md) that may be pointed to by this file.</span></span> <span data-ttu-id="18ebf-107">Un pacchetto contiene pertanto tutte le informazioni necessarie per l'Windows Installer l'esecuzione dell'interfaccia utente e per l'installazione o la disinstallazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="18ebf-107">A package therefore contains all the information the Windows Installer needs to run the UI and to install or uninstall the application.</span></span> <span data-ttu-id="18ebf-108">Per ulteriori informazioni, vedere anche [*database del programma di installazione*](i-gly.md).</span><span class="sxs-lookup"><span data-stu-id="18ebf-108">For more information, see also [*installer database*](i-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="18ebf-109"><span id="_msi_package_code_gly"></span><span id="_MSI_PACKAGE_CODE_GLY"></span>**codice pacchetto**</span><span class="sxs-lookup"><span data-stu-id="18ebf-109"><span id="_msi_package_code_gly"></span><span id="_MSI_PACKAGE_CODE_GLY"></span>**package code**</span></span>
</dt> <dd>

<span data-ttu-id="18ebf-110">GUID che identifica un pacchetto specifico.</span><span class="sxs-lookup"><span data-stu-id="18ebf-110">GUID that identifies a particular package.</span></span> <span data-ttu-id="18ebf-111">È necessario un codice di pacchetto univoco perché alcune trasformazioni o pacchetti di patch possono essere applicati a più di un'applicazione o possono aggiornare un'applicazione in un'altra applicazione o versione.</span><span class="sxs-lookup"><span data-stu-id="18ebf-111">A unique package code is required because some transforms or patch packages can be applied to more than one application or can upgrade an application into another application or version.</span></span> <span data-ttu-id="18ebf-112">Per ulteriori informazioni, vedere [codici di pacchetto](package-codes.md).</span><span class="sxs-lookup"><span data-stu-id="18ebf-112">For more information, see [Package Codes](package-codes.md).</span></span>

</dd> <dt>

<span data-ttu-id="18ebf-113"><span id="_msi_patching_gly"></span><span id="_MSI_PATCHING_GLY"></span>**patch**</span><span class="sxs-lookup"><span data-stu-id="18ebf-113"><span id="_msi_patching_gly"></span><span id="_MSI_PATCHING_GLY"></span>**patching**</span></span>
</dt> <dd>

<span data-ttu-id="18ebf-114">Metodo di aggiornamento di un file che sostituisce solo i bit modificati, anziché l'intero file.</span><span class="sxs-lookup"><span data-stu-id="18ebf-114">Method of updating a file that replaces only the bits being changed, rather than the entire file.</span></span> <span data-ttu-id="18ebf-115">Questo significa che gli utenti possono scaricare una patch di aggiornamento per un prodotto molto più piccolo dell'intero prodotto.</span><span class="sxs-lookup"><span data-stu-id="18ebf-115">This means that users can download an upgrade patch for a product that is much smaller than the entire product.</span></span> <span data-ttu-id="18ebf-116">Per ulteriori informazioni, vedere la pagina relativa ai [pacchetti di patch](patch-packages.md).</span><span class="sxs-lookup"><span data-stu-id="18ebf-116">For more information, see [Patch Packages](patch-packages.md).</span></span>

</dd> <dt>

<span data-ttu-id="18ebf-117"><span id="_msi_patch_file_gly"></span><span id="_MSI_PATCH_FILE_GLY"></span>**file patch**</span><span class="sxs-lookup"><span data-stu-id="18ebf-117"><span id="_msi_patch_file_gly"></span><span id="_MSI_PATCH_FILE_GLY"></span>**patch file**</span></span>
</dt> <dd>

<span data-ttu-id="18ebf-118">P [prodotto pacchetto](patch-packages.md) usato per l'applicazione di patch.</span><span class="sxs-lookup"><span data-stu-id="18ebf-118">P [atch package](patch-packages.md) used for patching.</span></span> <span data-ttu-id="18ebf-119">Per ulteriori informazioni, vedere applicazione di [patch e aggiornamenti](patching-and-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="18ebf-119">For more information, see [Patching and Upgrades](patching-and-upgrades.md).</span></span>

</dd> <dt>

<span data-ttu-id="18ebf-120"><span id="_msi_preview_mode_using_windows_installer_gly"></span><span id="_MSI_PREVIEW_MODE_USING_WINDOWS_INSTALLER_GLY"></span>**modalità anteprima**</span><span class="sxs-lookup"><span data-stu-id="18ebf-120"><span id="_msi_preview_mode_using_windows_installer_gly"></span><span id="_MSI_PREVIEW_MODE_USING_WINDOWS_INSTALLER_GLY"></span>**preview mode**</span></span>
</dt> <dd>

<span data-ttu-id="18ebf-121">Modalità per la visualizzazione della progettazione dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="18ebf-121">Mode for viewing the design of the UI.</span></span> <span data-ttu-id="18ebf-122">Per ulteriori informazioni, vedere [anteprima dell'interfaccia utente](previewing-the-user-interface.md).</span><span class="sxs-lookup"><span data-stu-id="18ebf-122">For more information, see [Previewing the User Interface](previewing-the-user-interface.md).</span></span>

</dd> <dt>

<span data-ttu-id="18ebf-123"><span id="_msi_progress_bar_gly"></span><span id="_MSI_PROGRESS_BAR_GLY"></span>**indicatore di stato**</span><span class="sxs-lookup"><span data-stu-id="18ebf-123"><span id="_msi_progress_bar_gly"></span><span id="_MSI_PROGRESS_BAR_GLY"></span>**progress bar**</span></span>
</dt> <dd>

<span data-ttu-id="18ebf-124">Controllo che il programma di installazione può visualizzare durante l'esecuzione dello script che rappresenta lo stato di avanzamento dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="18ebf-124">Control the installer can display during script execution time representing the progress of the installation.</span></span> <span data-ttu-id="18ebf-125">Per ulteriori informazioni, vedere la pagina relativa alla [creazione di un controllo ProgressBar](authoring-a-progressbar-control.md).</span><span class="sxs-lookup"><span data-stu-id="18ebf-125">For more information, see [Authoring a ProgressBar Control](authoring-a-progressbar-control.md).</span></span>

</dd> <dt>

<span data-ttu-id="18ebf-126"><span id="_msi_property_gly"></span><span id="_MSI_PROPERTY_GLY"></span>**Proprietà**</span><span class="sxs-lookup"><span data-stu-id="18ebf-126"><span id="_msi_property_gly"></span><span id="_MSI_PROPERTY_GLY"></span>**property**</span></span>
</dt> <dd>

<span data-ttu-id="18ebf-127">Variabili globali utilizzate durante un'installazione.</span><span class="sxs-lookup"><span data-stu-id="18ebf-127">Global variables used during an installation.</span></span> <span data-ttu-id="18ebf-128">Vedere [informazioni sulle proprietà](about-properties.md).</span><span class="sxs-lookup"><span data-stu-id="18ebf-128">(See [About Properties](about-properties.md).)</span></span>

<span data-ttu-id="18ebf-129">Il termine "Property" si riferisce anche a un attributo di un oggetto di automazione.</span><span class="sxs-lookup"><span data-stu-id="18ebf-129">The term "property" also refers to an attribute of an automation object.</span></span> <span data-ttu-id="18ebf-130">(Vedere [interfaccia di automazione](automation-interface.md)).</span><span class="sxs-lookup"><span data-stu-id="18ebf-130">(See [Automation Interface](automation-interface.md).)</span></span>

</dd> <dt>

<span data-ttu-id="18ebf-131"><span id="_msi_publishing_gly"></span><span id="_MSI_PUBLISHING_GLY"></span>**editrice**</span><span class="sxs-lookup"><span data-stu-id="18ebf-131"><span id="_msi_publishing_gly"></span><span id="_MSI_PUBLISHING_GLY"></span>**publishing**</span></span>
</dt> <dd>

<span data-ttu-id="18ebf-132">Metodo di [*annuncio*](a-gly.md) di una funzionalità o di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="18ebf-132">Method of [*advertising*](a-gly.md) a feature or application.</span></span> <span data-ttu-id="18ebf-133">La pubblicazione non popola l'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="18ebf-133">Publishing does not populate the UI.</span></span> <span data-ttu-id="18ebf-134">Tuttavia, se un'altra applicazione tenta di aprire un'applicazione pubblicata, per il programma di installazione sono disponibili informazioni sufficienti per l'assegnazione dell'applicazione pubblicata.</span><span class="sxs-lookup"><span data-stu-id="18ebf-134">However, if another application attempts to open a published application, there is enough information present for the installer to assign the published application.</span></span> <span data-ttu-id="18ebf-135">Per ulteriori informazioni, vedere [*assegnazione*](a-gly.md) di [componenti e funzionalità](components-and-features.md).</span><span class="sxs-lookup"><span data-stu-id="18ebf-135">For more information, see [*assigning*](a-gly.md) and [Components and Features](components-and-features.md).</span></span>

</dd> </dl>

 

 



