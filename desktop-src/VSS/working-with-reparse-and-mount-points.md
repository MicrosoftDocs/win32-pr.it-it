---
description: L'elaborazione di uno dei set di file di un componente può richiedere a un richiedente di attraversare in modo ricorsivo un albero di directory, che può richiedere al richiedente di gestire le cartelle montate e i reparse point (ad esempio i collegamenti) che puntano a dati che non si trova nel volume corrente.
ms.assetid: d0e08598-a8a2-489b-9cb2-e989bed1ce53
title: Uso di cartelle montate e reparse point
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1162d1d7da5869f588ae61d9235ec3d5827265c5eb9deaa23c38b8b9e85db68
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905061"
---
# <a name="working-with-mounted-folders-and-reparse-points"></a>Uso di cartelle montate e reparse point

L'elaborazione di uno dei set di file di un componente può richiedere a un richiedente di attraversare in modo ricorsivo un albero di directory, che può richiedere al richiedente di gestire le cartelle montate e i reparse point (ad esempio i collegamenti) che puntano a dati che non si trova nel volume corrente.

È previsto che i richiedenti seguano le cartelle montate e i reparse point durante l'attraversamento di un albero di directory e vss dispone di linee guida ben definite per gestirle per le operazioni di backup e ripristino.

Per illustrare queste linee guida, considerare l'esempio seguente:

-   Il volume \\ \\ ? \\ Il volume{GUID \_ 1} ha la lettera di unità C: \\ .
-   Un set di file ha il percorso C: \\ WriterData.
-   Il set di file usa una specifica di file con estensione \* dat.
-   La ricorsione del set di file è impostata su **TRUE.**
-   La directory C: \\ WriterData si trova nel volume \\ \\ ? \\ Volume{GUID \_ 1}.
-   La directory C: \\ WriterData \\ Archive è una cartella montata.
-   Il volume \\ \\ ? \\ Il volume{GUID \_ 2} è associato alla cartella montata C: \\ WriterData \\ Archive.

## <a name="handling-mounted-folders-and-reparse-points-during-backup"></a>Gestione di cartelle montate e reparse point durante il backup

Le regole di base per la gestione delle cartelle montate e dei reparse point in VSS durante l'esecuzione di un backup ricorsivo possono essere riepilogate come segue:

-   I percorsi vengono seguiti nelle cartelle montate e nei reparse point.
-   Se una cartella montata o un reparse point punta a un volume, tale volume deve essere copiato in shadow.
-   Se un volume contiene cartelle montate o reparse point, questi verranno visualizzati nella copia shadow del volume.
-   I dati presenti nella cartella montata o nel reparse point vengono acquisiti nella copia shadow del volume a cui punta la cartella montata o il reparse point.

Per illustrare l'uso dell'esempio precedente, poiché è impostato il flag ricorsivo, il richiedente deve esaminare tutti i dati in C: WriterData Archive e \\ \\ versioni precedenti.

Il richiedente deve aggiungere sia il volume con lettera di unità C: \\ ( \\ \\ ? \\ Volume{GUID 1}) e il volume associato alla cartella montata \_ C: \\ WriterData \\ Archive ( \\ \\ ? \\ Volume{GUID \_ 2}) nel set di copie shadow [**usando IVssBackupComponents::AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset).

La cartella montata C: \\ WriterData \\ Archive viene visualizzata nella copia shadow del volume \\ \\ ? \\ Volume{GUID \_ 1}, che ha un oggetto dispositivo denominato deviceObject1.

Tuttavia, il Servizio Copia Shadow del volume non copierà i dati nella cartella montata (i dati in \\ \\ ? \\ Volume{GUID \_ 2}) alla copia shadow a cui fa riferimento deviceObject1. Al contrario, i dati vengono acquisiti nella copia shadow di \\ \\ ? \\ Volume{GUID \_ 2}, che ha un oggetto dispositivo denominato deviceObject2.

Di conseguenza, un richiedente che sta backup di file copiati shadow in C: WriterData userà un percorso di deviceObject1 WriterData per cercare i file corrispondenti \\ a \\ C: \\ WriterData \\ \* .dat.

Per eseguire il backup di file copiati shadow in C: WriterData Archive, il richiedente userà un percorso \\ \\ di deviceObject2 (perché la directory radice di \\ \\ ? \\ Il volume{GUID 2} è stato associato alla cartella montata C: Writer Archive) per cercare i file corrispondenti a \_ \\ \\ C: \\ WriterData \\ Archive \\ \* .dat.

Si noti che un reparse point viene gestito nello stesso modo di una cartella montata. Il reparse point viene visualizzato nella copia shadow del primo volume. I dati nel reparse point vengono visualizzati nella copia shadow del secondo volume.

Durante il backup, i richiedenti devono archiviare le informazioni sulle cartelle montate e sui volumi associati, nonché i reparse point e le relative destinazioni per garantire che tutti i dati vengano sottoposti a backup e ripristinati correttamente.

## <a name="handling-mount-and-reparse-points-during-restore"></a>Gestione dei punti di montaggio e di analisi durante il ripristino

Quando si ripristinano i file, il richiedente deve seguire linee guida leggermente diverse da quelle usate durante il backup (ignorando i problemi come il [*mapping*](vssgloss-a.md) del percorso alternativo e il nuovo percorso [*di destinazione):*](vssgloss-n.md)

-   Come in precedenza, se è necessaria la ricorsione, i percorsi vengono seguiti nelle cartelle montate e nei reparse point.
-   Le cartelle montate devono essere ripristinate.
-   I percorsi di ripristino delle cartelle montate e dei reparse point sono quelli determinati dai percorsi originali.

Se i nomi dei volumi vengono mantenuti tra il backup e il ripristino, ovvero non si creano nuovamente i volumi, le cartelle montate ripristinate e i reparse point devono puntare ai volumi corretti.

Pertanto, nell'esempio illustrato in precedenza, se la cartella montata C: \\ WriterData \\ Archive è stata ripristinata in ( \\ \\ ? \\ Volume{GUID 1}) e il volume associato in precedenza è \_ stato ripristinato in ( \\ \\ ? \\ Volume{GUID \_ 2}), i file ripristinati e la struttura dei file sarebbero corretti e coerenti.

È possibile che i dati vengono ripristinati in un sistema in cui i nomi dei volumi sono cambiati. Ciò potrebbe essere dovuto a arresti anomali del disco, in cui potrebbe essere necessario eseguire un ripristino manuale del sistema e creare nuovamente i volumi. In questo tipo di situazione, le cartelle montate e i reparse point non saranno più validi dopo il ripristino. Per creare nuovamente i file e la struttura dei file nel volume ripristinato, sarà necessario eliminare le cartelle montate ripristinate e i reparse point e crearli nuovamente su disco. È l'applicazione di backup a decidere se è appropriato.

Si noti che è possibile che la destinazione di ripristino per una cartella montata sia già occupata. Ad esempio, C: \\ WriterData \\ Archive potrebbe già contenere alcuni file. È l'applicazione di backup a decidere come gestire questa situazione.

 

 



