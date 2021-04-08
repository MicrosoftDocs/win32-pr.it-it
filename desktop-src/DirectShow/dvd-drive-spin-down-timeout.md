---
description: Timeout della rotazione dell'unità DVD
ms.assetid: 2295253d-0199-41b4-95a8-cda049ca93c7
title: Timeout della rotazione dell'unità DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acda6853830ee7289e529d029c78fe4e56e4a0e3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876834"
---
# <a name="dvd-drive-spin-down-timeout"></a><span data-ttu-id="28098-103">Timeout della rotazione dell'unità DVD</span><span class="sxs-lookup"><span data-stu-id="28098-103">DVD Drive Spin Down Timeout</span></span>

<span data-ttu-id="28098-104">Nei computer portatili, per preservare la durata della batteria può essere opportuno ridurre il tempo di esecuzione di un'unità DVD dopo che l'utente ha sospeso la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="28098-104">On laptop computers, to conserve battery life it may be desirable to reduce the length of time that a DVD drive will continue to spin after the user has paused playback.</span></span> <span data-ttu-id="28098-105">Per impostazione predefinita, il navigatore DVD mantiene la rotazione del disco per due minuti.</span><span class="sxs-lookup"><span data-stu-id="28098-105">By default, the DVD Navigator keeps the disc spinning for two minutes.</span></span> <span data-ttu-id="28098-106">Questo valore può essere modificato nel registro di sistema di Windows in questa chiave:</span><span class="sxs-lookup"><span data-stu-id="28098-106">This value can be modified in the Windows Registry under this key:</span></span>


```C++
DWORD HKLM\SOFTWARE\Microsoft\DVDNavigator\DriveSpindown 
[Sec]
```



<span data-ttu-id="28098-107">dove</span><span class="sxs-lookup"><span data-stu-id="28098-107">where</span></span>


```
Sec
```



<span data-ttu-id="28098-108">tempo di inattività in secondi.</span><span class="sxs-lookup"><span data-stu-id="28098-108">is the spin down time in seconds.</span></span>

## <a name="related-topics"></a><span data-ttu-id="28098-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="28098-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28098-110">Appendici</span><span class="sxs-lookup"><span data-stu-id="28098-110">Appendixes</span></span>](appendixes.md)
</dt> </dl>

 

 



