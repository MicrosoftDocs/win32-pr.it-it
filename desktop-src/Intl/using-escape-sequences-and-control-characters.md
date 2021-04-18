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
# <a name="using-escape-sequences-and-control-characters"></a>Utilizzo di sequenze di escape e caratteri di controllo

Quando un'applicazione converte le stringhe da ASCII o da una [tabella codici di Windows (ANSI)](code-pages.md) a Unicode, deve tradurre le sequenze di escape carattere per carattere in Unicode. Quando un file di testo ASCII o un altro file di testo a 8 bit viene convertito in Unicode, esiste la possibilità che venga successivamente convertito nuovamente. La conversione di sequenze di escape in Unicode in modo carattere per carattere, anziché combinarle come singolo carattere Unicode, consente di eseguire la conversione inversa senza dover riconoscere e analizzare le sequenze di escape come tali. Ad esempio, ESC + A dovrebbe diventare 0x001B (ESC), 0x0041 (A), anziché 0x411B.

I primi valori di codice a 32 16 bit in Unicode sono destinati ai caratteri di controllo 32. Questa specifica supporta l'utilizzo esistente dei caratteri di controllo a scopo di formattazione. Le applicazioni Unicode possono trattare questi caratteri di controllo esattamente allo stesso modo in cui trattano gli equivalenti ASCII.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo di caratteri speciali in Unicode](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



