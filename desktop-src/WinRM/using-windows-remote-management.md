---
title: Utilizzo di Gestione remota Windows
description: Gestione remota Windows è progettato per migliorare la gestione dell'hardware in un ambiente di rete con vari dispositivi che eseguono un'ampia gamma di sistemi operativi.
ms.assetid: 6ee2b238-5bc2-4274-b7ca-49dbc728d8f1
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0c2934694de5913b467521510179fffdb220b601
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118110"
---
# <a name="using-windows-remote-management"></a>Utilizzo di Gestione remota Windows

Gestione remota Windows è progettato per migliorare la gestione dell'hardware in un ambiente di rete con vari dispositivi che eseguono un'ampia gamma di sistemi operativi. L'intera progettazione del servizio ha come obiettivo principale il monitoraggio e la gestione di computer remoti mediante l'implementazione di un protocollo interoperativo standard.

Poiché l' [API di scripting WinRM](winrm-scripting-api.md) e l' [API C++ WinRM](winrm-c---api.md) implementano e modellano attentamente le operazioni definite per il protocollo WS-Management, gli script e le applicazioni ricevono flussi di XML in risposta alle richieste. I parametri di input per le chiamate al metodo devono essere costruiti in XML. È possibile utilizzare i metodi dell'API [MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)) per visualizzare o costruire stringhe XML. Per un esempio, vedere [visualizzazione dell'output XML dagli script WinRM](displaying-xml-output-from-winrm-scripts.md).

Nell'elenco seguente sono inclusi gli argomenti che descrivono come utilizzare lo script WinRM:

-   [Rilevamento dell'eventuale supporto di WS-Management protocollo da un computer remoto](detecting-whether-a-remote-computer-supports-ws-management-protocol.md)
-   [Recupero di dati dal computer locale](obtaining-data-from-the-local-computer.md)
-   [Recupero di dati da un computer remoto](obtaining-data-from-a-remote-computer.md)
-   [Enumerazione o elenco di tutte le istanze di una risorsa](enumerating-or-listing-all-instances-of-a-resource.md)
-   [Esecuzione di query per istanze specifiche di una risorsa](querying-for-specific-instances-of-a-resource.md)
-   [Visualizzazione dell'output XML dagli script WinRM](displaying-xml-output-from-winrm-scripts.md)

## <a name="tracing-winrm-activity"></a>Traccia dell'attività WinRM

Poiché WinRM ottiene i dati tramite [Strumentazione gestione Windows (WMI)](/windows/desktop/WmiSdk/wmi-start-page), è possibile tracciare l'attività WMI risultante dai messaggi WinRM. A partire da Windows Vista, i [file di log WMI](/windows/desktop/WmiSdk/wmi-log-files)non vengono più utilizzati dal servizio WMI. USA invece [traccia eventi](/windows/desktop/ETW/event-tracing-portal) (ETW) ed eventi sono disponibili tramite l'interfaccia utente **Visualizzatore eventi** o lo strumento da riga di comando Evtutil.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione remota Windows](portal.md)
</dt> <dt>

[Informazioni su Gestione remota Windows](about-windows-remote-management.md)
</dt> <dt>

[Riferimento Gestione remota Windows](windows-remote-management-reference.md)
</dt> <dt>

[Creazione di script in Gestione remota Windows](scripting-in-windows-remote-management.md)
</dt> </dl>

 

 