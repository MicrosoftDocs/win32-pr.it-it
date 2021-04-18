---
title: Punti di ingresso del plug-in di autorizzazione
description: Punti di ingresso del plug-in di autorizzazione
ms.assetid: 6cbfa79a-b57b-44b8-a421-d5e79c1b3757
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ee0db76457860106e51bd6c29cead3d0f8227d7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300288"
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

Nella tabella seguente viene fornita una panoramica dei punti di ingresso del plug-in di autorizzazione nell'API del plug-in Gestione remota Windows (WinRM).



| Funzione                                                                                      | Descrizione                                                                                                                                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_operazione di \_ autorizzazione \_ plug-in WSMan**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_operation)              | Chiamato per autorizzare un'operazione specifica. <br/> Il nome del punto di ingresso della DLL per questo metodo deve essere [**WSManPluginAuthzOperation**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_operation).<br/>                                                                                                                                                                                                       |
| [**\_richiesta di \_ autorizzazione \_ plug \_ -in di WSMan**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_operation)           | Chiamato dopo che una connessione è stata autorizzata a recuperare le informazioni sulla quota per l'utente. <br/> Il nome del punto di ingresso della DLL per questo metodo deve essere [**WSManPluginAuthzQueryQuota**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_query_quota).<br/>                                                                                                                                                    |
| [**\_contesto di \_ \_ rilascio autorizzazione plug- \_ in WSMan**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_release_context) | Chiamato per rilasciare il contesto che un plug-in segnala dai metodi [**WSManPluginAuthzUserComplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzusercomplete) o [**WSManPluginAuthzOperationComplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzoperationcomplete) . <br/> Il nome del punto di ingresso della DLL per questo metodo deve essere [**WSManPluginAuthzReleaseContext**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_release_context).<br/> |
| [**\_ \_ utente autorizzato per il plug-in WSMan \_**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_user)                         | Chiamata eseguita per determinare se l'utente è autorizzato a eseguire una richiesta. <br/> Il nome del punto di ingresso della libreria di collegamento dinamico (DLL) per questo metodo deve essere [**WSManPluginAuthzUser**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_user).<br/>                                                                                                                                                            |



 

 

