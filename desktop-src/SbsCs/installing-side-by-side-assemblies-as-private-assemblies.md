---
description: Per installare assembly side-by-side come assembly privati, è possibile installare l'assembly come componente di un pacchetto di installazione.
ms.assetid: 1cfd836f-a1b9-4339-8756-5488c88b3c2b
title: Installazione di assembly side-by-side come assembly privati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7719a9887f9e92d81e2ad65fe2e75424f0b6957
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306478"
---
# <a name="installing-side-by-side-assemblies-as-private-assemblies"></a><span data-ttu-id="154be-103">Installazione di assembly side-by-side come assembly privati</span><span class="sxs-lookup"><span data-stu-id="154be-103">Installing Side-by-side Assemblies as Private Assemblies</span></span>

<span data-ttu-id="154be-104">Per installare [assembly side-by-side](about-side-by-side-assemblies-.md) come [assembly privati](/windows/desktop/Msi/private-assemblies), è possibile installare l'assembly come componente di un pacchetto di installazione.</span><span class="sxs-lookup"><span data-stu-id="154be-104">To install [side-by-side assemblies](about-side-by-side-assemblies-.md) as [private assemblies](/windows/desktop/Msi/private-assemblies), you can install the assembly as a component of an installer package.</span></span> <span data-ttu-id="154be-105">Può trattarsi dello stesso pacchetto di installazione usato per installare o aggiornare l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="154be-105">This can be the same installation package used to install or update your application.</span></span> <span data-ttu-id="154be-106">Per installare gli assembly è necessario Windows Installer versione 2,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="154be-106">Windows Installer version 2.0 or later is required to install assemblies.</span></span> <span data-ttu-id="154be-107">Per ulteriori informazioni, vedere il [Windows Installer](../msi/windows-installer-portal.md) SDK e le sezioni in [installazione degli assembly Win32](../msi/installation-of-win32-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="154be-107">For more information, see the [Windows Installer](../msi/windows-installer-portal.md) SDK and the sections under [Installation of Win32 Assemblies](../msi/installation-of-win32-assemblies.md).</span></span>

<span data-ttu-id="154be-108">In alternativa, è possibile usare il programma di installazione per copiare un assembly privato e un manifesto nella stessa cartella del file eseguibile dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="154be-108">As an alternative, you can use the installer to copy a private assembly and manifest into the same folder as the application's executable file.</span></span>

 

 
