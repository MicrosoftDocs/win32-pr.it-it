---
description: Un monitoraggio è una libreria a collegamento dinamico (DLL) che esamina le acquisizioni in tempo reale del traffico di rete.
ms.assetid: 96d04352-5f1c-4964-94d2-692c6b642cb8
title: Monitoraggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76ed9ad355ab02b5e130b896efd6654df81e492e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966768"
---
# <a name="monitors"></a>Monitoraggi

Un monitoraggio è una libreria a collegamento dinamico (DLL) che esamina le acquisizioni in tempo reale del traffico di rete. Cerca le condizioni predefinite e quindi genera eventi quando vengono rilevate tali condizioni. Ad esempio, un evento può essere generato quando si tenta di eseguire un'operazione di failover di rete, quando una workstation non autorizzata distribuisce indirizzi IP o quando un router non riesce.

> [!Note]  
> Se è necessario eseguire analisi dettagliate sui dati di rete che richiedono un'analisi di post-acquisizione, è necessario usare applicazioni di [*esperti*](e.md) e [*parser*](p.md) .

 

Il [*servizio di controllo di monitoraggio*](m.md) (MCSVC) fornisce il Framework per la gestione dei monitoraggi. Fornisce funzioni per caricare le DLL di monitoraggio e un'interfaccia di comunicazione per lo strumento di controllo del monitoraggio, in modo da poter creare, configurare, avviare, arrestare e disabilitare più istanze dei monitoraggi.

I monitoraggi vengono eseguiti in due thread di esecuzione. MCSVC fornisce il primo thread, che fornisce il controllo diretto del monitoraggio. Il secondo thread viene fornito dal [*provider di pacchetti di rete*](n.md) (NPP), che fornisce un modo per passare i dati di rete acquisiti, le statistiche e lo stato dell'acquisizione dall'oggetto NPP al monitoraggio.

Per ogni interfaccia NPP di runtime utilizzata per l'acquisizione dei dati può esistere più di un'istanza dello stesso monitoraggio.

 

 



