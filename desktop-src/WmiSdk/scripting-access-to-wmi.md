---
description: Gli script possono accedere a tutte le classi WMI per gli oggetti hardware e software.
ms.assetid: dbb29bc8-a675-4538-99f4-00613c83eeaa
ms.tgt_platform: multiple
title: Creazione di script per l'accesso a WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd487c127c670f9ddee9596e44c4b2b9691ed880
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226829"
---
# <a name="scripting-access-to-wmi"></a><span data-ttu-id="82189-103">Creazione di script per l'accesso a WMI</span><span class="sxs-lookup"><span data-stu-id="82189-103">Scripting Access to WMI</span></span>

<span data-ttu-id="82189-104">Gli script possono accedere a tutte le classi WMI per gli oggetti hardware e software.</span><span class="sxs-lookup"><span data-stu-id="82189-104">Scripts can access all WMI classes for hardware and software objects.</span></span> <span data-ttu-id="82189-105">Gli script di Windows script host (WSH) possono eseguire operazioni sugli oggetti file system, modificare le stampanti di rete o modificare le variabili di ambiente.</span><span class="sxs-lookup"><span data-stu-id="82189-105">Windows Script Host (WSH) scripts can perform operations on file system objects, manipulate network printers, or change environment variables.</span></span> <span data-ttu-id="82189-106">È possibile trovare una serie di attività amministrative e brevi istruzioni su come eseguirle in WMI nelle [attività WMI per gli script e le applicazioni](wmi-tasks-for-scripts-and-applications.md).</span><span class="sxs-lookup"><span data-stu-id="82189-106">You can find a variety of administrator tasks and brief guidance on how to accomplish them in WMI at [WMI Tasks for Scripts and Applications](wmi-tasks-for-scripts-and-applications.md).</span></span> <span data-ttu-id="82189-107">Per ulteriori informazioni ed esempi, vedere il repository di [script](https://www.microsoft.com/technet/scriptcenter/scripts/default.mspx)TechNet ScriptCenter.</span><span class="sxs-lookup"><span data-stu-id="82189-107">For more information and examples, see the TechNet ScriptCenter [Script Repository](https://www.microsoft.com/technet/scriptcenter/scripts/default.mspx).</span></span>

<span data-ttu-id="82189-108">Se non si ha familiarità con lo scripting o con lo scripting specifico di WMI, vedere la sezione TechNet ScriptCenter [Introduzione](https://www.microsoft.com/technet/scriptcenter/hubs/start.mspx).</span><span class="sxs-lookup"><span data-stu-id="82189-108">If you are new to scripting or to WMI-specific scripting, see the TechNet ScriptCenter section [Getting Started](https://www.microsoft.com/technet/scriptcenter/hubs/start.mspx).</span></span>

<span data-ttu-id="82189-109">Con l' [API di scripting per WMI](scripting-api-for-wmi.md)è possibile sviluppare script rapidi e semplici o applicazioni complesse.</span><span class="sxs-lookup"><span data-stu-id="82189-109">With the [Scripting API for WMI](scripting-api-for-wmi.md), you can develop quick, simple scripts or complex applications.</span></span> <span data-ttu-id="82189-110">Lo scripting offre la stessa funzionalità per ottenere informazioni o per configurare la maggior parte degli oggetti in un'organizzazione come se si trattasse di un'applicazione C++ o C#.</span><span class="sxs-lookup"><span data-stu-id="82189-110">Scripting gives you the same capability of getting information or of configuring most objects in an enterprise as you would have through a C++ or C# application.</span></span> <span data-ttu-id="82189-111">Per ulteriori informazioni, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="82189-111">For more information, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="82189-112">Non è possibile scrivere un [*provider WMI*](gloss-p.md) nello script.</span><span class="sxs-lookup"><span data-stu-id="82189-112">You cannot write a [*WMI provider*](gloss-p.md) in script.</span></span> <span data-ttu-id="82189-113">Per ulteriori informazioni, vedere la pagina relativa [alla fornitura di dati a WMI](providing-data-to-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="82189-113">For more information, see [Providing Data to WMI](providing-data-to-wmi.md).</span></span>

<span data-ttu-id="82189-114">Gli script WMI possono essere scritti in qualsiasi linguaggio di scripting in grado di interagire con gli oggetti ActiveX.</span><span class="sxs-lookup"><span data-stu-id="82189-114">WMI scripts can be written in any scripting language that can interact with ActiveX objects.</span></span>

<span data-ttu-id="82189-115">Windows PowerShell offre un ambiente semplice per l'amministrazione e lo script WMI.</span><span class="sxs-lookup"><span data-stu-id="82189-115">Windows PowerShell provides a simple environment for WMI administration and scripting.</span></span> <span data-ttu-id="82189-116">Per ulteriori informazioni su PowerShell, vedere [Introduzione con Windows PowerShell](/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="82189-116">For more information about PowerShell, see [Getting Started with Windows PowerShell](/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7&preserve-view=true).</span></span>

<span data-ttu-id="82189-117">Gli script di Active Directory Service Interfaces (ADSI) forniscono l'accesso agli oggetti di Active Directory Domain Services (AD DS).</span><span class="sxs-lookup"><span data-stu-id="82189-117">Active Directory Service Interfaces (ADSI) scripts provides access to Active Directory Domain Services (AD DS) objects.</span></span> <span data-ttu-id="82189-118">Gli script WSH e ADSI accedono agli oggetti e consentono procedure non disponibili tramite file batch.</span><span class="sxs-lookup"><span data-stu-id="82189-118">Both WSH and ADSI scripts access objects and allow procedures not available through batch files.</span></span>

## <a name="related-topics"></a><span data-ttu-id="82189-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="82189-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82189-120">Informazioni su WMI</span><span class="sxs-lookup"><span data-stu-id="82189-120">About WMI</span></span>](about-wmi.md)
</dt> <dt>

[<span data-ttu-id="82189-121">API di scripting per WMI</span><span class="sxs-lookup"><span data-stu-id="82189-121">Scripting API for WMI</span></span>](scripting-api-for-wmi.md)
</dt> </dl>

 

 
