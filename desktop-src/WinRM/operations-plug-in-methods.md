---
title: Metodi del plug-in per le operazioni
description: Metodi del plug-in per le operazioni
ms.assetid: 81fe751f-51fd-4da6-b44a-0af9007eea9a
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff64a53c4c63b9e552efe90ac057b8a31d603b64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955046"
---
# <a name="operations-plug-in-methods"></a>Metodi del plug-in per le operazioni

Tutti i punti di ingresso del plug-in per le operazioni hanno un meccanismo di callback per segnalare l'esito positivo o negativo della chiamata. Alcuni meccanismi di callback vengono chiamati più volte, fino a quando non vengono restituiti tutti i risultati.

Nella tabella seguente viene fornita una panoramica dei metodi di callback delle operazioni.



| Metodo                                                                         | Descrizione                                                                                                                                          |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WSManPluginFreeRequestDetails**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginfreerequestdetails)         | Rilascia la memoria allocata per la struttura della [**\_ \_ richiesta del plug**](/windows/desktop/api/Wsman/ns-wsman-wsman_plugin_request) -in WSMan.                                          |
| [**WSManPluginGetOperationParameters**](/windows/desktop/api/Wsman/nf-wsman-wsmanplugingetoperationparameters) | Ottiene informazioni operative, ad esempio timeout e restrizioni dei dati associate a un'operazione.                                         |
| [**WSManPluginOperationComplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginoperationcomplete)           | Registra il completamento di un'operazione.                                                                                                              |
| [**WSManPluginReceiveResult**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginreceiveresult)                   | Segnala i risultati ai plug-in di Gestione remota Windows (WinRM).                                                                                       |
| [**WSManPluginReportContext**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginreportcontext)                   | Segnala la shell e il contesto dei comandi all'infrastruttura WinRM in modo che sia possibile eseguire ulteriori operazioni sulla shell e/o sul comando. |



 

 

 




