---
description: In alternativa alla creazione e alla configurazione di partizioni locali tramite lo strumento di amministrazione Servizi componenti, è possibile gestire le partizioni a livello di codice usando proprietà e raccolte di amministrazione COM+ specifiche della partizione.
ms.assetid: 82f790cf-3f94-44d9-b722-89a6013d0300
title: Gestione delle partizioni locali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 124d0b9ef7bf54f07a6b28561428c57834a6e15ec11c4ed5c89fb92f95f0a950
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118306244"
---
# <a name="managing-local-partitions"></a>Gestione delle partizioni locali

In alternativa alla creazione e alla configurazione di partizioni locali tramite lo strumento di amministrazione Servizi componenti, è possibile gestire le partizioni a livello di codice usando proprietà e raccolte di amministrazione COM+ specifiche della partizione.

> [!Note]  
> Il servizio partizioni COM+ non è abilitato per impostazione predefinita. Per usare il servizio partizioni COM+, è necessario abilitarlo tramite lo strumento di amministrazione Servizi componenti o modificando la proprietà PartitionsEnabled nella raccolta [**LocalComputer**](localcomputer.md) impostandola su True.

 

La subroutine seguente scritta nello script Visual Basic illustra come creare una partizione nel computer locale:


```VB
Sub CreatePartition (PartitonGuid, PartitionName)
   Set cat = CreateObject("COMAdmin.COMAdminCatalog")
   Set collPartitions = cat.GetCollection("Partitions")
   collPartitions.Populate
   Set part = collPartitions.Add
   ' If you don't specify a partition GUID, one is created for you.
   ' Otherwise, you can specify one this way:
   part.Value("ID") = PartitonGuid
   part.Value("Name") = PartitionName
   collPartitions.SaveChanges
   Set part = Nothing
   Set collPartitions = Nothing
   Set cat = Nothing
End Sub 
```



La subroutine seguente scritta nello script Visual Basic illustra come eliminare una partizione dal computer locale:


```VB
Sub DeletePartition (PartitionName)
   Set cat = CreateObject("COMAdmin.COMAdminCatalog")
   Set collPartitions = cat.GetCollection("Partitions")
   collPartitions.Populate
   numPartitions = collPartitions.Count
   ' Begin with the last partition, and work forward through the list.
   For i = numPartitions - 1 To 0 Step -1 
       If collPartitions.Item(i).Value("Name") = PartitionName Then
           collPartitions.Remove i
       End If
   Next
   collPartitions.SaveChanges
   Set collPartitions = Nothing
   Set cat = Nothing
End Sub
```



La subroutine seguente scritta nello script Visual Basic illustra come impostare la partizione predefinita per un utente:


```VB
Sub SetDefaultPartitionForUser(UserName, PartitionGuid)
   Set cat = CreateObject("COMAdmin.COMAdminCatalog")
   Set collUsers = cat.GetCollection("PartitionUsers")
   collUsers.Populate
   Set user = collUsers.Add
   user.Value("AccountName") = UserName
   user.Value("DefaultPartitionID") = PartitionGuid
   collUsers.SaveChanges
   Set collUsers = Nothing
   Set cat = Nothing
End Sub
```



La subroutine seguente scritta nello script Visual Basic illustra come rimuovere la partizione predefinita per un utente:


```VB
Sub RemoveDefaultPartitionForUser(UserName)
   Set cat = CreateObject("COMAdmin.COMAdminCatalog")
   Set collUsers = cat.GetCollection("PartitionUsers")
   collUsers.Populate
   numUsers = collUsers.Count
   ' Begin with the last user, and work forward through the list.
   For i = numUsers - 1 To 0 Step -1
       If collUsers.Item(i).Value("AccountName") = UserName Then
           collUsers.Remove i
       End If
   Next
   collUsers.SaveChanges
   Set collUsers = Nothing
   Set cat = Nothing
End Sub
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Raccolta delle metriche delle partizioni](collecting-partition-metrics.md)
</dt> <dt>

[Configurazione della cache delle partizioni](configuring-the-partition-cache.md)
</dt> <dt>

[Raggruppamento di applicazioni in partizioni](grouping-applications-into-partitions.md)
</dt> <dt>

[Gestione delle partizioni all'interno di Active Directory](managing-partitions-within-active-directory.md)
</dt> <dt>

[Impostazione dei diritti amministrativi per una partizione](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



