---
description: Un processo in due passaggi estende il modello di transazione Windows Installer ai prodotti contenenti Common Language Runtime assembly. Ciò consente al programma di installazione di eseguire il rollback di installazioni e rimozioni non riuscite degli assembly.
ms.assetid: 065a380c-4eb5-48a5-ab0a-7f1229b77898
title: Rollback degli assembly nella global assembly cache
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c84bc3107355cb50c17043ee571edff708ba3f6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751119"
---
# <a name="rollback-of-assemblies-in-the-global-assembly-cache"></a><span data-ttu-id="309a1-104">Rollback degli assembly nella global assembly cache</span><span class="sxs-lookup"><span data-stu-id="309a1-104">Rollback of Assemblies in the Global Assembly Cache</span></span>

<span data-ttu-id="309a1-105">Un processo in due passaggi estende il modello di transazione Windows Installer ai prodotti contenenti Common Language Runtime assembly.</span><span class="sxs-lookup"><span data-stu-id="309a1-105">A two-step process extends the Windows Installer's transaction model to products containing common language runtime assemblies.</span></span> <span data-ttu-id="309a1-106">Ciò consente al programma di installazione di eseguire il rollback di installazioni e rimozioni non riuscite degli assembly.</span><span class="sxs-lookup"><span data-stu-id="309a1-106">This enables the installer to rollback unsuccessful installations and removals of assemblies.</span></span>

<span data-ttu-id="309a1-107">Durante il primo passaggio, il Windows Installer utilizza il Framework Microsoft .NET per creare un'interfaccia per ogni assembly.</span><span class="sxs-lookup"><span data-stu-id="309a1-107">During the first step, the Windows Installer uses the Microsoft .NET Framework to create one interface for each assembly.</span></span> <span data-ttu-id="309a1-108">Il Windows Installer utilizza il numero di interfacce disponibili per l'installazione degli assembly.</span><span class="sxs-lookup"><span data-stu-id="309a1-108">The Windows Installer uses as many interfaces as there are assemblies being installed.</span></span> <span data-ttu-id="309a1-109">Il commit di un assembly tramite una di queste interfacce significa solo che l'assembly è pronto per sostituire qualsiasi assembly esistente con lo stesso nome, ma non lo sostituisce.</span><span class="sxs-lookup"><span data-stu-id="309a1-109">Committing an assembly using one of these interfaces only means that the assembly is ready to replace any existing assembly with the same name, it does not yet replace it.</span></span> <span data-ttu-id="309a1-110">Se l'utente annulla l'installazione o se si verifica un errore di installazione irreversibile, il Windows Installer può comunque eseguire il rollback dell'assembly allo stato precedente rilasciando tali interfacce.</span><span class="sxs-lookup"><span data-stu-id="309a1-110">If the user cancels the installation, or if there is a fatal installation error, the Windows Installer can still rollback the assembly to its previous state by releasing these interfaces.</span></span>

<span data-ttu-id="309a1-111">Al termine Windows Installer dell'installazione di tutti gli assembly e dei componenti Windows Installer, il programma di installazione può avviare il secondo passaggio dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="309a1-111">After the Windows Installer completes installing all assemblies and Windows Installer components, the installer may initiate the second step of the installation.</span></span> <span data-ttu-id="309a1-112">Il secondo passaggio usa una funzione separata per eseguire il commit finale di tutti i nuovi assembly di Common Language Runtime.</span><span class="sxs-lookup"><span data-stu-id="309a1-112">The second step uses a separate function to do the final commit of all the new common language runtime assemblies.</span></span> <span data-ttu-id="309a1-113">Vengono sostituiti tutti gli assembly esistenti con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="309a1-113">This replaces any existing assemblies with the same name.</span></span>

 

 



