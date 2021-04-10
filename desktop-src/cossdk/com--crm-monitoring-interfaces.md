---
description: L'infrastruttura CRM fornisce un set di interfacce che è possibile utilizzare per il monitoraggio dei dispongono all'interno di una particolare applicazione server.
ms.assetid: b8f40c91-001b-4003-b377-57a918988100
title: Interfacce di monitoraggio COM+ CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c893040c46810c980c647cbacdc808200e8d5f5e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225587"
---
# <a name="com-crm-monitoring-interfaces"></a>Interfacce di monitoraggio COM+ CRM

L'infrastruttura CRM fornisce un set di interfacce che è possibile utilizzare per il monitoraggio dei dispongono all'interno di una particolare applicazione server. Per accedere alle interfacce di monitoraggio, un componente in esecuzione all'interno dell'applicazione server deve prima creare un clerk CRM specializzato denominato Clerk Recovery CRM.

Nell'uso normale di dispongono, le transazioni devono essere di breve durata e, di conseguenza, i ruoli di lavoro e i compensatori CRM sono disponibili per un breve periodo di tempo, in genere solo pochi secondi. Le interfacce di monitoraggio sono pertanto progettate per fornire uno snapshot dello stato del dispongono in esecuzione in un determinato momento. Se si verificano problemi in uno dei dispongono, le interfacce di monitoraggio possono essere usate per azzerare il CRM problematico, esaminare i record di log e interrompere la transazione, se necessario.

Di seguito sono riportate le tre interfacce di monitoraggio CRM e le descrizioni del loro funzionamento.



| Interfaccia                                                         | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICrmMonitor**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitor)<br/>                     | L'uso di [**ICrmMonitor:: Getclerks**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmmonitor-getclerks)consente di ottenere uno snapshot del set corrente di clerk CRM attivi all'interno dell'applicazione server. Da questo, è possibile trovare ed eseguire query su un particolare oggetto raccolta Clerk CRM di interesse, incluso lo stato corrente della transazione e i record di log scritti dal CRM.<br/> Quando lo strumento di monitoraggio ha determinato quale Clerk è di interesse, viene chiamato [**ICrmMonitor:: HoldClerk**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmmonitor-holdclerk) per ottenere un'interfaccia [**ICrmMonitorLogRecords**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorlogrecords) su quel particolare Clerk. A questo punto, lo strumento di monitoraggio contiene un riferimento a tale Clerk e, se la transazione viene completata, il clerk viene mantenuto in memoria e non viene rilasciato fino a quando non viene eseguito lo strumento di monitoraggio.<br/>                                                                                                                                                                                                    |
| [**ICrmMonitorClerks**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorclerks)<br/>         | Utilizzando questa interfaccia, è possibile esplorare l'oggetto raccolta Clerk per ottenere informazioni sullo stato della raccolta Clerk nel momento in cui è stato ottenuto. Queste informazioni includono il numero di Clerk, il ProgID del compensatore CRM usato dal Clerk, la descrizione fornita nel momento in cui il compensatore CRM è stato registrato (usando [**ICrmLogControl:: RegisterCompensator**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmlogcontrol-registercompensator)), l'ID unità di transazione e l'ID attività. I singoli Clerk sono anche identificati in modo univoco da un "CLSID dell'istanza Clerk", che non è un CLSID COM nel normale senso del termine, ma semplicemente un GUID univoco che identifica questo clerk specifico per la sua durata.<br/>                                                                                                                                                                                                                                                                                                |
| [**ICrmMonitorLogRecords**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorlogrecords)<br/> | Questa interfaccia può essere utilizzata per eseguire una query sullo stato corrente della transazione, per individuare il numero di record di log scritti da questo clerk CRM e per ottenere i dati effettivi del record di log. I record di log vengono forniti dall'interfaccia [**ICrmMonitorLogRecords**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorlogrecords) nello stesso formato in cui sono stati originariamente scritti (tramite [**ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol)). Inoltre, è possibile implementare facoltativamente **ICrmMonitorLogRecords** per convertire i record di log in formato visualizzabile, in modo che possano essere presentati usando uno strumento di monitoraggio generico.<br/> Poiché [**ICrmMonitorLogRecords**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorlogrecords) viene implementato direttamente nel Clerk CRM, è possibile [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per [**ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol) (implementato anche nel Clerk CRM). Questo può essere usato per interrompere direttamente la transazione, se necessario ([**ICrmLogControl:: ForceTransactionToAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmlogcontrol-forcetransactiontoabort)).<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti Gestione risorse di compensazione COM+](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

