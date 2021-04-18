---
description: Oggetto PLEX LUN
ms.assetid: db6eabaa-1b84-4613-ab2a-8d5904305e08
title: Oggetto PLEX LUN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f1b51657ccbfc0f1bd3d73e54128cac3f0b507c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318596"
---
# <a name="lun-plex-object"></a>Oggetto PLEX LUN

\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un oggetto PLEX LUN modella un PLEX LUN contenuto in un LUN. Solo un LUN con mirroring può avere più Plex; tutti gli altri tipi LUN hanno un plex. Ogni plex contiene una copia dei dati nel LUN. È possibile aggiungere nuovi Plex a un LUN e, ad eccezione del Plex originale, i plex esistenti possono essere rimossi. VDS supporta quattro tipi di PLEX LUN: semplici, con spanning, con striping e con striping con parità. Per una descrizione di ognuno di questi tipi LUN, vedere l' [oggetto lun](lun-object.md).

Usare il metodo [**IVdsLun:: AddPlex**](/windows/desktop/api/Vds/nf-vds-ivdslun-addplex) per aggiungere un plex a un LUN e il metodo [**IVdsLun:: RemovePlex**](/windows/desktop/api/Vds/nf-vds-ivdslun-removeplex) per eliminare il plex. È possibile eseguire una query per i PLEX LUN richiamando il metodo [**IVdsLun:: QueryPlexes**](/windows/desktop/api/Vds/nf-vds-ivdslun-queryplexes) . È possibile ottenere un puntatore a un PLEX LUN specifico selezionando l'oggetto Plex desiderato dall'enumerazione restituita dal metodo **QueryPlexes** . Con un oggetto Plex è possibile eseguire una query per gli extent delle unità e i suggerimenti di automagic e applicare nuovi hint.

Oltre a un identificatore di oggetto, un nome e un numero di serie, le proprietà dell'oggetto LUN Plex includono il tipo di Plex, le dimensioni, lo stato, l'integrità, lo stato di transizione e i flag. elenco e dimensioni di striping senza maschera; e un'impostazione della priorità di ricompilazione.

Nella tabella seguente sono elencate le interfacce, le enumerazioni e le strutture correlate.



| Tipo                                              | Elemento                                                                                                                                                          |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce sempre esposte da questo oggetto | [**IVdsLunPlex**](/windows/desktop/api/Vds/nn-vds-ivdslunplex).                                                                                                                              |
| Enumerazioni associate                           | [**VDS \_ LUN \_ Plex \_ flag**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_flag), [**VDS \_ lun \_ Plex \_ status**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_status)e [**VDS \_ lun \_ Plex \_ Type**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_type). |
| Strutture associate                             | [**VDS \_ \_ \_ prop Plex di lun**](/windows/desktop/api/Vds/ns-vds-vds_lun_plex_prop).                                                                                                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetti provider hardware](hardware-provider-objects.md)
</dt> <dt>

[LUN (oggetto)](lun-object.md)
</dt> </dl>

 

 
