---
description: I riconoscitori del testo dividono un campione di input penna in segmenti e traslano i segmenti di input penna in testo.
ms.assetid: 9fbdde0e-5312-48ec-9273-ded6703b99a9
title: Riconoscitori di testo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8372af61d45bb1cc8bcd8377202149073c3decc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759512"
---
# <a name="text-recognizers"></a>Riconoscitori di testo

I riconoscitori del testo dividono un campione di input penna in segmenti e traslano i segmenti di input penna in testo. Questa operazione è utile per il riconoscimento della grafia. È utile anche negli scenari di scrittura complessi, ad esempio riconoscendo i singoli glifi kanji e offrendo agli utenti il completamento automatico di un carattere durante la scrittura.

Un riconoscimento di testo restituisce una stringa Unicode per ogni segmento di riconoscimento dell'input penna. Accompagnando la stringa è il livello di confidenza assegnato dal riconoscimento al risultato e un mapping del risultato all'input penna originale. Questo mapping Mostra il segmento nell'input penna originale che corrisponde alla stringa di codice Unicode. La stringa che rappresenta l'output del riconoscimento del testo è sempre rappresentata nell'ordine lineare, anziché nell'ordine spaziale o nell'ordine cronologico in cui sono stati inseriti i segmenti.

La tabella seguente elenca le lingue supportate dai riconoscitori della grafia Microsoft e le versioni di Windows in cui questi linguaggi sono stati introdotti per la prima volta. Si noti che alcuni riconoscitori di linguaggio potrebbero non essere disponibili in determinate versioni di Windows e dovranno essere scaricati separatamente. I riconoscitori di terze parti possono anche essere disponibili per altre lingue, ma non sono necessariamente approvati da Microsoft.



| Linguaggio                                   | Windows XP Tablet PC Edition | Windows XP Tablet PC Edition 2005 | Windows Vista | Windows 7 |
|--------------------------------------------|------------------------------|-----------------------------------|---------------|-----------|
| Cinese (semplificato e tradizionale)       | X                            |                                   |               |           |
| Inglese (Stati Uniti, Regno Unito, Canada e Australia)    | X                            |                                   |               |           |
| Francese                                     | X                            |                                   |               |           |
| Tedesco                                     | X                            |                                   |               |           |
| Giapponese                                   | X                            |                                   |               |           |
| Coreano                                     | X                            |                                   |               |           |
| Spagnolo                                    | X                            |                                   |               |           |
| Italiano                                    |                              | X                                 |               |           |
| Olandese (Paesi Bassi e Belgio)            |                              |                                   | X             |           |
| Portoghese (Brasile e portoghese/neutro) |                              |                                   | X             |           |
| Catalano                                    |                              |                                   |               | X         |
| Croato                                   |                              |                                   |               | X         |
| Ceco                                      |                              |                                   |               | X         |
| Danese                                     |                              |                                   |               | X         |
| Finlandese                                    |                              |                                   |               | X         |
| Tedesco (Svizzera)                       |                              |                                   |               | X         |
| Norvegese (Bokmal e Nynorsk)             |                              |                                   |               | X         |
| Polacco                                     |                              |                                   |               | X         |
| Portoghese (Portogallo)                      |                              |                                   |               | X         |
| Romeno                                   |                              |                                   |               | X         |
| Russo                                    |                              |                                   |               | X         |
| Serbo (alfabeto cirillico e alfabeto latino)               |                              |                                   |               | X         |
| Spagnolo (Argentina e Messico)             |                              |                                   |               | X         |
| Svedese                                    |                              |                                   |               | X         |



 

 

 



