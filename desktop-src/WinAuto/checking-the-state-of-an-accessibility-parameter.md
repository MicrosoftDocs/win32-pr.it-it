---
title: Verifica dello stato di un parametro di accessibilità
description: Il frammento di codice seguente usa la funzione GetSystemMetrics per controllare il parametro ShowSounds. Se GetSystemMetrics restituisce TRUE, l'applicazione deve presentare tutte le informazioni importanti in formato visivo.
ms.assetid: fb6a0adf-ca38-4e21-9edd-1abb2efd59e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75409f5af96f83bf13f4834f83503579862caa97
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046835"
---
# <a name="checking-the-state-of-an-accessibility-parameter"></a><span data-ttu-id="e34af-104">Verifica dello stato di un parametro di accessibilità</span><span class="sxs-lookup"><span data-stu-id="e34af-104">Checking the State of an Accessibility Parameter</span></span>

<span data-ttu-id="e34af-105">Il frammento di codice seguente usa la funzione [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) per controllare il parametro ShowSounds.</span><span class="sxs-lookup"><span data-stu-id="e34af-105">The following code fragment uses the [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) function to check the ShowSounds parameter.</span></span> <span data-ttu-id="e34af-106">Se **GetSystemMetrics** restituisce **true**, l'applicazione deve presentare tutte le informazioni importanti in formato visivo.</span><span class="sxs-lookup"><span data-stu-id="e34af-106">If **GetSystemMetrics** returns **TRUE**, the application should present all important information in visual form.</span></span>


```C++
BOOL fShowSounds; 
fShowSounds = GetSystemMetrics(SM_SHOWSOUNDS); 
```



 

 