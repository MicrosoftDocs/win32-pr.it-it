---
description: Oggetto Pack
ms.assetid: e84a05a0-ea12-4bc1-83e1-1eb0dd291dc9
title: Oggetto Pack
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02b01978747df5ccc273a31ae2f516b35c01df96
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "104554701"
---
# <a name="pack-object"></a>Oggetto Pack

\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un oggetto Pack modella un gruppo di dischi, una raccolta di dischi e volumi gestiti dal provider di software di base o dinamico. Un provider può contenere più oggetti Pack.

Usando l'API, le applicazioni possono indirizzare VDS per aggiungere uno o più dischi a un pacchetto, associare i dischi ai volumi e, facoltativamente, spostare i dischi come unità tra gli host. Non è possibile importare un volume esistente in un pacchetto.

> [!Note]  
> L'appartenenza a un pacchetto non implica la coerenza tra i dischi per quanto riguarda le prestazioni, i supporti, il protocollo di interconnessione o altre caratteristiche.

 

Gli oggetti disco non sono allocati e gestiti da VDS oppure sono membri di un unico pacchetto. Il provider di software di base può avere zero o più pacchetti, ognuno dei quali contiene un singolo disco di base. Il provider non impone alcun limite al numero di volumi su un disco di base. Il provider dinamico può avere zero o più pacchetti con più dischi dinamici in ogni pacchetto. Questo provider limita il numero di volumi su un disco, in base alle dimensioni di un megabyte del database di gestione dischi logici (LDM). Dato che un volume include almeno un plex e un extent del disco, il numero massimo di volumi per un pacchetto è approssimativamente 1000. Il numero massimo diminuisce con l'aumentare del numero di dischi.

Oltre agli oggetti disco, un pacchetto può contenere uno o più oggetti LUN implementati da uno o più provider hardware. Al kernel di Windows, un LUN è semplicemente un altro disco. È necessario annullare il mascheramento degli oggetti LUN nel computer in cui è in esecuzione il programma del provider. Quando il disco è un LUN, l'oggetto LUN espone entrambe le interfacce [**IVdsLun**](/windows/desktop/api/Vds/nn-vds-ivdslun) e [**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk) . Un oggetto Pack Usa **IVdsDisk**, anziché **IVdsLun**, per enumerare i LUN in un pacchetto. Per una descrizione più dettagliata di un LUN, vedere l' [oggetto lun](lun-object.md).

La figura seguente mostra un pacchetto con due membri: un disco e un LUN. Un'applicazione può aggiungere questi oggetti a un pacchetto online e creare un volume dal disco sottostante e gli extent di unità rappresentati dagli assi.

![Diagramma che mostra un "Pack" con un disco e un LUN aggiunto da un'applicazione per creare un volume rappresentato da un'unità e da un "mandrino".](images/vdsdisksareluns.png)

Usare il metodo [**IVdsSwProvider:: CreatePack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) per creare un nuovo oggetto Pack. I chiamanti possono ottenere un puntatore a un pacchetto specifico selezionando l'oggetto Pack desiderato dall'enumerazione restituita dal metodo [**IVdsSwProvider:: QueryPacks**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-querypacks) . Con un oggetto Pack è possibile aggiungere, rimuovere o sostituire i membri di un pacchetto. Quando si aggiunge un oggetto disco a un pacchetto, VDS Inizializza un disco per annullare l'associazione di tutti i volumi esistenti. Al contrario, un LUN mantiene tutti i dettagli dell'associazione quando viene aggiunto a un pacchetto. Se si rimuove l'ultimo disco da un pacchetto, VDS Elimina l'oggetto Pack quando il chiamante rilascia l'ultimo riferimento all'oggetto.

Le proprietà dell'oggetto includono un identificatore di oggetto, un nome, lo stato di un pacchetto e i flag. Un pacchetto online è disponibile per la configurazione e l'uso, un pacchetto offline non è disponibile. VDS supporta un numero qualsiasi di pacchetti online e offline.

**Windows Server 2003:** Supporta un solo pacchetto online alla volta.

VDS impone un quorum di dischi online all'interno di un pacchetto. Il quorum determina se un pacchetto può avere uno stato online e impedisce a più host di concedere uno stato online allo stesso pacchetto. Se il numero di dischi online in un pacchetto scende al di sotto del quorum (n/2 + 1), VDS porta offline il pacchetto online.

Nella tabella seguente sono elencate le interfacce, le enumerazioni e le strutture correlate.



| Tipo                                              | Elemento                                                                                                |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| Interfacce sempre esposte da questo oggetto | [**IVdsPack**](/windows/desktop/api/Vds/nn-vds-ivdspack) e [**IVdsPack2**](/windows/desktop/api/Vds/nn-vds-ivdspack2) \* .                                     |
| Enumerazioni associate                           | [**VDS \_ Stato del \_ flag Pack**](/windows/desktop/api/Vds/ne-vds-vds_pack_flag) e del [**\_ pacchetto \_ VDS**](/windows/desktop/api/Vds/ne-vds-vds_pack_status).             |
| Strutture associate                             | [**VDS \_ Notifica Pack \_ prop**](/windows/desktop/api/Vds/ns-vds-vds_pack_prop) e [**VDS \_ \_ Pack**](/windows/desktop/api/Vds/ns-vds-vds_pack_notification). |



 

**\* Windows Server 2003:** questa interfaccia non è supportata fino a Windows Vista.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetti provider di software](software-provider-objects.md)
</dt> <dt>

[LUN (oggetto)](lun-object.md)
</dt> <dt>

[**IVdsLun**](/windows/desktop/api/Vds/nn-vds-ivdslun)
</dt> <dt>

[**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk)
</dt> </dl>

 

 
