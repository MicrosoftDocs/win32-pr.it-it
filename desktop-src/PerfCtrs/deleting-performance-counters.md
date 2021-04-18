---
description: Per rimuovere i contatori delle prestazioni delle applicazioni dal sistema, seguire questa procedura.
ms.assetid: 40fc9831-1025-4052-a941-70767ee4e10f
title: Eliminazione dei contatori delle prestazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba257a1a44b5272543b7e61dcdc4b4e96225c160
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312176"
---
# <a name="deleting-performance-counters"></a><span data-ttu-id="5108f-103">Eliminazione dei contatori delle prestazioni</span><span class="sxs-lookup"><span data-stu-id="5108f-103">Deleting Performance Counters</span></span>

<span data-ttu-id="5108f-104">Per rimuovere i contatori delle prestazioni dell'applicazione dal sistema, seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="5108f-104">To remove your application's performance counters from the system, perform the following steps.</span></span>

1.  <span data-ttu-id="5108f-105">Utilizzare lo strumento **unlodctr** incluso con il computer per rimuovere i dati correlati al contatore dal registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="5108f-105">Use the **unlodctr** tool included with the computer to remove the counter related data from the registry.</span></span> <span data-ttu-id="5108f-106">Si noti che la chiave **delle prestazioni** dell'applicazione deve esistere perché lo strumento **unlodctr** abbia esito positivo.</span><span class="sxs-lookup"><span data-stu-id="5108f-106">Note that the application's **Performance** key must exist for the **unlodctr** tool to succeed.</span></span> <span data-ttu-id="5108f-107">Per informazioni dettagliate, vedere [rimozione di nomi e descrizioni di contatori dal registro di sistema](removing-counter-names-and-descriptions-from-the-registry.md).</span><span class="sxs-lookup"><span data-stu-id="5108f-107">For details, see [Removing Counter Names and Descriptions from the Registry](removing-counter-names-and-descriptions-from-the-registry.md).</span></span>
2.  <span data-ttu-id="5108f-108">Eliminare le chiavi di **prestazioni** e **collegamento** nella chiave **dei servizi** dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5108f-108">Delete the **Performance** and **Linkage** keys under the application's **Services** key.</span></span> <span data-ttu-id="5108f-109">Per eliminare queste chiavi, utilizzare l'utilità Regedt32.exe o chiamare [**RegDeleteKey**](/windows/desktop/api/winreg/nf-winreg-regdeletekeya).</span><span class="sxs-lookup"><span data-stu-id="5108f-109">To delete these keys, use either the Regedt32.exe utility or call [**RegDeleteKey**](/windows/desktop/api/winreg/nf-winreg-regdeletekeya).</span></span>

 

 
