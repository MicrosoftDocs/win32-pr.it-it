---
description: Un richiedente deve selezionare un provider specifico solo se contiene alcune informazioni sui provider disponibili.
ms.assetid: 1a3bc938-2754-4fa2-bd7f-e9b3e876bf6c
title: Selezione di provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39435f8f34091ccef51a6cce85b2c596f0c687d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131255"
---
# <a name="selecting-providers"></a><span data-ttu-id="81d0f-103">Selezione di provider</span><span class="sxs-lookup"><span data-stu-id="81d0f-103">Selecting Providers</span></span>

<span data-ttu-id="81d0f-104">Un richiedente deve selezionare un provider specifico solo se contiene alcune informazioni sui provider disponibili.</span><span class="sxs-lookup"><span data-stu-id="81d0f-104">A requester should select a specific provider only if it has some information about the providers available.</span></span>

<span data-ttu-id="81d0f-105">Poiché non si tratta in genere del caso, è consigliabile che un richiedente fornisca il GUID \_ null come ID provider a [**IVssBackupComponents:: AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset), che consente al sistema di scegliere un provider secondo l'algoritmo seguente:</span><span class="sxs-lookup"><span data-stu-id="81d0f-105">Because this will not generally be the case, it is recommended that a requester supply GUID\_NULL as a provider ID to [**IVssBackupComponents::AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset), which allows the system to choose a provider according to the following algorithm:</span></span>

1.  <span data-ttu-id="81d0f-106">Se è disponibile un provider hardware che supporta il volume specificato, viene selezionato.</span><span class="sxs-lookup"><span data-stu-id="81d0f-106">If a hardware provider that supports the given volume is available, it is selected.</span></span>
2.  <span data-ttu-id="81d0f-107">Se non è disponibile alcun provider hardware, viene selezionato se è disponibile un provider software specifico per il volume specificato.</span><span class="sxs-lookup"><span data-stu-id="81d0f-107">If no hardware provider is available, then if any software provider specific to the given volume is available, it is selected.</span></span>
3.  <span data-ttu-id="81d0f-108">Se non è disponibile alcun provider hardware e nessun provider software specifico per i volumi, viene selezionato il provider di sistema.</span><span class="sxs-lookup"><span data-stu-id="81d0f-108">If no hardware provider and no software provider specific to the volumes is available, the system provider is selected.</span></span>

<span data-ttu-id="81d0f-109">Un richiedente può tuttavia ottenere informazioni sui provider disponibili usando [**IVssBackupComponents:: query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query).</span><span class="sxs-lookup"><span data-stu-id="81d0f-109">However, a requester can obtain information about available providers by using [**IVssBackupComponents::Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query).</span></span> <span data-ttu-id="81d0f-110">Con queste informazioni e solo se l'applicazione di backup dispone di una conoscenza corretta dei diversi provider, un richiedente può fornire un ID provider valido a [**IVssBackupComponents:: AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset).</span><span class="sxs-lookup"><span data-stu-id="81d0f-110">With this information, and only if the backup application has a good understanding of the various providers, a requester can supply a valid provider ID to [**IVssBackupComponents::AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset).</span></span>

<span data-ttu-id="81d0f-111">Si noti che non è necessario che tutti i volumi abbiano lo stesso provider.</span><span class="sxs-lookup"><span data-stu-id="81d0f-111">Note that all volumes do not need to have the same provider.</span></span>

 

 



