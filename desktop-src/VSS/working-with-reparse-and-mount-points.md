---
description: L'elaborazione di uno dei set di file di un componente potrebbe richiedere a un richiedente di attraversare un albero di directory in modo ricorsivo, che può richiedere al richiedente di gestire le cartelle montate e i reparse point, ad esempio i collegamenti, che puntano a dati che non si trova nel volume corrente.
ms.assetid: d0e08598-a8a2-489b-9cb2-e989bed1ce53
title: Uso delle cartelle e dei reparse point montati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 397a7aa88f39361f788f9aac882b4f9d337fd6f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307125"
---
# <a name="working-with-mounted-folders-and-reparse-points"></a>Uso delle cartelle e dei reparse point montati

L'elaborazione di uno dei set di file di un componente potrebbe richiedere a un richiedente di attraversare un albero di directory in modo ricorsivo, che può richiedere al richiedente di gestire le cartelle montate e i reparse point, ad esempio i collegamenti, che puntano a dati che non si trova nel volume corrente.

Si prevede che i richiedenti seguano le cartelle montate e i reparse point durante l'attraversamento di un albero di directory, mentre VSS include linee guida ben definite per gestirle per le operazioni di backup e ripristino.

Per illustrare queste linee guida, prendere in considerazione l'esempio seguente:

-   Il volume \\ \\ ? \\ Il volume {GUID \_ 1} contiene la lettera di unità C: \\ .
-   Il percorso di un set di file è C: \\ WriterData.
-   Un file Specification \* . dat viene utilizzato dal set di file.
-   La ricorsione del set di file è impostata su **true**.
-   La directory C: \\ WriterData si trova nel volume \\ \\ ? \\ Volume {GUID \_ 1}.
-   La directory C: \\ WriterData \\ Archive è una cartella montata.
-   Il volume \\ \\ ? \\ Il volume {GUID \_ 2} è associato alla cartella montata C: \\ WriterData \\ Archive.

## <a name="handling-mounted-folders-and-reparse-points-during-backup"></a>Gestione delle cartelle montate e dei reparse point durante il backup

Le regole di base per la gestione delle cartelle montate e dei reparse point in VSS durante l'esecuzione di un backup ricorsivo possono essere riepilogate come segue:

-   I percorsi vengono seguiti tra le cartelle montate e i reparse point.
-   Se una cartella montata o un punto di analisi punta a un volume, tale volume deve essere replicato.
-   Se un volume contiene cartelle montate o punti di analisi, questi verranno visualizzati nella copia shadow del volume.
-   I dati che si trova nella cartella montata o nel punto di analisi vengono acquisiti nella copia shadow del volume a cui punta la cartella montata o il punto di analisi.

Per illustrare l'uso dell'esempio precedente, poiché è impostato il flag ricorsivo, il richiedente deve esaminare tutti i dati nell' \\ Archivio C: WriterData \\ e sotto.

Il richiedente deve aggiungere il volume con la lettera di unità C: \\ ( \\ \\ ? \\ Volume {GUID \_ 1}) e volume associato alla cartella montata C: \\ WriterData \\ Archive ( \\ \\ ? \\ Volume {GUID \_ 2}) per il set di copie shadow con [**IVssBackupComponents:: AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset).

La cartella montata C: \\ WriterData \\ Archive viene visualizzata nella copia shadow del volume \\ \\ ? \\ Volume {GUID \_ 1}, che include un oggetto dispositivo denominato deviceObject1.

Tuttavia, il servizio Copia Shadow del volume non copia i dati nella cartella montata (dati su \\ \\ ? \\ Volume {GUID \_ 2}) per la copia shadow a cui fa riferimento deviceObject1. I dati vengono invece acquisiti nella copia shadow di \\ \\ ? \\ Volume {GUID \_ 2}, che include un oggetto dispositivo denominato deviceObject2.

Pertanto, un richiedente che esegue il backup dei file copiati Shadow in C: \\ WriterData utilizzerà il percorso deviceObject1 \\ WriterData per cercare i file corrispondenti a C: \\ WriterData \\ \* . dat.

Per eseguire il backup dei file con copia shadow nell'archivio C: \\ WriterData \\ , il richiedente userà un percorso di deviceObject2 (perché la directory radice di \\ \\ ? \\ Il volume {GUID \_ 2} è stato associato alla cartella montata c: \\ Archivio del writer \\ ) per cercare i file corrispondenti a c: \\ WriterData \\ Archive \\ \* . dat.

Si noti che un reparse point viene gestito allo stesso modo di una cartella montata. Il punto di analisi viene visualizzato nella copia shadow del primo volume. I dati nel punto di analisi vengono visualizzati nella copia shadow del secondo volume.

Durante il backup, i richiedenti devono archiviare le informazioni sulle cartelle montate e i volumi associati, nonché i reparse point e le relative destinazioni per garantire che tutti i dati vengano sottoposti a backup e ripristinati correttamente.

## <a name="handling-mount-and-reparse-points-during-restore"></a>Gestione del montaggio e dei reparse point durante il ripristino

Quando si ripristinano i file, il richiedente deve seguire le linee guida in modo diverso rispetto a quelle usate durante il backup (ignorando i problemi, ad esempio il [*mapping del percorso alternativo*](vssgloss-a.md) e il [*nuovo percorso di destinazione*](vssgloss-n.md)):

-   Come prima, se è necessaria la ricorsione, i percorsi vengono seguiti tra le cartelle montate e i reparse point.
-   Le cartelle montate devono essere ripristinate.
-   I percorsi di ripristino delle cartelle e dei reparse point montati sono quelli determinati dai percorsi originali.

Se i nomi dei volumi vengono mantenuti tra backup e ripristino, ovvero se non si ricreano i volumi, le cartelle montate ripristinate e i punti di analisi devono puntare ai volumi corretti.

Quindi, nell'esempio illustrato in precedenza, se la cartella montata C: \\ WriterData \\ Archive è stata ripristinata ( \\ \\ ? \\ Il volume {GUID \_ 1}) e il volume precedentemente associato sono stati ripristinati in ( \\ \\ ? \\ Volume {GUID \_ 2}), i file ripristinati e la struttura del file sarebbero corretti e coerenti.

È possibile che i dati vengano ripristinati in un sistema in cui sono stati modificati i nomi dei volumi. La causa potrebbe essere un arresto anomalo del disco, in cui potrebbe essere necessario eseguire un ripristino manuale del sistema e ricreare i volumi. In questo tipo di situazione, le cartelle e i reparse point montati non saranno più validi dopo il ripristino. Per ricreare i file e la struttura dei file nel volume ripristinato, è necessario eliminare le cartelle montate e reparse point ripristinate e ricrearle su disco. Spetta all'applicazione di backup decidere se è appropriato.

Si noti che è possibile che la destinazione di ripristino per una cartella montata sia già occupata. Ad esempio, C: \\ WriterData \\ Archive potrebbe già contenere alcuni file. Spetta all'applicazione di backup decidere come gestire questa situazione.

 

 



