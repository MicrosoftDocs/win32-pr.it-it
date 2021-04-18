---
description: Le funzioni seguenti vengono utilizzate o implementate dai servizi.
ms.assetid: 63666848-cbac-4853-8b91-89303f9854c0
title: Funzioni di servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0431a672e93c94e06a71812471aa3c74d0ac2f96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306532"
---
# <a name="service-functions"></a>Funzioni di servizio

Le funzioni seguenti vengono utilizzate o implementate dai servizi.



| Funzione                                                             | Descrizione                                                                                                                           |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**Gestore**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function)                                           | Funzione di callback definita dall'applicazione utilizzata con la funzione [**RegisterServiceCtrlHandler**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlera) .     |
| [**HandlerEx**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex)                                       | Funzione di callback definita dall'applicazione utilizzata con la funzione [**RegisterServiceCtrlHandlerEx**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlerexa) . |
| [**RegisterServiceCtrlHandler**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlera)     | Registra una funzione per gestire le richieste di controllo del servizio.                                                                              |
| [**RegisterServiceCtrlHandlerEx**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlerexa) | Registra una funzione per gestire le richieste estese di controllo del servizio.                                                                     |
| [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona)                                   | Funzione definita dall'applicazione che funge da punto di partenza per un servizio.                                                      |
| [**SetServiceBits**](/windows/desktop/api/Lmserver/nf-lmserver-setservicebits)                             | Registra un tipo di servizio con Gestione controllo servizi e il servizio Server.                                                     |
| [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus)                         | Aggiorna le informazioni sullo stato di gestione controllo servizi per il servizio chiamante.                                                     |
| [**Impossibile eseguire StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera)     | Connette il thread principale di un processo del servizio a gestione controllo servizi.                                                         |



 

Le funzioni seguenti vengono utilizzate dai programmi che controllano, configurano o interagiscono con i servizi.



| Funzione                                                                 | Descrizione                                                                                                                                 |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga)                       | Modifica i parametri di configurazione di un servizio.                                                                                          |
| [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a)                     | Modifica i parametri di configurazione facoltativi di un servizio.                                                                                 |
| [**CloseServiceHandle**](/windows/desktop/api/Winsvc/nf-winsvc-closeservicehandle)                         | Chiude l'handle specificato a un oggetto di gestione controllo servizi o a un oggetto servizio.                                                        |
| [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice)                                 | Invia un codice di controllo a un servizio.                                                                                                          |
| [**ControlServiceEx**](/windows/desktop/api/Winsvc/nf-winsvc-controlserviceexa)                             | Invia un codice di controllo a un servizio.                                                                                                          |
| [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)                                   | Crea un oggetto servizio e lo aggiunge al database di gestione controllo servizi specificato.                                                     |
| [**DeleteService**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice)                                   | Contrassegna il servizio specificato per l'eliminazione dal database di gestione controllo servizi.                                                         |
| [**EnumDependentServices**](/windows/desktop/api/Winsvc/nf-winsvc-enumdependentservicesa)                   | Recupera il nome e lo stato di ogni servizio che dipende dal servizio specificato.                                                        |
| [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa)                     | Enumera i servizi nel database di gestione controllo servizi specificato in base al livello di informazioni specificato.                             |
| [**GetServiceDisplayName**](/windows/desktop/api/Winsvc/nf-winsvc-getservicedisplaynamea)                   | Recupera il nome visualizzato del servizio specificato.                                                                                        |
| [**GetServiceKeyName**](/windows/desktop/api/Winsvc/nf-winsvc-getservicekeynamea)                           | Recupera il nome del servizio specificato.                                                                                        |
| [**NotifyBootConfigStatus**](/windows/desktop/api/Winsvc/nf-winsvc-notifybootconfigstatus)                 | Segnala lo stato di avvio a gestione controllo servizi.                                                                                     |
| [**NotifyServiceStatusChange**](/windows/desktop/api/Winsvc/nf-winsvc-notifyservicestatuschangea)           | Consente a un'applicazione di ricevere una notifica quando il servizio specificato viene creato o eliminato o quando viene modificato lo stato.                 |
| [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera)                                   | Stabilisce una connessione a gestione controllo servizi nel computer specificato e apre il database di gestione controllo servizi specificato. |
| [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea)                                       | Apre un servizio esistente.                                                                                                                  |
| [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga)                         | Recupera i parametri di configurazione del servizio specificato.                                                                            |
| [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a)                       | Recupera i parametri di configurazione facoltativi del servizio specificato.                                                                   |
| [**QueryServiceDynamicInformation**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicedynamicinformation) | Recupera le informazioni dinamiche correlate all'avvio del servizio corrente.                                                                         |
| [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity)    | Recupera una copia del descrittore di sicurezza associato a un oggetto servizio.                                                               |
| [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex)                     | Recupera lo stato corrente del servizio specificato in base al livello di informazioni specificato.                                             |
| [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity)        | Imposta il descrittore di sicurezza di un oggetto servizio.                                                                                           |
| [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea)                                     | Avvia un servizio.                                                                                                                           |



 

## <a name="obsolete-functions"></a>Funzioni obsolete

Le funzioni seguenti sono obsolete.<dl>

[**EnumServicesStatus**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusa)  
[**LockServiceDatabase**](/windows/desktop/api/Winsvc/nf-winsvc-lockservicedatabase)  
[**QueryServiceLockStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa)  
[**QueryServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatus)  
[**UnlockServiceDatabase**](/windows/desktop/api/Winsvc/nf-winsvc-unlockservicedatabase)  
</dl>

 

 
