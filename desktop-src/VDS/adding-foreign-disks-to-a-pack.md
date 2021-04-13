---
description: Aggiunta di dischi esterni a un pacchetto
ms.assetid: 4018c742-1d23-47b9-a787-69bf8847b54a
title: Aggiunta di dischi esterni a un pacchetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fbfa2ff3d00857fd4e1b92e78f1760c25ce516b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349281"
---
# <a name="adding-foreign-disks-to-a-pack"></a><span data-ttu-id="248b9-103">Aggiunta di dischi esterni a un pacchetto</span><span class="sxs-lookup"><span data-stu-id="248b9-103">Adding Foreign Disks to a Pack</span></span>

<span data-ttu-id="248b9-104">\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="248b9-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="248b9-105">In genere, un disco esterno è un disco dinamico allocato in un computer e spostato fisicamente in un altro computer.</span><span class="sxs-lookup"><span data-stu-id="248b9-105">Most commonly, a foreign disk is a dynamic disk that is allocated on one computer and physically moved to another computer.</span></span> <span data-ttu-id="248b9-106">Tuttavia, qualsiasi disco che appartiene a un pacchetto diverso dal pacchetto online viene considerato un disco esterno che appartiene a un disco Pack esterno.</span><span class="sxs-lookup"><span data-stu-id="248b9-106">However, any disk that belongs to a pack other than the online pack is considered to be a foreign disk that belongs to a foreign disk pack.</span></span>

<span data-ttu-id="248b9-107">Un pacchetto esterno dispone del flag di **\_ PKF \_ esterno VDS** impostato nel membro **ulFlags** della struttura [**della \_ \_ prop del pacchetto VDS**](/windows/desktop/api/Vds/ns-vds-vds_pack_prop) .</span><span class="sxs-lookup"><span data-stu-id="248b9-107">A foreign pack has the **VDS\_PKF\_FOREIGN** flag set in the **ulFlags** member of the [**VDS\_PACK\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_pack_prop) structure.</span></span> <span data-ttu-id="248b9-108">I pacchetti stranieri sono sempre offline.</span><span class="sxs-lookup"><span data-stu-id="248b9-108">Foreign packs are always offline.</span></span>

<span data-ttu-id="248b9-109">Nella procedura seguente viene descritto come importare uno o più dischi esterni.</span><span class="sxs-lookup"><span data-stu-id="248b9-109">The following procedure describes how to import one or more foreign disks.</span></span>

<span data-ttu-id="248b9-110">**Per importare uno o più dischi esterni**</span><span class="sxs-lookup"><span data-stu-id="248b9-110">**To import one or more foreign disks**</span></span>

1.  <span data-ttu-id="248b9-111">Spostare i dischi nel nuovo computer.</span><span class="sxs-lookup"><span data-stu-id="248b9-111">Move disks to the new computer.</span></span>
2.  <span data-ttu-id="248b9-112">Nel nuovo computer usare il metodo [**IVdsService:: Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) per installare i dischi esterni.</span><span class="sxs-lookup"><span data-stu-id="248b9-112">On the new computer, use the [**IVdsService::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) method to install the foreign disks.</span></span>
3.  <span data-ttu-id="248b9-113">Selezionare il pacchetto online come pacchetto di destinazione che riceve i dischi esterni.</span><span class="sxs-lookup"><span data-stu-id="248b9-113">Select the online pack to be the target pack that receives the foreign disks.</span></span> <span data-ttu-id="248b9-114">Se non esiste alcun pacchetto online, usare il metodo [**IVdsSwProvider:: CreatePack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) per creare un nuovo pacchetto vuoto.</span><span class="sxs-lookup"><span data-stu-id="248b9-114">If no online pack exists, use the [**IVdsSwProvider::CreatePack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) method to create a new empty pack.</span></span>
4.  <span data-ttu-id="248b9-115">Usare il metodo [**IVdsPack:: MigrateDisks**](/windows/desktop/api/Vds/nf-vds-ivdspack-migratedisks) per importare i dischi nel nuovo Dynamic Pack.</span><span class="sxs-lookup"><span data-stu-id="248b9-115">Use the [**IVdsPack::MigrateDisks**](/windows/desktop/api/Vds/nf-vds-ivdspack-migratedisks) method to import the disks to the new dynamic pack.</span></span>
5.  <span data-ttu-id="248b9-116">Usare il metodo [**IVdsSwProvider:: QueryPacks**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-querypacks) per enumerare i pacchetti e [**IVdsPack:: GetProperties**](/windows/desktop/api/Vds/nf-vds-ivdspack-getproperties) per determinare quale Pack è ora il pacchetto online.</span><span class="sxs-lookup"><span data-stu-id="248b9-116">Use the [**IVdsSwProvider::QueryPacks**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-querypacks) method to enumerate the packs and [**IVdsPack::GetProperties**](/windows/desktop/api/Vds/nf-vds-ivdspack-getproperties) to determine which pack is now the online pack.</span></span>

<span data-ttu-id="248b9-117">Se si crea un nuovo pacchetto di destinazione vuoto, non viene effettivamente eseguita la migrazione dei dischi esterni a tale pacchetto.</span><span class="sxs-lookup"><span data-stu-id="248b9-117">If you create a new empty target pack, the foreign disks are not actually migrated to that pack.</span></span> <span data-ttu-id="248b9-118">Al contrario, il pacchetto esterno è contrassegnato come online, il flag **\_ \_ esterno PKF VDS** per il pacchetto viene cancellato (quindi il pacchetto non è più esterno) e il pacchetto di destinazione creato viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="248b9-118">Instead, the foreign pack is marked online, the **VDS\_PKF\_FOREIGN** flag for the pack is cleared (so the pack is no longer foreign), and the target pack that you created is discarded.</span></span>

> [!Note]  
> <span data-ttu-id="248b9-119">Usare il metodo [**IVdsPack:: AddDisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) per aggiungere dischi non allocati, ovvero dischi non richiesti da un provider, a un pacchetto.</span><span class="sxs-lookup"><span data-stu-id="248b9-119">Use the [**IVdsPack::AddDisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) method to add unallocated disks—disks not claimed by a provider—to a pack.</span></span> <span data-ttu-id="248b9-120">Un disco non allocato non può essere esterno.</span><span class="sxs-lookup"><span data-stu-id="248b9-120">An unallocated disk cannot be foreign.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="248b9-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="248b9-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="248b9-122">Uso di VDS</span><span class="sxs-lookup"><span data-stu-id="248b9-122">Using VDS</span></span>](using-vds.md)
</dt> <dt>

[<span data-ttu-id="248b9-123">**IVdsService:: Reenumerate**</span><span class="sxs-lookup"><span data-stu-id="248b9-123">**IVdsService::Reenumerate**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate)
</dt> <dt>

[<span data-ttu-id="248b9-124">**IVdsSwProvider::CreatePack**</span><span class="sxs-lookup"><span data-stu-id="248b9-124">**IVdsSwProvider::CreatePack**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack)
</dt> <dt>

[<span data-ttu-id="248b9-125">**IVdsPack::MigrateDisks**</span><span class="sxs-lookup"><span data-stu-id="248b9-125">**IVdsPack::MigrateDisks**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdspack-migratedisks)
</dt> <dt>

[<span data-ttu-id="248b9-126">**IVdsPack::AddDisk**</span><span class="sxs-lookup"><span data-stu-id="248b9-126">**IVdsPack::AddDisk**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk)
</dt> </dl>

 

 
