---
description: Un server di distribuzione automatica delle chiamate (ACD) è una combinazione di hardware e software che consente di classificare, accodare e distribuire le chiamate in ingresso agli agenti o alle chiamate in uscita alle righe.
ms.assetid: 29fb0bd7-0ca9-4490-82d2-39550f00a97b
title: Proxy ACD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c345fbcac3ac3471098e964336a0c3135fd1f582
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967991"
---
# <a name="acd-proxy"></a>Proxy ACD

Un server di distribuzione automatica delle chiamate (ACD) è una combinazione di hardware e software che consente di classificare, accodare e distribuire le chiamate in ingresso agli agenti o alle chiamate in uscita alle righe.

L'applicazione server ACD è un'applicazione proxy TAPI, che per la massima efficienza deve essere eseguita nello stesso server del provider di servizi di telefonia (TSP). Con un switch ACD tradizionale, l'applicazione proxy si interfaccia con il ACD interno del Commuter ed espone l'operazione. Un'applicazione proxy ACD basata su software o "virtuale" sarà completamente responsabile del rilevamento di chiamate, code, gruppi e agenti e utilizzerebbe le interfacce TAPI standard per controllare l'hardware di cambio. Le applicazioni client di Agent vengono in genere eseguite sulle workstation del singolo agente e utilizzano il provider di servizi remoti TAPI per comunicare con TAPISRV nel computer server e, di conseguenza, l'applicazione proxy.

La classificazione delle chiamate in ingresso è progettata per ottenere una chiamata a un agente che sarà in grado di gestirlo in modo efficace. La classificazione può essere basata sul numero con connessione, un sistema IVR (Interactive Voice Recognition) o altri criteri. TAPI usa il concetto di [Gruppo ACD](about-call-center-controls.md) per rappresentare questa operazione.

Le code sono un modo normale e previsto per i Call Center per gestire i periodi di carico intensivo. Una coda è in genere associata a un gruppo ACD, ma può essere creata per gestire le righe in uscita o le chiamate in ingresso in attesa di un'applicazione IVR. Per ulteriori informazioni, vedere [Code](about-call-center-controls.md) .

La distribuzione delle chiamate a agenti o gruppi di agenti può essere uniforme, ma in genere si basa su dati quali le informazioni sulle chiamate, la disponibilità degli agenti e la capacità. Il [gestore dell'agente](about-call-center-controls.md) di TAPI fornisce l'accesso a informazioni quali disponibilità e indirizzi degli agenti per il trasferimento di chiamate agli agenti.

Oltre alla distribuzione delle chiamate di base, un sistema ACD fornisce funzionalità per la gestione e la creazione di report sulle prestazioni del sistema. Le statistiche raccolte per le code di chiamate, i gruppi e gli agenti vengono utilizzate per perfezionare e migliorare le prestazioni del sistema e vengono in genere utilizzate come base per la retribuzione degli agenti.

 

 



