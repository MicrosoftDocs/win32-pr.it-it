---
description: Informazioni su Windows Installer concetti che iniziano con la lettera P, ad esempio il codice del pacchetto e l'applicazione di patch.
ms.assetid: 868f5ed3-b179-404b-9462-1d3a179103f8
title: P (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8923359197916a1186fe28ab0d12e4118b989bc
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011103"
---
# <a name="p-windows-installer"></a><span data-ttu-id="bb356-103">P (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="bb356-103">P (Windows Installer)</span></span>

<span data-ttu-id="bb356-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) P [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) T [](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="bb356-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) P [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="bb356-105"><span id="_msi_package_using_windows_installer_gly"></span><span id="_MSI_PACKAGE_USING_WINDOWS_INSTALLER_GLY"></span>**Pacchetto**</span><span class="sxs-lookup"><span data-stu-id="bb356-105"><span id="_msi_package_using_windows_installer_gly"></span><span id="_MSI_PACKAGE_USING_WINDOWS_INSTALLER_GLY"></span>**package**</span></span>
</dt> <dd>

<span data-ttu-id="bb356-106">[*.msi file ed*](m-gly.md) eventuali [*file di origine esterni*](e-gly.md) a cui può fare riferimento questo file.</span><span class="sxs-lookup"><span data-stu-id="bb356-106">[*.msi file*](m-gly.md) and any [*external source files*](e-gly.md) that may be pointed to by this file.</span></span> <span data-ttu-id="bb356-107">Un pacchetto contiene quindi tutte le informazioni necessarie Windows Installer per eseguire l'interfaccia utente e per installare o disinstallare l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bb356-107">A package therefore contains all the information the Windows Installer needs to run the UI and to install or uninstall the application.</span></span> <span data-ttu-id="bb356-108">Per altre informazioni, vedere anche database [*del programma di installazione.*](i-gly.md)</span><span class="sxs-lookup"><span data-stu-id="bb356-108">For more information, see also [*installer database*](i-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb356-109"><span id="_msi_package_code_gly"></span><span id="_MSI_PACKAGE_CODE_GLY"></span>**codice del pacchetto**</span><span class="sxs-lookup"><span data-stu-id="bb356-109"><span id="_msi_package_code_gly"></span><span id="_MSI_PACKAGE_CODE_GLY"></span>**package code**</span></span>
</dt> <dd>

<span data-ttu-id="bb356-110">GUID che identifica un pacchetto specifico.</span><span class="sxs-lookup"><span data-stu-id="bb356-110">GUID that identifies a particular package.</span></span> <span data-ttu-id="bb356-111">È necessario un codice di pacchetto univoco perché alcune trasformazioni o pacchetti di patch possono essere applicati a più di un'applicazione o aggiornare un'applicazione in un'altra applicazione o versione.</span><span class="sxs-lookup"><span data-stu-id="bb356-111">A unique package code is required because some transforms or patch packages can be applied to more than one application or can upgrade an application into another application or version.</span></span> <span data-ttu-id="bb356-112">Per altre informazioni, vedere [Codici di pacchetto.](package-codes.md)</span><span class="sxs-lookup"><span data-stu-id="bb356-112">For more information, see [Package Codes](package-codes.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb356-113"><span id="_msi_patching_gly"></span><span id="_MSI_PATCHING_GLY"></span>**Patch**</span><span class="sxs-lookup"><span data-stu-id="bb356-113"><span id="_msi_patching_gly"></span><span id="_MSI_PATCHING_GLY"></span>**patching**</span></span>
</dt> <dd>

<span data-ttu-id="bb356-114">Metodo di aggiornamento di un file che sostituisce solo i bit modificati, anziché l'intero file.</span><span class="sxs-lookup"><span data-stu-id="bb356-114">Method of updating a file that replaces only the bits being changed, rather than the entire file.</span></span> <span data-ttu-id="bb356-115">Ciò significa che gli utenti possono scaricare una patch di aggiornamento per un prodotto molto più piccolo dell'intero prodotto.</span><span class="sxs-lookup"><span data-stu-id="bb356-115">This means that users can download an upgrade patch for a product that is much smaller than the entire product.</span></span> <span data-ttu-id="bb356-116">Per altre informazioni, vedere [Patch Packages](patch-packages.md).</span><span class="sxs-lookup"><span data-stu-id="bb356-116">For more information, see [Patch Packages](patch-packages.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb356-117"><span id="_msi_patch_file_gly"></span><span id="_MSI_PATCH_FILE_GLY"></span>**file di patch**</span><span class="sxs-lookup"><span data-stu-id="bb356-117"><span id="_msi_patch_file_gly"></span><span id="_MSI_PATCH_FILE_GLY"></span>**patch file**</span></span>
</dt> <dd>

<span data-ttu-id="bb356-118">Pacchetto [P atch usato](patch-packages.md) per l'applicazione di patch.</span><span class="sxs-lookup"><span data-stu-id="bb356-118">P [atch package](patch-packages.md) used for patching.</span></span> <span data-ttu-id="bb356-119">Per altre informazioni, vedere [Applicazione di patch e aggiornamenti.](patching-and-upgrades.md)</span><span class="sxs-lookup"><span data-stu-id="bb356-119">For more information, see [Patching and Upgrades](patching-and-upgrades.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb356-120"><span id="_msi_preview_mode_using_windows_installer_gly"></span><span id="_MSI_PREVIEW_MODE_USING_WINDOWS_INSTALLER_GLY"></span>**modalità di anteprima**</span><span class="sxs-lookup"><span data-stu-id="bb356-120"><span id="_msi_preview_mode_using_windows_installer_gly"></span><span id="_MSI_PREVIEW_MODE_USING_WINDOWS_INSTALLER_GLY"></span>**preview mode**</span></span>
</dt> <dd>

<span data-ttu-id="bb356-121">Modalità per la visualizzazione della progettazione dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="bb356-121">Mode for viewing the design of the UI.</span></span> <span data-ttu-id="bb356-122">Per altre informazioni, vedere [Anteprima del Interfaccia utente](previewing-the-user-interface.md).</span><span class="sxs-lookup"><span data-stu-id="bb356-122">For more information, see [Previewing the User Interface](previewing-the-user-interface.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb356-123"><span id="_msi_progress_bar_gly"></span><span id="_MSI_PROGRESS_BAR_GLY"></span>**Indicatore**</span><span class="sxs-lookup"><span data-stu-id="bb356-123"><span id="_msi_progress_bar_gly"></span><span id="_MSI_PROGRESS_BAR_GLY"></span>**progress bar**</span></span>
</dt> <dd>

<span data-ttu-id="bb356-124">Controllare che il programma di installazione possa essere visualizzato durante l'esecuzione dello script che rappresenta lo stato di avanzamento dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="bb356-124">Control the installer can display during script execution time representing the progress of the installation.</span></span> <span data-ttu-id="bb356-125">Per altre informazioni, vedere [Creazione di un controllo ProgressBar.](authoring-a-progressbar-control.md)</span><span class="sxs-lookup"><span data-stu-id="bb356-125">For more information, see [Authoring a ProgressBar Control](authoring-a-progressbar-control.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb356-126"><span id="_msi_property_gly"></span><span id="_MSI_PROPERTY_GLY"></span>**Proprietà**</span><span class="sxs-lookup"><span data-stu-id="bb356-126"><span id="_msi_property_gly"></span><span id="_MSI_PROPERTY_GLY"></span>**property**</span></span>
</dt> <dd>

<span data-ttu-id="bb356-127">Variabili globali usate durante un'installazione.</span><span class="sxs-lookup"><span data-stu-id="bb356-127">Global variables used during an installation.</span></span> <span data-ttu-id="bb356-128">Vedere [Informazioni sulle proprietà.](about-properties.md)</span><span class="sxs-lookup"><span data-stu-id="bb356-128">(See [About Properties](about-properties.md).)</span></span>

<span data-ttu-id="bb356-129">Il termine "proprietà" si riferisce anche a un attributo di un oggetto di automazione.</span><span class="sxs-lookup"><span data-stu-id="bb356-129">The term "property" also refers to an attribute of an automation object.</span></span> <span data-ttu-id="bb356-130">Vedere Interfaccia [di automazione.](automation-interface.md)</span><span class="sxs-lookup"><span data-stu-id="bb356-130">(See [Automation Interface](automation-interface.md).)</span></span>

</dd> <dt>

<span data-ttu-id="bb356-131"><span id="_msi_publishing_gly"></span><span id="_MSI_PUBLISHING_GLY"></span>**Pubblicazione**</span><span class="sxs-lookup"><span data-stu-id="bb356-131"><span id="_msi_publishing_gly"></span><span id="_MSI_PUBLISHING_GLY"></span>**publishing**</span></span>
</dt> <dd>

<span data-ttu-id="bb356-132">Metodo di [*annuncio di*](a-gly.md) una funzionalità o di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bb356-132">Method of [*advertising*](a-gly.md) a feature or application.</span></span> <span data-ttu-id="bb356-133">La pubblicazione non popola l'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="bb356-133">Publishing does not populate the UI.</span></span> <span data-ttu-id="bb356-134">Tuttavia, se un'altra applicazione tenta di aprire un'applicazione pubblicata, sono disponibili informazioni sufficienti per il programma di installazione per assegnare l'applicazione pubblicata.</span><span class="sxs-lookup"><span data-stu-id="bb356-134">However, if another application attempts to open a published application, there is enough information present for the installer to assign the published application.</span></span> <span data-ttu-id="bb356-135">Per altre informazioni, vedere [*Assegnazione di*](a-gly.md) componenti [e funzionalità.](components-and-features.md)</span><span class="sxs-lookup"><span data-stu-id="bb356-135">For more information, see [*assigning*](a-gly.md) and [Components and Features](components-and-features.md).</span></span>

</dd> </dl>

 

 



