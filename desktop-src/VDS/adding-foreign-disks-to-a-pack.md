---
description: Aggiunta di dischi estere a un pacchetto
ms.assetid: 4018c742-1d23-47b9-a787-69bf8847b54a
title: Aggiunta di dischi estere a un pacchetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26b83dd76cdc3f1637c07d8d9d818fdaf61fb093151f23aea06f0e9c7f81d6a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117755456"
---
# <a name="adding-foreign-disks-to-a-pack"></a>Aggiunta di dischi estere a un pacchetto

\[A partire Windows 8 e Windows Server 2012, l'interfaccia [COM](virtual-disk-service-portal.md) del servizio disco virtuale viene sostituita dal Windows Archiviazione API Gestione [.](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)\]

In genere, un disco esterna è un disco dinamico allocato in un computer e spostato fisicamente in un altro computer. Tuttavia, qualsiasi disco appartenente a un pacchetto diverso da quello online viene considerato un disco esterna appartenente a un pacchetto di dischi esterna.

Per un pacchetto foreign è impostato il flag **\_ FOREIGN di VDS PKF \_** nel membro **ulFlags** della [**struttura VDS PACK \_ \_ PROP.**](/windows/desktop/api/Vds/ns-vds-vds_pack_prop) I Pacchetti estere sono sempre offline.

La procedura seguente descrive come importare uno o più dischi estere.

**Per importare uno o più dischi estere**

1.  Spostare i dischi nel nuovo computer.
2.  Nel nuovo computer usare il [**metodo IVdsService::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) per installare i dischisterici.
3.  Selezionare il pacchetto online come pacchetto di destinazione che riceve i dischi estere. Se non esiste alcun pacchetto online, usare il [**metodo IVdsSwProvider::CreatePack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) per creare un nuovo pacchetto vuoto.
4.  Usare il [**metodo IVdsPack::MigrateDisks**](/windows/desktop/api/Vds/nf-vds-ivdspack-migratedisks) per importare i dischi nel nuovo pacchetto dinamico.
5.  Usare il [**metodo IVdsSwProvider::QueryPacks**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-querypacks) per enumerare i pacchetti e [**IVdsPack::GetProperties**](/windows/desktop/api/Vds/nf-vds-ivdspack-getproperties) per determinare quale pack è ora il pacchetto online.

Se si crea un nuovo pacchetto di destinazione vuoto, non viene effettivamente eseguita la migrazione dei dischi all'insieme. Al contrario, il pacchetto foreign viene contrassegnato come online, il flag **\_ FOREIGN PKF \_ VDS** per il pacchetto viene cancellato (in modo che il pacchetto non sia più estraneo) e il pacchetto di destinazione creato viene eliminato.

> [!Note]  
> Usare il [**metodo IVdsPack::AddDisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) per aggiungere dischi non allocati, ovvero dischi non dichiarati da un provider, a un pacchetto. Un disco non allocato non può essere estraneo.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di VDS](using-vds.md)
</dt> <dt>

[**IVdsService::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate)
</dt> <dt>

[**IVdsSwProvider::CreatePack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack)
</dt> <dt>

[**IVdsPack::MigrateDisks**](/windows/desktop/api/Vds/nf-vds-ivdspack-migratedisks)
</dt> <dt>

[**IVdsPack::AddDisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk)
</dt> </dl>

 

 
