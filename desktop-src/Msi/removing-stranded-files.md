---
description: Elenco dei possibili motivi per cui una disinstallazione di Windows Installer non è stata in grado di rimuovere tutti i file di un'applicazione.
ms.assetid: 0a856f0f-a829-478e-a83b-dade7b05b4f2
title: Rimozione di file bloccati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d5eeceb45c2139d146c32bdf9917e41885688df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313799"
---
# <a name="removing-stranded-files"></a><span data-ttu-id="fbc48-103">Rimozione di file bloccati</span><span class="sxs-lookup"><span data-stu-id="fbc48-103">Removing Stranded Files</span></span>

<span data-ttu-id="fbc48-104">Se un file che dovrebbe essere stato rimosso dal computer dell'utente rimane installato dopo l'esecuzione di una disinstallazione, il programma di installazione potrebbe non rimuovere il componente contenente il file per uno o più dei seguenti motivi:</span><span class="sxs-lookup"><span data-stu-id="fbc48-104">If a file that should have been removed from the user's computer remains installed after running an uninstall, the installer may not be removing the component containing the file for one or more of the following reasons:</span></span>

-   <span data-ttu-id="fbc48-105">Il bit msidbComponentAttributesPermanent è stato impostato per il componente nella colonna Attributes della [tabella Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="fbc48-105">The msidbComponentAttributesPermanent bit was set for the component in the Attributes column of the [Component table](component-table.md).</span></span>
-   <span data-ttu-id="fbc48-106">Nessun valore immesso per il componente nella colonna ComponentId della tabella Component.</span><span class="sxs-lookup"><span data-stu-id="fbc48-106">No value was entered for the component in the ComponentId column of the Component table.</span></span>
-   <span data-ttu-id="fbc48-107">Il componente viene utilizzato da un'altra applicazione o funzionalità ancora installata.</span><span class="sxs-lookup"><span data-stu-id="fbc48-107">The component is used by another application or feature that is still installed.</span></span>
-   <span data-ttu-id="fbc48-108">Nella tabella della [condizione](condition-table.md) è specificata una condizione che Abilita una funzionalità durante l'installazione e Disabilita la funzionalità durante la disinstallazione.</span><span class="sxs-lookup"><span data-stu-id="fbc48-108">There is a condition specified in the [Condition](condition-table.md) table that enables a feature during installation and disables the feature during uninstallation.</span></span>
-   <span data-ttu-id="fbc48-109">Il file di chiave per il componente presenta un conteggio dei riferimenti precedente in **HKLM** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **SharedDLLs**.</span><span class="sxs-lookup"><span data-stu-id="fbc48-109">The key file for the component has a previous reference count under **HKLM**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**SharedDLLs**.</span></span>
-   <span data-ttu-id="fbc48-110">Il componente viene installato nella cartella di sistema e tutti i file nel componente hanno un conteggio dei riferimenti precedente in **HKLM** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **SharedDLLs**.</span><span class="sxs-lookup"><span data-stu-id="fbc48-110">The component is installed in the System folder and any file in the component has a previous reference count under **HKLM**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**SharedDLLs**.</span></span>
-   <span data-ttu-id="fbc48-111">Il Windows Installer non rimuove i file o le chiavi del registro di sistema protetti da [Protezione risorse di Windows](../wfp/windows-resource-protection-portal.md) (WRP).</span><span class="sxs-lookup"><span data-stu-id="fbc48-111">The Windows Installer does not remove any files or registry keys that are protected by [Windows Resource Protection](../wfp/windows-resource-protection-portal.md) (WRP).</span></span> <span data-ttu-id="fbc48-112">Per ulteriori informazioni, vedere [utilizzo di Windows Installer e protezione risorse di Windows](windows-resource-protection-on-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="fbc48-112">For more information, see [Using Windows Installer and Windows Resource Protection](windows-resource-protection-on-windows-vista.md).</span></span> <span data-ttu-id="fbc48-113">In Windows Server 2003, Windows XP e Windows 2000, il programma di installazione non rimuove i file protetti da protezione file Windows (PAM).</span><span class="sxs-lookup"><span data-stu-id="fbc48-113">On Windows Server 2003, Windows XP, and Windows 2000, the installer does not remove any files that are protected by Windows File Protection (WFP).</span></span> <span data-ttu-id="fbc48-114">Se il file del percorso della chiave o la chiave del registro di sistema di un componente è protetta da WFP o WRP, il programma di installazione non rimuove il componente.</span><span class="sxs-lookup"><span data-stu-id="fbc48-114">If a component's key path file or registry key is protected by WFP or WRP, the installer does not remove the component.</span></span>
    > [!Note]  
    > <span data-ttu-id="fbc48-115">Poiché Windows Installer non installa, aggiorna o rimuove alcuna risorsa protetta da WRP, è consigliabile non includere le risorse protette in un pacchetto di installazione.</span><span class="sxs-lookup"><span data-stu-id="fbc48-115">Because Windows Installer does not install, update, or remove any resource that is protected by WRP, you should not include protected resources in an installation package.</span></span> <span data-ttu-id="fbc48-116">Usare invece solo i [meccanismi di sostituzione delle risorse supportati](../wfp/supported-file-replacement-mechanisms.md) descritti nella sezione [Protezione risorse di Windows](../wfp/windows-resource-protection-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="fbc48-116">Instead, use only the [supported resource replacement mechanisms](../wfp/supported-file-replacement-mechanisms.md) described in the [Windows Resource Protection](../wfp/windows-resource-protection-portal.md) section.</span></span>

     

 

 
