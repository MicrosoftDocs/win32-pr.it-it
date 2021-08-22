---
description: I tipi di dati supportati da VDS definiscono i valori restituiti della funzione, i parametri di funzione e i membri della struttura. I tipi di dati definiscono le dimensioni e il significato di questi elementi.
ms.assetid: f17e8c7e-e3cb-49ca-9060-2299dda55770
title: Tipi di dati VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d83a0f3586cb73b823feb6b41990d1f305056a23f9ac0e47ef8fbfc1e4853267
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007931"
---
# <a name="vds-data-types"></a>Tipi di dati VDS

\[A partire da Windows 8 e Windows Server 2012, [l'interfaccia](virtual-disk-service-portal.md) COM del servizio dischi virtuali viene sostituita dal Windows Archiviazione API Gestione [.](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)\]

I tipi di dati supportati da VDS definiscono i valori restituiti della funzione, i parametri di funzione e i membri della struttura. I tipi di dati definiscono le dimensioni e il significato di questi elementi.



| Tipo di dati                                                                                      | Descrizione                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VDS_OBJECT_ID"></span><span id="vds_object_id"></span>**ID OGGETTO VDS \_ \_**<br/> | ID oggetto VDS. Non è garantito che questi valori siano univoci tra i riavvii. <br/> Questo tipo è dichiarato in Vds.h (VdsHwPrv.h per i provider di hardware) come GUID. <br/> |
| <span id="VDS_PATH_ID"></span><span id="vds_path_id"></span>**ID PERCORSO VDS \_ \_**<br/>       | ID percorso VDS per multipath I/O (MPIO). <br/> Questo tipo è dichiarato in Vds.h (VdsHwPrv.h per i provider di hardware) come UINT64.<br/>                                      |



 

 

