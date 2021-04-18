---
description: Il sistema operativo Windows accumula un set di statistiche operative per le workstation e i server dal momento in cui viene avviata la workstation o il servizio Server.
ms.assetid: 4e0217bf-7550-40a2-b47c-8e898a586005
title: Funzioni statistiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce62e12f3c4894ba86ff5e5aaaa38801d272195c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315884"
---
# <a name="statistics-functions"></a>Funzioni statistiche

Il sistema operativo Windows accumula un set di statistiche operative per le workstation e i server dal momento in cui viene avviata la workstation o il servizio Server. Per recuperare queste statistiche, è possibile chiamare la seguente funzione di statistiche di gestione di rete.



| Funzione                                     | Descrizione                                                                                 |
|----------------------------------------------|---------------------------------------------------------------------------------------------|
| [**NetStatisticsGet**](/windows/desktop/api/Lmstats/nf-lmstats-netstatisticsget) | Recupera le statistiche operative per un servizio. supporta i servizi workstation e server. |



 

La funzione **NetStatisticsGet** restituisce una struttura [**Stat \_ workstation \_ 0**](/windows/win32/api/lmstats/ns-lmstats-stat_workstation_0-r1) quando vengono richieste statistiche Workstation; la funzione restituisce una struttura [**Stat \_ server \_ 0**](/windows/desktop/api/Lmstats/ns-lmstats-stat_server_0) quando vengono richieste le statistiche del server.

 

 



