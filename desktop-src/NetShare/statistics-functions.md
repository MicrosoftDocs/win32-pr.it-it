---
description: Il Windows sistema operativo accumula un set di statistiche operative per workstation e server dal momento in cui viene avviata la workstation o il servizio server.
ms.assetid: 4e0217bf-7550-40a2-b47c-8e898a586005
title: Funzioni statistiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2261f0c4f8f8249b401e658759827d6471d3ac47b6eb10df769ad5f37d8ce7af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063591"
---
# <a name="statistics-functions"></a>Funzioni statistiche

Il Windows sistema operativo accumula un set di statistiche operative per workstation e server dal momento in cui viene avviata la workstation o il servizio server. Per recuperare queste statistiche, è possibile chiamare la funzione di statistiche di gestione della rete seguente.



| Funzione                                     | Descrizione                                                                                 |
|----------------------------------------------|---------------------------------------------------------------------------------------------|
| [**NetStatisticsGet**](/windows/desktop/api/Lmstats/nf-lmstats-netstatisticsget) | Recupera le statistiche operative per un servizio. supporta i servizi workstation e server. |



 

La **funzione NetStatisticsGet** restituisce una struttura [**WORKSTATION \_ \_ 0 STAT**](/windows/win32/api/lmstats/ns-lmstats-stat_workstation_0-r1) quando vengono richieste statistiche della workstation. La funzione restituisce una struttura [**STAT SERVER \_ \_ 0**](/windows/desktop/api/Lmstats/ns-lmstats-stat_server_0) quando vengono richieste le statistiche del server.

 

 



