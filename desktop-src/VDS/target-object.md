---
description: Oggetto di destinazione
ms.assetid: e88d65ad-9b56-4620-a0f5-573c5e245b3e
title: Oggetto di destinazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e1e81ea94a2f608378eba069defc83a721e0fb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318209"
---
# <a name="target-object"></a>Oggetto di destinazione

\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un oggetto di destinazione modella una destinazione iSCSI contenuta all'interno di un sottosistema iSCSI.

Usare il metodo [**IVdsSubSystemIscsi:: QueryTargets**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-querytargets) per determinare le destinazioni iSCSI del sottosistema. I chiamanti possono ottenere un puntatore a una destinazione specifica selezionando l'oggetto di destinazione desiderato dall'enumerazione restituita dal metodo **QueryTargets** . Con un oggetto di destinazione è possibile impostare il nome descrittivo e la query della destinazione per le proprietà di destinazione, i LUN associati e il sottosistema che contiene la destinazione.

I computer host devono accedere alle destinazioni per accedere ai Lun associati. Per eseguire un accesso a una destinazione, è necessario che la destinazione disponga di almeno un portale associato in uno dei relativi gruppi di portale. L'input e l'output dei lun associati vengono gestiti tramite questa sessione di accesso.

Le proprietà dell'oggetto di destinazione includono un identificatore di oggetto, un nome iSCSI, un nome descrittivo e un flag abilitato per CHAP.

Nella tabella seguente sono elencate le interfacce, le enumerazioni e le strutture correlate.



| Tipo                                                                                      | Elemento                                                                                                                     |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| Interfacce sempre esposte da questo oggetto nei soli provider iSCSI VDS 1,1 e 2,0 | [**IVdsIscsiTarget**](/windows/desktop/api/Vds/nn-vds-ivdsiscsitarget).                                                                                 |
| Enumerazioni associate                                                                   | Nessuna.                                                                                                                       |
| Strutture associate                                                                     | [**VDS \_ Notifica \_ di \_ destinazione iSCSI**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_target_prop) e [**\_ destinazione \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_target_notification). |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetti provider hardware](hardware-provider-objects.md)
</dt> <dt>

[**IVdsSubSystemIscsi::QueryTargets**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-querytargets)
</dt> </dl>

 

 
