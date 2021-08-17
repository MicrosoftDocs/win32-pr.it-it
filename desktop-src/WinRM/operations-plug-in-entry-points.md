---
title: Punti di ingresso del plug-in operazioni
description: Punti di ingresso del plug-in operazioni
ms.assetid: 9a3ddc2b-9fde-4915-b0e8-0a5e79e73c00
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5941746e8e6b952f2f1cd6f21c697398cb4cbb60b024daa557e65151a0a1cfd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119412771"
---
# <a name="operations-plug-in-entry-points"></a>Punti di ingresso del plug-in operazioni

Un plug-in delle operazioni deve implementare determinati punti di ingresso a seconda delle funzionalità che vuole supportare.

Un plug-in deve registrarsi con il Windows gestione remota (WinRM) che contiene i nomi dei punti di ingresso dll plug-in. Tutte le operazioni hanno punti di ingresso DLL predefiniti che devono essere esposti se tale operazione è supportata.

La tabella seguente offre una panoramica dei punti di ingresso del plug-in delle operazioni nell'API del plug-in WinRM.



| Funzione                                                                                 | Descrizione                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**COMANDO DEL PLUG-IN WSMAN \_ \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_command)                                   | Definisce il callback del comando per un plug-in.<br/> Tutti i plug-in WinRM che supportano le funzionalità della shell devono implementare questo callback.<br/> Il nome del punto di ingresso DLL per questo metodo deve [**essere WSManPluginCommand.**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_command)<br/> |
| [**WSMAN \_ PLUGIN \_ CONNECT**](/windows/desktop/api/WsMan/nc-wsman-wsman_plugin_connect)                                   | Definisce il callback di connessione per un plug-in.<br/> Il nome del punto di ingresso DLL per questo metodo deve [**essere WSManPluginConnect.**](/windows/desktop/api/WsMan/nc-wsman-wsman_plugin_connect)<br/>                                                                                                |
| [**RICEZIONE PLUG-IN WSMAN \_ \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_receive)                                   | Definisce il callback di ricezione per un plug-in.<br/> Tutti i plug-in WinRM che supportano le funzionalità della shell devono implementare questo callback.<br/> Il nome del punto di ingresso DLL per questo metodo [**deve essere WSManPluginReceive.**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_receive)<br/> |
| [**CONTESTO DEL COMANDO \_ DI RILASCIO \_ DEL \_ PLUG-IN \_ WSMAN**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_release_command_context) | Definisce il callback del comando di rilascio per il plug-in.<br/> Il nome del punto di ingresso dll deve [**essere WSManPluginReleaseCommandContext.**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_release_command_context)<br/>                                                                        |
| [**CONTESTO DELLA \_ SHELL DI RILASCIO DEL \_ \_ PLUG-IN \_ WSMAN**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_release_shell_context)     | Definisce il callback della shell di rilascio per il plug-in.<br/> Il nome del punto di ingresso dll deve [**essere WSManPluginReleaseCommandContext.**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_release_command_context)<br/>                                                                          |
| [**INVIO DEL PLUG-IN WSMAN \_ \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_send)                                         | Definisce il callback di invio per un plug-in.<br/> Tutti i plug-in WinRM che supportano le funzionalità della shell devono implementare questo callback.<br/> Il nome del punto di ingresso DLL per questo metodo deve [**essere WSManPluginSend.**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_send)<br/>          |
| [**SHELL DEL PLUG-IN WSMAN \_ \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_shell)                                       | Definisce il callback della shell per un plug-in.<br/> Tutti i plug-in WinRM che supportano le funzionalità della shell devono implementare questo callback.<br/> Il nome del punto di ingresso DLL per questo metodo [**deve essere WSManPluginShell.**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_shell)<br/>       |
| [**ARRESTO DEL PLUG-IN WSMAN \_ \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_shutdown)                                 | Definisce il callback di arresto per il plug-in.<br/> Tutti i plug-in WinRM devono implementare questa funzione di callback.<br/> Il nome del punto di ingresso DLL per questo metodo [**deve essere WSManPluginShutdown.**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_shutdown)<br/>                      |
| [**WSMAN \_ PLUGIN \_ SIGNAL**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_signal)                                     | Definisce il callback del segnale per un plug-in.<br/> Tutti i plug-in WinRM che supportano le funzionalità della shell devono implementare questo callback.<br/> Il nome del punto di ingresso DLL per questo metodo [**deve essere WSManPluginSignal.**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_signal)<br/>    |
| [**AVVIO DEL PLUG-IN WSMAN \_ \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_startup)                                   | Definisce il callback di avvio per il plug-in.<br/> Tutti i plug-in WinRM devono implementare questa funzione di callback.<br/> Il nome del punto di ingresso DLL per questo metodo [**deve essere WSManPluginStartup.**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_startup)<br/>                         |



 

 

