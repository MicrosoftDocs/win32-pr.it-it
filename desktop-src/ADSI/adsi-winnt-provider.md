---
title: Provider ADSI WinNT
description: Il provider Microsoft ADSI implementa un set di oggetti ADSI per supportare varie interfacce ADSI.
ms.assetid: 6341be08-2e53-4708-a403-09c86fcc31a8
ms.tgt_platform: multiple
keywords:
- ADSI del provider ADSI WinNT
- ADSI provider di servizi WinNT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9748e17185417eb382281774c31554cb983742
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395298"
---
# <a name="adsi-winnt-provider"></a><span data-ttu-id="e4380-105">Provider ADSI WinNT</span><span class="sxs-lookup"><span data-stu-id="e4380-105">ADSI WinNT Provider</span></span>

<span data-ttu-id="e4380-106">Il provider Microsoft ADSI implementa un set di oggetti ADSI per supportare varie interfacce ADSI.</span><span class="sxs-lookup"><span data-stu-id="e4380-106">The Microsoft ADSI provider implements a set of ADSI objects to support various ADSI interfaces.</span></span> <span data-ttu-id="e4380-107">Il nome dello spazio dei nomi per il provider di Windows è "WinNT" e questo provider è comunemente denominato provider WinNT.</span><span class="sxs-lookup"><span data-stu-id="e4380-107">The namespace name for the Windows provider is "WinNT" and this provider is commonly referred to as the WinNT provider.</span></span> <span data-ttu-id="e4380-108">Per accedere al provider WinNT, eseguire l'associazione a uno degli [oggetti ADSI di WinNT](adsi-objects-of-winnt.md), usando [WinNT ADsPath](winnt-adspath.md).</span><span class="sxs-lookup"><span data-stu-id="e4380-108">To access the WinNT provider, bind to any of the [ADSI objects of WinNT](adsi-objects-of-winnt.md), using the [WinNT AdsPath](winnt-adspath.md).</span></span>

<span data-ttu-id="e4380-109">Il provider WinNT è incluso nel componente di sistema ADSI per Windows e Windows Server.</span><span class="sxs-lookup"><span data-stu-id="e4380-109">The WinNT provider is included in the ADSI system component for Windows and Windows Server.</span></span>

> [!Note]  
> <span data-ttu-id="e4380-110">Il provider WinNT predefinito non può essere considerato completamente thread-safe.</span><span class="sxs-lookup"><span data-stu-id="e4380-110">The default WinNT provider cannot be assumed to be completely thread-safe.</span></span> <span data-ttu-id="e4380-111">I writer di applicazioni multithread devono gestire il multithreading per coordinare correttamente l'accesso tra thread attraverso l'uso corretto di oggetti di sincronizzazione quali semafori, mutex, sezioni critiche e così via.</span><span class="sxs-lookup"><span data-stu-id="e4380-111">Writers of multithreaded applications should handle multithreading to properly coordinate any access between threads through the proper use of synchronization objects such as semaphores, mutexes, critical sections, and so on.</span></span>

 

 

 




