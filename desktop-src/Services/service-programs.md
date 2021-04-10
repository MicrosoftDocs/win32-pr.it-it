---
description: Un programma del servizio contiene codice eseguibile per uno o più servizi.
ms.assetid: 697db543-6149-46ac-add3-c8c6ca3aadbe
title: Programmi di servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b5e78574f46549956325bc19ffb6d51f4a114ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884830"
---
# <a name="service-programs"></a>Programmi di servizio

Un *programma del servizio* contiene codice eseguibile per uno o più servizi. Un programma di servizio creato con il processo del servizio di tipo \_ Win32 \_ own \_ contiene il codice per un solo servizio. Un programma di servizio creato con il \_ processo di condivisione Win32 del servizio di tipo contiene il \_ \_ codice per più di un servizio, consentendo loro di condividere il codice. Un esempio di un programma di servizio che esegue questa operazione è il processo host del servizio generico, Svchost.exe, che ospita servizi Windows interni. Si noti che Svchost.exe è riservata per l'utilizzo da parte del sistema operativo e non deve essere utilizzata da servizi non Windows. Gli sviluppatori devono invece implementare i propri programmi di hosting dei servizi.

Un programma del servizio può essere configurato per l'esecuzione nel contesto di un account utente dal dominio predefinito (locale), primario o attendibile. Può anche essere configurato per l'esecuzione in un [account utente di servizio](service-user-accounts.md)speciale.

Negli argomenti seguenti vengono descritti i requisiti di interfaccia di [Gestione controllo servizi](service-control-manager.md) (SCM) che un programma del servizio deve includere:

-   [Punto di ingresso del servizio](service-entry-point.md)
-   [Funzione ServiceMain del servizio](service-servicemain-function.md)
-   [Funzione Handler di controllo dei servizi](service-control-handler-function.md)

Questi argomenti non si applicano ai servizi del driver. Per informazioni sui requisiti di interfaccia dei servizi driver, vedere Windows Driver Kit (WDK).

Un servizio viene eseguito come processo in background che può influire sulle prestazioni del sistema, sulla velocità di risposta, sull'efficienza energetica e sulla sicurezza. Per le linee guida sull'ottimizzazione dei servizi, vedere [sviluppo di processi in background efficienti per Windows](/windows-hardware/drivers/kernel/implementing-power-management). Gli argomenti seguenti descrivono considerazioni aggiuntive sulla programmazione:

-   [Transizioni di stato del servizio](service-status-transitions.md)
-   [Ricezione di eventi in un servizio](receiving-events-in-a-service.md)
-   [Servizi multithreading](multithreaded-services.md)
-   [Servizi e registro di sistema](services-and-the-registry.md)
-   [Servizi e unità reindirizzate](services-and-redirected-drives.md)
-   [Eventi trigger del servizio](service-trigger-events.md)

Si noti che se il programma del servizio funziona come server RPC, deve usare endpoint dinamici e l'autenticazione reciproca.

 

 
