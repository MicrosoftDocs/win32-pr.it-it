---
description: Nel file system NTFS i flussi contengono i dati scritti in un file e che forniscono altre informazioni su un file rispetto agli attributi e alle proprietà.
ms.assetid: 41dda6f1-a6d1-4e76-94f3-a72f9e491bee
title: Flussi di file (file system locali)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a934a51225a886e3d5a7de4d9e1e91900fab460
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755162"
---
# <a name="file-streams-local-file-systems"></a>Flussi di file (file system locali)

Un flusso è una sequenza di byte. Nel file system NTFS i flussi contengono i dati scritti in un file e che forniscono altre informazioni su un file rispetto agli attributi e alle proprietà. Ad esempio, è possibile creare un flusso che contiene parole chiave di ricerca o l'identità dell'account utente che crea un file.

Ogni flusso associato a un file ha dimensioni di allocazione, dimensioni effettive e lunghezza dei dati valide:

-   La dimensione di allocazione è la quantità di spazio su disco riservata per un flusso.
-   Le dimensioni effettive corrispondono al numero di byte utilizzati da un chiamante.
-   La lunghezza dei dati valida (VDL) è il numero di byte inizializzati dalla dimensione di allocazione per il flusso.

Ogni flusso mantiene anche il proprio stato per la compressione, la crittografia e la sparsità. L' **attributo \_ file \_ \_ sparse** file attributo nel file è impostato nel membro **DwFileAttributes** della struttura di [**\_ \_ dati Find Win32**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) restituita dalle funzioni [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa)e [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) se uno dei flussi è mai stato sparse. [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa), [**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa), [**GetFileAttributesTransacted**](/windows/desktop/api/WinBase/nf-winbase-getfileattributestransacteda), [**GetFileInformationByHandle**](/windows/desktop/api/FileAPI/nf-fileapi-getfileinformationbyhandle)e [**GetFileInformationByHandleEx**](/windows/desktop/api/WinBase/nf-winbase-getfileinformationbyhandleex) restituiscono lo stato di tipo sparse del flusso di dati predefinito se non è specificato alcun flusso.

Non sono disponibili orari dei file associati a un flusso. Le ore dei file per un file vengono aggiornate quando viene aggiornato un flusso in un file.

I blocchi opportunistici vengono mantenuti per ogni flusso. Anche le modalità di condivisione vengono mantenute per ogni flusso. Quando si richiede l'accesso DELETE per un file, il sistema operativo verifica l'accesso DELETE per tutti i flussi aperti in un file. Se un altro processo ha aperto un flusso senza l'autorizzazione di **\_ \_ eliminazione della condivisione file** , non è possibile aprire il file per l'accesso DELETE.

Se un file copiato ha un flusso di dati e viene usato il redirector di rete, il file può essere copiato solo se il client dispone sia dell'autorizzazione lettura che dell'autorizzazione lettura attributi.

## <a name="naming-conventions-for-streams"></a>Convenzioni di denominazione per i flussi

Quando viene specificato dalla riga di comando della shell di Windows, il nome completo di un flusso è "*filename*:*Stream name*:*Stream Type*", come nell'esempio seguente: "myfile. dat: stream1: $data".

I caratteri validi per un nome file sono validi anche per il nome del flusso, inclusi gli spazi. Per ulteriori informazioni, vedere [denominazione di un file](naming-a-file.md). Il tipo di flusso, detto anche codice di tipo di attributo, è interno al file system NTFS. Pertanto, gli utenti non possono creare nuovi tipi di flusso, ma possono aprire i tipi di file system NTFS esistenti. I valori dell'identificatore del tipo di flusso iniziano sempre con il simbolo del dollaro ($). Per un elenco dei tipi di flusso, vedere di seguito.

Per impostazione predefinita, il flusso di dati predefinito è senza nome. Per specificare completamente il flusso di dati predefinito, usare "*filename*:: $data", dove $data è il tipo di flusso. Equivale a "*filename*". È possibile creare un flusso denominato nel file usando le [convenzioni di denominazione dei file](naming-a-file.md). Si noti che "$DATA" è un nome di flusso valido. Ad esempio, il nome completo di un flusso denominato "$DATA" in un file denominato "*Sample*" sarà "*Sample*: $data: $data". Se è stato creato un flusso denominato "barra" nello stesso file, il nome completo sarà "*Sample*: bar: $data".

Quando si creano e si utilizzano file con nomi di un carattere, anteporre al nome del file il periodo seguito da una barra rovesciata (. in \) alternativa, utilizzare un nome di percorso completo. Il motivo è che Windows considera i nomi di file di un solo carattere come lettere di unità. Quando si specifica una lettera di unità con un percorso relativo, i due punti separano la lettera di unità dal percorso. Quando si verifica un'ambiguità sul fatto che il nome di un solo carattere sia una lettera di unità o un nome di file, Windows presuppone che si tratti di una lettera di unità se la stringa che segue i due punti è un percorso valido, anche se la lettera di unità non è valida.

## <a name="stream-types"></a>Tipi di flusso

Di seguito è riportato l'elenco dei tipi di flusso NTFS, denominati anche codici di tipo di attributo. Alcuni tipi di flusso sono interni a NTFS e il formato non è documentato.



| Tipo di flusso                | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| elenco:: $ATTRIBUTE \_         | Contiene un elenco di tutti gli attributi che compongono il file e identifica la posizione in cui si trova ogni attributo.                                                                                                                                                                                                                                                                                                                                          |
| :: $BITMAP                  | Bitmap utilizzata dagli indici per gestire lo spazio disponibile nell'albero b per una directory. L'albero b è gestito in blocchi da 4 KB (indipendentemente dalle dimensioni del cluster) e viene usato per gestire l'allocazione di questi blocchi. Questo tipo di flusso è presente in ogni directory.                                                                                                                                                                                           |
| :: $DATA                    | Flusso di dati. Il flusso di dati predefinito non ha un nome. I flussi di dati possono essere enumerati usando le funzioni [**FindFirstStreamW**](/windows/desktop/api/fileapi/nf-fileapi-findfirststreamw) e [**FindNextStreamW**](/windows/desktop/api/fileapi/nf-fileapi-findnextstreamw) .                                                                                                                                                                                                                                                |
| :: $EA                      | Contiene i dati degli attributi estesi.|
| :: $EA \_ informazioni         | Contiene informazioni di supporto sugli attributi estesi.                                                                                                                                                                                                                                                                                                                                                                                      |
| :: $FILE \_ nome              | Nome del file, in caratteri Unicode. Sono inclusi il nome breve del file e tutti i collegamenti reali.                                                                                                                                                                                                                                                                                                                                 |
| allocazione $INDEX:: \_       | Tipo di flusso di una directory. Utilizzato per implementare l'allocazione di file per directory di grandi dimensioni. Questo flusso rappresenta la directory stessa e contiene tutti i dati della directory. Le modifiche apportate ai flussi di questo tipo vengono registrate nel journal delle modifiche NTFS. Il nome del flusso predefinito di un \_ tipo di flusso di allocazione $index è $I 30, quindi "*dirname*", "*dirname*:: $index \_ allocation" e "*dirname*: $I 30: $index \_ allocation" sono tutti equivalenti. |
| radice $INDEX:: \_             | Questo flusso rappresenta la radice dell'albero b di un indice. Questo tipo di flusso è presente in ogni directory.                                                                                                                                                                                                                                                                                                                                           |
| flusso dell'utilità:: $LOGGED \_ \_ | Simile a:: $DATA ma le operazioni vengono registrate nel journal delle modifiche NTFS. Utilizzato da EFS e [transazionale NTFS (TXF)](transactional-ntfs-portal.md). La coppia ":*streamName*: $*STREAMTYPE*" per EFS è ": $EFS: $Logged \_ \_ flusso di utilità" e per TXF è ": $TXF \_ Data: \_ flusso di utilità $logged \_ ".                                                                                                                                                    |
| ID:: $OBJECT \_              | ID a 16 byte utilizzato per identificare il file per il servizio di rilevamento dei collegamenti.                                                                                                                                                                                                                                                                                                                                                                           |
| :: \_ punto $REPARSE          | Dati di [reparse point](reparse-points.md) .|



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di flussi](using-streams.md)
</dt> </dl>

 

 



