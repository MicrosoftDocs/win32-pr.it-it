---
title: Punti di ingresso del plug-in di autorizzazione
description: Punti di ingresso del plug-in di autorizzazione
ms.assetid: 6cbfa79a-b57b-44b8-a421-d5e79c1b3757
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d16ca861df6b6546920aaf3f778c61117776ff3861556377b280c990c03711fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118324079"
---
# <a name="authorization-plug-in-entry-points"></a>Punti di ingresso del plug-in di autorizzazione

I plug-in di autorizzazione sono configurati solo per un processo host Internet Information Services (IIS). È possibile configurare un solo plug-in di autorizzazione per ogni directory virtuale.

Tutti i plug-in di autorizzazione devono supportare i punti di ingresso seguenti:

-   [**WSManPluginStartup**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_startup)
-   [**WSManPluginShutdown**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_shutdown)
-   [**WSManPluginAuthzUser**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_user)
-   [**WSManPluginAuthzOperation**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_operation)

Il punto di ingresso seguente è facoltativo:

-   [**WSManPluginAuthzQueryQuota**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_query_quota)

La tabella seguente offre una panoramica dei punti di ingresso del plug-in di autorizzazione nell'API plug-in gestione remota Windows (WinRM).



| Funzione                                                                                      | Descrizione                                                                                                                                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OPERAZIONE \_ AUTHORIZE DEL \_ PLUG-IN WSMAN \_**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_operation)              | Chiamato per autorizzare un'operazione specifica. <br/> Il nome del punto di ingresso DLL per questo metodo [**deve essere WSManPluginAuthzOperation.**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_operation)<br/>                                                                                                                                                                                                       |
| [**QUOTA DI AUTORIZZAZIONI \_ QUERY \_ PER IL \_ PLUG-IN \_ WSMAN**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_operation)           | Chiamato dopo che una connessione è stata autorizzata a recuperare le informazioni sulla quota per l'utente. <br/> Il nome del punto di ingresso DLL per questo metodo deve [**essere WSManPluginAuthzQueryQuota.**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_query_quota)<br/>                                                                                                                                                    |
| [**CONTESTO DI RILASCIO \_ \_ DELL'AUTORIZZAZIONE DEL \_ PLUG-IN \_ WSMAN**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_release_context) | Chiamato per rilasciare il contesto che un plug-in segnala dai metodi [**WSManPluginAuthzUserComplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzusercomplete) o [**WSManPluginAuthzOperationComplete.**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzoperationcomplete) <br/> Il nome del punto di ingresso DLL per questo metodo [**deve essere WSManPluginAuthzReleaseContext.**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_release_context)<br/> |
| [**WSMAN \_ PLUGIN \_ AUTHORIZE \_ USER**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_user)                         | Chiamato per determinare se l'utente è autorizzato a eseguire una richiesta. <br/> Il nome del punto di ingresso della libreria a collegamento dinamico (DLL) per questo metodo deve [**essere WSManPluginAuthzUser.**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_user)<br/>                                                                                                                                                            |



 

 

