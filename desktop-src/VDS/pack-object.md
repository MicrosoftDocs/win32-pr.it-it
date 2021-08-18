---
description: Oggetto Pack
ms.assetid: e84a05a0-ea12-4bc1-83e1-1eb0dd291dc9
title: Oggetto Pack
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaa8c565c45b802258b9d8b9955a2d28adc13c73c989805ce6b2663bc3006d7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058025"
---
# <a name="pack-object"></a>Oggetto Pack

\[A partire da Windows 8 e Windows Server 2012, l'interfaccia [COM](virtual-disk-service-portal.md) del servizio dischi virtuali viene sostituita dal Windows Archiviazione API Gestione [.](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)\]

Un pacchetto a oggetti modella un gruppo di dischi, una raccolta di dischi e volumi gestiti dal provider software di base o dinamico. Un provider può contenere più oggetti pack.

Usando l'API, le applicazioni possono indirizzare VDS per aggiungere uno o più dischi a un pacchetto, associare i dischi in volumi e, facoltativamente, spostare i dischi come unità tra host. Non è possibile importare un volume esistente in un pacchetto.

> [!Note]  
> L'appartenenza a un pacchetto non implica coerenza tra i dischi per quanto riguarda le prestazioni, i supporti, il protocollo di interconnessione o altre caratteristiche.

 

Gli oggetti disco sono non allocati e gestiti da VDS o sono membri di esattamente un pacchetto. Il provider software di base può avere zero o più pacchetti, ognuno dei quali contiene un singolo disco di base. Il provider non impone limiti al numero di volumi in un disco di base. Il provider dinamico può avere zero o più pacchetti con più dischi dinamici in ogni pacchetto. Questo provider limita il numero di volumi in un disco, in base alle dimensioni di un megabyte del database di Gestione dischi logici (LDM). Dato che un volume ha almeno un plex e un extent del disco, il numero massimo di volumi per un pacchetto è di circa 1000. Il numero massimo scende quando il numero di dischi sale.

Oltre agli oggetti disco, un pacchetto può contenere uno o più oggetti LUN implementati da uno o più provider hardware. Per il kernel Windows, un LUN è solo un altro disco. Gli oggetti LUN devono essere smascherati nel computer che esegue il programma provider. Quando il disco è un LUN, l'oggetto LUN espone entrambe le interfacce [**IVdsLun**](/windows/desktop/api/Vds/nn-vds-ivdslun) e [**IVdsDisk.**](/windows/desktop/api/Vds/nn-vds-ivdsdisk) Un oggetto pack usa **IVdsDisk** anziché **IVdsLun** per enumerare i LUN in un pacchetto. Per una descrizione più dettagliata di un LUN, vedere l'oggetto [LUN](lun-object.md).

La figura seguente mostra un pacchetto con due membri: un disco e un LUN. Un'applicazione può aggiungere questi oggetti a un pacchetto online e creare un volume dal disco sottostante e dagli extent di unità rappresentati dai mandri.

![Diagramma che mostra un 'Pack' con un disco e un LUN aggiunti da un'applicazione per creare un volume rappresentato da un 'Drive' e da un 'Spindle'.](images/vdsdisksareluns.png)

Usare il [**metodo IVdsSwProvider::CreatePack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) per creare un nuovo oggetto pack. I chiamanti possono ottenere un puntatore a un pacchetto specifico selezionando l'oggetto pack desiderato dall'enumerazione restituita dal [**metodo IVdsSwProvider:: QueryPacks.**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-querypacks) Con un oggetto pack è possibile aggiungere, rimuovere o sostituire i membri di un pacchetto. Quando si aggiunge un oggetto disco a un pacchetto, VDS inizializza un disco per annullare l'associazione di tutti i volumi esistenti. Al contrario, un LUN mantiene tutti i dettagli di associazione quando viene aggiunto a un pacchetto. Se si rimuove l'ultimo disco da un pacchetto, VDS elimina l'oggetto pack quando il chiamante rilascia l'ultimo riferimento all'oggetto.

Le proprietà dell'oggetto includono un identificatore di oggetto, un nome, lo stato del pacchetto e i flag. È disponibile un pacchetto online per la configurazione e l'uso, un pacchetto offline non è disponibile. VDS supporta un numero qualsiasi di pacchetti online e offline.

**Windows Server 2003:** Supporta un solo pacchetto online alla volta.

VDS applica un quorum di dischi online all'interno di un pacchetto. Il quorum determina se un pacchetto può avere uno stato online e impedisce a più host di concedere uno stato online allo stesso pacchetto. Se il numero di dischi online in un pacchetto scende al di sotto del quorum (n/2 + 1), VDS porta offline il pacchetto online.

Nella tabella seguente sono elencate le interfacce, le enumerazioni e le strutture correlate.



| Tipo                                              | Elemento                                                                                                |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| Interfacce sempre esposte da questo oggetto | [**IVdsPack**](/windows/desktop/api/Vds/nn-vds-ivdspack) e [**IVdsPack2**](/windows/desktop/api/Vds/nn-vds-ivdspack2) \* .                                     |
| Enumerazioni associate                           | [**VDS \_ PACK \_ FLAG**](/windows/desktop/api/Vds/ne-vds-vds_pack_flag) e [**VDS PACK \_ \_ STATUS**](/windows/desktop/api/Vds/ne-vds-vds_pack_status).             |
| Strutture associate                             | [**VDS \_ PACK \_ PROP**](/windows/desktop/api/Vds/ns-vds-vds_pack_prop) e [**VDS PACK \_ \_ NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_pack_notification). |



 

**\* Windows Server 2003: questa** interfaccia non è supportata fino a Windows Vista.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetti provider software](software-provider-objects.md)
</dt> <dt>

[Oggetto LUN](lun-object.md)
</dt> <dt>

[**IVdsLun**](/windows/desktop/api/Vds/nn-vds-ivdslun)
</dt> <dt>

[**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk)
</dt> </dl>

 

 
