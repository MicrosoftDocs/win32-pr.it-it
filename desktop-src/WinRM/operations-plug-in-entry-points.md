---
title: Punti di ingresso del plug-in per le operazioni
description: Punti di ingresso del plug-in per le operazioni
ms.assetid: 9a3ddc2b-9fde-4915-b0e8-0a5e79e73c00
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0834363c7447bc50269da09d361e630d9bc0615a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473147"
---
# <a name="operations-plug-in-entry-points"></a>Punti di ingresso del plug-in per le operazioni

Un plug-in per le operazioni deve implementare determinati punti di ingresso in base alle funzionalità che intende supportare.

Un plug-in deve essere registrato con il servizio Gestione remota Windows (WinRM), che contiene i nomi dei punti di ingresso della DLL del plug-in. Tutte le operazioni hanno punti di ingresso DLL predefiniti che devono essere esposti se tale operazione è supportata.

Nella tabella seguente viene fornita una panoramica dei punti di ingresso del plug-in per le operazioni nell'API del plug-in WinRM.



| Funzione                                                                                 | Descrizione                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_comando plug-in WSMan \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_command)                                   | Definisce il callback del comando per un plug-in.<br/> Tutti i plug-in WinRM che supportano le funzionalità Shell devono implementare questo callback.<br/> Il nome del punto di ingresso della DLL per questo metodo deve essere [**WSManPluginCommand**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_command).<br/> |
| [**\_connessione del plug-in WSMan \_**](/windows/desktop/api/WsMan/nc-wsman-wsman_plugin_connect)                                   | Definisce il callback di connessione per un plug-in.<br/> Il nome del punto di ingresso della DLL per questo metodo deve essere [**WSManPluginConnect**](/windows/desktop/api/WsMan/nc-wsman-wsman_plugin_connect).<br/>                                                                                                |
| [**\_ricezione plug-in WSMan \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_receive)                                   | Definisce il callback di ricezione per un plug-in.<br/> Tutti i plug-in WinRM che supportano le funzionalità Shell devono implementare questo callback.<br/> Il nome del punto di ingresso della DLL per questo metodo deve essere [**WSManPluginReceive**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_receive).<br/> |
| [**\_contesto del \_ comando di versione del plug-in \_ WSMan \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_release_command_context) | Definisce il callback del comando Release per il plug-in.<br/> Il nome del punto di ingresso della DLL deve essere [**WSManPluginReleaseCommandContext**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_release_command_context).<br/>                                                                        |
| [**\_contesto della \_ Shell di versione del plug-in \_ WSMan \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_release_shell_context)     | Definisce il callback della shell della versione per il plug-in.<br/> Il nome del punto di ingresso della DLL deve essere [**WSManPluginReleaseCommandContext**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_release_command_context).<br/>                                                                          |
| [**\_invio plug-in WSMan \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_send)                                         | Definisce il callback di invio per un plug-in.<br/> Tutti i plug-in WinRM che supportano le funzionalità Shell devono implementare questo callback.<br/> Il nome del punto di ingresso della DLL per questo metodo deve essere [**WSManPluginSend**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_send).<br/>          |
| [**\_Shell plug-in WSMan \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_shell)                                       | Definisce il callback della Shell per un plug-in.<br/> Tutti i plug-in WinRM che supportano le funzionalità Shell devono implementare questo callback.<br/> Il nome del punto di ingresso della DLL per questo metodo deve essere [**WSManPluginShell**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_shell).<br/>       |
| [**\_arresto plug-in WSMan \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_shutdown)                                 | Definisce il callback di arresto per il plug-in.<br/> Tutti i plug-in WinRM devono implementare questa funzione di callback.<br/> Il nome del punto di ingresso della DLL per questo metodo deve essere [**WSManPluginShutdown**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_shutdown).<br/>                      |
| [**\_segnale plug-in WSMan \_**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_signal)                                     | Definisce il callback del segnale per un plug-in.<br/> Tutti i plug-in WinRM che supportano le funzionalità Shell devono implementare questo callback.<br/> Il nome del punto di ingresso della DLL per questo metodo deve essere [**WSManPluginSignal**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_signal).<br/>    |
| [**\_avvio del plug-in WSMan \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_startup)                                   | Definisce il callback di avvio per il plug-in.<br/> Tutti i plug-in WinRM devono implementare questa funzione di callback.<br/> Il nome del punto di ingresso della DLL per questo metodo deve essere [**WSManPluginStartup**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_startup).<br/>                         |



 

 

