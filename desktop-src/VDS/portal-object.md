---
description: Oggetto portale
ms.assetid: 6655bbae-07d3-416b-9e45-ddcbe3433f40
title: Oggetto portale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01328d8dccfe7a29c0686cde9b531df63d56e63e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318594"
---
# <a name="portal-object"></a>Oggetto portale

\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un oggetto portale modella un portale iSCSI contenuto all'interno di un sottosistema iSCSI.

Usare il metodo [**IVdsSubSystemIscsi:: QueryPortals**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-queryportals) per determinare i portali iSCSI del sottosistema. I chiamanti possono ottenere un puntatore a un portale specifico selezionando l'oggetto portale desiderato dall'enumerazione restituita dal metodo **QueryPortals** . Con un oggetto portale è possibile impostare lo stato del portale e la query per le proprietà del portale, i gruppi di portale associati e il sottosistema che contiene il portale.

Un oggetto portale può essere associato al massimo un gruppo di portale di una destinazione specificata.

I portali servono come uno degli endpoint dei percorsi MPIO nei provider di hardware iSCSI, su cui è possibile imporre i criteri di bilanciamento del carico.

Le proprietà dell'oggetto portale includono un identificatore di oggetto, un indirizzo IP e una porta e lo stato del portale.

Nella tabella seguente sono elencate le interfacce, le enumerazioni e le strutture correlate.



| Tipo                                                                                      | Elemento                                                                                                                 |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Interfacce sempre esposte da questo oggetto nei soli provider iSCSI VDS 1,1 e 2,0 | [**IVdsIscsiPortal**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiportal).                                                                             |
| Enumerazioni associate                                                                   | [**VDS \_ \_ \_ stato del portale iSCSI**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_portal_status).                                                          |
| Strutture associate                                                                     | [**VDS \_ \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_portal_prop) [**Notifica delle \_ porte \_**](/windows/desktop/api/Vds/ns-vds-vds_port_notification)del portale iSCSI e VDS. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetti provider hardware](hardware-provider-objects.md)
</dt> <dt>

[**IVdsSubSystemIscsi::QueryPortals**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-queryportals)
</dt> </dl>

 

 
