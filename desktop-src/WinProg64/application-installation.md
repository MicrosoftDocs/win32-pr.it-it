---
title: Installazione di applicazioni su sistemi a 64 bit
description: Il Windows Installer a 64 bit può installare facilmente applicazioni basate su MSI a 32 bit in Windows a 64 bit.
ms.assetid: fb9c5720-9906-4827-9daf-d7caa453e818
keywords:
- Programmazione Windows a 64 bit per l'installazione dell'applicazione
- installazione della programmazione Windows a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13a5f8f623776ffa637718fc0d565f2c71a7b8e6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118015"
---
# <a name="application-installation-on-64-bit-systems"></a><span data-ttu-id="01339-105">Installazione di applicazioni su sistemi a 64 bit</span><span class="sxs-lookup"><span data-stu-id="01339-105">Application Installation on 64-bit Systems</span></span>

<span data-ttu-id="01339-106">Il [Windows Installer a 64 bit](/windows/desktop/Msi/windows-installer-on-64-bit-operating-systems) può installare facilmente applicazioni basate su MSI a 32 bit in Windows a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="01339-106">The [64-bit Windows Installer](/windows/desktop/Msi/windows-installer-on-64-bit-operating-systems) can seamlessly install 32-bit MSI-based applications on 64-bit Windows.</span></span> <span data-ttu-id="01339-107">Per le applicazioni meno recenti che usano uno stub a 16 bit per avviare un motore di installazione a 32 bit, Windows a 64 bit riconosce specifici programmi del programma di installazione a 16 bit e sostituisce una versione a 32 bit portata.</span><span class="sxs-lookup"><span data-stu-id="01339-107">For older applications that use a 16-bit stub to launch a 32-bit installation engine, 64-bit Windows recognizes specific 16-bit installer programs and substitutes a ported 32-bit version.</span></span>

<span data-ttu-id="01339-108">le applicazioni DOS, Windows o OS/2 a 16 bit utilizzano spesso uno stub a 16 bit per verificare il tipo di computer, quindi avviano un motore di installazione a 32 bit per eseguire effettivamente l'installazione.</span><span class="sxs-lookup"><span data-stu-id="01339-108">16-bit DOS, Windows, or OS/2 applications often use a 16-bit stub to check the machine type, then launch a 32-bit installation engine to actually perform the installation.</span></span> <span data-ttu-id="01339-109">Per consentire l'installazione di applicazioni che utilizzano questa tecnica, Windows a 64 bit sostituisce le versioni a 32 bit per i seguenti programmi del programma di installazione a 16 bit:</span><span class="sxs-lookup"><span data-stu-id="01339-109">To enable installation of applications that use this technique, 64-bit Windows substitutes 32-bit versions for the following 16-bit installer programs:</span></span>

* <span data-ttu-id="01339-110">Installazione Microsoft per Windows 1,2</span><span class="sxs-lookup"><span data-stu-id="01339-110">Microsoft Setup for Windows 1.2</span></span>  
* <span data-ttu-id="01339-111">Installazione Microsoft per Windows 2,6</span><span class="sxs-lookup"><span data-stu-id="01339-111">Microsoft Setup for Windows 2.6</span></span>  
* <span data-ttu-id="01339-112">Installazione Microsoft per Windows 3,0</span><span class="sxs-lookup"><span data-stu-id="01339-112">Microsoft Setup for Windows 3.0</span></span>  
* <span data-ttu-id="01339-113">Installazione Microsoft per Windows 3,01</span><span class="sxs-lookup"><span data-stu-id="01339-113">Microsoft Setup for Windows 3.01</span></span>  
* <span data-ttu-id="01339-114">InstallShield 5. x</span><span class="sxs-lookup"><span data-stu-id="01339-114">InstallShield 5.x</span></span>  

<span data-ttu-id="01339-115">L'elenco di sostituzioni viene archiviato nel registro di sistema con la chiave seguente: **HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ NtVdm64**.</span><span class="sxs-lookup"><span data-stu-id="01339-115">The list of substitutions is stored in the registry under the following key: **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows NT\\CurrentVersion\\NtVdm64**.</span></span>

> [!Note]  
> <span data-ttu-id="01339-116">Questo meccanismo è disponibile solo per la compatibilità con le applicazioni a 32 bit che usano i programmi Microsoft Installer a 16 bit elencati in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="01339-116">This mechanism is provided only for compatibility with 32-bit applications that use the 16-bit Microsoft installer programs listed in this topic.</span></span> <span data-ttu-id="01339-117">L'aggiunta di programmi di installazione di terze parti non è supportata.</span><span class="sxs-lookup"><span data-stu-id="01339-117">Addition of third-party installer programs is not supported.</span></span>

 

> [!Note]  
> <span data-ttu-id="01339-118">Questo meccanismo non è incluso in Windows 10 su ARM.</span><span class="sxs-lookup"><span data-stu-id="01339-118">This mechanism is not included on Windows 10 on ARM.</span></span>

 

 

 