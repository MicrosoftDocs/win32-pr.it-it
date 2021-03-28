---
description: In genere, le applicazioni meno recenti non necessitano di modifiche per lavorare su più sistemi di monitoraggio.
ms.assetid: 908cf88c-69ed-4855-817d-ba749e14ff85
title: Considerazioni su più monitor per i programmi precedenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feebb356cb2f9c5480c84f1718b51d6e866ef621
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978522"
---
# <a name="multiple-monitor-considerations-for-older-programs"></a>Considerazioni su più monitor per i programmi precedenti

In genere, le applicazioni meno recenti non necessitano di modifiche per lavorare su più sistemi di monitoraggio. Per la maggior parte, il sistema apparirà solo una visualizzazione. Le metriche di sistema riflettono lo schermo principale e le applicazioni a schermo intero vengono visualizzate nel database primario. Il sistema gestisce la riduzione a icona, la massimizzazione, i menu e le finestre di dialogo.

Tuttavia, in alcuni programmi si verificano problemi. Alcune che potrebbero avere problemi sono le applicazioni di controllo remoto, quelle che dispongono di accesso diretto all'hardware e quelle con patch per GDI o driver di visualizzazione. In questi casi, è possibile che l'utente debba disabilitare qualsiasi monitoraggio oltre il monitor primario.

 

 



