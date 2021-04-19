---
title: Guida alla programmazione di WPD
description: Guida per programmatori
ms.assetid: 87777b0b-a7a0-4032-99bb-92b717d3c452
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f774ffd9d7576a07b34c467a5a155d98e4f3e703
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317848"
---
# <a name="wpd-programming-guide"></a><span data-ttu-id="d838d-103">Guida alla programmazione di WPD</span><span class="sxs-lookup"><span data-stu-id="d838d-103">WPD programming guide</span></span>

<span data-ttu-id="d838d-104">L'origine primaria per questa guida di programmazione è un esempio fornito con il Software Development Kit (SDK) Windows Portable Devices (WPD).</span><span class="sxs-lookup"><span data-stu-id="d838d-104">The primary source for this programming guide is a sample that ships with the Windows Portable Devices (WPD) Software Development Kit (SDK).</span></span> <span data-ttu-id="d838d-105">Questo esempio, denominato WpdApiSample.exe, è costituito da sette moduli cpp.</span><span class="sxs-lookup"><span data-stu-id="d838d-105">This sample, named WpdApiSample.exe, consists of seven .cpp modules.</span></span> <span data-ttu-id="d838d-106">Sei di questi moduli contengono il codice che illustra 26 attività che un'applicazione può eseguire usando WPD Application Programming Interface (API).</span><span class="sxs-lookup"><span data-stu-id="d838d-106">Six of these modules contain the code that demonstrates 26 tasks that an application can accomplish using the WPD application programming interface (API).</span></span>

<span data-ttu-id="d838d-107">Le eccezioni al precedente sono gli argomenti che descrivono le attività del servizio del dispositivo, il menu di scelta rapida e le estensioni della finestra delle proprietà. questi argomenti non sono stati ricavati da WpdApiSample.</span><span class="sxs-lookup"><span data-stu-id="d838d-107">The exceptions to the above are the topics that describe: device service tasks, the context menu and property sheet extensions; these topics were not taken from WpdApiSample.</span></span> <span data-ttu-id="d838d-108">Le attività del servizio del dispositivo sono basate sull'esempio denominato WpdServiceApiSample.</span><span class="sxs-lookup"><span data-stu-id="d838d-108">The device service tasks are based on the sample named WpdServiceApiSample.</span></span> <span data-ttu-id="d838d-109">Il menu di scelta rapida e le estensioni della finestra delle proprietà sono frammenti di codice ricavati da applicazioni che non vengono fornite con il Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="d838d-109">The context menu and property sheet extensions are snippets taken from applications that do not ship with the Windows SDK.</span></span>

<span data-ttu-id="d838d-110">Le sezioni seguenti sono incentrate sulle attività eseguite da questi esempi e spiegano come ciascuna viene eseguita utilizzando le interfacce WPD e un numero di metodi individuati in tali interfacce.</span><span class="sxs-lookup"><span data-stu-id="d838d-110">The following sections focus on the tasks accomplished by these samples and explain how each is accomplished using the WPD interfaces and a number of the methods found in these interfaces.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d838d-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d838d-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d838d-112">**Dispositivi portatili Windows**</span><span class="sxs-lookup"><span data-stu-id="d838d-112">**Windows Portable Devices**</span></span>](/windows/desktop/windows-portable-devices)
</dt> </dl>

 

 
