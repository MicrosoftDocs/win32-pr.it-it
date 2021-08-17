---
description: Oggetto di destinazione
ms.assetid: e88d65ad-9b56-4620-a0f5-573c5e245b3e
title: Oggetto di destinazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b528d66fb789e4d237dacae151c3dda596e834f84f529c3677905672de3b7588
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057949"
---
# <a name="target-object"></a>Oggetto di destinazione

\[A partire da Windows 8 e Windows Server 2012, [l'interfaccia](virtual-disk-service-portal.md) COM del servizio dischi virtuali viene sostituita dal Windows Archiviazione API Gestione [.](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)\]

Un oggetto di destinazione modella una destinazione iSCSI contenuta in un sottosistema iSCSI.

Usare il [**metodo IVdsSubSystemIscsi::QueryTargets**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-querytargets) per determinare le destinazioni iSCSI del sottosistema. I chiamanti possono ottenere un puntatore a una destinazione specifica selezionando l'oggetto di destinazione desiderato dall'enumerazione restituita dal **metodo QueryTargets.** Con un oggetto di destinazione, è possibile impostare il nome descrittivo e la query della destinazione per le proprietà di destinazione, i LUN associati e il sottosistema che contiene la destinazione.

I computer host devono accedere alle destinazioni per accedere ai LUN associati. Per eseguire un accesso a una destinazione, la destinazione deve avere almeno un portale associato in uno dei relativi gruppi del portale. L'input e l'output dai LUN associati vengono gestiti tramite questa sessione di accesso.

Le proprietà dell'oggetto di destinazione includono un identificatore di oggetto, un nome iSCSI, un nome descrittivo e un flag abilitato per CHAP.

Nella tabella seguente sono elencate le interfacce, le enumerazioni e le strutture correlate.



| Tipo                                                                                      | Elemento                                                                                                                     |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| Interfacce sempre esposte da questo oggetto solo nei provider iSCSI VDS 1.1 e 2.0 | [**IVdsIscsiTarget**](/windows/desktop/api/Vds/nn-vds-ivdsiscsitarget).                                                                                 |
| Enumerazioni associate                                                                   | Nessuno.                                                                                                                       |
| Strutture associate                                                                     | [**VDS \_ ISCSI \_ TARGET \_ PROP**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_target_prop) e [**VDS TARGET \_ \_ NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_target_notification). |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetti provider di hardware](hardware-provider-objects.md)
</dt> <dt>

[**IVdsSubSystemIscsi::QueryTargets**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-querytargets)
</dt> </dl>

 

 
