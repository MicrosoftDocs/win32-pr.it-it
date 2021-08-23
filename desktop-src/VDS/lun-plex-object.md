---
description: Oggetto LUN Plex
ms.assetid: db6eabaa-1b84-4613-ab2a-8d5904305e08
title: Oggetto LUN Plex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df52b60bcbd23269d766435749b40b8c636361390359182a38a695ab6252a27f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999442"
---
# <a name="lun-plex-object"></a>Oggetto LUN Plex

\[A partire Windows 8 e Windows Server 2012, l'interfaccia [COM](virtual-disk-service-portal.md) del servizio disco virtuale viene sostituita dal Windows Archiviazione API Gestione [.](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)\]

Un oggetto lun plex modella un plex LUN contenuto in un LUN. Solo un LUN con mirroring può avere più plex. tutti gli altri tipi di LUN hanno un plex. Ogni plex contiene una copia dei dati nel LUN. È possibile aggiungere nuovi plex a un LUN e, ad eccezione del plex originale, è possibile rimuovere iplex esistenti. VDS supporta quattro tipi di lun plex: semplice, con spanning, con striped e strip con parità. Per una descrizione di ognuno di questi tipi di LUN, vedere l'oggetto [LUN](lun-object.md).

Usare il [**metodo IVdsLun::AddPlex**](/windows/desktop/api/Vds/nf-vds-ivdslun-addplex) per aggiungere un plex a un LUN e il metodo [**IVdsLun::RemovePlex**](/windows/desktop/api/Vds/nf-vds-ivdslun-removeplex) per eliminare il plex. È possibile eseguire una query per i plex LUN richiamando il [**metodo IVdsLun::QueryPlexes.**](/windows/desktop/api/Vds/nf-vds-ivdslun-queryplexes) È possibile ottenere un puntatore a un plex LUN specifico selezionando l'oggetto plex desiderato dall'enumerazione restituita dal **metodo QueryPlexes.** Con un oggetto plex, è possibile eseguire una query per gli extent di unità e gli hint automagic e applicare nuovi hint.

Oltre a un identificatore di oggetto, un nome e un numero di serie, le proprietà dell'oggetto plex LUN includono il tipo plex, le dimensioni, lo stato, l'integrità, lo stato di transizione e i flag. un elenco di annullamento del mascheramento e le dimensioni di striping; e un'impostazione di priorità di ricompilazione.

Nella tabella seguente sono elencate le interfacce, le enumerazioni e le strutture correlate.



| Tipo                                              | Elemento                                                                                                                                                          |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce sempre esposte da questo oggetto | [**IVdsLunPlex**](/windows/desktop/api/Vds/nn-vds-ivdslunplex).                                                                                                                              |
| Enumerazioni associate                           | [**VDS \_ LUN \_ PLEX \_ FLAG,**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_flag) [**VDS \_ LUN \_ PLEX \_ STATUS**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_status)E [**VDS LUN \_ \_ PLEX \_ TYPE**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_type). |
| Strutture associate                             | [**VDS \_ LUN \_ PLEX \_ PROP**](/windows/desktop/api/Vds/ns-vds-vds_lun_plex_prop).                                                                                                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetti provider hardware](hardware-provider-objects.md)
</dt> <dt>

[Oggetto LUN](lun-object.md)
</dt> </dl>

 

 
