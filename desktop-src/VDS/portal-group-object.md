---
description: Oggetto gruppo portale
ms.assetid: e5892e96-b6ad-447a-9627-b44fc6f1b27a
title: Oggetto gruppo portale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c915e76debac959a1dc7684d87c9770033b4aa34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530151"
---
# <a name="portal-group-object"></a>Oggetto gruppo portale

\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un oggetto gruppo di portali modella un gruppo di portale iSCSI contenuto all'interno di una destinazione iSCSI.

Usare il metodo [**IVdsIscsiTarget:: QueryPortalGroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsitarget-queryportalgroups) per determinare i gruppi di portali contenuti in una destinazione specifica. Usare il metodo [**IVdsIscsiPortal:: QueryAssociatedPortalGroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsiportal-queryassociatedportalgroups) per determinare i gruppi di portale associati a un portale specificato. I chiamanti possono ottenere un puntatore a un gruppo di portale specifico selezionando l'oggetto gruppo portale desiderato dall'enumerazione restituita dal metodo **QueryPortalGroups** o dal metodo **QueryAssociatedPortalGroups** . Con un oggetto gruppo di portale è possibile aggiungere o rimuovere portali ed eseguire query per le proprietà dei gruppi di portali, i portali associati e la destinazione contenente il gruppo di portale.

Le proprietà dell'oggetto gruppo portale includono un [identificatore di oggetto](vds-data-types.md) e il tag di gruppo del portale. Per ulteriori informazioni sui tag dei gruppi di portale, vedere la specifica iSCSI all'indirizzo <https://go.microsoft.com/fwlink/p/?linkid=158752> .

Nella tabella seguente sono elencate le interfacce, le enumerazioni e le strutture correlate.



| Tipo                                                                                      | Elemento                                                                                                                                            |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce sempre esposte da questo oggetto nei soli provider iSCSI VDS 1,1 e 2,0 | [**IVdsIscsiPortalGroup**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiportalgroup).                                                                                              |
| Enumerazioni associate                                                                   | Nessuna.                                                                                                                                              |
| Strutture associate                                                                     | [**VDS \_ Notifica del gruppo ISCSI \_ PORTALGROUP \_**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_portalgroup_prop) e del [**\_ portale \_ \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_portal_group_notification). |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetti provider hardware](hardware-provider-objects.md)
</dt> <dt>

[**IVdsIscsiPortal::QueryAssociatedPortalGroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsiportal-queryassociatedportalgroups)
</dt> <dt>

[**IVdsIscsiTarget::QueryPortalGroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsitarget-queryportalgroups)
</dt> </dl>

 

 
