---
description: Un'operazione di clonazione a blocchi indica al file system di copiare un intervallo di byte di file per conto di un'applicazione.
ms.assetid: E18E8D79-3985-40B8-A4C5-A73A21E5C527
title: Clonazione del blocco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b33aa1c1eee693b6ed4b502aedc6da6176ece3e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530007"
---
# <a name="block-cloning"></a>Clonazione del blocco

Un'operazione di *clonazione a blocchi* indica al file System di copiare un intervallo di byte di file per conto di un'applicazione. Il file di destinazione può essere uguale o diverso da quello del file di origine.

Un file system gestisce i mapping di [cluster ed extent](clusters-and-extents.md)e può essere in grado di eseguire la copia modificando il numero di cluster virtuale (VCN) in mapping del numero di cluster logico (LCN) come operazione di metadati a basso costo, anziché leggere e scrivere i dati di file sottostanti. In questo modo la copia viene completata più velocemente e genera un minor numero di I/O nell'archivio sottostante. Inoltre, più file possono ora condividere i cluster logici dopo il clone del blocco, salvando la capacità senza archiviare cluster identici più volte su disco.

Un'operazione di clonazione A blocchi non interrompe l'isolamento fornito tra i file. Al termine di un clone del blocco, le scritture nel file di origine non vengono visualizzate nella destinazione o viceversa.

La clonazione a blocchi è disponibile solo nel tipo di [file System refs](/windows/desktop/w8cookbook/resilient-file-system--refs-) a partire da Windows Server 2016.

## <a name="block-cloning-on-refs"></a>Blocca la clonazione su ReFS

ReFS in Windows Server 2016 implementa la clonazione del blocco mediante la modifica del mapping dei cluster logici (ovvero percorsi fisici su un volume) dall'area di origine all'area di destinazione. USA quindi un meccanismo di allocazione in scrittura per garantire l'isolamento tra tali aree. Le aree di origine e di destinazione possono trovarsi nello stesso file o in file diversi.

Questa implementazione richiede che gli offset del file iniziale e finale siano allineati ai limiti del cluster. In ReFS in Windows Server 2016, le dimensioni dei cluster sono 4KB per impostazione predefinita, ma è possibile impostare facoltativamente 64KB. Le dimensioni del cluster sono un set di parametri a livello di volume in fase di formattazione.

## <a name="restrictions-and-remarks"></a>Restrizioni e osservazioni

-   Le aree di origine e di destinazione devono iniziare e terminare in corrispondenza di un limite del cluster.
-   L'area clonata deve avere una lunghezza minore di 4 GB.
-   L'area di destinazione non deve estendersi oltre la fine del file. Se l'applicazione desidera estendere la destinazione con dati clonati, deve prima chiamare [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile).
-   Se le aree di origine e di destinazione si trovano nello stesso file, non si devono sovrapporre. (L'applicazione può procedere suddividendo l'operazione di clonazione del blocco in più cloni di blocco che non si sovrappongono più.)
-   I file di origine e di destinazione devono essere nello stesso volume ReFS.
-   I file di origine e di destinazione devono avere la stessa impostazione dei [**flussi di integrità**](file-attribute-constants.md) , ovvero i flussi di integrità devono essere abilitati in entrambi i file o disabilitati in entrambi i file.
-   Se il file di origine è un file sparse, anche il file di destinazione deve essere sparse.
-   L'operazione di clonazione del blocco interrompe i blocchi opportunistici condivisi (noti anche come [blocchi opportunistici di livello 2](types-of-opportunistic-locks.md)).
-   Il volume ReFS deve essere stato formattato con Windows Server 2016 e se è in uso il clustering di failover di Windows, il livello di funzionalità del clustering deve essere Windows Server 2016 o versione successiva al momento del formato.

## <a name="example"></a>Esempio

Si supponga di avere due file, X e Y, in cui ogni file è composto da tre aree distinte. Ogni area del file è archiviata in un'area distinta del volume. Il file system archivia le informazioni a cui viene fatto riferimento a ognuna di queste aree del volume in un'area del file:

![prima del clone](images/before-clone.png)

Si supponga ora che un'applicazione verifichi un'operazione di clonazione a blocchi dal file X, sulle aree dei file A e B, al file Y in corrispondenza dell'offset in cui E attualmente è. Viene generato lo stato di file system seguente:

![dopo clone](images/after-clone.png)

I dati nelle aree A e B sono stati duplicati in modo efficace dal file X al file Y modificando i mapping di VCN in LCN all'interno del volume ReFS. Gli extent del disco che fanno parte delle aree A e B non sono stati letti, né gli extent del disco che eseguono il backup delle aree precedenti e e F sovrascritti durante l'operazione.

I file X e Y ora condividono i cluster logici su disco. Questa operazione viene riflessa nei conteggi dei riferimenti indicati nella tabella. La condivisione comporta un consumo più basso della capacità del volume rispetto alle aree A e B duplicate nel volume sottostante.

A questo punto, si supponga che l'applicazione sovrascriva l'area A nel file X. ReFS crea una copia duplicata di un, che ora chiameremo G. ReFS, quindi esegue il mapping di G nel file X e applica la modifica. In questo modo viene mantenuto l'isolamento dei file. I conteggi dei riferimenti vengono aggiornati in modo appropriato:

![Dopo la modifica della scrittura](images/after-modifying-write.png)

Dopo la modifica della scrittura, l'area B è ancora condivisa sul disco. Notare che se l'area A fosse stata più grande di un cluster, sarebbe stato duplicato solo il cluster modificato e la parte rimanente sarebbe rimasta condivisa.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**\_dati extent duplicati \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-duplicate_extents_data)
</dt> <dt>

[**FSCTL \_ gli \_ extent duplicati \_ nel \_ file**](/windows/win32/api/winioctl/ni-winioctl-fsctl_duplicate_extents_to_file)
</dt> </dl>

 

 
