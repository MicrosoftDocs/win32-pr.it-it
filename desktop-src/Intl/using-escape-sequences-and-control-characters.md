---
description: Quando un'applicazione converte stringhe da ASCII o da una tabella codici Windows (ANSI) in Unicode, deve convertire le sequenze di escape carattere per carattere in Unicode.
ms.assetid: 4be0fd47-0903-44d3-a323-0adc6e9c0cc9
title: Uso di sequenze di escape e caratteri di controllo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ea89997a8f94a9fdd573b2c8360dbdd5342d38ca8bd2e7a133aa29943c07e9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118389920"
---
# <a name="using-escape-sequences-and-control-characters"></a>Uso di sequenze di escape e caratteri di controllo

Quando un'applicazione converte stringhe da ASCII o da una tabella codici [Windows (ANSI)](code-pages.md) in Unicode, deve convertire le sequenze di escape carattere per carattere in Unicode. Quando un file di testo ASCII o un altro file di testo a 8 bit viene convertito in Unicode, è probabile che verrà successivamente convertito nuovamente. La conversione di sequenze di escape in Unicode carattere per carattere, anziché combinarle come singolo carattere Unicode, consente di eseguire la conversione inversa senza dover riconoscere e analizzare le sequenze di escape come tali. Ad esempio, ESC+A deve diventare 0x001B (ESC), 0x0041 (A), anziché 0x411B.

I primi 32 valori di codice a 16 bit in Unicode sono destinati ai 32 caratteri di controllo. Questa specifica supporta l'uso esistente di caratteri di controllo a scopo di formattazione. Le applicazioni Unicode possono trattare questi caratteri di controllo esattamente nello stesso modo in cui trattano gli equivalenti ASCII.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di caratteri speciali in Unicode](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



