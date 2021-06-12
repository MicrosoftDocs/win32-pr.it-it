---
description: Informazioni sui Windows Installer concetti che iniziano con la lettera E, ad esempio file di origine con privilegi elevati ed esterni.
ms.assetid: 8f180e2c-06f4-41d5-b167-52525f4a9985
title: E (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a2c65c50427b1f8271be838971a387388ea53db
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011095"
---
# <a name="e-windows-installer"></a><span data-ttu-id="51aa7-103">E (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="51aa7-103">E (Windows Installer)</span></span>

<span data-ttu-id="51aa7-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) E [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P Q](p-gly.md) [](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="51aa7-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) E [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="51aa7-105"><span id="_msi_elevated_gly"></span><span id="_MSI_ELEVATED_GLY"></span>**Elevato**</span><span class="sxs-lookup"><span data-stu-id="51aa7-105"><span id="_msi_elevated_gly"></span><span id="_MSI_ELEVATED_GLY"></span>**elevated**</span></span>
</dt> <dd>

<span data-ttu-id="51aa7-106">Le azioni eseguite con privilegi di sistema sono denominate con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="51aa7-106">Actions performed with system privileges are called elevated.</span></span>

</dd> <dt>

<span data-ttu-id="51aa7-107"><span id="_msi_execution_phase_gly"></span><span id="_MSI_EXECUTION_PHASE_GLY"></span>**fase di esecuzione**</span><span class="sxs-lookup"><span data-stu-id="51aa7-107"><span id="_msi_execution_phase_gly"></span><span id="_MSI_EXECUTION_PHASE_GLY"></span>**execution phase**</span></span>
</dt> <dd>

<span data-ttu-id="51aa7-108">Quando il programma di installazione esegue uno script di azioni del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="51aa7-108">When the installer executes a script of installer actions.</span></span> <span data-ttu-id="51aa7-109">In Microsoft Windows 2000 questo processo viene eseguito dal servizio di installazione.</span><span class="sxs-lookup"><span data-stu-id="51aa7-109">In Microsoft Windows 2000, this process is performed by the installer service.</span></span> <span data-ttu-id="51aa7-110">In un'applicazione gestita lo script viene eseguito con privilegi di sistema.</span><span class="sxs-lookup"><span data-stu-id="51aa7-110">In a managed application, the script is executed with system privileges.</span></span> <span data-ttu-id="51aa7-111">Per altre informazioni, vedere [Meccanismo di installazione](installation-mechanism.md).</span><span class="sxs-lookup"><span data-stu-id="51aa7-111">For more information, see [Installation Mechanism](installation-mechanism.md).</span></span>

</dd> <dt>

<span data-ttu-id="51aa7-112"><span id="_msi_execution_script_gly"></span><span id="_MSI_EXECUTION_SCRIPT_GLY"></span>**script di esecuzione**</span><span class="sxs-lookup"><span data-stu-id="51aa7-112"><span id="_msi_execution_script_gly"></span><span id="_MSI_EXECUTION_SCRIPT_GLY"></span>**execution script**</span></span>
</dt> <dd>

<span data-ttu-id="51aa7-113">Azioni del programma di installazione per un'installazione.</span><span class="sxs-lookup"><span data-stu-id="51aa7-113">Installer actions for an installation.</span></span> <span data-ttu-id="51aa7-114">Lo script di esecuzione viene generato durante la fase [*di acquisizione*](a-gly.md) dell'installazione ed eseguito durante la fase [*di esecuzione*](/windows).</span><span class="sxs-lookup"><span data-stu-id="51aa7-114">The execution script is generated during the [*acquisition phase*](a-gly.md) of installation and executed during the [*execution phase*](/windows).</span></span> <span data-ttu-id="51aa7-115">Per altre informazioni, vedere [Meccanismo di installazione](installation-mechanism.md).</span><span class="sxs-lookup"><span data-stu-id="51aa7-115">For more information, see [Installation Mechanism](installation-mechanism.md).</span></span>

</dd> <dt>

<span data-ttu-id="51aa7-116"><span id="_msi_external_source_files_gly"></span><span id="_MSI_EXTERNAL_SOURCE_FILES_GLY"></span>**file di origine esterni**</span><span class="sxs-lookup"><span data-stu-id="51aa7-116"><span id="_msi_external_source_files_gly"></span><span id="_MSI_EXTERNAL_SOURCE_FILES_GLY"></span>**external source files**</span></span>
</dt> <dd>

<span data-ttu-id="51aa7-117">File di origine dell'applicazione installata archiviati all'esterno [*del file.msi file*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="51aa7-117">Source files of the application being installed that are stored outside of the [*.msi file*](m-gly.md).</span></span> <span data-ttu-id="51aa7-118">Più file di origine esterni possono essere compressi e archiviati insieme all'interno di un [*file cab*](c-gly.md) incluso nel [*pacchetto*](p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="51aa7-118">Multiple external source files can be compressed and stored together inside of a [*cabinet file*](c-gly.md) included in the [*package*](p-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="51aa7-119"><span id="_msi_external_user_interface_gly"></span><span id="_MSI_EXTERNAL_USER_INTERFACE_GLY"></span>**interfaccia utente esterna**</span><span class="sxs-lookup"><span data-stu-id="51aa7-119"><span id="_msi_external_user_interface_gly"></span><span id="_MSI_EXTERNAL_USER_INTERFACE_GLY"></span>**external user interface**</span></span>
</dt> <dd>

<span data-ttu-id="51aa7-120">Interfaccia utente fornita dall'autore di un pacchetto di installazione.</span><span class="sxs-lookup"><span data-stu-id="51aa7-120">UI provided by the author of an installation package.</span></span> <span data-ttu-id="51aa7-121">Non usa le funzionalità interne dell'interfaccia utente del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="51aa7-121">It does not use the internal UI capabilities of the installer.</span></span> <span data-ttu-id="51aa7-122">Per altre informazioni, vedere [About the Interfaccia utente](about-the-user-interface.md).</span><span class="sxs-lookup"><span data-stu-id="51aa7-122">For more information, see [About the User Interface](about-the-user-interface.md).</span></span>

</dd> </dl>

 

 
