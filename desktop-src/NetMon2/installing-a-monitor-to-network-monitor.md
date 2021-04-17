---
description: L'installazione di una DLL di monitoraggio è un processo semplice.
ms.assetid: f2c18faa-0010-4d26-b7e9-e8a7b5d11981
title: Installazione di un monitoraggio per Network Monitor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7fb6847d1ea93895b190ce2377247c586c06f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234348"
---
# <a name="installing-a-monitor-to-network-monitor"></a><span data-ttu-id="8f724-103">Installazione di un monitoraggio per Network Monitor</span><span class="sxs-lookup"><span data-stu-id="8f724-103">Installing a Monitor to Network Monitor</span></span>

<span data-ttu-id="8f724-104">L'installazione di una DLL di monitoraggio è un processo semplice.</span><span class="sxs-lookup"><span data-stu-id="8f724-104">Installing a monitor DLL is a simple process.</span></span> <span data-ttu-id="8f724-105">Prima di tutto, copiare la DLL e il modulo di configurazione HTML associato nella sottodirectory dei monitoraggi di NPP (ad esempio, C: \\ Windows \\ system32 \\ NPP \\ Monitors).</span><span class="sxs-lookup"><span data-stu-id="8f724-105">First, copy the DLL and the associated HTML configuration form to your NPP Monitors subdirectory (for example, C:\\Windows\\System32\\Npp\\Monitors).</span></span> <span data-ttu-id="8f724-106">Quando viene copiato nella directory, il monitoraggio verrà riconosciuto e disponibile alla successiva attivazione dello strumento di controllo di monitoraggio o del servizio di controllo di monitoraggio (MCSVC).</span><span class="sxs-lookup"><span data-stu-id="8f724-106">When copied to the directory, the monitor will be recognized and available the next time the Monitor Control Tool or Monitor Control Service (MCSVC) is activated.</span></span>

<span data-ttu-id="8f724-107">Se, ad esempio, la variabile di ambiente% SystemRoot% è C: \\ Windows, il monitoraggio sottodirectory è c: \\ Windows \\ system32 \\ NPP \\ Monitors.</span><span class="sxs-lookup"><span data-stu-id="8f724-107">For example, if the environment variable, %SystemRoot% is C:\\Windows, then the monitor subdirectory is C:\\Windows\\System32\\Npp\\Monitors.</span></span>

 

 



