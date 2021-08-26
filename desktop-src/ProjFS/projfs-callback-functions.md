---
title: Funzioni di callback ProjFS
description: Le funzioni di callback seguenti sono dichiarate in projectedfslib.h.
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: 595fac418ce57e1e6caff718d75b458390efd31c2e8727cd2feb8ee5a5d86eb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031161"
---
# <a name="callback-functions"></a>Funzioni di callback

Le funzioni di callback seguenti sono dichiarate in projectedfslib.h.

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
|-|-|
| [**PRJ_CANCEL_COMMAND_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_cancel_command_cb) | Notifica al provider che un'operazione eseguita da una chiamata precedente di un callback deve essere annullata. |
| [**PRJ_END_DIRECTORY_ENUMERATION_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_end_directory_enumeration_cb) | Informa il provider che un'enumerazione di directory è finita. |
| [**PRJ_GET_DIRECTORY_ENUMERATION_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb) | Richiede le informazioni di enumerazione della directory dal provider.
| [**PRJ_GET_FILE_DATA_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb) | Richiede il contenuto del flusso di dati primario di un file.
| [**PRJ_GET_PLACEHOLDER_INFO_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_placeholder_info_cb) | Richiede informazioni per un file o una directory dal provider.
| [**PRJ_NOTIFICATION_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_notification_cb) | Recapita al provider le notifiche relative file system operazioni.
| [**PRJ_QUERY_FILE_NAME_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_query_file_name_cb) | Determina se un percorso di file specificato esiste nell'archivio di backup del provider.
| [**PRJ_START_DIRECTORY_ENUMERATION_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb) | Informa il provider che è in corso l'avvio di un'enumerazione di directory.