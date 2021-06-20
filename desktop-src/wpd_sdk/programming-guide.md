---
title: Guida alla programmazione WPD
description: Questa guida alla programmazione è incentrata sul modo in cui le attività di esempio vengono eseguite usando le interfacce e i metodi WPD disponibili nelle interfacce.
ms.assetid: 87777b0b-a7a0-4032-99bb-92b717d3c452
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db13d50942c28cd4937d27a745d61d7a30a01a15
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409864"
---
# <a name="wpd-programming-guide"></a><span data-ttu-id="41973-103">Guida alla programmazione WPD</span><span class="sxs-lookup"><span data-stu-id="41973-103">WPD programming guide</span></span>

<span data-ttu-id="41973-104">L'origine principale per questa guida alla programmazione è un esempio fornito con Il Software Development Kit (SDK) WPD (Windows Portable Devices).</span><span class="sxs-lookup"><span data-stu-id="41973-104">The primary source for this programming guide is a sample that ships with the Windows Portable Devices (WPD) Software Development Kit (SDK).</span></span> <span data-ttu-id="41973-105">Questo esempio, denominato WpdApiSample.exe, è costituito da sette moduli con estensione cpp.</span><span class="sxs-lookup"><span data-stu-id="41973-105">This sample, named WpdApiSample.exe, consists of seven .cpp modules.</span></span> <span data-ttu-id="41973-106">Sei di questi moduli contengono il codice che illustra 26 attività che un'applicazione può eseguire usando l'API (Application Programming Interface) WPD.</span><span class="sxs-lookup"><span data-stu-id="41973-106">Six of these modules contain the code that demonstrates 26 tasks that an application can accomplish using the WPD application programming interface (API).</span></span>

<span data-ttu-id="41973-107">Le eccezioni a precedenti sono gli argomenti che descrivono le attività del servizio dispositivo, il menu di scelta rapida e le estensioni della finestra delle proprietà; questi argomenti non sono stati presi da WpdApiSample.</span><span class="sxs-lookup"><span data-stu-id="41973-107">The exceptions to the above are the topics that describe: device service tasks, the context menu and property sheet extensions; these topics were not taken from WpdApiSample.</span></span> <span data-ttu-id="41973-108">Le attività del servizio dispositivo si basano sull'esempio denominato WpdServiceApiSample.</span><span class="sxs-lookup"><span data-stu-id="41973-108">The device service tasks are based on the sample named WpdServiceApiSample.</span></span> <span data-ttu-id="41973-109">Le estensioni del menu di scelta rapida e della finestra delle proprietà sono frammenti di codice provenienti da applicazioni che non vengono forniti con il Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="41973-109">The context menu and property sheet extensions are snippets taken from applications that do not ship with the Windows SDK.</span></span>

<span data-ttu-id="41973-110">Le sezioni seguenti sono incentrate sulle attività eseguite da questi esempi e illustrano come ognuna viene eseguita usando le interfacce WPD e alcuni dei metodi disponibili in queste interfacce.</span><span class="sxs-lookup"><span data-stu-id="41973-110">The following sections focus on the tasks accomplished by these samples and explain how each is accomplished using the WPD interfaces and a number of the methods found in these interfaces.</span></span>

## <a name="related-topics"></a><span data-ttu-id="41973-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="41973-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41973-112">**Dispositivi portatili Windows**</span><span class="sxs-lookup"><span data-stu-id="41973-112">**Windows Portable Devices**</span></span>](/windows/desktop/windows-portable-devices)
</dt> </dl>

 

 
