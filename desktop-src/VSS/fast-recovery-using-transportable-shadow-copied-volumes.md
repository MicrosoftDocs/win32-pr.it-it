---
description: Le copie shadow trasportabili possono essere utilizzate per facilitare un ripristino rapido.
ms.assetid: 2eaffcf7-01b2-44ce-8bc4-fd9fa42c8a8c
title: Ripristino rapido tramite volumi di copie shadow trasportabili
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a588395de36b0e6773eacf7f46a45452a69c13c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318581"
---
# <a name="fast-recovery-using-transportable-shadow-copied-volumes"></a><span data-ttu-id="c35f8-103">Ripristino rapido tramite volumi di copie shadow trasportabili</span><span class="sxs-lookup"><span data-stu-id="c35f8-103">Fast Recovery Using Transportable Shadow Copied Volumes</span></span>

<span data-ttu-id="c35f8-104">Le [*copie shadow trasportabili*](vssgloss-t.md) possono essere utilizzate per facilitare un *ripristino rapido*.</span><span class="sxs-lookup"><span data-stu-id="c35f8-104">[*Transportable shadow copies*](vssgloss-t.md) can be used to facilitate a *fast recovery*.</span></span>

<span data-ttu-id="c35f8-105">Il ripristino rapido può essere usato per ripristinare rapidamente una copia shadow precedente.</span><span class="sxs-lookup"><span data-stu-id="c35f8-105">Fast recovery can be used to quickly revert to an earlier shadow copy.</span></span> <span data-ttu-id="c35f8-106">I passaggi necessari sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c35f8-106">The steps involved are:</span></span>

1.  <span data-ttu-id="c35f8-107">Creare la copia shadow trasportabile dei LUN appropriati.</span><span class="sxs-lookup"><span data-stu-id="c35f8-107">Create the transportable shadow copy of the appropriate LUNs.</span></span> <span data-ttu-id="c35f8-108">La copia shadow può essere [*persistente*](vssgloss-p.md) o non permanente.</span><span class="sxs-lookup"><span data-stu-id="c35f8-108">The shadow copy can be either [*persistent*](vssgloss-p.md) or nonpersistent.</span></span>
2.  <span data-ttu-id="c35f8-109">Rimuovere i LUN originali</span><span class="sxs-lookup"><span data-stu-id="c35f8-109">Remove the original LUNs</span></span>
    1.  <span data-ttu-id="c35f8-110">Se il computer si trova all'interno di un cluster, contrassegnare le risorse disco interessate come offline o abilitare la [modalità di manutenzione](/previous-versions/windows/desktop/mscs/maintaining-physical-disk-resources) per queste risorse disco.</span><span class="sxs-lookup"><span data-stu-id="c35f8-110">If the computer is inside a cluster, mark the affected disk resources as offline, or enable the [maintenance mode](/previous-versions/windows/desktop/mscs/maintaining-physical-disk-resources) for these disk resources.</span></span>
    2.  <span data-ttu-id="c35f8-111">Mascherare i LUN interessati dal computer (e tutti gli altri nodi se il computer si trova in un cluster).</span><span class="sxs-lookup"><span data-stu-id="c35f8-111">Mask the affected LUNs from this computer (and all other nodes if the computer is in a cluster).</span></span>
3.  <span data-ttu-id="c35f8-112">Importare la copia shadow usando il metodo [**IVssBackupComponents:: ImportSnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-importsnapshots) .</span><span class="sxs-lookup"><span data-stu-id="c35f8-112">Import the shadow copy using the [**IVssBackupComponents::ImportSnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-importsnapshots) method.</span></span>
4.  <span data-ttu-id="c35f8-113">Suddividere la copia shadow usando il metodo [**IVssBackupComponents:: BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) .</span><span class="sxs-lookup"><span data-stu-id="c35f8-113">Break the shadow copy using the [**IVssBackupComponents::BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) method.</span></span>
5.  <span data-ttu-id="c35f8-114">Contrassegnare i nuovi volumi di copia shadow come di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="c35f8-114">Mark the new shadow copy volumes as read/write.</span></span>
6.  <span data-ttu-id="c35f8-115">Se il computer si trova in un cluster, esporre i nuovi LUN delle copie shadow come lun originali.</span><span class="sxs-lookup"><span data-stu-id="c35f8-115">If the computer is in a cluster, expose the new shadow copy LUNs as the original LUNs.</span></span>
    1.  <span data-ttu-id="c35f8-116">Annullare il mascheramento dei lun delle copie shadow negli altri nodi del cluster.</span><span class="sxs-lookup"><span data-stu-id="c35f8-116">Unmask the shadow copy LUNs to the other nodes in the cluster.</span></span>
    2.  <span data-ttu-id="c35f8-117">Contrassegnare le risorse contrassegnate in precedenza come offline come online o disabilitare la modalità di manutenzione per tali risorse disco.</span><span class="sxs-lookup"><span data-stu-id="c35f8-117">Mark the resources that were previously marked as offline as online, or disable the maintenance mode for those disk resources.</span></span>

> [!Note]  
> <span data-ttu-id="c35f8-118">Le copie shadow trasportabili in un cluster non sono supportate prima di Windows Server 2003 con Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="c35f8-118">Transportable shadow copies in a cluster are not supported before Windows Server 2003 with Service Pack 1 (SP1).</span></span> <span data-ttu-id="c35f8-119">Questa operazione è supportata solo con i LUN conformi, che hanno almeno una pagina di dati del prodotto SCSI Vital (Vital) 0x83 \_ identificatore di archiviazione di tipo 1, 2 o 8 e associazione 0 e i LUN devono mantenere un disco di base con il partizionamento MBR.</span><span class="sxs-lookup"><span data-stu-id="c35f8-119">This is only supported with compliant LUNs, which have at least one SCSI Vital Product Data (VPD) page 0x83 STORAGE\_IDENTIFIER of type 1,2, or 8, and association 0, and the LUNs must maintain a basic disk with MBR partitioning.</span></span>

 

 

 
