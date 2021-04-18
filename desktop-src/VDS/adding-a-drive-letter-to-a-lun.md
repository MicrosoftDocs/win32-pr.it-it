---
description: Aggiunta di una lettera di unità a un LUN
ms.assetid: 3f350312-3f1f-4020-90d0-85521ea9c7c8
title: Aggiunta di una lettera di unità a un LUN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 426a4f3bf720b21a02462edde4a381012d2084d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306515"
---
# <a name="adding-a-drive-letter-to-a-lun"></a><span data-ttu-id="2633c-103">Aggiunta di una lettera di unità a un LUN</span><span class="sxs-lookup"><span data-stu-id="2633c-103">Adding a Drive Letter to a LUN</span></span>

<span data-ttu-id="2633c-104">\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2633c-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="2633c-105">È possibile assegnare direttamente le lettere di unità agli oggetti volume; Tuttavia, se il disco è un oggetto LUN, sono necessari alcuni passaggi aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="2633c-105">You can assign drive letters to volume objects directly; however, if your disk is a LUN object, you have a few additional steps.</span></span>

<span data-ttu-id="2633c-106">**Per assegnare una lettera di unità a un oggetto LUN**</span><span class="sxs-lookup"><span data-stu-id="2633c-106">**To assign a drive letter to a LUN object**</span></span>

1.  <span data-ttu-id="2633c-107">Se necessario, annullare il mascheramento del LUN nell'host locale.</span><span class="sxs-lookup"><span data-stu-id="2633c-107">If necessary, unmask the LUN to the local host.</span></span>
    > [!Note]  
    > <span data-ttu-id="2633c-108">Non è possibile eseguire operazioni amministrative del software su un oggetto LUN di cui è stato annullato il mascheramento in un altro computer all'interno della sessione VDS corrente.</span><span class="sxs-lookup"><span data-stu-id="2633c-108">You cannot perform software administrative operations on a LUN object that is unmasked to another computer within the current VDS session.</span></span>

     

2.  <span data-ttu-id="2633c-109">Richiamare il metodo [**IVdsService:: Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) nel computer in cui è in esecuzione il provider hardware.</span><span class="sxs-lookup"><span data-stu-id="2633c-109">Invoke the [**IVdsService::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) method on the computer that is running the hardware provider.</span></span>
3.  <span data-ttu-id="2633c-110">Inizializzare il LUN come disco di base, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="2633c-110">Initialize the LUN as a basic disk as follows:</span></span>
    1.  <span data-ttu-id="2633c-111">Richiamare il metodo [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sull'oggetto lun per eseguire una query per l'interfaccia [**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk) .</span><span class="sxs-lookup"><span data-stu-id="2633c-111">Invoke the [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method on the LUN object to query for the [**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk) interface.</span></span>
    2.  <span data-ttu-id="2633c-112">Richiamare il metodo [**IVdsSwProvider:: CreatePack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) per creare un pacchetto di base.</span><span class="sxs-lookup"><span data-stu-id="2633c-112">Invoke the [**IVdsSwProvider::CreatePack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) method to create a basic pack.</span></span>
    3.  <span data-ttu-id="2633c-113">Richiamare il metodo [**IVdsPack:: AddDisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) per aggiungere il disco al nuovo pacchetto.</span><span class="sxs-lookup"><span data-stu-id="2633c-113">Invoke the [**IVdsPack::AddDisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) method to add the disk to the new pack.</span></span>
4.  <span data-ttu-id="2633c-114">Creare una partizione sul disco e ottenere l'oggetto volume come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="2633c-114">Create a partition on the disk and obtain the volume object as follows:</span></span>
    1.  <span data-ttu-id="2633c-115">Richiamare il metodo [**IVdsCreatePartitionEx:: CreatePartitionEx**](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex) per creare una partizione.</span><span class="sxs-lookup"><span data-stu-id="2633c-115">Invoke the [**IVdsCreatePartitionEx::CreatePartitionEx**](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex) method to create a partition.</span></span>
    2.  <span data-ttu-id="2633c-116">Richiamare il metodo [**IVdsAsync:: wait**](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait) sull'oggetto asincrono restituito da [**CreatePartitionEx**](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex) per ottenere l'identificatore di volume dalla struttura di [**\_ \_ output Async di VDS**](/windows/desktop/api/Vds/ns-vds-vds_async_output) .</span><span class="sxs-lookup"><span data-stu-id="2633c-116">Invoke the [**IVdsAsync::Wait**](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait) method on the async object that is returned by [**CreatePartitionEx**](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex) to get the volume identifier from the [**VDS\_ASYNC\_OUTPUT**](/windows/desktop/api/Vds/ns-vds-vds_async_output) structure.</span></span>
    3.  <span data-ttu-id="2633c-117">Passare l'identificatore del volume come parametro al metodo [**IVdsService:: GetObject**](/windows/desktop/api/Vds/nf-vds-ivdsservice-getobject) per ottenere un puntatore all'oggetto volume.</span><span class="sxs-lookup"><span data-stu-id="2633c-117">Pass the volume identifier as a parameter to the [**IVdsService::GetObject**](/windows/desktop/api/Vds/nf-vds-ivdsservice-getobject) method to get a volume object pointer.</span></span>
5.  <span data-ttu-id="2633c-118">Richiamare il metodo [**IVdsVolumeMF:: AddAccessPath**](/windows/desktop/api/Vds/nf-vds-ivdsvolumemf-addaccesspath) per assegnare la lettera di unità.</span><span class="sxs-lookup"><span data-stu-id="2633c-118">Invoke the [**IVdsVolumeMF::AddAccessPath**](/windows/desktop/api/Vds/nf-vds-ivdsvolumemf-addaccesspath) method to assign the drive letter.</span></span>

> [!Note]  
> <span data-ttu-id="2633c-119">Il metodo [**IVdsAdvancedDisk:: AssignDriveLetter**](/windows/desktop/api/Vds/nf-vds-ivdsadvanceddisk-assigndriveletter) assegna lettere di unità alle partizioni senza volumi associati, ad esempio partizioni OEM o ESP.</span><span class="sxs-lookup"><span data-stu-id="2633c-119">The [**IVdsAdvancedDisk::AssignDriveLetter**](/windows/desktop/api/Vds/nf-vds-ivdsadvanceddisk-assigndriveletter) method assigns drive letters to partitions without associated volumes, such as OEM or ESP partitions.</span></span> <span data-ttu-id="2633c-120">Non è possibile usarlo per assegnare una lettera di unità a un oggetto LUN.</span><span class="sxs-lookup"><span data-stu-id="2633c-120">You cannot use it to assign a drive letter to a LUN object.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="2633c-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2633c-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2633c-122">Uso di VDS</span><span class="sxs-lookup"><span data-stu-id="2633c-122">Using VDS</span></span>](using-vds.md)
</dt> <dt>

[<span data-ttu-id="2633c-123">**IVdsService:: Reenumerate**</span><span class="sxs-lookup"><span data-stu-id="2633c-123">**IVdsService::Reenumerate**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate)
</dt> <dt>

[<span data-ttu-id="2633c-124">**IVdsDisk**</span><span class="sxs-lookup"><span data-stu-id="2633c-124">**IVdsDisk**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsdisk)
</dt> <dt>

[<span data-ttu-id="2633c-125">**IVdsSwProvider::CreatePack**</span><span class="sxs-lookup"><span data-stu-id="2633c-125">**IVdsSwProvider::CreatePack**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack)
</dt> <dt>

[<span data-ttu-id="2633c-126">**IVdsPack::AddDisk**</span><span class="sxs-lookup"><span data-stu-id="2633c-126">**IVdsPack::AddDisk**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk)
</dt> <dt>

[<span data-ttu-id="2633c-127">**IVdsCreatePartitionEx::CreatePartitionEx**</span><span class="sxs-lookup"><span data-stu-id="2633c-127">**IVdsCreatePartitionEx::CreatePartitionEx**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex)
</dt> <dt>

[<span data-ttu-id="2633c-128">**IVdsAsync:: wait**</span><span class="sxs-lookup"><span data-stu-id="2633c-128">**IVdsAsync::Wait**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait)
</dt> <dt>

[<span data-ttu-id="2633c-129">**\_output asincrono \_ VDS**</span><span class="sxs-lookup"><span data-stu-id="2633c-129">**VDS\_ASYNC\_OUTPUT**</span></span>](/windows/desktop/api/Vds/ns-vds-vds_async_output)
</dt> <dt>

[<span data-ttu-id="2633c-130">**IVdsVolumeMF::AddAccessPath**</span><span class="sxs-lookup"><span data-stu-id="2633c-130">**IVdsVolumeMF::AddAccessPath**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsvolumemf-addaccesspath)
</dt> <dt>

[<span data-ttu-id="2633c-131">**IVdsAdvancedDisk::AssignDriveLetter**</span><span class="sxs-lookup"><span data-stu-id="2633c-131">**IVdsAdvancedDisk::AssignDriveLetter**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsadvanceddisk-assigndriveletter)
</dt> </dl>

 

 
