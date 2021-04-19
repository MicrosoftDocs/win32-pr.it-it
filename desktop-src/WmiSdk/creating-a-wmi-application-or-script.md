---
description: Qualsiasi linguaggio di scripting, ad esempio VBScript, che funziona con gli oggetti ActiveX può accedere ai dati WMI. Le applicazioni possono accedere a WMI in C++, usando l'API COM per WMI o in Visual Basic, usando la libreria dei tipi wbemdisp. tlb e l'API di scripting per WMI. .
ms.assetid: c0d18827-6b36-4817-8cd9-06cd0f267b28
ms.tgt_platform: multiple
title: Creazione di un'applicazione o di uno script WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b27e3cffd7e4d9bea4ce36e7c0da77ae5d72cdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317563"
---
# <a name="creating-a-wmi-application-or-script"></a><span data-ttu-id="4320a-105">Creazione di un'applicazione o di uno script WMI</span><span class="sxs-lookup"><span data-stu-id="4320a-105">Creating a WMI Application or Script</span></span>

<span data-ttu-id="4320a-106">Qualsiasi linguaggio di scripting, ad esempio VBScript, che funziona con gli oggetti ActiveX può accedere ai dati WMI.</span><span class="sxs-lookup"><span data-stu-id="4320a-106">Any scripting language, such as VBScript, that works with ActiveX objects can access WMI data.</span></span> <span data-ttu-id="4320a-107">Le applicazioni possono accedere a WMI in C++, usando l' [API com per WMI](com-api-for-wmi.md) o in Visual Basic, usando la [libreria dei tipi](using-the-wmi-scripting-type-library.md) wbemdisp. tlb e l' [API di scripting per WMI](scripting-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="4320a-107">Applications can access WMI in C++, using the [COM API for WMI](com-api-for-wmi.md) or in Visual Basic, using the Wbemdisp.tlb [type library](using-the-wmi-scripting-type-library.md) and the [Scripting API for WMI](scripting-api-for-wmi.md).</span></span> <span data-ttu-id="4320a-108">.</span><span class="sxs-lookup"><span data-stu-id="4320a-108">.</span></span> <span data-ttu-id="4320a-109">È possibile ottenere dati tramite WMI scrivendo uno script, una pagina di Active Server (ASP) o un'applicazione HTML (HTA).</span><span class="sxs-lookup"><span data-stu-id="4320a-109">You can obtain data through WMI by writing a script, an Active Server Page (ASP), or an HTML application (HTA).</span></span> <span data-ttu-id="4320a-110">È anche possibile usare Windows PowerShell per ottenere dati o scrivere script.</span><span class="sxs-lookup"><span data-stu-id="4320a-110">You can also use Windows PowerShell to obtain data or write scripts.</span></span> <span data-ttu-id="4320a-111">Per ulteriori informazioni, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script) e [Introduzione con Windows PowerShell](/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="4320a-111">For more information, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script) and [Getting Started with Windows PowerShell](/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7&preserve-view=true).</span></span> <span data-ttu-id="4320a-112">TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) contiene centinaia di esempi di scripting.</span><span class="sxs-lookup"><span data-stu-id="4320a-112">The TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) contains hundreds of scripting examples.</span></span> <span data-ttu-id="4320a-113">Per ulteriori informazioni sulle risorse di stampa e online, vedere [ulteriori informazioni](further-information.md).</span><span class="sxs-lookup"><span data-stu-id="4320a-113">For more information about print and online resources, see [Further Information](further-information.md).</span></span>

<span data-ttu-id="4320a-114">Nella procedura riportata di seguito viene descritto come connettersi all'archivio dati e al servizio WMI.</span><span class="sxs-lookup"><span data-stu-id="4320a-114">The following procedure describes how to connect to the WMI service and data store.</span></span>

<span data-ttu-id="4320a-115">**Per connettersi al servizio WMI e all'archivio dati**</span><span class="sxs-lookup"><span data-stu-id="4320a-115">**To connect to the WMI service and data store**</span></span>

1.  <span data-ttu-id="4320a-116">Individuare il servizio WMI in un computer specifico.</span><span class="sxs-lookup"><span data-stu-id="4320a-116">Locate the WMI service on a specific machine.</span></span>
2.  <span data-ttu-id="4320a-117">Connettersi a uno o più spazi dei nomi WMI.</span><span class="sxs-lookup"><span data-stu-id="4320a-117">Connect to one or more WMI namespaces.</span></span>

<span data-ttu-id="4320a-118">Queste operazioni sono diverse in C++, Visual Basic, .NET Framework linguaggi o quando si usa uno script.</span><span class="sxs-lookup"><span data-stu-id="4320a-118">These operations are different in C++, Visual Basic, .NET Framework languages, or when using a script.</span></span> <span data-ttu-id="4320a-119">Gli script e le applicazioni Visual Basic devono accedere alle classi le cui istanze vengono fornite con i dati dai provider esistenti.</span><span class="sxs-lookup"><span data-stu-id="4320a-119">Scripts and Visual Basic applications must access classes whose instances are supplied with data by existing providers.</span></span> <span data-ttu-id="4320a-120">Tuttavia, le applicazioni scritte in C++ possono eseguire altre operazioni.</span><span class="sxs-lookup"><span data-stu-id="4320a-120">But applications written in C++ can do more.</span></span> <span data-ttu-id="4320a-121">Ad esempio, un'applicazione scritta in C++ può inviare eventi, ma uno script WMI può solo sottoscrivere gli eventi di ricezione.</span><span class="sxs-lookup"><span data-stu-id="4320a-121">For example, an application written in C++ can send events, but a WMI script can only subscribe to receive events.</span></span>

<span data-ttu-id="4320a-122">Un provider WMI può essere scritto solo in C++ o utilizzando il .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="4320a-122">A WMI provider can be written only in C++ or using the .NET Framework.</span></span> <span data-ttu-id="4320a-123">Per ulteriori informazioni sulla scrittura di applicazioni in C# o Visual Basic .NET, vedere [Panoramica di WMI .NET](/previous-versions/bb404655(v=vs.90)).</span><span class="sxs-lookup"><span data-stu-id="4320a-123">For more information about writing applications in C# or Visual Basic .NET, see [WMI .NET Overview](/previous-versions/bb404655(v=vs.90)).</span></span>

<span data-ttu-id="4320a-124">Per ulteriori informazioni sulla creazione di applicazioni e script per WMI, vedere:</span><span class="sxs-lookup"><span data-stu-id="4320a-124">For more information about creating applications and scripts for WMI, see:</span></span>

-   [<span data-ttu-id="4320a-125">Creazione di un'applicazione WMI con C++</span><span class="sxs-lookup"><span data-stu-id="4320a-125">Creating a WMI Application Using C++</span></span>](creating-a-wmi-application-using-c-.md)
-   [<span data-ttu-id="4320a-126">Creazione di uno script WMI</span><span class="sxs-lookup"><span data-stu-id="4320a-126">Creating a WMI Script</span></span>](creating-a-wmi-script.md)
-   [<span data-ttu-id="4320a-127">Creazione di un client WMI gestito</span><span class="sxs-lookup"><span data-stu-id="4320a-127">Creating a Managed WMI Client</span></span>](creating-a-managed-wmi-client.md)

<span data-ttu-id="4320a-128">Per eseguire la maggior parte delle attività, utilizzare le [classi WMI](wmi-classes.md)preinstallate.</span><span class="sxs-lookup"><span data-stu-id="4320a-128">To perform most tasks, use the preinstalled [WMI classes](wmi-classes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4320a-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4320a-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4320a-130">Utilizzo di WMI</span><span class="sxs-lookup"><span data-stu-id="4320a-130">Using WMI</span></span>](using-wmi.md)
</dt> </dl>

 

 
