---
description: .
ms.assetid: 92F628E4-6106-42F7-B868-A3101C7A3F0A
title: Protezione DEP/NX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c4a4cedead32504b6b78ba34bb72ee6b2ef400
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885398"
---
# <a name="depnx-protection"></a><span data-ttu-id="d9752-103">Protezione DEP/NX</span><span class="sxs-lookup"><span data-stu-id="d9752-103">DEP/NX Protection</span></span>

<span data-ttu-id="d9752-104">A partire da Windows Internet Explorer 7 in Windows Vista, l'elemento del pannello di controllo Internet include un'opzione **Abilita protezione della memoria** che consente di attenuare gli attacchi online.</span><span class="sxs-lookup"><span data-stu-id="d9752-104">Starting with Windows Internet Explorer 7 on Windows Vista, the Internet control panel item includes an **Enable memory protection** option to help mitigate online attacks.</span></span> <span data-ttu-id="d9752-105">Questa opzione è definita anche protezione *esecuzione* programmi (DEP) o *No-Execute* (NX).</span><span class="sxs-lookup"><span data-stu-id="d9752-105">This option is also referred to as *Data Execution Prevention* (DEP) or *No-Execute* (NX).</span></span> <span data-ttu-id="d9752-106">Quando questa opzione è abilitata, funziona con il processore per prevenire gli attacchi di overflow del buffer bloccando l'esecuzione del codice dalla memoria contrassegnata come non eseguibile.</span><span class="sxs-lookup"><span data-stu-id="d9752-106">When this option is enabled, it works with the processor to help prevent buffer overflow attacks by blocking code execution from memory that is marked as non-executable.</span></span>

<span data-ttu-id="d9752-107">In Windows Internet Explorer 8 sul sistema operativo Windows Vista con Service Pack 1 (SP1) o versione successiva questa opzione è abilitata per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="d9752-107">In Windows Internet Explorer 8 on the Windows Vista with Service Pack 1 (SP1) operating system or a later version, this option is enabled by default.</span></span> <span data-ttu-id="d9752-108">DEP/NX non protegge da tutte le vulnerabilità basate sulla memoria.</span><span class="sxs-lookup"><span data-stu-id="d9752-108">DEP/NX does not protect against all memory-based vulnerabilities.</span></span> <span data-ttu-id="d9752-109">Tuttavia, quando è combinato con altre tecnologie come la sequenza di ASLR (Address Space Layout), consente di evitare vulnerabilità comuni di overflow del buffer in Windows Internet Explorer e i componenti aggiuntivi caricati.</span><span class="sxs-lookup"><span data-stu-id="d9752-109">But when it is combined with other technologies like Address Space Layout Randomization (ASLR), it helps prevent common buffer overflow vulnerabilities in Windows Internet Explorer and the add-ons that it loads.</span></span> <span data-ttu-id="d9752-110">Non è necessaria alcuna interazione con l'utente aggiuntiva per fornire questa protezione e non vengono introdotti nuovi messaggi di richiesta.</span><span class="sxs-lookup"><span data-stu-id="d9752-110">No additional user interaction is required to provide this protection, and no new prompts are introduced.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d9752-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d9752-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9752-112">Correzione dei problemi di compatibilità nelle applicazioni Web utilizzando visualizzazione compatibilità</span><span class="sxs-lookup"><span data-stu-id="d9752-112">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



