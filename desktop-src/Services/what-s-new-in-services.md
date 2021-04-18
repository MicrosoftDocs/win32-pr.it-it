---
description: Windows 7 e Windows Server 2008 R2 includono i seguenti elementi di programmazione nuovi e aggiornati per i servizi di.
ms.assetid: 4be7e244-ad4c-440d-b04e-23afb4c7ddf2
title: Novità dei servizi per Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51bd2e8bfa5426447e24485ed026f27e90fdcaa1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318218"
---
# <a name="whats-new-in-services-for-windows-7"></a>Novità dei servizi per Windows 7

Windows 7 e Windows Server 2008 R2 includono i seguenti elementi di programmazione nuovi e aggiornati per i servizi di.

## <a name="new-capabilities"></a>Nuove funzionalità

Un servizio può registrarsi per l'avvio o l'arresto quando si verifica un evento trigger. In questo modo si elimina la necessità di avviare i servizi all'avvio del sistema o per i servizi per eseguire il polling o attendere attivamente un evento. un servizio può essere avviato quando necessario, anziché iniziare automaticamente indipendentemente dal fatto che esista o meno lavoro da eseguire. Per altre informazioni, vedere [eventi del trigger del servizio](service-trigger-events.md).

## <a name="updated-functions"></a>Funzioni aggiornate



| Funzione                                                        | Descrizione                                                                                                                                                                                                                                                                                |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga)<br/>   | Modifica i parametri di configurazione di un servizio. Questa funzione supporta gli account del servizio gestito e gli account virtuali. Per ulteriori informazioni, vedere la [Guida dettagliata agli account di servizio](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd548356(v=ws.10)).<br/>                                      |
| [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a)<br/> | Modifica i parametri di configurazione facoltativi di un servizio. Questa funzione supporta nuovi livelli di informazioni di configurazione per i gruppi di processori e gli eventi di trigger del servizio.<br/>                                                                                                        |
| [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)<br/>               | Crea un oggetto servizio e lo aggiunge al database di gestione controllo servizi specificato. Questa funzione supporta gli account del servizio gestito e gli account virtuali. Per ulteriori informazioni, vedere la [Guida dettagliata agli account di servizio](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd548356(v=ws.10)).<br/> |
| [**HandlerEx**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex)<br/>                       | Funzione di callback definita dall'applicazione utilizzata con la funzione [**RegisterServiceCtrlHandlerEx**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlerexa) . Questa funzione di callback supporta nuovi codici di controllo estesi per le modifiche dell'ora di sistema e gli eventi di attivazione del servizio.<br/>                            |
| [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a)<br/>   | Recupera i parametri di configurazione facoltativi di un servizio. Questa funzione supporta nuovi livelli di informazioni di configurazione per i gruppi di processori e gli eventi di trigger del servizio.<br/>                                                                                                      |
| [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus)<br/>         | Aggiorna le informazioni sullo stato di gestione controllo servizi per il servizio chiamante. Questa funzione supporta nuovi codici di controllo estesi per le modifiche dell'ora di sistema e gli eventi di attivazione del servizio.<br/>                                                                                         |



 

## <a name="new-structures"></a>Nuove strutture



| Struttura                                                                                       | Descrizione                                                            |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**informazioni sul servizio \_ TIMECHANGE \_**](/windows/desktop/api/winsvc/ns-winsvc-service_timechange_info)<br/>                         | Contiene le impostazioni di modifica dell'ora di sistema. <br/>                      |
| [**TRIGGER del servizio \_**](/windows/desktop/api/winsvc/ns-winsvc-service_trigger)<br/>                                          | Rappresenta un evento del trigger del servizio.<br/>                         |
| [**\_informazioni sul trigger del servizio \_**](/windows/desktop/api/winsvc/ns-winsvc-service_trigger_info)<br/>                               | Contiene informazioni sull'evento trigger per un servizio.<br/>           |
| [**\_ \_ \_ elemento dati specifico dell'attivazione del servizio \_**](/windows/desktop/api/winsvc/ns-winsvc-service_trigger_specific_data_item)<br/> | Contiene dati specifici del trigger per un evento di attivazione del servizio.<br/> |



 

 

