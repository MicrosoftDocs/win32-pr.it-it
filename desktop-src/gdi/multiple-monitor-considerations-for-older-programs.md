---
description: In genere, le applicazioni meno recenti non necessitano di modifiche per funzionare in più sistemi di monitoraggio.
ms.assetid: 908cf88c-69ed-4855-817d-ba749e14ff85
title: Considerazioni su più monitor per i programmi meno recenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4444d3de54886c4743c17f7348482f154e21a11d027cd05014ac5eb26cb6a249
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117698767"
---
# <a name="multiple-monitor-considerations-for-older-programs"></a>Considerazioni su più monitor per i programmi meno recenti

In genere, le applicazioni meno recenti non necessitano di modifiche per funzionare in più sistemi di monitoraggio. Per la maggior parte, il sistema sembra avere un solo display. Le metriche di sistema riflettono la visualizzazione principale e le applicazioni a schermo intero visualizzate nella schermata primaria. Il sistema gestisce la minimizzazione, l'ottimizzazione, i menu e le finestre di dialogo.

Tuttavia, alcuni programmi avranno problemi. Alcuni problemi possono essere applicazioni di controllo remoto, quelle con accesso diretto all'hardware e quelle che hanno patch per il driver GDI o DISPLAY. In questi casi, l'utente potrebbe essere necessario disabilitare qualsiasi monitoraggio oltre il monitoraggio primario.

 

 



