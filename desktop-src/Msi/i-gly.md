---
description: Informazioni su Windows Installer concetti che iniziano con la lettera I, ad esempio la tabella Importa indirizzo e il livello di installazione.
ms.assetid: b8e0a14f-ebdc-4b8f-a884-f6276dccda49
title: I (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e33b5cfb9c4545a5482b214e0413ab3e3d981109
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010654"
---
# <a name="i-windows-installer"></a><span data-ttu-id="357ae-103">I (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="357ae-103">I (Windows Installer)</span></span>

<span data-ttu-id="357ae-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H I J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) T [](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="357ae-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H I J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="357ae-105"><span id="_msi_.idt_file_gly"></span><span id="_MSI_.IDT_FILE_GLY"></span>**File con estensione idt**</span><span class="sxs-lookup"><span data-stu-id="357ae-105"><span id="_msi_.idt_file_gly"></span><span id="_MSI_.IDT_FILE_GLY"></span>**.idt file**</span></span>
</dt> <dd>

<span data-ttu-id="357ae-106">Tabella del database del programma di installazione esportata.</span><span class="sxs-lookup"><span data-stu-id="357ae-106">Exported installer database table.</span></span> <span data-ttu-id="357ae-107">Per altre informazioni, vedere [Importing and Exporting](importing-and-exporting.md) and [Windows Installer File Extensions](windows-installer-file-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="357ae-107">For more information, see [Importing and Exporting](importing-and-exporting.md) and [Windows Installer File Extensions](windows-installer-file-extensions.md).</span></span>

</dd> <dt>

<span data-ttu-id="357ae-108"><span id="_msi_import_address_table_gly"></span><span id="_MSI_IMPORT_ADDRESS_TABLE_GLY"></span>**Importare la tabella degli indirizzi (IAT)**</span><span class="sxs-lookup"><span data-stu-id="357ae-108"><span id="_msi_import_address_table_gly"></span><span id="_MSI_IMPORT_ADDRESS_TABLE_GLY"></span>**Import Address table (IAT)**</span></span>
</dt> <dd>

<span data-ttu-id="357ae-109">Posizione in cui l'indirizzo virtuale calcolato viene salvato da ogni funzione importata da tutte le DLL.</span><span class="sxs-lookup"><span data-stu-id="357ae-109">Where the computed virtual address is saved from each function imported from all DLLs.</span></span>

</dd> <dt>

<span data-ttu-id="357ae-110"><span id="_msi_internal_user_interface_gly"></span><span id="_MSI_INTERNAL_USER_INTERFACE_GLY"></span>**interfaccia utente interna**</span><span class="sxs-lookup"><span data-stu-id="357ae-110"><span id="_msi_internal_user_interface_gly"></span><span id="_MSI_INTERNAL_USER_INTERFACE_GLY"></span>**internal user interface**</span></span>
</dt> <dd>

<span data-ttu-id="357ae-111">Funzionalità incorporate del programma di installazione che possono essere usate per creare un'interfaccia utente grafica per l'installazione.</span><span class="sxs-lookup"><span data-stu-id="357ae-111">Built-in capabilities of the installer that can be used to author a graphical UI for installation.</span></span> <span data-ttu-id="357ae-112">Un autore può scegliere [*un'interfaccia utente esterna.*](e-gly.md)</span><span class="sxs-lookup"><span data-stu-id="357ae-112">An author may choose an [*external user interface*](e-gly.md).</span></span> <span data-ttu-id="357ae-113">Per altre informazioni, vedere [Informazioni sul Interfaccia utente](about-the-user-interface.md).</span><span class="sxs-lookup"><span data-stu-id="357ae-113">For more information, see [About the User Interface](about-the-user-interface.md).</span></span>

</dd> <dt>

<span data-ttu-id="357ae-114"><span id="_msi_install_level_gly"></span><span id="_MSI_INSTALL_LEVEL_GLY"></span>**livello di installazione**</span><span class="sxs-lookup"><span data-stu-id="357ae-114"><span id="_msi_install_level_gly"></span><span id="_MSI_INSTALL_LEVEL_GLY"></span>**install level**</span></span>
</dt> <dd>

<span data-ttu-id="357ae-115">Valore di installazione specificato.</span><span class="sxs-lookup"><span data-stu-id="357ae-115">Specified installation value.</span></span> <span data-ttu-id="357ae-116">Un'applicazione viene installata solo se il relativo livello è minore o uguale al livello di installazione.</span><span class="sxs-lookup"><span data-stu-id="357ae-116">An application is installed only if its own level is less than or equal to the install level.</span></span> <span data-ttu-id="357ae-117">Il set di applicazioni scelto per l'installazione può quindi essere modificato modificando il livello di installazione.</span><span class="sxs-lookup"><span data-stu-id="357ae-117">The set of applications chosen for installation can therefore be changed by altering the install level.</span></span> <span data-ttu-id="357ae-118">Per altre informazioni, vedere [Tabella delle funzionalità.](feature-table.md)</span><span class="sxs-lookup"><span data-stu-id="357ae-118">For more information, see [Feature Table](feature-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="357ae-119"><span id="_msi_install_on_demand_gly"></span><span id="_MSI_INSTALL_ON_DEMAND_GLY"></span>**installazione su richiesta**</span><span class="sxs-lookup"><span data-stu-id="357ae-119"><span id="_msi_install_on_demand_gly"></span><span id="_MSI_INSTALL_ON_DEMAND_GLY"></span>**installation-on-demand**</span></span>
</dt> <dd>

<span data-ttu-id="357ae-120">Servizio che installa applicazioni o funzionalità come richiesto dall'utente o da un'altra applicazione.</span><span class="sxs-lookup"><span data-stu-id="357ae-120">Service that installs applications or features as requested by the user or another application.</span></span> <span data-ttu-id="357ae-121">[*La*](a-gly.md) pubblicità rende disponibile una funzionalità o un'applicazione per l'installazione su richiesta.</span><span class="sxs-lookup"><span data-stu-id="357ae-121">[*Advertising*](a-gly.md) makes a feature or application available for install-on-demand installation.</span></span> <span data-ttu-id="357ae-122">Per altre informazioni, vedere: [Installation-on-Demand](installation-on-demand.md).</span><span class="sxs-lookup"><span data-stu-id="357ae-122">For more information, see: [Installation-on-Demand](installation-on-demand.md).</span></span>

</dd> <dt>

<span data-ttu-id="357ae-123"><span id="_msi_installation_context_gly"></span><span id="_MSI_INSTALLATION_CONTEXT_GLY"></span>**contesto di installazione**</span><span class="sxs-lookup"><span data-stu-id="357ae-123"><span id="_msi_installation_context_gly"></span><span id="_MSI_INSTALLATION_CONTEXT_GLY"></span>**installation context**</span></span>
</dt> <dd>

<span data-ttu-id="357ae-124">La combinazione di diritti di installazione e tipi di installazione produce tre diversi contesti di installazione: per utente non gestito, gestito per utente e gestito per computer.</span><span class="sxs-lookup"><span data-stu-id="357ae-124">The combination of installation rights and installation types produces three different installation contexts: per-user non-managed, per-user managed, and per-machine managed.</span></span> <span data-ttu-id="357ae-125">Non esiste alcuna soluzione, ad esempio per computer non gestito.</span><span class="sxs-lookup"><span data-stu-id="357ae-125">There is no such thing as per-machine non-managed.</span></span>

</dd> <dt>

<span data-ttu-id="357ae-126"><span id="_msi_installer_gly"></span><span id="_MSI_INSTALLER_GLY"></span>**Installer**</span><span class="sxs-lookup"><span data-stu-id="357ae-126"><span id="_msi_installer_gly"></span><span id="_MSI_INSTALLER_GLY"></span>**installer**</span></span>
</dt> <dd>

<span data-ttu-id="357ae-127">Oggetto [*Windows Installer*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="357ae-127">The [*Windows Installer*](m-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="357ae-128"><span id="_msi_installer_database_gly"></span><span id="_MSI_INSTALLER_DATABASE_GLY"></span>**database del programma di installazione**</span><span class="sxs-lookup"><span data-stu-id="357ae-128"><span id="_msi_installer_database_gly"></span><span id="_MSI_INSTALLER_DATABASE_GLY"></span>**installer database**</span></span>
</dt> <dd>

<span data-ttu-id="357ae-129">Database relazionale contenente le istruzioni di installazione per un'installazione.</span><span class="sxs-lookup"><span data-stu-id="357ae-129">Relational database containing setup instructions for an installation.</span></span> <span data-ttu-id="357ae-130">Il database del programma di installazione viene archiviato [*nel file.msi .*](m-gly.md)</span><span class="sxs-lookup"><span data-stu-id="357ae-130">The installer database is stored in the [*.msi file*](m-gly.md).</span></span> <span data-ttu-id="357ae-131">Per altre informazioni, vedere Database [del programma di installazione.](installer-database.md)</span><span class="sxs-lookup"><span data-stu-id="357ae-131">For more information, see [Installer Database](installer-database.md).</span></span>

</dd> <dt>

<span data-ttu-id="357ae-132"><span id="_msi_installer_function_gly"></span><span id="_MSI_INSTALLER_FUNCTION_GLY"></span>**funzione installer**</span><span class="sxs-lookup"><span data-stu-id="357ae-132"><span id="_msi_installer_function_gly"></span><span id="_MSI_INSTALLER_FUNCTION_GLY"></span>**installer function**</span></span>
</dt> <dd>

<span data-ttu-id="357ae-133">Chiamato da un utente o da un'applicazione per ottenere i servizi e le funzionalità del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="357ae-133">Called by a user or application to obtain installer services and functionality.</span></span> <span data-ttu-id="357ae-134">Si tratta dell'interfaccia di programmazione dell'applicazione del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="357ae-134">This is the application programming interface of the installer.</span></span> <span data-ttu-id="357ae-135">Per informazioni, vedere Informazioni [di riferimento sulle funzioni del programma di installazione.](installer-function-reference.md)</span><span class="sxs-lookup"><span data-stu-id="357ae-135">For information, see [Installer Function Reference](installer-function-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="357ae-136"><span id="_msi_installer_package_authoring_tool_gly"></span><span id="_MSI_INSTALLER_PACKAGE_AUTHORING_TOOL_GLY"></span>**strumento di creazione pacchetti del programma di installazione**</span><span class="sxs-lookup"><span data-stu-id="357ae-136"><span id="_msi_installer_package_authoring_tool_gly"></span><span id="_MSI_INSTALLER_PACKAGE_AUTHORING_TOOL_GLY"></span>**installer package authoring tool**</span></span>
</dt> <dd>

<span data-ttu-id="357ae-137">Software che consente a uno sviluppatore di creare e modificare [*un file.msi .*](m-gly.md)</span><span class="sxs-lookup"><span data-stu-id="357ae-137">Software that enables a developer to create and edit an [*.msi file*](m-gly.md).</span></span> <span data-ttu-id="357ae-138">Insieme a tutti i [*file di origine esterni è*](e-gly.md) costituito da un [*pacchetto*](p-gly.md) contenente tutte le informazioni necessarie per un'installazione.</span><span class="sxs-lookup"><span data-stu-id="357ae-138">This together with any [*external source files*](e-gly.md) comprise a [*package*](p-gly.md) containing all the information required for an installation.</span></span>

</dd> <dt>

<span data-ttu-id="357ae-139"><span id="_msi_internal_source_files_gly"></span><span id="_MSI_INTERNAL_SOURCE_FILES_GLY"></span>**file di origine interni**</span><span class="sxs-lookup"><span data-stu-id="357ae-139"><span id="_msi_internal_source_files_gly"></span><span id="_MSI_INTERNAL_SOURCE_FILES_GLY"></span>**internal source files**</span></span>
</dt> <dd>

<span data-ttu-id="357ae-140">Archiviato nel [*file.msi .*](m-gly.md)</span><span class="sxs-lookup"><span data-stu-id="357ae-140">Stored in the [*.msi file*](m-gly.md).</span></span> <span data-ttu-id="357ae-141">Più file di origine interni possono essere compressi e archiviati insieme in un [*file CAB*](c-gly.md) archiviato all'interno di .msi file.</span><span class="sxs-lookup"><span data-stu-id="357ae-141">Multiple internal source files can be compressed and stored together in a [*cabinet file*](c-gly.md) that is stored within an .msi file.</span></span>

</dd> </dl>

 

 



