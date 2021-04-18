---
description: Attualmente, tutti i tempi delle chiamate vengono lasciati alle applicazioni.
ms.assetid: 9eb98b48-4bee-4f6d-b818-2f81b36591da
title: Timer stato chiamata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5d273d7f8439ebfee9d6668565745ed2c209f70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308088"
---
# <a name="call-state-timer"></a>Timer stato chiamata

Attualmente, tutti i tempi delle chiamate vengono lasciati alle applicazioni. Questa operazione può essere gravosa se l'applicazione sta monitorando un numero elevato di chiamate e, se sono presenti più applicazioni, possibilmente su più server, può essere necessario per tutti i timer per mantenere le stesse chiamate. Per questo motivo, è opportuno che la durata dello stato di chiamata venga gestita dal server.

Il membro **tStateEntryTime** in [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) consente la temporizzazione delle chiamate negli Stati da segnalare. Il membro (di tipo **sysTime**) indica l'ora in cui è stato immesso lo stato corrente.

 

 



