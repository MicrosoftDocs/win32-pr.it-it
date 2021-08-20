---
title: Strutture ProjFS
description: Le strutture seguenti vengono dichiarate in projectedfslib.h.
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: 9524b1244406c1de129ed0056fa6e2f3f7b0cb10552087e2d06639d168bb1d13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792422"
---
# <a name="projfs-structures"></a>Strutture ProjFS

Le strutture seguenti vengono dichiarate in projectedfslib.h.

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
|-|-|
| [**PRJ_CALLBACK_DATA**](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_callback_data) | Definisce le informazioni standard passate a un provider per ogni callback dell'operazione. |
| [**PRJ_CALLBACKS**](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_callbacks) | Set di puntatori alla posizione in cui il provider archivia le implementazioni delle routine di callback. |
| [**PRJ_COMPLETE_COMMAND_EXTENDED_PARAMETERS**](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_complete_command_extended_parameters) | Specifica i parametri necessari per il completamento di determinati callback. |
| [**PRJ_FILE_BASIC_INFO**](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_file_basic_info) | Informazioni di base su un elemento. |
| [**PRJ_NOTIFICATION_MAPPING**](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_notification_mapping) | Descrive un mapping di notifica, ovvero un'associazione tra una directory (definita "radice di notifica") e un set di notifiche, espresso come maschera di bit. |
| [**PRJ_NOTIFICATION_PARAMETERS**](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_notification_parameters) | Parametri aggiuntivi per le notifiche. |
| [**PRJ_PLACEHOLDER_INFO**](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_placeholder_info) | Buffer di metadati per il file o la directory segnaposto. |
| [**PRJ_PLACEHOLDER_VERSION_INFO**](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_placeholder_version_info) | Informazioni che identificano in modo univoco il contenuto di un file segnaposto. |
| [**PRJ_STARTVIRTUALIZING_OPTIONS**](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_startvirtualizing_options) | Opzioni da specificare all'avvio di un'istanza di virtualizzazione. |
| [**PRJ_VIRTUALIZATION_INSTANCE_INFO**](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_virtualization_instance_info) | Informazioni su un'istanza di virtualizzazione. |
