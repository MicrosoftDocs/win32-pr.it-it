---
description: Il Network Monitor BLOB (Binary Large Object) è una struttura di dati generica che contiene informazioni sulla configurazione e sulla posizione delle schede di interfaccia di rete (NIC).
ms.assetid: 910bf929-aa89-434d-83c3-07c80c627405
title: BLOB Network Monitor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dce6dd6ca8643eabe8ab49387c0ef39eb49b6f2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319929"
---
# <a name="network-monitor-blobs"></a>BLOB Network Monitor

Il Network Monitor BLOB (Binary Large Object) è una struttura di dati generica che contiene informazioni sulla configurazione e sulla posizione delle schede di interfaccia di rete (NIC). Usare i BLOB per rappresentare le schede di rete e filtrare le voci in un elenco di schede di rete. I BLOB possono inoltre contenere dati specifici dell'applicazione senza influire sugli altri dati che contengono. L'implementazione di BLOB è opaca a tutti i livelli che devono accedere ai BLOB con le API BLOB.

## <a name="blob-structure"></a>Struttura BLOB

Un BLOB può essere considerato come un albero gerarchico utilizzato per designare le stringhe. Questo albero è costituito da tre livelli: proprietario, categoria e tag. Owner è una stringa che indica, in generale, che legge una voce. La categoria è anche una stringa che designa un raggruppamento funzionale generale di tag sotto il proprietario. Il tag è il nome effettivo della voce.

Le caratteristiche strutturali dei BLOB includono:

-   Gli helper BLOB all'interno di un processo sono protetti l'uno dall'altro da un mutex incorporato in ogni BLOB.
-   Ogni BLOB ha un numero di versione interno, in modo che gli helper possano gestire i form BLOB sia presenti che futuri. È possibile che si verifichino conflitti di versione se si invia un BLOB a un altro computer tramite una chiamata di procedura remota.
-   Il BLOB è un puntatore a un void. Tenere presente che le applicazioni devono allocare BLOB con il modificatore **const** per evitare di modificare il contenuto.
-   Ogni designatore e i rispettivi valori sono stringhe. Tenere presente che le stringhe restituite dalle funzioni **GetString** sono in realtà puntatori al BLOB e non devono essere modificate. Per questo motivo, è necessario specificare queste stringhe come **const char** _ \_ px * per evitare che le applicazioni le modifichino accidentalmente.

In generale, tutti i parametri con l'indicatore **const** incoraggiano il chiamante ad evitare la modifica dei valori anziché impedire alle funzioni di supporto di modificarle. Infatti, le funzioni di supporto in genere modificano tali valori.

 

 



