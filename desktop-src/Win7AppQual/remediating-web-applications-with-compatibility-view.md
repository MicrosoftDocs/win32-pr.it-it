---
description: Correzione dei problemi di compatibilità nelle applicazioni Web tramite Visualizzazione Compatibilità
ms.assetid: ACAC2375-EA6C-4AA1-90B7-0BF237A51C02
title: Correzione dei problemi di compatibilità nelle applicazioni Web tramite Visualizzazione Compatibilità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7dd876dcf8d25ebe7e6cca15ea88bfeba52aa29e3e5d83680815c15f8bda46d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118329510"
---
# <a name="fixing-compatibility-issues-in-web-applications-by-using-compatibility-view"></a>Correzione dei problemi di compatibilità nelle applicazioni Web tramite Visualizzazione Compatibilità

Questa sezione descrive i passaggi di mitigazione di base e come pianificare la compatibilità futura delle applicazioni mentre si stanno attualmente affrontando eventuali problemi.

Windows Internet Explorer supporta i modelli di Internet Explorer legacy ogni volta che è possibile, in modo che i siti che si sviluppano in essi continuino a comportarsi come previsto nelle versioni più recenti di Internet Explorer. A partire Windows Internet Explorer 8, è possibile scegliere di supportare i comportamenti legacy selezionando la modalità di rendering pagina per pagina.

Internet Explorer 8 include le modalità di rendering seguenti che è possibile impostare usando l'intestazione compatibile con X-UA.



| Valore di content | Descrizione                                                                           |
|---------------|---------------------------------------------------------------------------------------|
| IE=5          | Usare la modalità non standard.                                                                      |
| IE=7          | Usare sempre la Windows Internet Explorer 7.                                          |
| IE=EmulateIE7 | Visualizzare in Internet Explorer 7 a meno che il sito non abbia i caratteri non standard DOCTYPE.           |
| IE=8          | Usare sempre Internet Explorer modalità 8.                                                  |
| IE=EmulateIE8 | Eseguire l Visualizzazione Compatibilità nei computer client e usare Internet Explorer modalità 8.      |
| IE=Edge       | Visualizzare nella modalità più recente. In Internet Explorer 8, questo valore equivale a IE=8. |



 

Gli argomenti seguenti descrivono come aggiornare le applicazioni Web usando Visualizzazione Compatibilità.



| Argomento                                                                                                  | Descrizione                                                                    |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Informazioni Visualizzazione Compatibilità](what-is-compatibility-view-.md)                                          | Viene descritto Visualizzazione Compatibilità.                                                  |
| [Perché è necessario Visualizzazione Compatibilità?](why-do-you-need-compatibility-view-.md)                         | Descrive i motivi per cui è consigliabile Visualizzazione Compatibilità.                               |
| [Usare il tag Meta per garantire la compatibilità futura](use-the-meta-tag-to-ensure-future-compatibility.md) | Viene descritto come usare l'elemento **meta** per garantire la compatibilità futura. |



 

 

 



