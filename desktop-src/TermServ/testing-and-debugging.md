---
title: Test e debug
description: È presente un \ 0034; Echo \ 0034; listener implementato dal client Connessione Desktop remoto (RDC), che è sempre presente e in ascolto delle connessioni in ingresso.
ms.assetid: ae14af04-7d19-406b-998e-a0579cfe73eb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9028ccf0eea97a8651392baba094ac6dcda242f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297882"
---
# <a name="testing-and-debugging"></a>Test e debug

È presente un listener "echo" implementato dal client Connessione Desktop remoto (RDC), che è sempre presente e in ascolto delle connessioni in ingresso. Quando si scrive il lato server di un modulo canale virtuale dinamico (DVC), come test rapido è possibile aprire un endpoint denominato "ECHO". Qualsiasi operazione di scrittura su un canale di cui viene creata un'istanza da questo endpoint comporterà la ricezione degli stessi dati.

È possibile utilizzare questa tecnica per testare un'implementazione di input/output (I/O) del modulo lato server, per misurare il tempo di risposta per un plug-in del client Connessione Desktop remoto (RDC) o per misurare il ritardo di rete per il client di Connessione Desktop remoto (RDC). Non esiste alcuna limitazione sulla quantità di dati che è possibile inviare su questo canale.

 

 




