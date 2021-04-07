---
description: Le interfacce CRM sono necessarie per fornire supporto per i ruoli di lavoro CRM e i compensatori CRM sviluppati con Visual Basic e Visual C++.
ms.assetid: 68a75da7-1f35-41a4-8872-e3f4ad1fc30d
title: Interfacce COM+ CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62ba3235b1cd2a82fc913dd676bbb78324f340cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749007"
---
# <a name="com-crm-interfaces"></a>Interfacce COM+ CRM

Le interfacce CRM sono necessarie per fornire supporto per i ruoli di lavoro CRM e i compensatori CRM sviluppati con Visual Basic e Visual C++.

È possibile utilizzare il Gestione risorse di compensazione COM+ (CRM) per integrare in modo rapido e semplice le risorse dell'applicazione con le transazioni Microsoft Distributed Transaction Coordinator (DTC).

È più facile per i componenti scritti con Visual Basic per creare un record di log come una raccolta di varianti. Inoltre, i componenti Visual Basic sono con threading Apartment, il che significa che deve essere possibile effettuare il marshalling delle interfacce dall'Apartment multithread a un Apartment a thread singolo. I componenti CRM sviluppati con Visual C++ possono anche usare il modello di threading dell'Apartment, sebbene sia consigliabile usare invece il modello di Threading.

Le interfacce descritte nella tabella seguente forniscono informazioni di riferimento dettagliate per gli sviluppatori di COM+ dispongono.



| Interfacce CRM                                             | Descrizione                                                                                                               |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**ICrmCompensator**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator)                 | Questa interfaccia recapita i record di log non strutturati in Visual C++.                                                           |
| [**ICrmCompensatorVariants**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensatorvariants) | Questa interfaccia recapita i record di log strutturati al compensatore CRM quando si usa Visual Basic.                            |
| [**ICrmFormatLogRecords**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmformatlogrecords)       | Questa interfaccia converte i record del log in formato visualizzabile in modo che possano essere presentati utilizzando uno strumento di monitoraggio generico. |
| [**ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol)                   | Questa interfaccia viene usata dal processo di lavoro CRM e dal compensatore CRM per scrivere record nel log e renderli durevoli.           |
| [**ICrmMonitor**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitor)                         | Questa interfaccia acquisisce uno snapshot dello stato corrente di un CRM e possiede un clerk CRM specifico.                          |
| [**ICrmMonitorClerks**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorclerks)             | Questa interfaccia ottiene informazioni sullo stato dei Clerk.                                                             |
| [**ICrmMonitorLogRecords**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorlogrecords)     | Questa interfaccia monitora i singoli record di log gestiti da uno specifico Clerk CRM per una determinata transazione.            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti Gestione risorse di compensazione COM+](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



