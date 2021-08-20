---
description: Un'operazione di clonazione a blocchi indica file system copiare un intervallo di byte di file per conto di un'applicazione.
ms.assetid: E18E8D79-3985-40B8-A4C5-A73A21E5C527
title: Bloccare la clonazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7d94afdb9b630f501de4baee0b690715f42d057a157f31b142c231e0a03f9f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582666"
---
# <a name="block-cloning"></a>Bloccare la clonazione

*Un'operazione di clonazione* in blocchi indica file system copiare un intervallo di byte di file per conto di un'applicazione. Il file di destinazione può essere uguale o diverso dal file di origine.

Un file system gestisce i mapping di [cluster](clusters-and-extents.md)ed extent e può essere in grado di eseguire la copia modificando il numero di cluster virtuale (VCN) al numero di cluster logico (LCN) come operazione di metadati a basso costo, anziché leggere e scrivere i dati dei file sottostanti. In questo modo la copia può essere completata più velocemente e genera meno operazioni di I/O nell'archiviazione sottostante. Inoltre, più file possono ora condividere cluster logici dopo il clone del blocco, risparmiando capacità non archiviando cluster identici più volte su disco.

Un'operazione di clonazione a blocchi non interrompe l'isolamento fornito tra i file. Al termine di un clone in blocchi, le scritture nel file di origine non vengono visualizzate nella destinazione o viceversa.

La clonazione a blocchi è disponibile solo nel tipo [di file system ReFS](/windows/desktop/w8cookbook/resilient-file-system--refs-) che inizia con Windows Server 2016.

## <a name="block-cloning-on-refs"></a>Bloccare la clonazione in ReFS

ReFS in Windows Server 2016 la clonazione dei blocchi tramite il mapping di cluster logici (ovvero posizioni fisiche in un volume) dall'area di origine all'area di destinazione. Usa quindi un meccanismo di allocazione in scrittura per garantire l'isolamento tra tali aree. Le aree di origine e di destinazione possono essere nello stesso file o in file diversi.

Questa implementazione richiede che gli offset di file iniziale e finale siano allineati ai limiti del cluster. In ReFS Windows Server 2016, i cluster hanno dimensioni di 4 KB per impostazione predefinita, ma facoltativamente possono essere impostati su 64 KB. Le dimensioni del cluster sono un set di parametri a livello di volume in fase di formato.

## <a name="restrictions-and-remarks"></a>Restrizioni e osservazioni

-   Le aree di origine e di destinazione devono iniziare e terminare in corrispondenza di un limite del cluster.
-   L'area clonata deve avere una lunghezza minore di 4 GB.
-   L'area di destinazione non deve estendersi oltre la fine del file. Se l'applicazione vuole estendere la destinazione con dati clonati, deve prima chiamare [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile).
-   Se le aree di origine e di destinazione si trovano nello stesso file, non si devono sovrapporre. L'applicazione può procedere suddividendo l'operazione di clonazione in blocchi multipli che non si sovrappongono più.
-   I file di origine e di destinazione devono essere nello stesso volume ReFS.
-   I file di origine e di destinazione devono avere la stessa impostazione di integrità [**Flussi**](file-attribute-constants.md) ,ovvero l'Flussi di integrità deve essere abilitata in entrambi i file o disabilitata in entrambi i file.
-   Se il file di origine è un file sparse, anche il file di destinazione deve essere sparse.
-   L'operazione di clonazione del blocco interrompe i blocchi opportunistici condivisi (noti anche come [blocchi opportunistici di livello 2).](types-of-opportunistic-locks.md)
-   Il volume ReFS deve essere stato formattato con Windows Server 2016 e se è in uso il clustering di failover di Windows, il livello di funzionalità clustering deve essere stato Windows Server 2016 o versione successiva in fase di formato.

## <a name="example"></a>Esempio

Si supponga di avere due file, X e Y, in cui ogni file è costituito da tre aree distinte. Ogni area file viene archiviata in un'area distinta del volume. L file system archivia la conoscenza che a ognuna di queste aree del volume viene fatto riferimento in un'area file:

![prima della clonazione](images/before-clone.png)

Si supponga ora che un'applicazione ese ta un'operazione di clonazione a blocchi dal file X, sulle aree di file A e B, al file Y in corrispondenza dell'offset in cui si trova attualmente E. Lo stato file system seguente:

![dopo la clonazione](images/after-clone.png)

I dati nelle aree A e B sono stati effettivamente duplicati dal file X al file Y modificando i mapping da VCN a LCN all'interno del volume ReFS. Le aree di backup degli extent del disco A e B non sono state lette, né gli extent del disco che supportano le aree E e F precedente sono stati sovrascritti durante l'operazione.

I file X e Y ora condividono cluster logici su disco. Ciò si riflette nei conteggi dei riferimenti visualizzati nella tabella. La condivisione comporta un consumo di capacità del volume inferiore rispetto al caso in cui le aree A e B fossero duplicate nel volume sottostante.

Si supponga ora che l'applicazione sovrascriva l'area A nel file X. ReFS crea una copia duplicata di A, che verrà ora chiamata G. ReFS, quindi esegue il mapping di G al file X e applica la modifica. In questo modo viene mantenuto l'isolamento dei file. I conteggi dei riferimenti vengono aggiornati in modo appropriato:

![dopo la modifica di write](images/after-modifying-write.png)

Dopo la modifica della scrittura, l'area B è ancora condivisa su disco. Notare che se l'area A fosse stata più grande di un cluster, sarebbe stato duplicato solo il cluster modificato e la parte rimanente sarebbe rimasta condivisa.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**\_DUPLICARE I DATI DEGLI \_ EXTENT**](/windows/desktop/api/WinIoCtl/ns-winioctl-duplicate_extents_data)
</dt> <dt>

[**EXTENT DUPLICATI FSCTL \_ \_ NEL \_ \_ FILE**](/windows/win32/api/winioctl/ni-winioctl-fsctl_duplicate_extents_to_file)
</dt> </dl>

 

 
