---
description: In questa sezione vengono descritti i file CAB inclusi nelle installazioni di. Per altre informazioni, vedere uso di cabinet e origini compresse.
ms.assetid: 17ea7f76-90b2-48fb-8187-64dc6d294443
title: Inclusione di un file CAB in un'installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 098e660de3f7ec7097ab02613d75219ac0a0d624
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310974"
---
# <a name="including-a-cabinet-file-in-an-installation"></a>Inclusione di un file CAB in un'installazione

In questa sezione vengono descritti i file CAB inclusi nelle installazioni di. Per altre informazioni, vedere [uso di cabinet e origini compresse](using-cabinets-and-compressed-sources.md).

**Per includere un file CAB in un pacchetto di installazione**

1.  Usare uno strumento di creazione del cabinet per comprimere i file di origine in un file CAB. Vedere [file CAB](cabinet-files.md).
2.  Il file CAB deve trovarsi in un flusso di dati all'interno del file con estensione msi o in un file CAB separato che si trova nella radice dell'albero di origine specificato dalla [tabella di directory](directory-table.md).
3.  Determinare se l'origine deve essere un tipo compresso o un tipo misto con file sia non compressi che compressi. Vedere [origini compresse e non compresse](compressed-and-uncompressed-sources.md). A seconda del tipo di immagine di origine, impostare i bit di flag compressi o non compressi della proprietà [**riepilogo Conteggio parole**](word-count-summary.md) .
4.  Aggiungere un record alla [tabella file](file-table.md) per ogni file nel file CAB. Immettere una chiave file nella colonna file che corrisponde esattamente alla chiave del file nel file CAB. Le chiavi del file fanno distinzione tra maiuscole e minuscole. Anche la sequenza di installazione dei file nella tabella file e nel file CAB deve essere la stessa. La sequenza di file è specificata dal numero di sequenza nella colonna sequenza. Per arrivare al numero di sequenza del primo file nell'archivio, effettuare le operazioni seguenti. Trovare il record esistente nella [tabella dei supporti](media-table.md) con il valore massimo nella colonna DiskID. Il campo LastSequence di questo record restituisce l'ultimo numero di sequenza del file utilizzato nei supporti. Nella tabella file assegnare il primo file del nuovo file CAB a un numero di sequenza maggiore di questo. Assegnare i numeri di sequenza a tutti i file rimanenti nello stesso ordine in cui si trovi nel file CAB. Per una descrizione dei campi record rimanenti, vedere [tabella file](file-table.md).
5.  Aggiungere un record alla [tabella dei supporti](media-table.md) per il file CAB. Specificare un valore nel campo DiskID del nuovo record che è maggiore del valore DiskID più grande già esistente nella tabella. Inserire il nome del file CAB nel campo CAB. Il nome deve essere nel formato di un tipo di dati [CAB](cabinet.md) . Anteporre il prefisso al nome con il simbolo di cancelletto " \# " se l'archivio è un flusso di dati archiviato nel file con estensione msi. Si noti che se l'archivio è un flusso di dati, il nome del cabinet fa distinzione tra maiuscole e minuscole. Se il file CAB è un file separato, il nome del file non fa distinzione tra maiuscole e minuscole.
6.  Determinare il numero di sequenza di file più grande nel nuovo file CAB controllando la colonna sequenza della tabella file aggiornata. Immettere un valore maggiore di questo nel campo LastSequence del nuovo record della tabella dei supporti. Per una descrizione dei campi record rimanenti, vedere la [tabella media](media-table.md).
7.  È possibile archiviare il file CAB nel pacchetto di installazione usando uno strumento come Msidb.exe o usando le [funzioni di database](database-functions.md)del programma di installazione. I quattro passaggi seguenti illustrano come aggiungere il file CAB da un programma usando le funzioni di database.
8.  Per aggiungere il file CAB al pacchetto di installazione da un programma, aprire una vista nella [ \_ tabella dei flussi](-streams-table.md) del database usando [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa).
9.  Usare [**MsiRecordSetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstringa) per impostare la colonna Name della \_ tabella streams sul nome visualizzato nella colonna CAB della [tabella media](media-table.md). Omettere il simbolo di cancelletto: \# .
10. Utilizzare [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) per impostare la colonna di dati della \_ tabella dei flussi sui dati dell'archivio.
11. Usare [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) per aggiornare il record nella \_ tabella dei flussi.
12. Per utilizzare Msidb.exe per aggiungere il file CAB Mycab.cab al pacchetto di installazione denominato Mydatabase.msi, utilizzare la seguente riga di comando: Msidb.exe-d mydatabase.msi-a mycab.cab. In questo caso, la colonna CAB della tabella media deve contenere la stringa: \#mycab.cab.

 

 



