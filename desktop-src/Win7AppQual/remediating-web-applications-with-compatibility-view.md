---
description: .
ms.assetid: ACAC2375-EA6C-4AA1-90B7-0BF237A51C02
title: Correzione dei problemi di compatibilità nelle applicazioni Web utilizzando visualizzazione compatibilità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a43f4ff54a919058127a5f72ba60f3683c6583e1
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320641"
---
# <a name="fixing-compatibility-issues-in-web-applications-by-using-compatibility-view"></a>Correzione dei problemi di compatibilità nelle applicazioni Web utilizzando visualizzazione compatibilità

In questa sezione vengono descritti i passaggi di mitigazione di base e viene illustrato come pianificare la compatibilità delle applicazioni in futuro mentre si sta risolvendo immediatamente eventuali problemi.

Windows Internet Explorer supporta i modelli di Internet Explorer legacy ogni volta che è possibile, in modo che i siti sviluppati continuino a comportarsi come previsto nelle versioni più recenti di Internet Explorer. A partire da Windows Internet Explorer 8, è possibile scegliere di supportare i comportamenti legacy selezionando la modalità di rendering in base alla pagina.

Internet Explorer 8 include le modalità di rendering seguenti che è possibile impostare utilizzando l'intestazione X-UA-Compatible.



| Valore di content | Descrizione                                                                           |
|---------------|---------------------------------------------------------------------------------------|
| IE=5          | Utilizzare la modalità non standard.                                                                      |
| IE = 7          | Utilizzare sempre la modalità Windows Internet Explorer 7.                                          |
| IE=EmulateIE7 | Viene visualizzato in modalità Internet Explorer 7, a meno che il sito non disponga di un DOCTYPE non standard.           |
| IE = 8          | Utilizzare sempre la modalità Internet Explorer 8.                                                  |
| IE=EmulateIE8 | Eseguire l'override della visualizzazione compatibilità nei computer client e utilizzare la modalità Internet Explorer 8.      |
| IE=Edge       | Viene visualizzato nella modalità più recente. In Internet Explorer 8, questo valore è equivalente a IE = 8. |



 

Negli argomenti seguenti viene descritto come aggiornare le applicazioni Web utilizzando visualizzazione compatibilità.



| Argomento                                                                                                  | Descrizione                                                                    |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Informazioni sulla visualizzazione compatibilità](what-is-compatibility-view-.md)                                          | Viene descritta la visualizzazione compatibilità.                                                  |
| [Perché è necessaria la visualizzazione compatibilità?](why-do-you-need-compatibility-view-.md)                         | Viene descritto il motivo per cui è consigliabile utilizzare la visualizzazione compatibilità.                               |
| [Usare il tag meta per garantire la compatibilità futura](use-the-meta-tag-to-ensure-future-compatibility.md) | Viene descritto come utilizzare l'elemento **meta** per garantire la compatibilità futura. |



 

 

 



