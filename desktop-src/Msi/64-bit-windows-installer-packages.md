---
description: Un pacchetto a 64 bit è costituito parzialmente o interamente da componenti Windows Installer a 64 bit.
ms.assetid: 615a5534-7c9e-4240-9a23-35f224122d0e
title: Pacchetti Windows Installer a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16b34c8ff7ce4809dc44932cc8a5daa978b6ff66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881185"
---
# <a name="64-bit-windows-installer-packages"></a><span data-ttu-id="b93ad-103">Pacchetti Windows Installer a 64 bit</span><span class="sxs-lookup"><span data-stu-id="b93ad-103">64-bit Windows Installer Packages</span></span>

<span data-ttu-id="b93ad-104">Un pacchetto a 64 bit è costituito parzialmente o interamente da componenti [Windows Installer](windows-installer-components.md) a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="b93ad-104">A 64-bit package consists partially or entirely of 64-bit [Windows Installer](windows-installer-components.md) components.</span></span> <span data-ttu-id="b93ad-105">L'elenco seguente identifica i requisiti per ogni pacchetto di Windows Installer a 64 bit:</span><span class="sxs-lookup"><span data-stu-id="b93ad-105">The following list identifies the requirements for every 64-bit Windows Installer package:</span></span>

-   <span data-ttu-id="b93ad-106">Il valore "Intel64" deve essere immesso nel campo piattaforma della proprietà [**Riepilogo modello**](template-summary.md) , se e solo se il pacchetto viene eseguito in un processore Intel64 (Itanium).</span><span class="sxs-lookup"><span data-stu-id="b93ad-106">The value "Intel64" must be entered in the platform field of the [**Template Summary**](template-summary.md) property if and only if the package runs on an Intel64 (Itanium) processor.</span></span>
-   <span data-ttu-id="b93ad-107">Il valore "x64" deve essere immesso nel campo piattaforma della proprietà [**Riepilogo modello**](template-summary.md) , se e solo se il pacchetto viene eseguito in un processore x64.</span><span class="sxs-lookup"><span data-stu-id="b93ad-107">The value "x64" must be entered in the platform field of the [**Template Summary**](template-summary.md) property if and only if the package runs on an x64 processor.</span></span>
-   <span data-ttu-id="b93ad-108">Il valore "Arm64" deve essere immesso nel campo piattaforma della proprietà [**Riepilogo modello**](template-summary.md) , se e solo se il pacchetto viene eseguito in un processore Arm64.</span><span class="sxs-lookup"><span data-stu-id="b93ad-108">The value "Arm64" must be entered in the platform field of the [**Template Summary**](template-summary.md) property if and only if the package runs on an Arm64 processor.</span></span>
-   <span data-ttu-id="b93ad-109">È necessario impostare la proprietà [**Riepilogo conteggio pagine**](page-count-summary.md) sull'intero 200 o su un valore maggiore, perché Windows Installer 2,0 è la versione minima in grado di installare i componenti a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="b93ad-109">The [**Page Count Summary**](page-count-summary.md) property must be set to the integer 200 or greater, because Windows Installer 2.0 is the minimum version that is capable of installing 64-bit components.</span></span> <span data-ttu-id="b93ad-110">I pacchetti per la piattaforma Arm64 richiedono un valore di 500 o superiore.</span><span class="sxs-lookup"><span data-stu-id="b93ad-110">Packages for the Arm64 platform require a value of 500 or greater.</span></span>
-   <span data-ttu-id="b93ad-111">Ogni componente Windows Installer a 64 bit nel pacchetto deve includere il bit **msidbComponentAttributes64bit** nella colonna Attributes della [tabella Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="b93ad-111">Each 64-bit Windows Installer component in the package must include the **msidbComponentAttributes64bit** bit in the Attributes column of the [Component Table](component-table.md).</span></span>

<span data-ttu-id="b93ad-112">Per ulteriori informazioni, vedere [Windows Installer nei sistemi operativi a 64 bit](windows-installer-on-64-bit-operating-systems.md) e [pacchetti di Windows Installer a 32 bit](32-bit-windows-installer-packages.md).</span><span class="sxs-lookup"><span data-stu-id="b93ad-112">For more information, see [Windows Installer on 64-bit Operating Systems](windows-installer-on-64-bit-operating-systems.md) and [32-bit Windows Installer Packages](32-bit-windows-installer-packages.md).</span></span>

 

 



