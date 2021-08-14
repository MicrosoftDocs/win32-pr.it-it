---
title: Metodi del plug-in operazioni
description: Metodi del plug-in operazioni
ms.assetid: 81fe751f-51fd-4da6-b44a-0af9007eea9a
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8bcfc2263a9ecd35c050499f0547b5bc5190e5896b430edabe6be8490239b62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118323893"
---
# <a name="operations-plug-in-methods"></a>Metodi del plug-in operazioni

Tutti i punti di ingresso del plug-in delle operazioni dispongono di un meccanismo di callback per segnalare l'esito positivo o negativo della chiamata. Alcuni meccanismi di callback vengono chiamati più volte, fino a quando non vengono segnalati tutti i risultati.

Nella tabella seguente viene fornita una panoramica dei metodi di callback delle operazioni.



| Metodo                                                                         | Descrizione                                                                                                                                          |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WSManPluginFreeRequestDetails**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginfreerequestdetails)         | Rilascia la memoria allocata per la [**struttura WSMAN \_ PLUGIN \_ REQUEST.**](/windows/desktop/api/Wsman/ns-wsman-wsman_plugin_request)                                          |
| [**WSManPluginGetOperationParameters**](/windows/desktop/api/Wsman/nf-wsman-wsmanplugingetoperationparameters) | Ottiene informazioni operative, ad esempio timeout e restrizioni dei dati associati a un'operazione.                                         |
| [**WSManPluginOperationComplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginoperationcomplete)           | Registra il completamento di un'operazione.                                                                                                              |
| [**WSManPluginReceiveResult**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginreceiveresult)                   | Segnala i risultati Windows plug-in gestione remota (WinRM).                                                                                       |
| [**WSManPluginReportContext**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginreportcontext)                   | Segnala la shell e il contesto di comando all'infrastruttura WinRM in modo che sia possibile eseguire altre operazioni sulla shell e/o sul comando. |



 

 

 




