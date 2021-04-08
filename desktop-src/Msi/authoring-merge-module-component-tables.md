---
description: In ogni modulo merge è necessaria una tabella di componenti.
ms.assetid: ef4a0678-bf6b-47c9-89e8-40e12da52d9b
title: Creazione di tabelle di componenti del modulo merge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46557541b3a6b89841fe3e26cef7c00e59dc3911
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049911"
---
# <a name="authoring-merge-module-component-tables"></a><span data-ttu-id="62876-103">Creazione di tabelle di componenti del modulo merge</span><span class="sxs-lookup"><span data-stu-id="62876-103">Authoring Merge Module Component Tables</span></span>

<span data-ttu-id="62876-104">In ogni modulo merge è necessaria una [tabella di componenti](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="62876-104">A [Component table](component-table.md) is required in every merge module.</span></span> <span data-ttu-id="62876-105">Questa tabella contiene un record per ogni componente fornito dal modulo merge al file con estensione msi di destinazione.</span><span class="sxs-lookup"><span data-stu-id="62876-105">This table contains a record for each component delivered by the merge module to the target .msi file.</span></span> <span data-ttu-id="62876-106">Si noti che ogni componente deve essere specificato anche nella [tabella ModuleComponents](modulecomponents-table.md) descritta in creazione di [tabelle ModuleComponents](authoring-modulecomponents-tables.md).</span><span class="sxs-lookup"><span data-stu-id="62876-106">Note that each of these components must also be specified in the [ModuleComponents table](modulecomponents-table.md) described in [Authoring ModuleComponents Tables](authoring-modulecomponents-tables.md).</span></span>

<span data-ttu-id="62876-107">Utilizzare la convenzione di denominazione standard quando si immettono i nomi nella colonna componente per assicurarsi che l'identificatore per ogni componente sia univoco per tutti i moduli unione e i database di installazione.</span><span class="sxs-lookup"><span data-stu-id="62876-107">Use the standard naming convention when entering names into the Component column to ensure that the identifier for each component is unique for all merge modules and installation databases.</span></span> <span data-ttu-id="62876-108">Per ulteriori informazioni, vedere [denominazione delle chiavi primarie nei database dei moduli di merge](naming-primary-keys-in-merge-module-databases.md).</span><span class="sxs-lookup"><span data-stu-id="62876-108">For more information, see [Naming Primary Keys in Merge Module Databases](naming-primary-keys-in-merge-module-databases.md).</span></span>

<span data-ttu-id="62876-109">Completare i campi rimanenti in ogni record come descritto per un database di installazione nella [tabella dei componenti](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="62876-109">Complete the remaining fields in each record as described for an installation database in [Component table](component-table.md).</span></span> <span data-ttu-id="62876-110">I componenti aggiunti a un pacchetto da un modulo merge devono rispettare le linee guida per i componenti Windows Installer validi descritti nelle sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="62876-110">The components added to a package by a merge module must adhere to the guidelines for valid Windows Installer Components described in the following sections:</span></span>

-   [<span data-ttu-id="62876-111">Componenti Windows Installer</span><span class="sxs-lookup"><span data-stu-id="62876-111">Windows Installer Components</span></span>](windows-installer-components.md)
-   [<span data-ttu-id="62876-112">Organizzazione di applicazioni in componenti</span><span class="sxs-lookup"><span data-stu-id="62876-112">Organizing Applications into Components</span></span>](organizing-applications-into-components.md)

 

 



