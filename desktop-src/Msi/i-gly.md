---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ms.assetid: b8e0a14f-ebdc-4b8f-a884-f6276dccda49
title: I (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca95a473f648ca9e1a08773d93f47bd198df11e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882950"
---
# <a name="i-windows-installer"></a><span data-ttu-id="0f7f6-103">I (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="0f7f6-103">I (Windows Installer)</span></span>

<span data-ttu-id="0f7f6-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [d](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H i J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="0f7f6-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H I J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="0f7f6-105"><span id="_msi_.idt_file_gly"></span><span id="_MSI_.IDT_FILE_GLY"></span>**file con estensione IDT**</span><span class="sxs-lookup"><span data-stu-id="0f7f6-105"><span id="_msi_.idt_file_gly"></span><span id="_MSI_.IDT_FILE_GLY"></span>**.idt file**</span></span>
</dt> <dd>

<span data-ttu-id="0f7f6-106">Tabella del database del programma di installazione esportata.</span><span class="sxs-lookup"><span data-stu-id="0f7f6-106">Exported installer database table.</span></span> <span data-ttu-id="0f7f6-107">Per ulteriori informazioni, vedere [importazione ed esportazione](importing-and-exporting.md) e [Windows Installer estensioni di file](windows-installer-file-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="0f7f6-107">For more information, see [Importing and Exporting](importing-and-exporting.md) and [Windows Installer File Extensions](windows-installer-file-extensions.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f7f6-108"><span id="_msi_import_address_table_gly"></span><span id="_MSI_IMPORT_ADDRESS_TABLE_GLY"></span>**Importa tabella indirizzi (IAT)**</span><span class="sxs-lookup"><span data-stu-id="0f7f6-108"><span id="_msi_import_address_table_gly"></span><span id="_MSI_IMPORT_ADDRESS_TABLE_GLY"></span>**Import Address table (IAT)**</span></span>
</dt> <dd>

<span data-ttu-id="0f7f6-109">Dove l'indirizzo virtuale calcolato viene salvato da ogni funzione importata da tutte le dll.</span><span class="sxs-lookup"><span data-stu-id="0f7f6-109">Where the computed virtual address is saved from each function imported from all DLLs.</span></span>

</dd> <dt>

<span data-ttu-id="0f7f6-110"><span id="_msi_internal_user_interface_gly"></span><span id="_MSI_INTERNAL_USER_INTERFACE_GLY"></span>**interfaccia utente interna**</span><span class="sxs-lookup"><span data-stu-id="0f7f6-110"><span id="_msi_internal_user_interface_gly"></span><span id="_MSI_INTERNAL_USER_INTERFACE_GLY"></span>**internal user interface**</span></span>
</dt> <dd>

<span data-ttu-id="0f7f6-111">Funzionalità predefinite del programma di installazione che possono essere utilizzate per creare un'interfaccia utente grafica per l'installazione.</span><span class="sxs-lookup"><span data-stu-id="0f7f6-111">Built-in capabilities of the installer that can be used to author a graphical UI for installation.</span></span> <span data-ttu-id="0f7f6-112">Un autore può scegliere un' [*interfaccia utente esterna*](e-gly.md).</span><span class="sxs-lookup"><span data-stu-id="0f7f6-112">An author may choose an [*external user interface*](e-gly.md).</span></span> <span data-ttu-id="0f7f6-113">Per ulteriori informazioni, vedere [informazioni sull'interfaccia utente](about-the-user-interface.md).</span><span class="sxs-lookup"><span data-stu-id="0f7f6-113">For more information, see [About the User Interface](about-the-user-interface.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f7f6-114"><span id="_msi_install_level_gly"></span><span id="_MSI_INSTALL_LEVEL_GLY"></span>**livello di installazione**</span><span class="sxs-lookup"><span data-stu-id="0f7f6-114"><span id="_msi_install_level_gly"></span><span id="_MSI_INSTALL_LEVEL_GLY"></span>**install level**</span></span>
</dt> <dd>

<span data-ttu-id="0f7f6-115">Valore di installazione specificato.</span><span class="sxs-lookup"><span data-stu-id="0f7f6-115">Specified installation value.</span></span> <span data-ttu-id="0f7f6-116">Un'applicazione viene installata solo se il proprio livello è minore o uguale al livello di installazione.</span><span class="sxs-lookup"><span data-stu-id="0f7f6-116">An application is installed only if its own level is less than or equal to the install level.</span></span> <span data-ttu-id="0f7f6-117">Il set di applicazioni scelto per l'installazione può pertanto essere modificato modificando il livello di installazione.</span><span class="sxs-lookup"><span data-stu-id="0f7f6-117">The set of applications chosen for installation can therefore be changed by altering the install level.</span></span> <span data-ttu-id="0f7f6-118">Per ulteriori informazioni, vedere [tabella delle funzionalità](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="0f7f6-118">For more information, see [Feature Table](feature-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f7f6-119"><span id="_msi_install_on_demand_gly"></span><span id="_MSI_INSTALL_ON_DEMAND_GLY"></span>**installazione su richiesta**</span><span class="sxs-lookup"><span data-stu-id="0f7f6-119"><span id="_msi_install_on_demand_gly"></span><span id="_MSI_INSTALL_ON_DEMAND_GLY"></span>**installation-on-demand**</span></span>
</dt> <dd>

<span data-ttu-id="0f7f6-120">Servizio che consente di installare applicazioni o funzionalità come richiesto dall'utente o da un'altra applicazione.</span><span class="sxs-lookup"><span data-stu-id="0f7f6-120">Service that installs applications or features as requested by the user or another application.</span></span> <span data-ttu-id="0f7f6-121">La [*pubblicità*](a-gly.md) rende disponibile una funzionalità o un'applicazione per l'installazione su richiesta.</span><span class="sxs-lookup"><span data-stu-id="0f7f6-121">[*Advertising*](a-gly.md) makes a feature or application available for install-on-demand installation.</span></span> <span data-ttu-id="0f7f6-122">Per ulteriori informazioni, vedere: [installazione su richiesta](installation-on-demand.md).</span><span class="sxs-lookup"><span data-stu-id="0f7f6-122">For more information, see: [Installation-on-Demand](installation-on-demand.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f7f6-123"><span id="_msi_installation_context_gly"></span><span id="_MSI_INSTALLATION_CONTEXT_GLY"></span>**contesto di installazione**</span><span class="sxs-lookup"><span data-stu-id="0f7f6-123"><span id="_msi_installation_context_gly"></span><span id="_MSI_INSTALLATION_CONTEXT_GLY"></span>**installation context**</span></span>
</dt> <dd>

<span data-ttu-id="0f7f6-124">La combinazione dei diritti di installazione e dei tipi di installazione produce tre diversi contesti di installazione: gestito per singolo utente, gestito per utente e gestito per computer.</span><span class="sxs-lookup"><span data-stu-id="0f7f6-124">The combination of installation rights and installation types produces three different installation contexts: per-user non-managed, per-user managed, and per-machine managed.</span></span> <span data-ttu-id="0f7f6-125">Non esiste alcun elemento come per computer non gestito.</span><span class="sxs-lookup"><span data-stu-id="0f7f6-125">There is no such thing as per-machine non-managed.</span></span>

</dd> <dt>

<span data-ttu-id="0f7f6-126"><span id="_msi_installer_gly"></span><span id="_MSI_INSTALLER_GLY"></span>**installazione**</span><span class="sxs-lookup"><span data-stu-id="0f7f6-126"><span id="_msi_installer_gly"></span><span id="_MSI_INSTALLER_GLY"></span>**installer**</span></span>
</dt> <dd>

<span data-ttu-id="0f7f6-127">[*Windows Installer*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="0f7f6-127">The [*Windows Installer*](m-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f7f6-128"><span id="_msi_installer_database_gly"></span><span id="_MSI_INSTALLER_DATABASE_GLY"></span>**database del programma di installazione**</span><span class="sxs-lookup"><span data-stu-id="0f7f6-128"><span id="_msi_installer_database_gly"></span><span id="_MSI_INSTALLER_DATABASE_GLY"></span>**installer database**</span></span>
</dt> <dd>

<span data-ttu-id="0f7f6-129">Database relazionale contenente le istruzioni di installazione per un'installazione.</span><span class="sxs-lookup"><span data-stu-id="0f7f6-129">Relational database containing setup instructions for an installation.</span></span> <span data-ttu-id="0f7f6-130">Il database del programma di installazione viene archiviato nel [*file con estensione msi*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="0f7f6-130">The installer database is stored in the [*.msi file*](m-gly.md).</span></span> <span data-ttu-id="0f7f6-131">Per ulteriori informazioni, vedere [database del programma di installazione](installer-database.md).</span><span class="sxs-lookup"><span data-stu-id="0f7f6-131">For more information, see [Installer Database](installer-database.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f7f6-132"><span id="_msi_installer_function_gly"></span><span id="_MSI_INSTALLER_FUNCTION_GLY"></span>**funzione Installer**</span><span class="sxs-lookup"><span data-stu-id="0f7f6-132"><span id="_msi_installer_function_gly"></span><span id="_MSI_INSTALLER_FUNCTION_GLY"></span>**installer function**</span></span>
</dt> <dd>

<span data-ttu-id="0f7f6-133">Chiamato da un utente o da un'applicazione per ottenere i servizi e le funzionalità del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="0f7f6-133">Called by a user or application to obtain installer services and functionality.</span></span> <span data-ttu-id="0f7f6-134">Questa è la Application Programming Interface del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="0f7f6-134">This is the application programming interface of the installer.</span></span> <span data-ttu-id="0f7f6-135">Per informazioni, vedere Guida di [riferimento alle funzioni del programma di installazione](installer-function-reference.md).</span><span class="sxs-lookup"><span data-stu-id="0f7f6-135">For information, see [Installer Function Reference](installer-function-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f7f6-136"><span id="_msi_installer_package_authoring_tool_gly"></span><span id="_MSI_INSTALLER_PACKAGE_AUTHORING_TOOL_GLY"></span>**strumento di creazione pacchetti di installazione**</span><span class="sxs-lookup"><span data-stu-id="0f7f6-136"><span id="_msi_installer_package_authoring_tool_gly"></span><span id="_MSI_INSTALLER_PACKAGE_AUTHORING_TOOL_GLY"></span>**installer package authoring tool**</span></span>
</dt> <dd>

<span data-ttu-id="0f7f6-137">Software che consente agli sviluppatori di creare e modificare un [*file con estensione msi*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="0f7f6-137">Software that enables a developer to create and edit an [*.msi file*](m-gly.md).</span></span> <span data-ttu-id="0f7f6-138">Questo insieme a tutti [*i file di origine esterni*](e-gly.md) comprende un [*pacchetto*](p-gly.md) contenente tutte le informazioni necessarie per un'installazione.</span><span class="sxs-lookup"><span data-stu-id="0f7f6-138">This together with any [*external source files*](e-gly.md) comprise a [*package*](p-gly.md) containing all the information required for an installation.</span></span>

</dd> <dt>

<span data-ttu-id="0f7f6-139"><span id="_msi_internal_source_files_gly"></span><span id="_MSI_INTERNAL_SOURCE_FILES_GLY"></span>**file di origine interni**</span><span class="sxs-lookup"><span data-stu-id="0f7f6-139"><span id="_msi_internal_source_files_gly"></span><span id="_MSI_INTERNAL_SOURCE_FILES_GLY"></span>**internal source files**</span></span>
</dt> <dd>

<span data-ttu-id="0f7f6-140">Archiviato nel [*file con estensione msi*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="0f7f6-140">Stored in the [*.msi file*](m-gly.md).</span></span> <span data-ttu-id="0f7f6-141">Più file di origine interni possono essere compressi e archiviati insieme in un [*file CAB*](c-gly.md) archiviato in un file con estensione msi.</span><span class="sxs-lookup"><span data-stu-id="0f7f6-141">Multiple internal source files can be compressed and stored together in a [*cabinet file*](c-gly.md) that is stored within an .msi file.</span></span>

</dd> </dl>

 

 



