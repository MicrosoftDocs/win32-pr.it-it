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
# <a name="adding-foreign-disks-to-a-pack"></a>Aggiunta di dischi esterni a un pacchetto

\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

In genere, un disco esterno è un disco dinamico allocato in un computer e spostato fisicamente in un altro computer. Tuttavia, qualsiasi disco che appartiene a un pacchetto diverso dal pacchetto online viene considerato un disco esterno che appartiene a un disco Pack esterno.

Un pacchetto esterno dispone del flag di **\_ PKF \_ esterno VDS** impostato nel membro **ulFlags** della struttura [**della \_ \_ prop del pacchetto VDS**](/windows/desktop/api/Vds/ns-vds-vds_pack_prop) . I pacchetti stranieri sono sempre offline.

Nella procedura seguente viene descritto come importare uno o più dischi esterni.

**Per importare uno o più dischi esterni**

1.  Spostare i dischi nel nuovo computer.
2.  Nel nuovo computer usare il metodo [**IVdsService:: Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) per installare i dischi esterni.
3.  Selezionare il pacchetto online come pacchetto di destinazione che riceve i dischi esterni. Se non esiste alcun pacchetto online, usare il metodo [**IVdsSwProvider:: CreatePack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) per creare un nuovo pacchetto vuoto.
4.  Usare il metodo [**IVdsPack:: MigrateDisks**](/windows/desktop/api/Vds/nf-vds-ivdspack-migratedisks) per importare i dischi nel nuovo Dynamic Pack.
5.  Usare il metodo [**IVdsSwProvider:: QueryPacks**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-querypacks) per enumerare i pacchetti e [**IVdsPack:: GetProperties**](/windows/desktop/api/Vds/nf-vds-ivdspack-getproperties) per determinare quale Pack è ora il pacchetto online.

Se si crea un nuovo pacchetto di destinazione vuoto, non viene effettivamente eseguita la migrazione dei dischi esterni a tale pacchetto. Al contrario, il pacchetto esterno è contrassegnato come online, il flag **\_ \_ esterno PKF VDS** per il pacchetto viene cancellato (quindi il pacchetto non è più esterno) e il pacchetto di destinazione creato viene ignorato.

> [!Note]  
> Usare il metodo [**IVdsPack:: AddDisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) per aggiungere dischi non allocati, ovvero dischi non richiesti da un provider, a un pacchetto. Un disco non allocato non può essere esterno.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di VDS](using-vds.md)
</dt> <dt>

[**IVdsService:: Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate)
</dt> <dt>

[**IVdsSwProvider::CreatePack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack)
</dt> <dt>

[**IVdsPack::MigrateDisks**](/windows/desktop/api/Vds/nf-vds-ivdspack-migratedisks)
</dt> <dt>

[**IVdsPack::AddDisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk)
</dt> </dl>

 

 
