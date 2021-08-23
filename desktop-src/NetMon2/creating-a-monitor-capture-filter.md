---
description: La creazione di un filtro di acquisizione che Network Monitor è un processo in cinque passaggi.
ms.assetid: 04be791c-43c5-44c2-8ab0-799a99974bf6
title: Creazione di un filtro di acquisizione monitoraggio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72e9e58aebd18f861ad8fc36c4d6f718ff3e3694c828b23436764e288d083fbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064154"
---
# <a name="creating-a-monitor-capture-filter"></a>Creazione di un filtro di acquisizione monitoraggio

La creazione di un filtro di acquisizione che Network Monitor è un processo in cinque passaggi:

-   [Impostazione del filtro Etype o SAP](writing-etypesap-filter-portion.md)
-   [Scrittura del filtro ADDRESSTABLE](writing-addresstable-filter-portion.md)
-   [Scrittura del filtro PATTERNMATCH](writing-the-patternmatch-filter.md)
-   [Ritaglio di un frame](clipping-a-frame.md)
-   [Implementazione del codice del filtro di acquisizione](implementing-the-capture-filter-code.md)

Un [*filtro di*](c.md) acquisizione è una serie di aggiunte al BLOB NPP che seleziona i frame che vengono passati di nuovo al monitoraggio. Se un monitoraggio non modifica il BLOB NPP, il servizio NPP passa in modalità promiscua e invia tutto il traffico di rete al monitoraggio. L'NPP è più efficiente se è in grado di ridurre i dati consegnati a un driver, quindi un monitoraggio deve creare un filtro di acquisizione. Un monitoraggio imposta il filtro di acquisizione scrivendo nel BLOB NPP nella chiamata alla [funzione DoConfigure.](imonitor-doconfigure.md) MCSVC chiama quindi NPP con il BLOB NPP. Per [altri dettagli sul](capture-filters.md) filtro di acquisizione, sui provider di pacchetti di rete nei server di rete e sui BLOB Network Monitor [BLOB,](network-monitor-blobs.md) vedere Filtri di acquisizione. [](network-packet-providers.md)

 

 



