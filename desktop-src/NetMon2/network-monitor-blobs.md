---
description: Il Network Monitor BLOB (Binary Large Object) è una struttura di dati generica che contiene informazioni sulla configurazione e sul percorso delle schede di interfaccia di rete (NIC).
ms.assetid: 910bf929-aa89-434d-83c3-07c80c627405
title: Network Monitor BLOB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d15ce2a8f85860720c6f38b0d6c019a33e57df0a1b589ba23455db0319d0436
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799551"
---
# <a name="network-monitor-blobs"></a>Network Monitor BLOB

Il Network Monitor BLOB (Binary Large Object) è una struttura di dati generica che contiene informazioni sulla configurazione e sul percorso delle schede di interfaccia di rete (NIC). Usare i BLOB per rappresentare le schede di interfaccia di rete e filtrare le voci in un elenco di schede di interfaccia di rete. I BLOB possono anche contenere dati specifici dell'applicazione senza influire sugli altri dati che contengono. L'implementazione di BLOB è opaca a tutti i livelli che devono accedere ai BLOB con le API BLOB.

## <a name="blob-structure"></a>Struttura BLOB

Un BLOB può essere considerato come un albero gerarchico usato per designare le stringhe. Questo albero ha tre livelli: Proprietario, Categoria e Tag. Owner è una stringa che indica, in generale, chi legge una voce. La categoria è anche una stringa che definisce un raggruppamento funzionale generale di tag sotto il proprietario. Tag è il nome effettivo della voce.

Le caratteristiche strutturali dei BLOB includono:

-   Gli helper BLOB all'interno di un processo sono protetti l'uno dall'altro da un mutex incorporato in ogni BLOB.
-   Ogni BLOB ha un numero di versione interno in modo che gli helper possano gestire i moduli BLOB presenti e futuri. Possono verificarsi conflitti di versione se si invia un BLOB a un altro computer tramite una chiamata di procedura remota.
-   Il BLOB stesso è un puntatore a un void. Tenere presente che le applicazioni devono allocare BLOB con il **modificatore const** per evitare di modificare il contenuto.
-   Ogni designatore, nonché i relativi valori, sono stringhe. Tenere presente che le stringhe restituite **dalle funzioni GetString** sono effettivamente puntatori al BLOB e non devono essere modificate. Per questo motivo, queste stringhe devono essere specificate come **const char** _ pX* per evitare che vengano \_ accidentalmente cambiate dalle applicazioni.

In generale, tutti i parametri con l'designatore **const** invitano il chiamante a evitare di modificare i valori anziché impedire alle funzioni helper di modificarli. In realtà, le funzioni helper modificheranno in genere tali valori.

 

 



