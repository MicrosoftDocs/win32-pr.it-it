---
description: Oggetto gruppo portale
ms.assetid: e5892e96-b6ad-447a-9627-b44fc6f1b27a
title: Oggetto gruppo portale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e1021d74a3c8a6a612372db56952be1dabe5380e8e4a49b1b83c5ae2fe54754
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057959"
---
# <a name="portal-group-object"></a>Oggetto gruppo portale

\[A partire da Windows 8 e Windows Server 2012, l'interfaccia [COM](virtual-disk-service-portal.md) del servizio dischi virtuali viene sostituita dal Windows Archiviazione API Gestione [.](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)\]

Un gruppo di oggetti del portale modella un gruppo del portale iSCSI contenuto in una destinazione iSCSI.

Usare il [**metodo IVdsIscsiTarget::QueryPortalGroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsitarget-queryportalgroups) per determinare i gruppi del portale contenuti in una destinazione specifica. Usare il [**metodo IVdsIscsiPortal::QueryAssociatedPortalGroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsiportal-queryassociatedportalgroups) per determinare i gruppi del portale associati a un portale specificato. I chiamanti possono ottenere un puntatore a un gruppo del portale specifico selezionando l'oggetto gruppo del portale desiderato dall'enumerazione restituita dal metodo **QueryPortalGroups** o **dal metodo QueryAssociatedPortalGroups.** Con un oggetto gruppo del portale è possibile aggiungere o rimuovere portali ed eseguire query per le proprietà del gruppo del portale, i portali associati e la destinazione che contiene il gruppo del portale.

Le proprietà dell'oggetto gruppo del portale includono [un identificatore di oggetto](vds-data-types.md) e il tag del gruppo del portale. Per altre informazioni sui tag dei gruppi del portale, vedere la specifica iSCSI all'indirizzo <https://go.microsoft.com/fwlink/p/?linkid=158752> .

Nella tabella seguente sono elencate le interfacce, le enumerazioni e le strutture correlate.



| Tipo                                                                                      | Elemento                                                                                                                                            |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce sempre esposte da questo oggetto solo nei provider iSCSI VDS 1.1 e 2.0 | [**IVdsIscsiPortalGroup**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiportalgroup).                                                                                              |
| Enumerazioni associate                                                                   | Nessuno.                                                                                                                                              |
| Strutture associate                                                                     | [**VDS \_ ISCSI \_ PORTALGROUP \_ PROP**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_portalgroup_prop) e [**NOTIFICA GRUPPO PORTALE VDS \_ \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_portal_group_notification). |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetti provider di hardware](hardware-provider-objects.md)
</dt> <dt>

[**IVdsIscsiPortal::QueryAssociatedPortalGroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsiportal-queryassociatedportalgroups)
</dt> <dt>

[**IVdsIscsiTarget::QueryPortalGroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsitarget-queryportalgroups)
</dt> </dl>

 

 
