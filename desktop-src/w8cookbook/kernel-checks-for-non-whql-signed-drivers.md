---
title: Verifica del kernel per i driver non WHQL firmati
description: Per i dispositivi che puliscono l'installazione di Windows 10 e l'avvio protetto (si noti che questo è lo standard per tutti i nuovi dispositivi rispetto alla versione di Windows 8,0), tutti i nuovi driver devono essere firmati da WHQL/sysdev anziché usare semplicemente certificati con firma incrociata.
ms.assetid: D2A13F91-BA44-4044-B1F4-54393A9F1063
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 582db864627a2945debca33c8e75ac74fb20acc4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396550"
---
# <a name="kernel-checks-for-non-whql-signed-drivers"></a><span data-ttu-id="53fb4-103">Verifica del kernel per i driver non WHQL firmati</span><span class="sxs-lookup"><span data-stu-id="53fb4-103">Kernel checks for non-WHQL signed drivers</span></span>

<span data-ttu-id="53fb4-104">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="53fb4-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="53fb4-105">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="53fb4-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="53fb4-106">Per i dispositivi che puliscono l'installazione di Windows 10 e l'avvio protetto (si noti che questo è lo standard per tutti i nuovi dispositivi rispetto alla versione di Windows 8,0), tutti i nuovi driver devono essere firmati da WHQL/sysdev anziché usare semplicemente certificati con firma incrociata.</span><span class="sxs-lookup"><span data-stu-id="53fb4-106">For devices that clean install Windows 10, and where Secure Boot is on (note that this is standard for all new devices since the release of Windows 8.0), all new drivers must be signed by WHQL/Sysdev rather than just use cross-signed certificates.</span></span> <span data-ttu-id="53fb4-107">I dispositivi aggiornati e i casi in cui i driver sono stati firmati con un certificato incrociato prima che questo criterio venisse applicato vengono esclusi da questi criteri per garantire la compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="53fb4-107">Devices that are upgraded and cases where drivers have been signed with a cross-cert before this policy went into effect are excluded from this policy to ensure backwards compatibility.</span></span> <span data-ttu-id="53fb4-108">Questo criterio è stato annunciato il 2015 aprile, ma verrà applicato con l'edizione dell'anniversario di Windows, rilasciato il 2016 agosto.</span><span class="sxs-lookup"><span data-stu-id="53fb4-108">This policy was announced April 2015, however it will be enforced with the Windows Anniversary Edition, released August 2016.</span></span>

<span data-ttu-id="53fb4-109">Nei casi in cui un driver non è firmato correttamente, si manifesterà come una notifica PCA che i driver vengono bloccati quando non vengono superati i requisiti di firma.</span><span class="sxs-lookup"><span data-stu-id="53fb4-109">In cases where a driver is not signed correctly, it will manifest as a PCA notification that the driver(s) is blocked when it doesn’t pass signature requirements.</span></span> <span data-ttu-id="53fb4-110">In questo modo si impedisce che un'esperienza utente disconnessa in un secondo momento del driver venga bloccata nel kernel in modo trasparente.</span><span class="sxs-lookup"><span data-stu-id="53fb4-110">This prevents a later disconnected user experience of the driver being blocked in kernel transparently.</span></span>

<span data-ttu-id="53fb4-111">Per altre informazioni, fare riferimento a [questo post di Blog](https://techcommunity.microsoft.com/t5/Windows-Hardware-Certification/bg-p/WindowsHardwareCertification/), che annuncia la modifica della firma del driver.</span><span class="sxs-lookup"><span data-stu-id="53fb4-111">For more information, please refer to [this blog post](https://techcommunity.microsoft.com/t5/Windows-Hardware-Certification/bg-p/WindowsHardwareCertification/), which announces the driver signing change.</span></span>

 

 




