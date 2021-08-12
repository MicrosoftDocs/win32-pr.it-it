---
description: Le strutture seguenti sono definite nell'API Copia Shadow del volume.
ms.assetid: 20cf12e4-4611-4e39-9f6f-e29f15e58b36
title: Strutture dell'API Copia Shadow del volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f95527f505430e0283b44d233605febb5695cada3f9740e850945f58e751f3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118590553"
---
# <a name="volume-shadow-copy-api-structures"></a>Strutture dell'API Copia Shadow del volume

Le strutture seguenti sono definite nell'API Copia Shadow del volume.



| Struttura                                                           | Descrizione                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**COMPONENTINFO DI VSS \_**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo)                     | Contiene informazioni su un determinato componente.                                                                                                                                                                                                                       |
| [**PROPRIETÀ \_ DELL'AREA DIFF DI VSS \_ \_**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_diff_area_prop)                 | Descrive le associazioni tra i volumi di origine contenenti i dati del file originale e i volumi contenenti l'area di archiviazione delle copie shadow.                                                                                                                                |
| [**VSS \_ DIFF \_ VOLUME \_ PROP**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_diff_volume_prop)             | Descrive un volume dell'area di archiviazione della copia shadow.                                                                                                                                                                                                                        |
| [**PROPRIETÀ DELL'OGGETTO \_ VSS MGMT \_ \_**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_mgmt_object_prop)             | Vengono descritte le proprietà di un volume, di un volume di archiviazione di copie shadow o di un'area di archiviazione delle copie shadow.                                                                                                                                                                    |
| [**UNIONE DI OGGETTI \_ MGMT \_ DI VSS \_**](/windows/desktop/api/VsMgmt/ns-vsmgmt-__midl___midl_itf_vsmgmt_0000_0000_0001)           | Unione delle strutture [**VSS \_ VOLUME \_ PROP,**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_volume_prop) [**VSS \_ DIFF \_ VOLUME \_ PROP**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_diff_volume_prop)e [**VSS \_ DIFF \_ AREA \_ PROP**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_diff_area_prop) usate dalla struttura [**VSS \_ MGMT \_ OBJECT \_ PROP.**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_mgmt_object_prop) |
| [**PROPRIETÀ \_ DELL'OGGETTO VSS \_**](/windows/desktop/api/Vss/ns-vss-vss_object_prop)                        | Descrive le proprietà di un provider, un volume, una copia shadow o un set di copie shadow.                                                                                                                                                                                    |
| [**UNIONE DI \_ OGGETTI VSS \_**](/windows/desktop/api/Vss/ns-vss-__midl___midl_itf_vss_0000_0000_0001)                      | Unione delle [**strutture VSS \_ SNAPSHOT \_ PROP**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) e [**VSS PROVIDER \_ \_ PROP,**](/windows/desktop/api/Vss/ns-vss-vss_provider_prop) usate dalla [**struttura VSS OBJECT \_ \_ PROP.**](/windows/desktop/api/Vss/ns-vss-vss_object_prop)                                                                    |
| [**PROPRIETÀ DEL PROVIDER VSS \_ \_**](/windows/desktop/api/Vss/ns-vss-vss_provider_prop)                    | Specifica le proprietà del provider di copie shadow.                                                                                                                                                                                                                          |
| [**PROPRIETÀ SNAPSHOT DI VSS \_ \_**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop)                    | Contiene le proprietà di una copia shadow o di un set di copie shadow.                                                                                                                                                                                                        |
| [**VOLUME PROP DI VSS \_ \_**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_volume_prop)                        | Descrive le proprietà di un volume di origine della copia shadow.                                                                                                                                                                                                            |
| [**INFORMAZIONI SULLA PROTEZIONE \_ DEI VOLUMI \_ DI VSS \_**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_volume_protection_info) | Contiene informazioni sul livello di protezione della copia shadow di un volume.                                                                                                                                                                                                 |



 

 

 



