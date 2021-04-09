---
description: Suggerimenti per le transazioni file system ottimali.
ms.assetid: 847939ff-5322-4023-8ef7-9d845e80d65c
title: Considerazioni sulle prestazioni per la funzionalità NTFS transazionale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a71f7e100e1ddd8524932a4a259a12092bddcb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968146"
---
# <a name="performance-considerations-for-transactional-ntfs"></a>Considerazioni sulle prestazioni per la funzionalità NTFS transazionale

Transactional NTFS (TxF) è stato progettato in modo accurato per le prestazioni e offre in genere prestazioni migliori rispetto alle alternative transazionali per utilizzo generico in scenari analoghi. Tuttavia, le transazioni file system hanno un sovraccarico maggiore rispetto alle operazioni non transazionali e una riduzione delle prestazioni di I/O rispetto all'I/O non transazionale è prevista. Le applicazioni critiche per le prestazioni devono eseguire un ciclo di qualificazione di adozione della tecnologia, valutando l'effetto sulle prestazioni delle operazioni transazionali file system.

## <a name="overview-of-txf-operations"></a>Panoramica delle operazioni di TxF

TxF utilizza la funzionalità di *annullamento* della registrazione per registrare le modifiche necessarie per riportare il file System in uno stato coerente, detto anche rollback, qualora si verifichi un'interruzione della transazione. Questa registrazione di annullamento genera ulteriori operazioni di I/O e rappresenta l'origine del sovraccarico delle prestazioni di TxF rispetto alle operazioni file system non transazionali.

Di seguito è riportato un riepilogo di alto livello del funzionamento di TxF:

-   Con l'avanzamento di una transazione, TxF scrive i record di *annullamento* nel relativo file di log per ogni modifica apportata al file System. Se si verifica un'interruzione, i record di annullamento vengono analizzati per riportare il file system nello stato in cui si trovava prima dell'inizio della transazione.
-   Un record di annullamento delle *modifiche dei metadati* descrive una modifica solo ai metadati del file System. Alcuni esempi sono gli spostamenti, i rinomi, le aggiunte e le modifiche di attributo. Per la modifica dei metadati annullare i record, tutte le informazioni necessarie per annullare la modifica si trovano nel record e vengono archiviate nel file di log.
-   Un record Annulla *sovrascrittura* descrive la sovrascrittura di una parte di un file. Quando si verifica una sovrascrittura di un file, il contenuto originale del file viene archiviato in un file di annullamento speciale in una directory nascosta e il record Annulla Sovrascrivi punta a questo file. Quando gli aggiornamenti dei file vengono scaricati dalla cache al disco, anche il contenuto del file di annullamento deve essere scaricato, quindi una sovrascrittura del file transazionale potrebbe generare fino a due operazioni di I/O casuali aggiuntive: una per la lettura dei dati precedenti e una per la scrittura nel file di rollback. Queste operazioni di I/O aggiuntive rappresentano un costo per le prestazioni di TxF.
-   Quando si verifica un commit, TxF Scarica innanzitutto tutte le informazioni di annullamento, quindi Scarica le modifiche effettive del file e quindi scrive e Scarica un record di commit. Se non sono presenti file di annullamento da scaricare, l'unico overhead TxF aggiuntivo relativo all'I/O non transazionale è lo svuotamento del log. Tuttavia, i cancellamenti dei log comportano Scritture sequenziali di grandi dimensioni, quindi il costo delle prestazioni è minimo.
-   TxF è ottimizzato per il commit. Si prevede che la maggior parte delle transazioni avrà esito positivo e non sarà necessario eseguire il rollback, pertanto tutti i record di annullamento per una transazione non verranno utilizzati. Dal punto di vista delle prestazioni, le operazioni di commit TxF sono veloci e i rollback sono a elevato utilizzo di risorse.
-   Il rollback comporta un uso più intensivo delle risorse rispetto al commit. Durante il rollback, è necessario annullare tutte le modifiche apportate nella transazione. In generale, la durata del rollback può essere approssimativamente la stessa che ha richiesto per apportare le modifiche in origine. Se, ad esempio, l'operazione ha richiesto 1 secondo per apportare tutte le modifiche, l'operazione potrebbe richiedere circa 1 secondo. Per transazioni molto lunghe, il rollback può creare ulteriori conseguenze sulle prestazioni. Ad esempio, l'ora di avvio del sistema può essere posticipata se il sistema deve eseguire automaticamente il rollback di una transazione nel caso in cui il sistema non risponda e debba eseguire un riavvio non pianificato.

Le conclusioni di riepilogo sulle prestazioni che è possibile trarre dall'elenco precedente sono le seguenti:

-   Il costo delle prestazioni di TxF per le transazioni che interessano sovrascritture di file può essere significativo.
-   Il costo delle prestazioni di TxF per le transazioni che coinvolgono solo le operazioni sui metadati può essere relativamente basso, purché vengano utilizzate transazioni di grandi dimensioni. Una transazione di grandi dimensioni si verifica quando sono presenti molti record di annullamento per ogni record di commit.

## <a name="recommendations-for-best-performance"></a>Suggerimenti per prestazioni ottimali

Ammortizzare il sovraccarico TxF per transazioni più grandi. Se, ad esempio, sono presenti *n* set di modifiche da apportare in cui ogni modifica presenta *m* e si ha la possibilità di eseguire questa operazione come *n* transazioni di *m* passaggi ciascuno o come una singola transazione con *m* \* *N* passaggi, quest'ultima opzione risulta più efficiente.

Prendere in considerazione il possibile effetto sull'avvio di transazioni di grandi dimensioni. Come indicato in precedenza, il rollback può essere lento e ritardare il tempo di avvio se il sistema deve eseguire rollback automatici come ora di avvio. Maggiore è la transazione, maggiore è il ritardo.

Mantieni le transazioni per la maggior parte delle operazioni sui metadati. Questo è ciò che TxF è ottimizzato per e, in generale, le prestazioni sono le stesse delle operazioni di i/O dei file non transazionali per transazioni di metadati di grandi dimensioni. Esempi di funzioni di TxF di metadati efficienti sono [**MoveFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-movefiletransacteda), [**SetFileAttributesTransacted**](/windows/desktop/api/WinBase/nf-winbase-setfileattributestransacteda), [**CopyFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-copyfiletransacteda), [**DeleteFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-deletefiletransacteda), [**CreateHardLinkTransacted**](/windows/desktop/api/WinBase/nf-winbase-createhardlinktransacteda)e scritture accodate (chiamate alla funzione [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) quando il puntatore del file è alla fine del file o *EOF*). Un esempio di operazioni non di metadati con utilizzo intensivo di risorse è costituito dalle chiamate alla funzione **WriteFile** quando il puntatore del file non si trova nella posizione EOF.

## <a name="summary-of-txf-performance-expectations"></a>Riepilogo delle aspettative sulle prestazioni di TxF

Per gli aggiornamenti sul posto, le sovrascritture in una sezione di un file saranno molto più lente rispetto all'I/O di file non transazionale, mentre le prestazioni TxF per le operazioni di file system metadati (ad esempio, create, Move e Append) sono paragonabili all'I/O di file non transazionale per le transazioni di grandi dimensioni.

 

 



