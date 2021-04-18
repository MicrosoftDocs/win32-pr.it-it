---
description: Quando un'applicazione converte le stringhe da ASCII o da una tabella codici di Windows (ANSI) a Unicode, deve tradurre le sequenze di escape carattere per carattere in Unicode.
ms.assetid: 4be0fd47-0903-44d3-a323-0adc6e9c0cc9
title: Utilizzo di sequenze di escape e caratteri di controllo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4211a487a31d5a79454d7be15159f48cdc3d5beb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319483"
---
# <a name="using-escape-sequences-and-control-characters"></a><span data-ttu-id="a82d8-103">Utilizzo di sequenze di escape e caratteri di controllo</span><span class="sxs-lookup"><span data-stu-id="a82d8-103">Using Escape Sequences and Control Characters</span></span>

<span data-ttu-id="a82d8-104">Quando un'applicazione converte le stringhe da ASCII o da una [tabella codici di Windows (ANSI)](code-pages.md) a Unicode, deve tradurre le sequenze di escape carattere per carattere in Unicode.</span><span class="sxs-lookup"><span data-stu-id="a82d8-104">When an application converts strings from ASCII or from a [Windows (ANSI) code page](code-pages.md) to Unicode, it should translate escape sequences character-by-character into Unicode.</span></span> <span data-ttu-id="a82d8-105">Quando un file di testo ASCII o un altro file di testo a 8 bit viene convertito in Unicode, esiste la possibilità che venga successivamente convertito nuovamente.</span><span class="sxs-lookup"><span data-stu-id="a82d8-105">When an ASCII or other 8-bit text file is converted to Unicode, there is a chance that it will subsequently be converted back.</span></span> <span data-ttu-id="a82d8-106">La conversione di sequenze di escape in Unicode in modo carattere per carattere, anziché combinarle come singolo carattere Unicode, consente di eseguire la conversione inversa senza dover riconoscere e analizzare le sequenze di escape come tali.</span><span class="sxs-lookup"><span data-stu-id="a82d8-106">Converting escape sequences into Unicode on a character-by-character basis, instead of combining them as a single Unicode character, makes it possible to perform the reverse conversion without needing to recognize and parse the escape sequences as such.</span></span> <span data-ttu-id="a82d8-107">Ad esempio, ESC + A dovrebbe diventare 0x001B (ESC), 0x0041 (A), anziché 0x411B.</span><span class="sxs-lookup"><span data-stu-id="a82d8-107">For example, ESC+A should become 0x001B (ESC), 0x0041 (A), instead of 0x411B.</span></span>

<span data-ttu-id="a82d8-108">I primi valori di codice a 32 16 bit in Unicode sono destinati ai caratteri di controllo 32.</span><span class="sxs-lookup"><span data-stu-id="a82d8-108">The first 32 16-bit code values in Unicode are intended for the 32 control characters.</span></span> <span data-ttu-id="a82d8-109">Questa specifica supporta l'utilizzo esistente dei caratteri di controllo a scopo di formattazione.</span><span class="sxs-lookup"><span data-stu-id="a82d8-109">This specification supports the existing use of control characters for formatting purposes.</span></span> <span data-ttu-id="a82d8-110">Le applicazioni Unicode possono trattare questi caratteri di controllo esattamente allo stesso modo in cui trattano gli equivalenti ASCII.</span><span class="sxs-lookup"><span data-stu-id="a82d8-110">Unicode applications can treat these control characters in exactly the same way as they treat their ASCII equivalents.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a82d8-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a82d8-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a82d8-112">Utilizzo di caratteri speciali in Unicode</span><span class="sxs-lookup"><span data-stu-id="a82d8-112">Using Special Characters in Unicode</span></span>](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



