---
description: Windows 7 e Windows Server 2008 R2 includono gli elementi di programmazione nuovi e aggiornati seguenti per i servizi.
ms.assetid: 4be7e244-ad4c-440d-b04e-23afb4c7ddf2
title: Novità dei servizi per Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e55cf7aae33522f141fbac68b727842b3dd2fbde21ba97fa46407cf8af6c2ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117966639"
---
# <a name="whats-new-in-services-for-windows-7"></a>Novità dei servizi per Windows 7

Windows 7 e Windows Server 2008 R2 includono gli elementi di programmazione nuovi e aggiornati seguenti per i servizi.

## <a name="new-capabilities"></a>Nuove funzionalità

Un servizio può essere registrato per essere avviato o arrestato quando si verifica un evento trigger. In questo modo si elimina la necessità di avviare i servizi all'avvio del sistema o di eseguire il polling dei servizi o di attendere attivamente un evento. un servizio può essere avviato quando è necessario, invece di avviarlo automaticamente indipendentemente dal fatto che sia necessario eseguire o meno operazioni. Per altre informazioni, vedere [Eventi trigger del servizio](service-trigger-events.md).

## <a name="updated-functions"></a>Funzioni aggiornate



| Funzione                                                        | Descrizione                                                                                                                                                                                                                                                                                |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga)<br/>   | Modifica i parametri di configurazione di un servizio. Questa funzione supporta gli account del servizio gestiti e gli account virtuali. Per altre informazioni, vedere Guida dettagliata agli account [del servizio](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd548356(v=ws.10)).<br/>                                      |
| [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a)<br/> | Modifica i parametri di configurazione facoltativi di un servizio. Questa funzione supporta nuovi livelli di informazioni di configurazione per i gruppi di processori e gli eventi trigger del servizio.<br/>                                                                                                        |
| [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)<br/>               | Crea un oggetto servizio e lo aggiunge al database di Gestione controllo servizi specificato. Questa funzione supporta gli account del servizio gestiti e gli account virtuali. Per altre informazioni, vedere Guida dettagliata agli account [del servizio](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd548356(v=ws.10)).<br/> |
| [**HandlerEx**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex)<br/>                       | Funzione di callback definita dall'applicazione usata con la [**funzione RegisterServiceCtrlHandlerEx.**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlerexa) Questa funzione di callback supporta nuovi codici di controllo estesi per le modifiche all'ora di sistema e gli eventi trigger del servizio.<br/>                            |
| [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a)<br/>   | Recupera i parametri di configurazione facoltativi di un servizio. Questa funzione supporta nuovi livelli di informazioni di configurazione per i gruppi di processori e gli eventi trigger del servizio.<br/>                                                                                                      |
| [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus)<br/>         | Aggiorna le informazioni sullo stato del gestore di controllo del servizio per il servizio chiamante. Questa funzione supporta nuovi codici di controllo estesi per le modifiche dell'ora di sistema e gli eventi trigger del servizio.<br/>                                                                                         |



 

## <a name="new-structures"></a>Nuove strutture



| Struttura                                                                                       | Descrizione                                                            |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**INFORMAZIONI \_ SUL TIMECHANGE \_ DEL SERVIZIO**](/windows/desktop/api/winsvc/ns-winsvc-service_timechange_info)<br/>                         | Contiene le impostazioni di modifica dell'ora di sistema. <br/>                      |
| [**TRIGGER DEL \_ SERVIZIO**](/windows/desktop/api/winsvc/ns-winsvc-service_trigger)<br/>                                          | Rappresenta un evento trigger del servizio.<br/>                         |
| [**INFORMAZIONI \_ SUL TRIGGER DEL \_ SERVIZIO**](/windows/desktop/api/winsvc/ns-winsvc-service_trigger_info)<br/>                               | Contiene informazioni sugli eventi trigger per un servizio.<br/>           |
| [**ELEMENTO DATI \_ SPECIFICO DEL TRIGGER DEL \_ \_ \_ SERVIZIO**](/windows/desktop/api/winsvc/ns-winsvc-service_trigger_specific_data_item)<br/> | Contiene dati specifici del trigger per un evento trigger del servizio.<br/> |



 

 

