---
description: I tipi di dati supportati da VDS definiscono i valori restituiti dalla funzione, i parametri della funzione e i membri della struttura. I tipi di dati definiscono le dimensioni e il significato di questi elementi.
ms.assetid: f17e8c7e-e3cb-49ca-9060-2299dda55770
title: Tipi di dati VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a868606110d9cf1c3cad5c3036789d041a5d86c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318204"
---
# <a name="vds-data-types"></a>Tipi di dati VDS

\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

I tipi di dati supportati da VDS definiscono i valori restituiti dalla funzione, i parametri della funzione e i membri della struttura. I tipi di dati definiscono le dimensioni e il significato di questi elementi.



| Tipo di dati                                                                                      | Descrizione                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VDS_OBJECT_ID"></span><span id="vds_object_id"></span>**\_ID oggetto \_ VDS**<br/> | ID oggetto VDS. Questi valori non sono necessariamente univoci tra i riavvii. <br/> Questo tipo viene dichiarato in VDS. h (VdsHwPrv. h per i provider hardware) come GUID. <br/> |
| <span id="VDS_PATH_ID"></span><span id="vds_path_id"></span>**\_ID percorso \_ VDS**<br/>       | ID percorso VDS per la funzionalità Multipath I/O (MPIO). <br/> Questo tipo viene dichiarato in VDS. h (VdsHwPrv. h per i provider hardware) come UINT64.<br/>                                      |



 

 

