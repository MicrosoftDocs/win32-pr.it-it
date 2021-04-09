---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ms.assetid: 541fd08c-c21a-4a51-aa1c-d65cc0f5da75
title: A (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46677d8823c5298307db922f2d61285564add437
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131514"
---
# <a name="a-windows-installer"></a><span data-ttu-id="deb0f-103">A (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="deb0f-103">A (Windows Installer)</span></span>

<span data-ttu-id="deb0f-104">A [B](b-gly.md) [C](c-gly.md) [d](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [i](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="deb0f-104">A [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="deb0f-105"><span id="_msi_accessibility_using_windows_installer_gly"></span><span id="_MSI_ACCESSIBILITY_USING_WINDOWS_INSTALLER_GLY"></span>**accessibilità**</span><span class="sxs-lookup"><span data-stu-id="deb0f-105"><span id="_msi_accessibility_using_windows_installer_gly"></span><span id="_MSI_ACCESSIBILITY_USING_WINDOWS_INSTALLER_GLY"></span>**accessibility**</span></span>
</dt> <dd>

<span data-ttu-id="deb0f-106">Implementazione di progettazione per rendere accessibile l'interfaccia utente del programma di installazione a tutti gli utenti.</span><span class="sxs-lookup"><span data-stu-id="deb0f-106">Design implementation for making the installer's user interface accessible to all users.</span></span> <span data-ttu-id="deb0f-107">Per ulteriori informazioni sull'accessibilità, vedere l'argomento introduttivo: [accessibilità](accessibility.md).</span><span class="sxs-lookup"><span data-stu-id="deb0f-107">For more information about accessibility, see the overview topic: [Accessibility](accessibility.md).</span></span>

</dd> <dt>

<span data-ttu-id="deb0f-108"><span id="_msi_acquisition_phase_gly"></span><span id="_MSI_ACQUISITION_PHASE_GLY"></span>**fase di acquisizione**</span><span class="sxs-lookup"><span data-stu-id="deb0f-108"><span id="_msi_acquisition_phase_gly"></span><span id="_MSI_ACQUISITION_PHASE_GLY"></span>**acquisition phase**</span></span>
</dt> <dd>

<span data-ttu-id="deb0f-109">Fase di installazione durante la quale il programma di installazione determina la procedura.</span><span class="sxs-lookup"><span data-stu-id="deb0f-109">Phase of installation during which the installer determines procedure.</span></span> <span data-ttu-id="deb0f-110">La fase di acquisizione inizia quando un'applicazione o un utente indica [*Windows Installer*](m-gly.md) di installare un'applicazione o una funzionalità.</span><span class="sxs-lookup"><span data-stu-id="deb0f-110">Acquisition phase begins when an application or user instructs [*Windows Installer*](m-gly.md) to install an application or feature.</span></span> <span data-ttu-id="deb0f-111">Il programma di installazione esegue quindi una query nel [*database*](i-gly.md) per ottenere informazioni quando genera lo [*script di esecuzione*](e-gly.md) per l'installazione.</span><span class="sxs-lookup"><span data-stu-id="deb0f-111">The installer then queries the [*database*](i-gly.md) for information as it generates the [*execution script*](e-gly.md) for the installation.</span></span> <span data-ttu-id="deb0f-112">Per ulteriori informazioni sulle fasi di un'installazione di, vedere [meccanismo di installazione](installation-mechanism.md).</span><span class="sxs-lookup"><span data-stu-id="deb0f-112">For more information about the phases of an installation, see [Installation Mechanism](installation-mechanism.md).</span></span>

</dd> <dt>

<span data-ttu-id="deb0f-113"><span id="_msi_action_gly"></span><span id="_MSI_ACTION_GLY"></span>**azione**</span><span class="sxs-lookup"><span data-stu-id="deb0f-113"><span id="_msi_action_gly"></span><span id="_MSI_ACTION_GLY"></span>**action**</span></span>
</dt> <dd>

<span data-ttu-id="deb0f-114">Molte delle funzioni eseguite da Windows Installer sono incapsulate in azioni.</span><span class="sxs-lookup"><span data-stu-id="deb0f-114">Many of the functions performed by Windows Installer are encapsulated into actions.</span></span> <span data-ttu-id="deb0f-115">Ogni azione specifica l'esecuzione di una particolare funzione e il flusso procedurale totale dell'installazione viene richiesto dalla sequenza di azioni nelle [*tabelle di sequenza*](s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="deb0f-115">Each action specifies the execution of a particular function and the total procedural flow of the installation is prescribed by the sequence of actions in the [*Sequence tables*](s-gly.md).</span></span> <span data-ttu-id="deb0f-116">Le [*azioni standard*](s-gly.md) sono incorporate in Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="deb0f-116">[*Standard actions*](s-gly.md) are built into Windows Installer.</span></span> <span data-ttu-id="deb0f-117">Le [*azioni personalizzate*](c-gly.md) vengono scritte dall'autore del [*pacchetto*](p-gly.md)di installazione.</span><span class="sxs-lookup"><span data-stu-id="deb0f-117">[*Custom actions*](c-gly.md) are written by the author of the installation [*package*](p-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="deb0f-118"><span id="_msi_admin_approval_mode_gly"></span><span id="_MSI_ADMIN_APPROVAL_MODE_GLY"></span>**Modalità Approvazione amministratore**</span><span class="sxs-lookup"><span data-stu-id="deb0f-118"><span id="_msi_admin_approval_mode_gly"></span><span id="_MSI_ADMIN_APPROVAL_MODE_GLY"></span>**Admin Approval Mode**</span></span>
</dt> <dd>

<span data-ttu-id="deb0f-119">Lo stato di approvazione abilitato dalla protezione dell'account utente (UAC) che esegue tutti gli utenti con privilegi minimi, inclusi gli amministratori.</span><span class="sxs-lookup"><span data-stu-id="deb0f-119">The approval state enabled by User Account Protection (UAC) that runs all users with least privilege, including administrators.</span></span> <span data-ttu-id="deb0f-120">Agli utenti viene richiesto di fornire il consenso per elevare le installazioni che richiedono privilegi di amministratore.</span><span class="sxs-lookup"><span data-stu-id="deb0f-120">Users are required to provide consent to elevate installations that require administrator privileges.</span></span>

</dd> <dt>

<span data-ttu-id="deb0f-121"><span id="_msi_advertising_gly"></span><span id="_MSI_ADVERTISING_GLY"></span>**pubblicità**</span><span class="sxs-lookup"><span data-stu-id="deb0f-121"><span id="_msi_advertising_gly"></span><span id="_MSI_ADVERTISING_GLY"></span>**advertising**</span></span>
</dt> <dd>

<span data-ttu-id="deb0f-122">Funzionalità per rendere le interfacce necessarie per il caricamento e per rendere disponibile un'applicazione senza installare l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="deb0f-122">Capability to make the interfaces required for loading and to make an application available without installing the application.</span></span> <span data-ttu-id="deb0f-123">Quando un utente o un'applicazione attiva un'interfaccia annunciata, il programma di installazione procede quindi con l'installazione dei componenti necessari.</span><span class="sxs-lookup"><span data-stu-id="deb0f-123">When a user or application activates an advertised interface, the installer then proceeds to install the necessary components.</span></span> <span data-ttu-id="deb0f-124">I due tipi di annunci pubblicitari sono [*assegnazione*](/windows) e [*pubblicazione*](p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="deb0f-124">The two types of advertising are [*assigning*](/windows) and [*publishing*](p-gly.md).</span></span> <span data-ttu-id="deb0f-125">Per altre informazioni, vedere anche [*installare su richiesta*](i-gly.md).</span><span class="sxs-lookup"><span data-stu-id="deb0f-125">For more information, see also [*install-on-demand*](i-gly.md).</span></span> <span data-ttu-id="deb0f-126">Per ulteriori informazioni sul modo in cui il programma di installazione annuncia le applicazioni, vedere l' [annuncio](advertisement.md).</span><span class="sxs-lookup"><span data-stu-id="deb0f-126">For more information about how the installer advertises applications, see [Advertisement](advertisement.md).</span></span>

</dd> <dt>

<span data-ttu-id="deb0f-127"><span id="_msi_application_information_service_gly"></span><span id="_MSI_APPLICATION_INFORMATION_SERVICE_GLY"></span>**Servizio informazioni applicazioni (AIS)**</span><span class="sxs-lookup"><span data-stu-id="deb0f-127"><span id="_msi_application_information_service_gly"></span><span id="_MSI_APPLICATION_INFORMATION_SERVICE_GLY"></span>**Application Information Service (AIS)**</span></span>
</dt> <dd>

<span data-ttu-id="deb0f-128">Un servizio di sistema di Windows Vista che facilita l'avvio di installazioni che richiedono privilegi elevati per l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="deb0f-128">A system service of Windows Vista that facilitates starting installations that require elevated privileges to run.</span></span> <span data-ttu-id="deb0f-129">Fornisce l'interfaccia utente di consenso utilizzata da controllo dell'account utente per richiedere all'utente l'autorizzazione di amministratore.</span><span class="sxs-lookup"><span data-stu-id="deb0f-129">Provides the Consent UI used by User Account Control to prompt a user for administrator authorization.</span></span>

</dd> <dt>

<span data-ttu-id="deb0f-130"><span id="_msi_assigning_gly"></span><span id="_MSI_ASSIGNING_GLY"></span>**assegnazione**</span><span class="sxs-lookup"><span data-stu-id="deb0f-130"><span id="_msi_assigning_gly"></span><span id="_MSI_ASSIGNING_GLY"></span>**assigning**</span></span>
</dt> <dd>

<span data-ttu-id="deb0f-131">Rende disponibile un'applicazione e la rende visibile come se fosse stata installata a un utente, senza installarla effettivamente.</span><span class="sxs-lookup"><span data-stu-id="deb0f-131">Makes an application available, and makes it appear as if it has been installed to a user, without actually installing it.</span></span> <span data-ttu-id="deb0f-132">L'assegnazione di aggiunge collegamenti e icone al menu **Start** , associa i file appropriati e scrive le voci del registro di sistema per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="deb0f-132">Assigning adds shortcuts and icons to the **Start** menu, associates appropriate files, and writes registry entries for the application.</span></span> <span data-ttu-id="deb0f-133">Quando un utente tenta di aprire un'applicazione assegnata, il programma di installazione installa l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="deb0f-133">When a user tries to open an assigned application, then the installer installs the application.</span></span> <span data-ttu-id="deb0f-134">L'assegnazione e la [*pubblicazione*](p-gly.md) sono due metodi di [*annuncio pubblicitario*](/windows).</span><span class="sxs-lookup"><span data-stu-id="deb0f-134">Assigning and [*publishing*](p-gly.md) are two methods of [*advertising*](/windows).</span></span> <span data-ttu-id="deb0f-135">Per ulteriori informazioni, vedere l' [annuncio](advertisement.md).</span><span class="sxs-lookup"><span data-stu-id="deb0f-135">For more information, see [Advertisement](advertisement.md).</span></span>

</dd> <dt>

<span data-ttu-id="deb0f-136"><span id="_msi_asynchronous_execution_using_windows_installer_gly"></span><span id="_MSI_ASYNCHRONOUS_EXECUTION_USING_WINDOWS_INSTALLER_GLY"></span>**esecuzione asincrona**</span><span class="sxs-lookup"><span data-stu-id="deb0f-136"><span id="_msi_asynchronous_execution_using_windows_installer_gly"></span><span id="_MSI_ASYNCHRONOUS_EXECUTION_USING_WINDOWS_INSTALLER_GLY"></span>**asynchronous execution**</span></span>
</dt> <dd>

<span data-ttu-id="deb0f-137">[*Azione personalizzata*](c-gly.md) durante la quale il programma di installazione esegue contemporaneamente thread distinti dell'azione personalizzata e dell'installazione corrente.</span><span class="sxs-lookup"><span data-stu-id="deb0f-137">[*Custom action*](c-gly.md) during which the installer runs separate threads of the custom action and the current installation simultaneously.</span></span> <span data-ttu-id="deb0f-138">Per altre informazioni, vedere [azioni personalizzate sincrone e asincrone](synchronous-and-asynchronous-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="deb0f-138">For more information, see [Synchronous and Asynchronous Custom Actions](synchronous-and-asynchronous-custom-actions.md).</span></span>

</dd> </dl>

 

 
