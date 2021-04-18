---
description: Un servizio, un driver o un'applicazione che desidera fornire dati del contatore può scrivere una DLL di prestazioni per fornire i dati.
ms.assetid: 030316e5-f9f3-4333-9bb4-7ad301bbe7bf
title: Fornire dati del contatore mediante una DLL di prestazioni
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: e14b8a0e59b1fc9af3d8cad6e895d4a0067b9ae6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312098"
---
# <a name="providing-counter-data-using-a-performance-dll"></a><span data-ttu-id="6402e-103">Fornire dati del contatore mediante una DLL di prestazioni</span><span class="sxs-lookup"><span data-stu-id="6402e-103">Providing Counter Data Using a Performance DLL</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6402e-104">A causa di limitazioni significative in merito a prestazioni e affidabilità, il metodo per fornire i dati dei contatori delle prestazioni descritti in questo argomento può essere modificato o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="6402e-104">Due to significant performance and reliability limitations, the method for providing performance counter data that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="6402e-105">Microsoft consiglia invece di usare il metodo descritto in [fornire i dati del contatore usando la versione 2,0](providing-counter-data-using-version-2-0.md) per la creazione di nuovi contatori delle prestazioni e di migrare i contatori delle prestazioni esistenti per usare anche tale metodo.</span><span class="sxs-lookup"><span data-stu-id="6402e-105">Instead, Microsoft recommends that you use the method described in [Providing Counter Data Using Version 2.0](providing-counter-data-using-version-2-0.md) for creating new performance counters, and that you migrate existing performance counters to use that method as well.</span></span>

<span data-ttu-id="6402e-106">Un servizio, un driver o un'applicazione che desidera fornire dati del contatore può scrivere una DLL di prestazioni per fornire i dati.</span><span class="sxs-lookup"><span data-stu-id="6402e-106">A service, driver, or application that wants to provide counter data can write a performance DLL to provide the data.</span></span> <span data-ttu-id="6402e-107">Quando un consumer esegue una query sui dati sulle prestazioni, il sistema carica la DLL del provider nel processo del consumer e chiama il provider per raccogliere i dati.</span><span class="sxs-lookup"><span data-stu-id="6402e-107">When a consumer queries performance data, the system loads the provider DLL into the consumer's process and calls the provider to collect the data.</span></span> <span data-ttu-id="6402e-108">Per informazioni dettagliate sulla scrittura della DLL di prestazioni, vedere [creazione di una DLL di estensione](creating-a-performance-extension-dll.md)per le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="6402e-108">For details on writing the performance DLL, see [Creating a Performance Extension DLL](creating-a-performance-extension-dll.md).</span></span>

<span data-ttu-id="6402e-109">Il sistema utilizza il registro di sistema per determinare il provider da chiamare.</span><span class="sxs-lookup"><span data-stu-id="6402e-109">The system uses the registry to determine which provider to call.</span></span> <span data-ttu-id="6402e-110">Per informazioni sulla registrazione del provider e dei contatori supportati, vedere [aggiunta di contatori delle prestazioni](adding-performance-counters.md).</span><span class="sxs-lookup"><span data-stu-id="6402e-110">For information on registering your provider and the counters that it supports, see [Adding Performance Counters](adding-performance-counters.md).</span></span>

> [!Note]
> <span data-ttu-id="6402e-111">Le DLL delle prestazioni non sono supportate in Windows OneCore.</span><span class="sxs-lookup"><span data-stu-id="6402e-111">Performance DLLs are not supported on Windows OneCore.</span></span> <span data-ttu-id="6402e-112">Se si scrive un componente che deve essere eseguito in Windows OneCore, usare il metodo descritto in [fornire dati del contatore usando la versione 2,0](providing-counter-data-using-version-2-0.md).</span><span class="sxs-lookup"><span data-stu-id="6402e-112">If writing a component that must run on Windows OneCore, use the method described in [Providing Counter Data Using Version 2.0](providing-counter-data-using-version-2-0.md).</span></span>
