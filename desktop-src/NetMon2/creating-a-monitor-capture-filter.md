---
description: La creazione di un filtro di acquisizione che funziona con Network Monitor è un processo in cinque passaggi.
ms.assetid: 04be791c-43c5-44c2-8ab0-799a99974bf6
title: Creazione di un filtro di acquisizione monitoraggio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 097a8276bd6a1f311b343787b3f06175d9b7091f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311627"
---
# <a name="creating-a-monitor-capture-filter"></a>Creazione di un filtro di acquisizione monitoraggio

La creazione di un filtro di acquisizione che funziona con Network Monitor è un processo in cinque passaggi:

-   [Impostazione del filtro ETYPE o SAP](writing-etypesap-filter-portion.md)
-   [Scrittura del filtro ADDRESSTABLE](writing-addresstable-filter-portion.md)
-   [Scrittura del filtro PATTERNMATCH](writing-the-patternmatch-filter.md)
-   [Ritaglio di un frame](clipping-a-frame.md)
-   [Implementazione del codice del filtro di acquisizione](implementing-the-capture-filter-code.md)

Un [*filtro di acquisizione*](c.md) è una serie di aggiunte al BLOB di NPP che seleziona i frame che vengono passati di nuovo al monitoraggio. Se un monitoraggio non modifica il BLOB di NPP, la NPP entra in modalità promiscua e invia tutto il traffico di rete al monitoraggio. L'oggetto NPP è più efficiente se può ridurre i dati passati a un driver, quindi un monitoraggio deve creare un filtro di acquisizione. Un monitoraggio imposta il relativo filtro di acquisizione scrivendo nel BLOB NPP nella chiamata alla funzione [DoConfigure](imonitor-doconfigure.md) . Il MCSVC chiama quindi l'oggetto NPP con il BLOB NPP. Per altri dettagli sul filtro di acquisizione, sui provider di [pacchetti di rete](network-packet-providers.md) in centrali e sui [BLOB di Network Monitor](network-monitor-blobs.md) nelle funzioni BLOB, vedere i [filtri di acquisizione](capture-filters.md) .

 

 



