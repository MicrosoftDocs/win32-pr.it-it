---
description: Un monitoraggio è una libreria a collegamento dinamico (DLL) che esamina le acquisizioni in tempo reale del traffico di rete.
ms.assetid: 96d04352-5f1c-4964-94d2-692c6b642cb8
title: Monitoraggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29adc2e3abaa165903b78ac10683f76ce07719b7513cd25b8b4a7ca4377bb6c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118364634"
---
# <a name="monitors"></a>Monitoraggi

Un monitoraggio è una libreria a collegamento dinamico (DLL) che esamina le acquisizioni in tempo reale del traffico di rete. Cerca le condizioni predefinite e quindi genera eventi quando vengono rilevate tali condizioni. Ad esempio, un evento può essere generato quando viene tentata un'interruzione di rete, quando una workstation non autorizzata sta consegnando indirizzi IP o quando un router ha esito negativo.

> [!Note]  
> Se è necessario eseguire analisi dettagliate sui dati di rete che richiedono un'analisi post-acquisizione, è necessario usare applicazioni [*esperte*](e.md) [*e parser.*](p.md)

 

Il [*servizio di controllo del monitoraggio*](m.md) (MCSVC) fornisce il framework per la gestione dei monitoraggi. Fornisce funzioni per caricare le DLL di monitoraggio e un'interfaccia di comunicazione per lo strumento di controllo monitoraggio in modo che sia possibile creare, configurare, avviare, arrestare e disabilitare più istanze dei monitoraggi.

I monitoraggi vengono eseguiti in due thread di esecuzione. MCSVC fornisce il primo thread, che fornisce il controllo diretto del monitoraggio. Il secondo thread viene fornito dal [*provider*](n.md) di pacchetti di rete (NPP), che consente di passare al monitoraggio i dati di rete acquisiti, le statistiche e lo stato dell'acquisizione da NPP.

Possono esistere più istanze dello stesso monitoraggio per ogni interfaccia NPP di run-time usata per acquisire i dati.

 

 



