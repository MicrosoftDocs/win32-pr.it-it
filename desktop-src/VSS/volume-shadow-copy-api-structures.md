---
description: Le strutture seguenti sono definite nell'API copia shadow del volume.
ms.assetid: 20cf12e4-4611-4e39-9f6f-e29f15e58b36
title: Strutture API copia shadow del volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1bb699277faa30c6a570203cd820d552cc9f1b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307174"
---
# <a name="volume-shadow-copy-api-structures"></a>Strutture API copia shadow del volume

Le strutture seguenti sono definite nell'API copia shadow del volume.



| Struttura                                                           | Descrizione                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_COMPONENTINFO VSS**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo)                     | Contiene informazioni su un determinato componente.                                                                                                                                                                                                                       |
| [**\_ \_ prop area diff \_ VSS**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_diff_area_prop)                 | Descrive le associazioni tra i volumi di origine contenenti i dati e i volumi originali dei file contenenti l'area di archiviazione della copia shadow.                                                                                                                                |
| [**\_ \_ prop volume diff \_ VSS**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_diff_volume_prop)             | Descrive un volume dell'area di archiviazione della copia shadow.                                                                                                                                                                                                                        |
| [**\_prop dell' \_ oggetto \_ Mgmt di VSS**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_mgmt_object_prop)             | Descrive le proprietà di un volume, di un volume di archiviazione copia shadow o di un'area di archiviazione copia shadow.                                                                                                                                                                    |
| [**\_ \_ Unione oggetti VSS \_ Mgmt**](/windows/desktop/api/VsMgmt/ns-vsmgmt-__midl___midl_itf_vsmgmt_0000_0000_0001)           | Unione di strutture [**VSS \_ volume \_ prop**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_volume_prop), [**VSS \_ diff \_ volume \_ prop**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_diff_volume_prop)e [**VSS \_ diff \_ area \_ prop**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_diff_area_prop) , utilizzate dalla struttura [**\_ \_ \_ prop dell'oggetto Mgmt Mgmt**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_mgmt_object_prop) . |
| [**\_prop oggetto \_ VSS**](/windows/desktop/api/Vss/ns-vss-vss_object_prop)                        | Descrive le proprietà di un provider, un volume, una copia shadow o un set di copie shadow.                                                                                                                                                                                    |
| [**\_Unione oggetti \_ VSS**](/windows/desktop/api/Vss/ns-vss-__midl___midl_itf_vss_0000_0000_0001)                      | Unione di strutture di prop del provider VSS [**\_ snapshot \_ VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) e del [**\_ provider \_ VSS**](/windows/desktop/api/Vss/ns-vss-vss_provider_prop) , utilizzate dalla struttura [**\_ \_ prop dell'oggetto VSS**](/windows/desktop/api/Vss/ns-vss-vss_object_prop) .                                                                    |
| [**\_prop del provider VSS \_**](/windows/desktop/api/Vss/ns-vss-vss_provider_prop)                    | Specifica le proprietà del provider di copie shadow.                                                                                                                                                                                                                          |
| [**\_prop snapshot \_ VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop)                    | Contiene le proprietà di una copia shadow o di un set di copie shadow.                                                                                                                                                                                                        |
| [**\_prop volume \_ VSS**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_volume_prop)                        | Descrive le proprietà di un volume di origine della copia shadow.                                                                                                                                                                                                            |
| [**\_informazioni sulla \_ protezione del volume VSS \_**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_volume_protection_info) | Contiene informazioni sul livello di protezione della copia shadow di un volume.                                                                                                                                                                                                 |



 

 

 



