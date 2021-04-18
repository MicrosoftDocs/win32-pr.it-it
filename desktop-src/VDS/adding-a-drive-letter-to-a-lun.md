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
# <a name="adding-a-drive-letter-to-a-lun"></a>Aggiunta di una lettera di unità a un LUN

\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

È possibile assegnare direttamente le lettere di unità agli oggetti volume; Tuttavia, se il disco è un oggetto LUN, sono necessari alcuni passaggi aggiuntivi.

**Per assegnare una lettera di unità a un oggetto LUN**

1.  Se necessario, annullare il mascheramento del LUN nell'host locale.
    > [!Note]  
    > Non è possibile eseguire operazioni amministrative del software su un oggetto LUN di cui è stato annullato il mascheramento in un altro computer all'interno della sessione VDS corrente.

     

2.  Richiamare il metodo [**IVdsService:: Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) nel computer in cui è in esecuzione il provider hardware.
3.  Inizializzare il LUN come disco di base, come indicato di seguito:
    1.  Richiamare il metodo [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sull'oggetto lun per eseguire una query per l'interfaccia [**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk) .
    2.  Richiamare il metodo [**IVdsSwProvider:: CreatePack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) per creare un pacchetto di base.
    3.  Richiamare il metodo [**IVdsPack:: AddDisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) per aggiungere il disco al nuovo pacchetto.
4.  Creare una partizione sul disco e ottenere l'oggetto volume come indicato di seguito:
    1.  Richiamare il metodo [**IVdsCreatePartitionEx:: CreatePartitionEx**](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex) per creare una partizione.
    2.  Richiamare il metodo [**IVdsAsync:: wait**](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait) sull'oggetto asincrono restituito da [**CreatePartitionEx**](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex) per ottenere l'identificatore di volume dalla struttura di [**\_ \_ output Async di VDS**](/windows/desktop/api/Vds/ns-vds-vds_async_output) .
    3.  Passare l'identificatore del volume come parametro al metodo [**IVdsService:: GetObject**](/windows/desktop/api/Vds/nf-vds-ivdsservice-getobject) per ottenere un puntatore all'oggetto volume.
5.  Richiamare il metodo [**IVdsVolumeMF:: AddAccessPath**](/windows/desktop/api/Vds/nf-vds-ivdsvolumemf-addaccesspath) per assegnare la lettera di unità.

> [!Note]  
> Il metodo [**IVdsAdvancedDisk:: AssignDriveLetter**](/windows/desktop/api/Vds/nf-vds-ivdsadvanceddisk-assigndriveletter) assegna lettere di unità alle partizioni senza volumi associati, ad esempio partizioni OEM o ESP. Non è possibile usarlo per assegnare una lettera di unità a un oggetto LUN.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di VDS](using-vds.md)
</dt> <dt>

[**IVdsService:: Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate)
</dt> <dt>

[**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk)
</dt> <dt>

[**IVdsSwProvider::CreatePack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack)
</dt> <dt>

[**IVdsPack::AddDisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk)
</dt> <dt>

[**IVdsCreatePartitionEx::CreatePartitionEx**](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex)
</dt> <dt>

[**IVdsAsync:: wait**](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait)
</dt> <dt>

[**\_output asincrono \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_async_output)
</dt> <dt>

[**IVdsVolumeMF::AddAccessPath**](/windows/desktop/api/Vds/nf-vds-ivdsvolumemf-addaccesspath)
</dt> <dt>

[**IVdsAdvancedDisk::AssignDriveLetter**](/windows/desktop/api/Vds/nf-vds-ivdsadvanceddisk-assigndriveletter)
</dt> </dl>

 

 
