---
description: Protezione DEP/NX
ms.assetid: 92F628E4-6106-42F7-B868-A3101C7A3F0A
title: Protezione DEP/NX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3565460cbfd2e6b13c3c5ba6b1f0693a3d5b25ba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088569"
---
# <a name="depnx-protection"></a><span data-ttu-id="855d4-103">Protezione DEP/NX</span><span class="sxs-lookup"><span data-stu-id="855d4-103">DEP/NX Protection</span></span>

<span data-ttu-id="855d4-104">A partire da Windows Internet Explorer 7 in Windows Vista,  l'elemento del Pannello di controllo Internet include l'opzione Abilita protezione della memoria per ridurre gli attacchi online.</span><span class="sxs-lookup"><span data-stu-id="855d4-104">Starting with Windows Internet Explorer 7 on Windows Vista, the Internet control panel item includes an **Enable memory protection** option to help mitigate online attacks.</span></span> <span data-ttu-id="855d4-105">Questa opzione è detta anche Protezione *esecuzione* programmi (DEP) o *No-Execute* (NX).</span><span class="sxs-lookup"><span data-stu-id="855d4-105">This option is also referred to as *Data Execution Prevention* (DEP) or *No-Execute* (NX).</span></span> <span data-ttu-id="855d4-106">Quando questa opzione è abilitata, funziona con il processore per impedire attacchi di overflow del buffer bloccando l'esecuzione di codice dalla memoria contrassegnata come non eseguibile.</span><span class="sxs-lookup"><span data-stu-id="855d4-106">When this option is enabled, it works with the processor to help prevent buffer overflow attacks by blocking code execution from memory that is marked as non-executable.</span></span>

<span data-ttu-id="855d4-107">In Windows Internet Explorer 8 nel sistema operativo Windows Vista con Service Pack 1 (SP1) o versione successiva, questa opzione è abilitata per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="855d4-107">In Windows Internet Explorer 8 on the Windows Vista with Service Pack 1 (SP1) operating system or a later version, this option is enabled by default.</span></span> <span data-ttu-id="855d4-108">DEP/NX non protegge da tutte le vulnerabilità basate sulla memoria.</span><span class="sxs-lookup"><span data-stu-id="855d4-108">DEP/NX does not protect against all memory-based vulnerabilities.</span></span> <span data-ttu-id="855d4-109">Tuttavia, quando viene combinato con altre tecnologie come ASLR (Address Space Layout Randomization), consente di evitare vulnerabilità comuni di overflow del buffer in Windows Internet Explorer e i componenti aggiuntivi caricati.</span><span class="sxs-lookup"><span data-stu-id="855d4-109">But when it is combined with other technologies like Address Space Layout Randomization (ASLR), it helps prevent common buffer overflow vulnerabilities in Windows Internet Explorer and the add-ons that it loads.</span></span> <span data-ttu-id="855d4-110">Non è necessaria alcuna interazione dell'utente aggiuntiva per fornire questa protezione e non vengono introdotte nuove richieste.</span><span class="sxs-lookup"><span data-stu-id="855d4-110">No additional user interaction is required to provide this protection, and no new prompts are introduced.</span></span>

## <a name="related-topics"></a><span data-ttu-id="855d4-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="855d4-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="855d4-112">Correzione dei problemi di compatibilità nelle applicazioni Web tramite Visualizzazione Compatibilità</span><span class="sxs-lookup"><span data-stu-id="855d4-112">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



