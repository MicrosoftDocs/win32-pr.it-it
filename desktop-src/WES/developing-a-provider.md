---
title: Sviluppo di un provider
description: Per scrivere gli eventi definiti nel manifesto, è possibile usare le funzioni incluse nell'API traccia eventi (ETW). Per informazioni dettagliate sulla scrittura di un provider, vedere la pagina relativa alla fornitura di eventi.
ms.assetid: 23de19c4-5f8d-4faa-acd9-fe6208ca17a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83939429f1dc4d499e7c2d0e0c2bfa7a47522ffe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118315"
---
# <a name="developing-a-provider"></a><span data-ttu-id="5f510-104">Sviluppo di un provider</span><span class="sxs-lookup"><span data-stu-id="5f510-104">Developing a Provider</span></span>

<span data-ttu-id="5f510-105">Per scrivere gli eventi definiti nel manifesto, è possibile usare le funzioni incluse nell'API [traccia eventi](/windows/desktop/ETW/event-tracing-portal) (ETW).</span><span class="sxs-lookup"><span data-stu-id="5f510-105">To write the events that you define in your manifest, you use the functions included in the [Event Tracing](/windows/desktop/ETW/event-tracing-portal) (ETW) API.</span></span> <span data-ttu-id="5f510-106">Per informazioni dettagliate sulla scrittura di un provider, vedere la pagina relativa alla [fornitura di eventi](/windows/desktop/ETW/providing-events).</span><span class="sxs-lookup"><span data-stu-id="5f510-106">For details on writing a provider, see [Providing Events](/windows/desktop/ETW/providing-events).</span></span>

<span data-ttu-id="5f510-107">Dopo aver scritto il provider, usare lo strumento WevtUtil.exe per registrare il provider e lo schema.</span><span class="sxs-lookup"><span data-stu-id="5f510-107">After writing the provider, use the WevtUtil.exe tool to register the provider and schema.</span></span> <span data-ttu-id="5f510-108">Per informazioni dettagliate sull'uso di WevtUtil, vedere [strumenti del registro eventi di Windows](windows-event-log-tools.md).</span><span class="sxs-lookup"><span data-stu-id="5f510-108">For details on using WevtUtil, see [Windows Event Log Tools](windows-event-log-tools.md).</span></span> <span data-ttu-id="5f510-109">Di seguito viene illustrato come utilizzare WevtUtil per registrare un provider e rimuovere la registrazione.</span><span class="sxs-lookup"><span data-stu-id="5f510-109">The following shows how to use WevtUtil to register a provider and to remove the registration.</span></span>


```cmd
wevtutil im provider.man

wevtutil um provider.man
```