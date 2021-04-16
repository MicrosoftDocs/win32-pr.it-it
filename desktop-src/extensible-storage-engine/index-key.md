---
description: 'Altre informazioni su: chiave di indice'
title: Chiave di indice
TOCTitle: Index Key
ms:assetid: 104bdb1c-71ac-44f4-bbda-c553131aaad4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269188(v=EXCHG.10)
ms:contentKeyID: 32765491
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: eff0812f363fa83d133ab087140d415d8e2dbad3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104562049"
---
# <a name="index-key"></a>Chiave di indice


_**Si applica a:** Windows | Windows Server_

## <a name="index-key"></a>Chiave di indice

Viene creato un indice sui dati della tabella con [JetCreateIndex](./jetcreateindex-function.md) oppure è possibile creare più indici contemporaneamente con [JetCreateIndex2](./jetcreateindex2-function.md) usando la struttura [JET_INDEXCREATE](./jet-indexcreate-structure.md) . L'indice è definito in termini di una matrice di colonne, in ordine di precedenza. Questa matrice di colonne viene chiamata anche chiave di indice. La chiave di indice può essere definita come indice primario quando l'opzione JET_bitIndexPrimary è impostata nel parametro *grbit* di [JetCreateIndex](./jetcreateindex-function.md) o [JET_INDEXCREATE](./jet-indexcreate-structure.md). La chiave di indice è una stringa con terminazione null di token con terminazione null, come illustrato nell'esempio seguente:

\+Col1 \\ 0-Col2 \\ 0 + Col3 \\ 0 \\ 0

La chiave nell'esempio può essere utilizzata per creare un indice in tre colonne della tabella. Ogni colonna specificata nell'indice viene definita "segmento di indice" o "colonna chiave". È possibile che il segmento di indice sia crescente o decrescente in termini di contributo dell'ordine. Nell'esempio precedente, il nome della prima colonna nell'indice è col1. Il + indica che col1 è indicizzato in ordine crescente. Il – prima di col2 indica che è indicizzato in ordine decrescente.

Quando nell'indice sono presenti colonne condizionali, la struttura [JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md) viene utilizzata per indicare il modo in cui vengono indicizzate. Una colonna condizionale può essere utilizzata per controllare la presenza o l'assenza di una voce di indice in un indice in base al valore nella colonna condizionale corrispondente senza influire sull'ordinamento dell'indice. Una colonna condizionale può includere o escludere una voce di indice dall'indice se il valore della colonna condizionale è NULL per il record corrispondente.

Per impostazione predefinita, la dimensione massima della chiave di indice viene fornita dalla costante JET_cbKeyMost che ha sempre avuto 255 byte di dati normalizzati (byte di dati, incluso l'overhead di indicizzazione). A partire da Windows Vista, è possibile impostare la dimensione massima della chiave di indice con la struttura [JET_INDEXCREATE](./jet-indexcreate-structure.md) . La dimensione massima della chiave di indice corrisponde alla dimensione della pagina del database. Per abilitare una dimensione massima personalizzata della chiave, specificare l'opzione Jet_bitIndexKeyMost nel membro grbits di [JET_INDEXCREATE](./jet-indexcreate-structure.md)e impostare il membro **cbKeyMost** su uno dei valori seguenti:

  - JET_cbKeyMost2KBytePage: se le dimensioni della pagina del database sono pari a 2048 byte, le dimensioni massime della chiave di indice possono essere comprese tra 255 byte e il valore massimo 500 byte.

  - JET_cbKeyMost4KBytePage: se le dimensioni della pagina del database sono pari a 4096 byte, le dimensioni massime della chiave di indice possono essere comprese tra 255 byte e il valore massimo 1000 byte.

  - JET_cbKeyMost8KBytePage: se le dimensioni della pagina del database sono pari a 8196 byte, le dimensioni massime della chiave di indice possono essere comprese tra 255 byte e il valore massimo 2000 byte.

Nell'esempio riportato di seguito viene illustrata una tabella contenente informazioni sui dipendenti. La tabella contiene 6 colonne, ognuna delle quali definisce un attributo dipendente specifico. Un record della tabella contiene valori per un dipendente, ad esempio il nome del dipendente nella colonna 1 e l'ID dipendente nella colonna 2. Un indice primario creato per questa tabella consente di organizzare i dati in base al nome del dipendente per primo e all'ID dipendente. Il nome e l'ID sono indicizzati in ordine crescente. Ad esempio, un record contenente il nome Johnson e il dipendente ID 12345 verrà elencato prima di un record con il nome di un dipendente Jones e l'ID 10000. Tutti i record per Jones vengono archiviati insieme nella tabella, con gli ID dei dipendenti in ordine crescente, come illustrato nella tabella.

![ESE_Documentation_IndexTable](images/Gg269188.ESE_Documentation_IndexTable(EXCHG.10).gif "ESE_Documentation_IndexTable")

La chiave nell'indice primario deve essere univoca, ma le chiavi nell'indice secondario possono essere duplicate. Se, ad esempio, viene creato un indice in base al cognome e sono presenti due persone con Stevens nel database, ESE restituisce un errore di Jet_errKeyDuplicate da [JetUpdate](./jetupdate-function.md) o [JetUpdate2](./jetupdate2-function.md), quando l'applicazione tenta di inserire il secondo "Stevens". Quando la chiave effettiva è maggiore della dimensione massima della chiave, la chiave viene troncata. La ricerca e l'univocità degli effetti di troncamento chiave e devono essere gestiti dall'applicazione. Se, ad esempio, "Stevens" e "Stevenson" sono stati archiviati in un indice in base al cognome e le dimensioni massime della chiave erano troppo piccole per archiviare la parte "on" di "Stevenson", il troncamento della chiave provocherebbe il fatto che il motore di database dichiara che "Stevens" e "Stevenson" sono duplicati anche se non lo sono. L'applicazione deve essere preparata a gestire i casi di questo tipo durante la ricerca e l'aggiornamento se la definizione dell'indice e i valori di colonna indicizzati sono tali che il troncamento delle chiavi è una possibilità. A partire da Windows Vista, le applicazioni possono specificare l'opzione Jet_bitIndexDisallowTruncation in [JET_INDEXCREATE](./jet-indexcreate-structure.md) o [JetMakeKey](./jetmakekey-function.md). Se si specifica questo flag, eventuali aggiornamenti all'indice che comporteranno la mancata riuscita di una chiave troncata con JET_errKeyTruncated. In caso contrario, le chiavi verranno troncate automaticamente. Ciò consentirà all'applicazione di funzionare senza problemi per gli artefatti causati da un troncamento della chiave descritto in precedenza.
