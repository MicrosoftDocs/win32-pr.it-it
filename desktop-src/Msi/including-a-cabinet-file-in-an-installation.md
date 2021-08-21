---
description: Questa sezione descrive l'inclusione di file CAB nelle installazioni. Per altre informazioni, vedere Uso di archivi e origini compresse.
ms.assetid: 17ea7f76-90b2-48fb-8187-64dc6d294443
title: Inclusione di un file CAB in un'installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c0970d87b8b219e1558c6b3f1daf78a6a01100a7bc41f9ae1dad51a25048b46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787341"
---
# <a name="including-a-cabinet-file-in-an-installation"></a>Inclusione di un file CAB in un'installazione

Questa sezione descrive l'inclusione di file CAB nelle installazioni. Per altre informazioni, vedere [Using Cabinets and Compressed Sources](using-cabinets-and-compressed-sources.md).

**Per includere un file cab in un pacchetto di installazione**

1.  Usare uno strumento di creazione di file cab per comprimere i file di origine in un file CAB. Vedere [File CAB](cabinet-files.md).
2.  Il file cab deve trovarsi in un flusso di dati all'interno del file .msi o in un file cab separato che si trova nella radice dell'albero di origine specificato dalla [tabella directory](directory-table.md).
3.  Determinare se l'origine deve essere un tipo compresso o misto con file sia non compressi che compressi. Vedere [Origini compresse e non compresse](compressed-and-uncompressed-sources.md). A seconda del tipo di immagine di origine, impostare i bit di flag compressi o non compressi della [**proprietà Riepilogo conteggio**](word-count-summary.md) parole.
4.  Aggiungere un record alla [tabella File](file-table.md) per ogni file nel file cab. Immettere una chiave file nella colonna File che corrisponda esattamente alla chiave del file nel file cab. Per le chiavi di file viene fatto distinzione tra maiuscole e minuscole. Anche la sequenza di installazione dei file nella tabella File e nell'archivio deve essere la stessa. La sequenza di file viene specificata dal numero di sequenza nella colonna Sequenza. Per arrivare al numero di sequenza per il primo file nell'archivio, seguire questa procedura. Trovare il record esistente nella [tabella Media con](media-table.md) il valore più grande nella colonna DiskID. Il campo LastSequence di questo record fornisce l'ultimo numero di sequenza del file usato sul supporto. Nella tabella File assegnare al primo file del nuovo file cab un numero di sequenza maggiore di questo. Assegnare i numeri di sequenza a tutti i file rimanenti nello stesso ordine del file cab. Per una descrizione dei campi record rimanenti, vedere [Tabella file](file-table.md).
5.  Aggiungere un record alla tabella [Media per](media-table.md) l'archivio. Specificare un valore nel campo DiskID del nuovo record maggiore del valore DiskID più grande già esistente nella tabella. Inserire il nome dell'archivio nel campo Cabinet. Questo nome deve essere sotto forma di [tipo di dati Cabinet.](cabinet.md) Antefiorare il nome con un simbolo di numero " " se l'archivio dati è un flusso di dati archiviato nel \# file .msi file. Si noti che se il file cab è un flusso di dati, il nome dell'archivio fa distinzione tra maiuscole e minuscole. Se l'archivio è un file separato, il nome del file non fa distinzione tra maiuscole e minuscole.
6.  Determinare il numero di sequenza di file più grande nel nuovo file cab controllando la colonna Sequenza della tabella File aggiornata. Immettere un valore maggiore di questo nel campo LastSequence del nuovo record della tabella Media. Per una descrizione dei campi record rimanenti, vedere [Media table](media-table.md).
7.  È possibile archiviare il file cab nel pacchetto di installazione usando uno strumento come Msidb.exe o funzioni di database del programma [di installazione.](database-functions.md) I quattro passaggi seguenti illustrano come aggiungere il file cab da un programma usando le funzioni di database.
8.  Per aggiungere il file cab al pacchetto di installazione da un programma, aprire una vista [ \_ Flussi tabella](-streams-table.md) del database usando [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa).
9.  Usare [**MsiRecordSetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstringa) per impostare la colonna Name della tabella Flussi sul nome visualizzato \_ nella colonna Cabinet della tabella [Media](media-table.md). Omettere il simbolo di numero: \# .
10. Usare [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) per impostare la colonna Data Flussi tabella sui dati \_ dell'archivio.
11. Usare [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) per aggiornare il record nella \_ Flussi tabella.
12. Per usare Msidb.exe per aggiungere il file cab Mycab.cab al pacchetto di installazione denominato Mydatabase.msi, usare la riga di comando seguente: Msidb.exe -d mydatabase.msi -a mycab.cab. In questo caso, la colonna Cabinet della tabella Media deve contenere la stringa \#mycab.cab.

 

 



