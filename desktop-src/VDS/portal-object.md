---
description: Oggetto portale
ms.assetid: 6655bbae-07d3-416b-9e45-ddcbe3433f40
title: Oggetto portale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b7004f648b11b16c8c6279a0a74bae775fa539d8f0a93fc83d7effccea68915
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864521"
---
# <a name="portal-object"></a>Oggetto portale

\[A partire da Windows 8 e Windows Server 2012, l'interfaccia [COM](virtual-disk-service-portal.md) del servizio dischi virtuali viene sostituita dal Windows Archiviazione API Gestione [.](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)\]

Un oggetto del portale modella un portale iSCSI contenuto in un sottosistema iSCSI.

Usare il [**metodo IVdsSubSystemIscsi::QueryPortals**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-queryportals) per determinare i portali iSCSI del sottosistema. I chiamanti possono ottenere un puntatore a un portale specifico selezionando l'oggetto portale desiderato dall'enumerazione restituita dal **metodo QueryPortals.** Con un oggetto portale è possibile impostare lo stato del portale ed eseguire query per le proprietà del portale, i gruppi del portale associati e il sottosistema che contiene il portale.

Un oggetto del portale può essere associato al massimo a un gruppo del portale di una destinazione specificata.

I portali fungono da endpoint dei percorsi MPIO nei provider hardware iSCSI, su cui è possibile imporre criteri di bilanciamento del carico.

Le proprietà dell'oggetto del portale includono un identificatore di oggetto, un indirizzo IP e una porta e lo stato del portale.

Nella tabella seguente sono elencate le interfacce, le enumerazioni e le strutture correlate.



| Tipo                                                                                      | Elemento                                                                                                                 |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Interfacce sempre esposte da questo oggetto solo nei provider iSCSI VDS 1.1 e 2.0 | [**IVdsIscsiPortal**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiportal).                                                                             |
| Enumerazioni associate                                                                   | [**VDS \_ STATO DEL \_ \_ PORTALE ISCSI**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_portal_status).                                                          |
| Strutture associate                                                                     | [**VDS \_ ISCSI \_ PORTAL \_ PROP**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_portal_prop) e [**VDS PORT \_ \_ NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_port_notification). |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetti provider di hardware](hardware-provider-objects.md)
</dt> <dt>

[**IVdsSubSystemIscsi::QueryPortals**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-queryportals)
</dt> </dl>

 

 
