---
description: 'Ulteriori informazioni su: Panoramica database'
title: Panoramica sul database
TOCTitle: Database Overview
ms:assetid: 6e4ebfab-8bd2-4fcf-9d91-2148a693596c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269290(v=EXCHG.10)
ms:contentKeyID: 32765582
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 473ffc7f11b3688f0f0904ae15a366ef7d6812d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104560065"
---
# <a name="database-overview"></a>Panoramica sul database


_**Si applica a:** Windows | Windows Server_

## <a name="database-overview"></a>Panoramica sul database

Il database ESE è un Indexed Sequential Access Method (ISAM) per l'archiviazione e il recupero dei dati. Un database ESE viene archiviato in un unico file ed è costituito da una o più tabelle definite dall'utente. I dati sono organizzati nei record della tabella con una o più colonne definite dall'utente. Gli indici creati forniscono un'organizzazione diversa per l'intero set o un subset di record nella tabella. Utilizzando l'API ESE, le applicazioni possono creare cursori che consentono di spostarsi tra i record del database in ordini sequenziali diversi. Gli elementi della tabella sono definiti di seguito:

  - **Column**: la colonna è un campo della tabella in cui è archiviato un tipo di informazioni specifico. Le colonne possono essere fisse o a lunghezza variabile, a seconda del tipo di dati archiviato. Alcune colonne, ad esempio le colonne con tag, non accettano spazio se **null** o sono impostate sul valore predefinito e possono contenere più valori.

  - **Record**: un record è una raccolta di valori di colonne che hanno un'identità univoca definita dalla chiave primaria.

  - **Index**: l'indice è una raccolta di colonne chiave che definiscono un ordine archiviato di record nella tabella. L'indice cluster, o primario, definisce l'ordine in cui i record vengono archiviati all'interno della tabella. È possibile definire più indici per specificare ordini diversi di attraversamento tramite record nella tabella. Un indice può anche limitare il set di record visibili in base a criteri semplici, ad esempio la presenza o l'assenza di un particolare valore della colonna chiave nel record.

  - **Cursor**: il cursore indica il record corrente nella tabella e passa ai record della tabella usando l'indice corrente. Il cursore contiene anche informazioni sullo stato dell'aggiornamento attualmente preparato.

Le colonne e gli indici possono essere aggiunti o rimossi dalla tabella in qualsiasi momento. Sebbene sia possibile definire più indici, i dati nella tabella vengono archiviati fisicamente e raggruppati logicamente in base alla definizione dell'indice primario in un albero B +. Ogni indice secondario viene archiviato in un albero B + separato che contiene solo puntatori logici ai dati effettivi archiviati nella tabella primaria. Se non viene definito alcun indice, i record della tabella vengono archiviati in un albero B + nell'ordine di inserimento e vengono definiti indice sequenziale.

Il diagramma seguente è un esempio di come vengono archiviati i dati della tabella in un albero B + in base all'indice primario. L'indice primario è per nome e ID e viene creato un indice secondario per il numero di ufficio del dipendente. Le voci per l'indice secondario vengono archiviate in un albero B + separato che contiene solo i puntatori ai record archiviati nella tabella primaria. Il numero di ufficio 12348 nella tabella secondaria, ad esempio, è correlato al record 3 nella tabella primaria. Il record 3 contiene i valori di colonna per il dipendente in Office 12348. Per ulteriori informazioni, vedere l'argomento [indicizzazione nell'argomento tabella](./indexing-in-the-table.md) .

![ESE_Documentation_tableandrow2](images/Gg269290.ESE_Documentation_tableandrow2(EXCHG.10).gif "ESE_Documentation_tableandrow2")
