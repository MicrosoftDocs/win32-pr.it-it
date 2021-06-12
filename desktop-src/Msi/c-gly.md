---
description: Informazioni sui Windows Installer concetti che iniziano con la lettera C, ad esempio file cab e checksum.
ms.assetid: f98d19c5-5187-4718-b241-3ec69454c2d6
title: C (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47e7af99ad32d8dff7f4e8509976b0004045477b
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010924"
---
# <a name="c-windows-installer"></a><span data-ttu-id="331c6-103">C (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="331c6-103">C (Windows Installer)</span></span>

<span data-ttu-id="331c6-104">[A](a-gly.md) [B](b-gly.md) C [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P Q](p-gly.md) [](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="331c6-104">[A](a-gly.md) [B](b-gly.md) C [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="331c6-105"><span id="_msi_cabinet_file_using_windows_installer_gly"></span><span id="_MSI_CABINET_FILE_USING_WINDOWS_INSTALLER_GLY"></span>**file cab**</span><span class="sxs-lookup"><span data-stu-id="331c6-105"><span id="_msi_cabinet_file_using_windows_installer_gly"></span><span id="_MSI_CABINET_FILE_USING_WINDOWS_INSTALLER_GLY"></span>**cabinet file**</span></span>
</dt> <dd>

<span data-ttu-id="331c6-106">Singolo file, in genere con un'.cab, che archivia i file compressi in una libreria di file.</span><span class="sxs-lookup"><span data-stu-id="331c6-106">Single file, usually with a .cab extension, that stores compressed files in a file library.</span></span> <span data-ttu-id="331c6-107">Il formato cab è un modo efficiente per creare un pacchetto di più file perché la compressione viene eseguita tra i limiti dei file, migliorando in modo significativo il rapporto di compressione.</span><span class="sxs-lookup"><span data-stu-id="331c6-107">The cabinet format is an efficient way to package multiple files because compression is performed across file boundaries, significantly improving compression ratio.</span></span> <span data-ttu-id="331c6-108">Per informazioni sulla creazione di file cab, vedere [File CAB](cabinet-files.md).</span><span class="sxs-lookup"><span data-stu-id="331c6-108">For information about creating cabinets, see [Cabinet Files](cabinet-files.md).</span></span>

</dd> <dt>

<span data-ttu-id="331c6-109"><span id="_msi_checksum_gly"></span><span id="_MSI_CHECKSUM_GLY"></span>**Checksum**</span><span class="sxs-lookup"><span data-stu-id="331c6-109"><span id="_msi_checksum_gly"></span><span id="_MSI_CHECKSUM_GLY"></span>**checksum**</span></span>
</dt> <dd>

<span data-ttu-id="331c6-110">Valore calcolato che dipende dal contenuto di un file.</span><span class="sxs-lookup"><span data-stu-id="331c6-110">Computed value that depends on the contents of a file.</span></span> <span data-ttu-id="331c6-111">Viene archiviato con i dati per rilevare il danneggiamento dei file.</span><span class="sxs-lookup"><span data-stu-id="331c6-111">It is stored with data to detect file corruption.</span></span> <span data-ttu-id="331c6-112">Il sistema controlla questo valore per assicurarsi che i dati non siano interrotta.</span><span class="sxs-lookup"><span data-stu-id="331c6-112">The system checks this value to ensure that the data is uncorrupted.</span></span>

</dd> <dt>

<span data-ttu-id="331c6-113"><span id="_msi_component_using_windows_installer_gly"></span><span id="_MSI_COMPONENT_USING_WINDOWS_INSTALLER_GLY"></span>**Componente**</span><span class="sxs-lookup"><span data-stu-id="331c6-113"><span id="_msi_component_using_windows_installer_gly"></span><span id="_MSI_COMPONENT_USING_WINDOWS_INSTALLER_GLY"></span>**component**</span></span>
</dt> <dd>

<span data-ttu-id="331c6-114">Parte più piccola di un'installazione gestita dal programma di installazione, anche un blocco predefinito di un'applicazione o di una funzionalità dal punto di vista del programmatore.</span><span class="sxs-lookup"><span data-stu-id="331c6-114">Smallest piece of an installation handled by the installer, also a building-block of an application or feature from the programmer's perspective.</span></span> <span data-ttu-id="331c6-115">Esempi di componenti sono un gruppo di file correlati, un oggetto COM o una libreria.</span><span class="sxs-lookup"><span data-stu-id="331c6-115">Examples of components are a group of related files, a COM object, or a library.</span></span> <span data-ttu-id="331c6-116">Per altre informazioni, vedere [Componenti e funzionalità](components-and-features.md).</span><span class="sxs-lookup"><span data-stu-id="331c6-116">For more information, see [Components and Features](components-and-features.md).</span></span>

</dd> <dt>

<span data-ttu-id="331c6-117"><span id="_msi_committing_databases_using_windows_installer_gly"></span><span id="_MSI_COMMITTING_DATABASES_USING_WINDOWS_INSTALLER_GLY"></span>**commit di database**</span><span class="sxs-lookup"><span data-stu-id="331c6-117"><span id="_msi_committing_databases_using_windows_installer_gly"></span><span id="_MSI_COMMITTING_DATABASES_USING_WINDOWS_INSTALLER_GLY"></span>**committing databases**</span></span>
</dt> <dd>

<span data-ttu-id="331c6-118">Modifiche accumulate apportate in un database.</span><span class="sxs-lookup"><span data-stu-id="331c6-118">Accumulated changes made in a database.</span></span> <span data-ttu-id="331c6-119">Le modifiche vengono riflesse nel database effettivo solo dopo il commit del database.</span><span class="sxs-lookup"><span data-stu-id="331c6-119">The changes are not reflected in the actual database until the database is committed.</span></span> <span data-ttu-id="331c6-120">Per altre informazioni, vedere [Commit di database](committing-databases.md).</span><span class="sxs-lookup"><span data-stu-id="331c6-120">For more information, see [Committing Databases](committing-databases.md).</span></span>

</dd> <dt>

<span data-ttu-id="331c6-121"><span id="_msi_controlevent_gly"></span><span id="_MSI_CONTROLEVENT_GLY"></span>**ControlEvent**</span><span class="sxs-lookup"><span data-stu-id="331c6-121"><span id="_msi_controlevent_gly"></span><span id="_MSI_CONTROLEVENT_GLY"></span>**ControlEvent**</span></span>
</dt> <dd>

<span data-ttu-id="331c6-122">Aspetto della funzionalità dell'interfaccia utente del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="331c6-122">Aspect of functionality of the installer's user interface.</span></span> <span data-ttu-id="331c6-123">Un tipico ControlEvent attiva un'azione da parte del programma di installazione all'attivazione di un controllo della finestra di dialogo o di un altro evento.</span><span class="sxs-lookup"><span data-stu-id="331c6-123">A typical ControlEvent triggers some action by the installer upon the activation of a dialog box control or other event.</span></span> <span data-ttu-id="331c6-124">Per altre informazioni, vedere [Cenni preliminari su ControlEvent](controlevent-overview.md).</span><span class="sxs-lookup"><span data-stu-id="331c6-124">For more information, see [ControlEvent Overview](controlevent-overview.md).</span></span>

</dd> <dt>

<span data-ttu-id="331c6-125"><span id="_msi_costing_gly"></span><span id="_MSI_COSTING_GLY"></span>**Costano**</span><span class="sxs-lookup"><span data-stu-id="331c6-125"><span id="_msi_costing_gly"></span><span id="_MSI_COSTING_GLY"></span>**costing**</span></span>
</dt> <dd>

<span data-ttu-id="331c6-126">Metodo usato dal programma di installazione per determinare i requisiti di spazio su disco per l'installazione.</span><span class="sxs-lookup"><span data-stu-id="331c6-126">Method used by the installer to determine disk space requirements for installation.</span></span> <span data-ttu-id="331c6-127">La determinazione dei costi tiene conto di fattori quali la necessità di sovrascrittura dei file esistenti.</span><span class="sxs-lookup"><span data-stu-id="331c6-127">Costing takes into account factors such as whether existing files need to be overwritten.</span></span> <span data-ttu-id="331c6-128">Per altre informazioni, vedere [Determinazione dei costi dei file.](file-costing.md)</span><span class="sxs-lookup"><span data-stu-id="331c6-128">For more information, see [File Costing](file-costing.md).</span></span>

</dd> <dt>

<span data-ttu-id="331c6-129"><span id="_msi_.cub_file_gly"></span><span id="_MSI_.CUB_FILE_GLY"></span>**File con estensione cub**</span><span class="sxs-lookup"><span data-stu-id="331c6-129"><span id="_msi_.cub_file_gly"></span><span id="_MSI_.CUB_FILE_GLY"></span>**.cub file**</span></span>
</dt> <dd>

<span data-ttu-id="331c6-130">Modulo di convalida che archivia e fornisce l'accesso alle azioni personalizzate ICE.</span><span class="sxs-lookup"><span data-stu-id="331c6-130">Validation module that stores and provides access to ICE custom actions.</span></span> <span data-ttu-id="331c6-131">Per altre informazioni, vedere [File con estensione cub di esempio.](sample--cub-file.md)</span><span class="sxs-lookup"><span data-stu-id="331c6-131">For more information, see [Sample .cub File](sample--cub-file.md).</span></span> <span data-ttu-id="331c6-132">Per altre informazioni, vedere anche Windows Installer [file .](windows-installer-file-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="331c6-132">For more information, see also [Windows Installer File Extensions](windows-installer-file-extensions.md).</span></span>

</dd> <dt>

<span data-ttu-id="331c6-133"><span id="_msi_custom_action_using_windows_installer_gly"></span><span id="_MSI_CUSTOM_ACTION_USING_WINDOWS_INSTALLER_GLY"></span>**azione personalizzata**</span><span class="sxs-lookup"><span data-stu-id="331c6-133"><span id="_msi_custom_action_using_windows_installer_gly"></span><span id="_MSI_CUSTOM_ACTION_USING_WINDOWS_INSTALLER_GLY"></span>**custom action**</span></span>
</dt> <dd>

<span data-ttu-id="331c6-134">Scritto dall'autore del [*pacchetto ma*](p-gly.md) non incorporato nel programma di installazione come azione standard.</span><span class="sxs-lookup"><span data-stu-id="331c6-134">Written by the author of the [*package*](p-gly.md) but not built into the installer as a standard action.</span></span> <span data-ttu-id="331c6-135">Per altre informazioni, vedere [Azioni personalizzate](custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="331c6-135">For more information, see [Custom Actions](custom-actions.md).</span></span>

</dd> </dl>

 

 



