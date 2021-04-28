---
description: Risoluzione dei problemi di compatibilità nelle applicazioni Web tramite Visualizzazione Compatibilità
ms.assetid: ACAC2375-EA6C-4AA1-90B7-0BF237A51C02
title: Correzione dei problemi di compatibilità nelle applicazioni Web tramite Visualizzazione Compatibilità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5acb7249854d9ac89b5601fdf83efa397c11c17
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116359"
---
# <a name="fixing-compatibility-issues-in-web-applications-by-using-compatibility-view"></a>Risoluzione dei problemi di compatibilità nelle applicazioni Web tramite Visualizzazione Compatibilità

Questa sezione descrive i passaggi di mitigazione di base e come pianificare la compatibilità futura delle applicazioni mentre si stanno affrontando i problemi.

Windows Internet Explorer supporta i modelli Internet Explorer legacy ogni volta che è possibile, in modo che i siti che si sviluppano continuino a comportarsi come previsto nelle versioni più recenti di Internet Explorer. A partire da Windows Internet Explorer 8, è possibile scegliere di supportare i comportamenti legacy selezionando la modalità di rendering pagina per pagina.

Internet Explorer 8 include le modalità di rendering seguenti che è possibile impostare usando l'intestazione compatibile con X-UA.



| Valore di content | Descrizione                                                                           |
|---------------|---------------------------------------------------------------------------------------|
| IE=5          | Usare la modalità non interattiva.                                                                      |
| IE=7          | Usare sempre la modalità windows Internet Explorer 7.                                          |
| IE=EmulateIE7 | Visualizzare in Internet Explorer 7, a meno che il sito non abbia i caratteri DOCTYPE.           |
| IE=8          | Usare sempre Internet Explorer modalità 8.                                                  |
| IE=EmulateIE8 | Eseguire Visualizzazione Compatibilità nei computer client e usare Internet Explorer modalità 8.      |
| IE=Edge       | Visualizzare nella modalità più recente. In Internet Explorer 8, questo valore equivale a IE=8. |



 

Negli argomenti seguenti viene descritto come aggiornare le applicazioni Web usando Visualizzazione Compatibilità.



| Argomento                                                                                                  | Descrizione                                                                    |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Informazioni Visualizzazione Compatibilità](what-is-compatibility-view-.md)                                          | Descrive Visualizzazione Compatibilità.                                                  |
| [Perché è necessario Visualizzazione Compatibilità?](why-do-you-need-compatibility-view-.md)                         | Descrive il motivo per cui è consigliabile usare Visualizzazione Compatibilità.                               |
| [Usare il meta tag per garantire la compatibilità futura](use-the-meta-tag-to-ensure-future-compatibility.md) | Viene descritto come usare l'elemento **meta** per garantire la compatibilità futura. |



 

 

 



