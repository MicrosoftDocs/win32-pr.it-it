---
description: I riconoscitori di testo suddividono un campione di input penna in segmenti e traducono i segmenti di input penna in testo.
ms.assetid: 9fbdde0e-5312-48ec-9273-ded6703b99a9
title: Riconoscitori di testo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f2a579681fbd06c6b5dd27e5388f2c797e6be50433e11490fb5fe204d1c65d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119842821"
---
# <a name="text-recognizers"></a>Riconoscitori di testo

I riconoscitori di testo suddividono un campione di input penna in segmenti e traducono i segmenti di input penna in testo. Ciò è utile per il riconoscimento della grafia. È utile anche in scenari di scrittura complessi, ad esempio il riconoscimento di singoli glifi Kanji e l'offerta agli utenti di completare automaticamente un carattere durante la scrittura.

Un riconoscitore di testo restituisce una stringa Unicode per ogni segmento di riconoscimento input penna. La stringa è accompagnata dal livello di attendibilità assegnato dal riconoscimento al risultato e da un mapping del risultato all'input penna originale. Questo mapping mostra quale segmento nell'input penna originale corrisponde alla stringa di codice Unicode. La stringa che rappresenta l'output del riconoscimento del testo è sempre rappresentata nell'ordine lineare, anziché nell'ordine spaziale o cronologico in cui sono stati immessi i segmenti.

Nella tabella seguente sono elencate le lingue supportate dai sistemi di riconoscimento della grafia Microsoft e le versioni Windows in cui queste lingue sono state introdotte per la prima volta. Si noti che alcuni riconoscitori della lingua potrebbero non essere disponibili in una determinata versione Windows e dovranno essere scaricati separatamente. I riconoscitori di terze parti potrebbero essere disponibili anche per altre lingue, ma non sono necessariamente approvati da Microsoft.



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
| Portoghese (Brasile e Portoghese/Neutro) |                              |                                   | X             |           |
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
| Serbo (alfabeto cirillico e latino)               |                              |                                   |               | X         |
| Spagnolo (Argentina e Messico)             |                              |                                   |               | X         |
| Svedese                                    |                              |                                   |               | X         |



 

 

 



