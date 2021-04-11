---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ms.assetid: f98d19c5-5187-4718-b241-3ec69454c2d6
title: C (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1970c8e9063657701183c91ff337d06d169914fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227201"
---
# <a name="c-windows-installer"></a><span data-ttu-id="59848-103">C (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="59848-103">C (Windows Installer)</span></span>

<span data-ttu-id="59848-104">[A](a-gly.md) [B](b-gly.md) C [d](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [i](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="59848-104">[A](a-gly.md) [B](b-gly.md) C [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="59848-105"><span id="_msi_cabinet_file_using_windows_installer_gly"></span><span id="_MSI_CABINET_FILE_USING_WINDOWS_INSTALLER_GLY"></span>**file CAB**</span><span class="sxs-lookup"><span data-stu-id="59848-105"><span id="_msi_cabinet_file_using_windows_installer_gly"></span><span id="_MSI_CABINET_FILE_USING_WINDOWS_INSTALLER_GLY"></span>**cabinet file**</span></span>
</dt> <dd>

<span data-ttu-id="59848-106">Singolo file, in genere con estensione cab, che archivia i file compressi in una libreria di file.</span><span class="sxs-lookup"><span data-stu-id="59848-106">Single file, usually with a .cab extension, that stores compressed files in a file library.</span></span> <span data-ttu-id="59848-107">Il formato CAB è un modo efficiente per creare un pacchetto di più file perché la compressione viene eseguita tra i limiti dei file, migliorando significativamente il rapporto di compressione.</span><span class="sxs-lookup"><span data-stu-id="59848-107">The cabinet format is an efficient way to package multiple files because compression is performed across file boundaries, significantly improving compression ratio.</span></span> <span data-ttu-id="59848-108">Per informazioni sulla creazione di file CAB, vedere [file CAB](cabinet-files.md).</span><span class="sxs-lookup"><span data-stu-id="59848-108">For information about creating cabinets, see [Cabinet Files](cabinet-files.md).</span></span>

</dd> <dt>

<span data-ttu-id="59848-109"><span id="_msi_checksum_gly"></span><span id="_MSI_CHECKSUM_GLY"></span>**checksum**</span><span class="sxs-lookup"><span data-stu-id="59848-109"><span id="_msi_checksum_gly"></span><span id="_MSI_CHECKSUM_GLY"></span>**checksum**</span></span>
</dt> <dd>

<span data-ttu-id="59848-110">Valore calcolato che dipende dal contenuto di un file.</span><span class="sxs-lookup"><span data-stu-id="59848-110">Computed value that depends on the contents of a file.</span></span> <span data-ttu-id="59848-111">Viene archiviato con i dati per rilevare il danneggiamento del file.</span><span class="sxs-lookup"><span data-stu-id="59848-111">It is stored with data to detect file corruption.</span></span> <span data-ttu-id="59848-112">Il sistema controlla questo valore per assicurarsi che i dati non siano danneggiati.</span><span class="sxs-lookup"><span data-stu-id="59848-112">The system checks this value to ensure that the data is uncorrupted.</span></span>

</dd> <dt>

<span data-ttu-id="59848-113"><span id="_msi_component_using_windows_installer_gly"></span><span id="_MSI_COMPONENT_USING_WINDOWS_INSTALLER_GLY"></span>**componente**</span><span class="sxs-lookup"><span data-stu-id="59848-113"><span id="_msi_component_using_windows_installer_gly"></span><span id="_MSI_COMPONENT_USING_WINDOWS_INSTALLER_GLY"></span>**component**</span></span>
</dt> <dd>

<span data-ttu-id="59848-114">Parte più piccola di un'installazione gestita dal programma di installazione, anche un blocco di compilazione di un'applicazione o di una funzionalità dal punto di vista del programmatore.</span><span class="sxs-lookup"><span data-stu-id="59848-114">Smallest piece of an installation handled by the installer, also a building-block of an application or feature from the programmer's perspective.</span></span> <span data-ttu-id="59848-115">Esempi di componenti sono un gruppo di file correlati, un oggetto COM o una libreria.</span><span class="sxs-lookup"><span data-stu-id="59848-115">Examples of components are a group of related files, a COM object, or a library.</span></span> <span data-ttu-id="59848-116">Per ulteriori informazioni, vedere [componenti e funzionalità](components-and-features.md).</span><span class="sxs-lookup"><span data-stu-id="59848-116">For more information, see [Components and Features](components-and-features.md).</span></span>

</dd> <dt>

<span data-ttu-id="59848-117"><span id="_msi_committing_databases_using_windows_installer_gly"></span><span id="_MSI_COMMITTING_DATABASES_USING_WINDOWS_INSTALLER_GLY"></span>**commit dei database**</span><span class="sxs-lookup"><span data-stu-id="59848-117"><span id="_msi_committing_databases_using_windows_installer_gly"></span><span id="_MSI_COMMITTING_DATABASES_USING_WINDOWS_INSTALLER_GLY"></span>**committing databases**</span></span>
</dt> <dd>

<span data-ttu-id="59848-118">Modifiche accumulate apportate in un database.</span><span class="sxs-lookup"><span data-stu-id="59848-118">Accumulated changes made in a database.</span></span> <span data-ttu-id="59848-119">Le modifiche non vengono riflesse nel database effettivo fino a quando non viene eseguito il commit del database.</span><span class="sxs-lookup"><span data-stu-id="59848-119">The changes are not reflected in the actual database until the database is committed.</span></span> <span data-ttu-id="59848-120">Per ulteriori informazioni, vedere [commit dei database](committing-databases.md).</span><span class="sxs-lookup"><span data-stu-id="59848-120">For more information, see [Committing Databases](committing-databases.md).</span></span>

</dd> <dt>

<span data-ttu-id="59848-121"><span id="_msi_controlevent_gly"></span><span id="_MSI_CONTROLEVENT_GLY"></span>**ControlEvent**</span><span class="sxs-lookup"><span data-stu-id="59848-121"><span id="_msi_controlevent_gly"></span><span id="_MSI_CONTROLEVENT_GLY"></span>**ControlEvent**</span></span>
</dt> <dd>

<span data-ttu-id="59848-122">Aspetto della funzionalità dell'interfaccia utente del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="59848-122">Aspect of functionality of the installer's user interface.</span></span> <span data-ttu-id="59848-123">Un ControlEvent tipico attiva un'azione da parte del programma di installazione al momento dell'attivazione di un controllo della finestra di dialogo o di un altro evento.</span><span class="sxs-lookup"><span data-stu-id="59848-123">A typical ControlEvent triggers some action by the installer upon the activation of a dialog box control or other event.</span></span> <span data-ttu-id="59848-124">Per altre informazioni, vedere [Panoramica di ControlEvent](controlevent-overview.md).</span><span class="sxs-lookup"><span data-stu-id="59848-124">For more information, see [ControlEvent Overview](controlevent-overview.md).</span></span>

</dd> <dt>

<span data-ttu-id="59848-125"><span id="_msi_costing_gly"></span><span id="_MSI_COSTING_GLY"></span>**costano**</span><span class="sxs-lookup"><span data-stu-id="59848-125"><span id="_msi_costing_gly"></span><span id="_MSI_COSTING_GLY"></span>**costing**</span></span>
</dt> <dd>

<span data-ttu-id="59848-126">Metodo utilizzato dal programma di installazione per determinare i requisiti di spazio su disco per l'installazione.</span><span class="sxs-lookup"><span data-stu-id="59848-126">Method used by the installer to determine disk space requirements for installation.</span></span> <span data-ttu-id="59848-127">Il costo prende in considerazione i fattori, ad esempio se i file esistenti devono essere sovrascritti.</span><span class="sxs-lookup"><span data-stu-id="59848-127">Costing takes into account factors such as whether existing files need to be overwritten.</span></span> <span data-ttu-id="59848-128">Per altre informazioni, vedere [costi](file-costing.md)per i file.</span><span class="sxs-lookup"><span data-stu-id="59848-128">For more information, see [File Costing](file-costing.md).</span></span>

</dd> <dt>

<span data-ttu-id="59848-129"><span id="_msi_.cub_file_gly"></span><span id="_MSI_.CUB_FILE_GLY"></span>**file con estensione cub**</span><span class="sxs-lookup"><span data-stu-id="59848-129"><span id="_msi_.cub_file_gly"></span><span id="_MSI_.CUB_FILE_GLY"></span>**.cub file**</span></span>
</dt> <dd>

<span data-ttu-id="59848-130">Modulo di convalida che archivia e fornisce l'accesso alle azioni personalizzate di ICE.</span><span class="sxs-lookup"><span data-stu-id="59848-130">Validation module that stores and provides access to ICE custom actions.</span></span> <span data-ttu-id="59848-131">Per altre informazioni, vedere [file Sample. cub](sample--cub-file.md).</span><span class="sxs-lookup"><span data-stu-id="59848-131">For more information, see [Sample .cub File](sample--cub-file.md).</span></span> <span data-ttu-id="59848-132">Per ulteriori informazioni, vedere anche [Windows Installer estensioni di file](windows-installer-file-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="59848-132">For more information, see also [Windows Installer File Extensions](windows-installer-file-extensions.md).</span></span>

</dd> <dt>

<span data-ttu-id="59848-133"><span id="_msi_custom_action_using_windows_installer_gly"></span><span id="_MSI_CUSTOM_ACTION_USING_WINDOWS_INSTALLER_GLY"></span>**azione personalizzata**</span><span class="sxs-lookup"><span data-stu-id="59848-133"><span id="_msi_custom_action_using_windows_installer_gly"></span><span id="_MSI_CUSTOM_ACTION_USING_WINDOWS_INSTALLER_GLY"></span>**custom action**</span></span>
</dt> <dd>

<span data-ttu-id="59848-134">Scritto dall'autore del [*pacchetto*](p-gly.md) , ma non incorporato nel programma di installazione come azione standard.</span><span class="sxs-lookup"><span data-stu-id="59848-134">Written by the author of the [*package*](p-gly.md) but not built into the installer as a standard action.</span></span> <span data-ttu-id="59848-135">Per altre informazioni, vedere [azioni personalizzate](custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="59848-135">For more information, see [Custom Actions](custom-actions.md).</span></span>

</dd> </dl>

 

 



