---
description: In alternativa alla creazione e alla configurazione di partizioni locali tramite lo strumento di amministrazione Servizi componenti, è possibile gestire le partizioni a livello di programmazione utilizzando le raccolte e le proprietà di amministrazione COM+ specifiche della partizione.
ms.assetid: 82f790cf-3f94-44d9-b722-89a6013d0300
title: Gestione delle partizioni locali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecd551fc73c76067c4ab2e988fba79ee702df53c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966319"
---
# <a name="managing-local-partitions"></a><span data-ttu-id="1a5e4-103">Gestione delle partizioni locali</span><span class="sxs-lookup"><span data-stu-id="1a5e4-103">Managing Local Partitions</span></span>

<span data-ttu-id="1a5e4-104">In alternativa alla creazione e alla configurazione di partizioni locali tramite lo strumento di amministrazione Servizi componenti, è possibile gestire le partizioni a livello di programmazione utilizzando le raccolte e le proprietà di amministrazione COM+ specifiche della partizione.</span><span class="sxs-lookup"><span data-stu-id="1a5e4-104">As an alternative to creating and configuring local partitions through the Component Services administrative tool, you can manage partitions programmatically by using partition-specific COM+ administration collections and properties.</span></span>

> [!Note]  
> <span data-ttu-id="1a5e4-105">Il servizio partizioni COM+ non è abilitato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="1a5e4-105">The COM+ partitions service is not enabled by default.</span></span> <span data-ttu-id="1a5e4-106">Per utilizzare il servizio partizioni COM+, è necessario abilitarlo tramite lo strumento di amministrazione Servizi componenti o modificando la proprietà PartitionsEnabled nella raccolta [**LocalComputer**](localcomputer.md) su true.</span><span class="sxs-lookup"><span data-stu-id="1a5e4-106">To use the COM+ partitions service, you must enable it through the Component Services administration tool or by changing the PartitionsEnabled property on the [**LocalComputer**](localcomputer.md) collection to True.</span></span>

 

<span data-ttu-id="1a5e4-107">La subroutine seguente scritta in Visual Basic script illustra come creare una partizione nel computer locale:</span><span class="sxs-lookup"><span data-stu-id="1a5e4-107">The following subroutine written in Visual Basic script demonstrates how to create a partition on the local computer:</span></span>


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



<span data-ttu-id="1a5e4-108">La subroutine seguente scritta in Visual Basic script illustra come eliminare una partizione dal computer locale:</span><span class="sxs-lookup"><span data-stu-id="1a5e4-108">The following subroutine written in Visual Basic script demonstrates how to delete a partition from the local computer:</span></span>


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



<span data-ttu-id="1a5e4-109">La subroutine seguente scritta in Visual Basic script illustra come impostare la partizione predefinita per un utente:</span><span class="sxs-lookup"><span data-stu-id="1a5e4-109">The following subroutine written in Visual Basic script demonstrates how to set the default partition for a user:</span></span>


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



<span data-ttu-id="1a5e4-110">La subroutine seguente scritta in Visual Basic script illustra come rimuovere la partizione predefinita per un utente:</span><span class="sxs-lookup"><span data-stu-id="1a5e4-110">The following subroutine written in Visual Basic script demonstrates how to remove the default partition for a user:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="1a5e4-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1a5e4-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a5e4-112">Raccolta delle metriche della partizione</span><span class="sxs-lookup"><span data-stu-id="1a5e4-112">Collecting Partition Metrics</span></span>](collecting-partition-metrics.md)
</dt> <dt>

[<span data-ttu-id="1a5e4-113">Configurazione della cache della partizione</span><span class="sxs-lookup"><span data-stu-id="1a5e4-113">Configuring the Partition Cache</span></span>](configuring-the-partition-cache.md)
</dt> <dt>

[<span data-ttu-id="1a5e4-114">Raggruppamento di applicazioni in partizioni</span><span class="sxs-lookup"><span data-stu-id="1a5e4-114">Grouping Applications into Partitions</span></span>](grouping-applications-into-partitions.md)
</dt> <dt>

[<span data-ttu-id="1a5e4-115">Gestione di partizioni all'interno Active Directory</span><span class="sxs-lookup"><span data-stu-id="1a5e4-115">Managing Partitions Within Active Directory</span></span>](managing-partitions-within-active-directory.md)
</dt> <dt>

[<span data-ttu-id="1a5e4-116">Impostazione dei diritti amministrativi per una partizione</span><span class="sxs-lookup"><span data-stu-id="1a5e4-116">Setting Administrative Rights for a Partition</span></span>](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



