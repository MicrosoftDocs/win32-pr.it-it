---
description: .
ms.assetid: d1014801-a93a-40e8-ae96-31784c192753
title: Controllo delle versioni (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2da50dae53fd2309f1a5de10996c57a2b4ac29c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319821"
---
# <a name="versioning-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a><span data-ttu-id="72c76-103">Controllo delle versioni (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)</span><span class="sxs-lookup"><span data-stu-id="72c76-103">Versioning (Windows 7 and Windows Server 2008 R2 Application Quality Cookbook)</span></span>

<span data-ttu-id="72c76-104">Uno dei problemi più comuni di compatibilità delle applicazioni per Windows Internet Explorer è costituito dalle stringhe degli agenti utente (UA) e dai vettori di versione.</span><span class="sxs-lookup"><span data-stu-id="72c76-104">One of the most common application compatibility issues for Windows Internet Explorer is User Agent (UA) Strings and Version Vectors.</span></span> <span data-ttu-id="72c76-105">Windows Internet Explorer 8 introduce una nuova stringa UA che consente alle applicazioni di rilevare la versione in esecuzione dagli utenti.</span><span class="sxs-lookup"><span data-stu-id="72c76-105">Windows Internet Explorer 8 introduces a new UA String to help applications detect which version that users are running.</span></span> <span data-ttu-id="72c76-106">Oltre ad aumentare semplicemente il valore di MSIE associato a Internet Explorer nella stringa UA, Internet Explorer 8 aggiunge un valore Trident/4.0 che consente di rilevare se Internet Explorer 8 è in esecuzione nella modalità di visualizzazione compatibilità.</span><span class="sxs-lookup"><span data-stu-id="72c76-106">In addition to simply increasing the MSIE value that is associated with Internet Explorer in the UA String, Internet Explorer 8 adds a Trident/4.0 value to help you detect if Internet Explorer 8 is running in Compatibility View mode.</span></span> <span data-ttu-id="72c76-107">Queste modifiche, oltre ai controlli di versione hardcoded, possono causare problemi di compatibilità tra i browser.</span><span class="sxs-lookup"><span data-stu-id="72c76-107">These changes, plus hardcoded version checks, can potentially introduce compatibility issues between browsers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="72c76-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="72c76-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72c76-109">Aggiornamenti della progettazione che incidono sulla compatibilità tra browser</span><span class="sxs-lookup"><span data-stu-id="72c76-109">Design Updates that Impact Compatibility between Browsers</span></span>](design-updates-that-impact-compatibility-between-browsers.md)
</dt> </dl>

 

 



