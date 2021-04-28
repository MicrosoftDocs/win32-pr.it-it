---
description: Controllo delle versioni (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)
ms.assetid: d1014801-a93a-40e8-ae96-31784c192753
title: Controllo delle versioni (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9c3bc1f63dc236c706fd8d9bd6a6053371dd363
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103699"
---
# <a name="versioning-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a><span data-ttu-id="57e2a-103">Controllo delle versioni (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)</span><span class="sxs-lookup"><span data-stu-id="57e2a-103">Versioning (Windows 7 and Windows Server 2008 R2 Application Quality Cookbook)</span></span>

<span data-ttu-id="57e2a-104">Uno dei problemi di compatibilità delle applicazioni più comuni per Windows Internet Explorer sono le stringhe dell'agente utente (UA) e i vettori di versione.</span><span class="sxs-lookup"><span data-stu-id="57e2a-104">One of the most common application compatibility issues for Windows Internet Explorer is User Agent (UA) Strings and Version Vectors.</span></span> <span data-ttu-id="57e2a-105">Windows Internet Explorer 8 introduce una nuova stringa UA per consentire alle applicazioni di rilevare la versione in esecuzione dagli utenti.</span><span class="sxs-lookup"><span data-stu-id="57e2a-105">Windows Internet Explorer 8 introduces a new UA String to help applications detect which version that users are running.</span></span> <span data-ttu-id="57e2a-106">Oltre ad aumentare semplicemente il valore MSIE associato a Internet Explorer nella stringa UA, Internet Explorer 8 aggiunge un valore Trident/4.0 per consentire di rilevare se Internet Explorer 8 è in esecuzione in modalità Visualizzazione Compatibilità.</span><span class="sxs-lookup"><span data-stu-id="57e2a-106">In addition to simply increasing the MSIE value that is associated with Internet Explorer in the UA String, Internet Explorer 8 adds a Trident/4.0 value to help you detect if Internet Explorer 8 is running in Compatibility View mode.</span></span> <span data-ttu-id="57e2a-107">Queste modifiche, oltre ai controlli delle versioni hardcoded, possono introdurre problemi di compatibilità tra i browser.</span><span class="sxs-lookup"><span data-stu-id="57e2a-107">These changes, plus hardcoded version checks, can potentially introduce compatibility issues between browsers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="57e2a-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="57e2a-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57e2a-109">Progettare aggiornamenti che influiscono sulla compatibilità tra browser</span><span class="sxs-lookup"><span data-stu-id="57e2a-109">Design Updates that Impact Compatibility between Browsers</span></span>](design-updates-that-impact-compatibility-between-browsers.md)
</dt> </dl>

 

 



