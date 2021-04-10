---
title: Uso dell'API client di Servizi di distribuzione Windows
description: Negli ambienti in cui non è possibile usare una soluzione standard di servizi di distribuzione Windows (WDS) per installare Windows, l'API del client WDS consente agli sviluppatori di scrivere applicazioni di distribuzione personalizzate.
ms.assetid: abe2a7c7-989a-456e-80df-90d5b816db38
keywords:
- Servizi di distribuzione Windows servizi di distribuzione Windows, utilizzo dell'API client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 872422a5c84bf1d8ea7c3688b122ba2389c1e968
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046889"
---
# <a name="using-the-windows-deployment-services-client-api"></a>Uso dell'API client di Servizi di distribuzione Windows

Negli ambienti in cui non è possibile usare una soluzione standard di servizi di distribuzione Windows (WDS) per installare Windows, l'API del client WDS consente agli sviluppatori di scrivere applicazioni di distribuzione personalizzate. Le applicazioni possono usare questa API per comunicare con il server WDS per ottenere informazioni sulle immagini di sistema disponibili dal server. Le applicazioni client WDS personalizzate devono rispettare le linee guida seguenti.

## <a name="install-the-wds-role-on-the-server"></a>Installare il ruolo WDS nel server

-   Servizi di distribuzione Windows (WDS) è la versione modificata di servizi di installazione remota (RIS), per implementare soluzioni client WDS personalizzate sarà necessario il ruolo server WDS nel server.
-   WDS sostituisce RIS come componente standard a partire da Windows Server 2008 e Windows Server 2003 con Service Pack 2 (SP2).
-   È necessario aggiornare il server RIS a WDS in Windows Server 2003 con Service Pack 1 (SP1). È possibile installare il ruolo server WDS con [Windows Automated Installation Kit (WAIK)](https://www.microsoft.com/download/details.aspx?id=10333).

## <a name="start-windows-pe-20"></a>Avviare Windows PE 2,0

È necessario avviare Windows PE 2,0, se non è già stato avviato. Il client WDS e le DLL di supporto vengono caricati solo da setup.exe quando si trova nella fase Microsoft Ambiente preinstallazione di Windows (Windows PE 2,0) dell'elaborazione del programma di installazione.

-   Quando un nuovo computer è connesso alla rete, è possibile usare la tecnologia PXE (Preboot Execution Environment) incorporata per scaricare il programma di avvio di rete. Per ulteriori informazioni sull'avvio PXE di un computer per l'installazione di Windows, vedere [la guida dettagliata all'aggiornamento di servizi di distribuzione Windows](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10)).
-   Un'immagine di avvio RAMDISK di Windows PE 2,0 può essere archiviata in. Formato WIM e scaricato come parte del processo di avvio di rete. Windows PE può quindi essere caricato ed eseguito direttamente da tale supporto.

## <a name="open-a-session-with-the-wds-server"></a>Aprire una sessione con il server WDS

Il client WDS deve aprire una sessione con un server WDS.

-   Usare la funzione [**WdsCliCreateSession**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclicreatesession) per aprire una sessione con un server WDS. Questa funzione accetta il nome o l'indirizzo IP del server e riceve l'indirizzo dell'handle per la sessione del client WDS.
-   Se l'apertura della sessione con il server richiede l'autenticazione del client WDS, l'applicazione deve fornire l'indirizzo di una struttura dell' [**\_ \_ interfaccia**](/windows/win32/api/wdsclientapi/ns-wdsclientapi-wds_cli_cred) della riga di comando di WDS contenente le credenziali client quando viene chiamata la funzione [**WdsCliCreateSession**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclicreatesession) . L'applicazione può usare la funzione [**WdsCliAuthorizeSession**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscliauthorizesession) per convertire una sessione anonima in una sessione autenticata.
-   Quando la sessione aperta con la funzione [**WdsCliCreateSession**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclicreatesession) non è più necessaria, l'applicazione deve usare la funzione [**WdsCliClose**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscliclose) per chiudere l'handle e rilasciare le risorse utilizzate dalla sessione.

## <a name="enumerate-system-images-on-the-wds-server"></a>Enumerare le immagini di sistema nel server WDS

Il client WDS può usare l'API per enumerare le immagini di sistema nel server WDS.

-   Utilizzare la funzione [**WdsCliFindFirstImage**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclifindfirstimage) per ottenere un handle per la prima immagine e per inizializzare l'enumerazione delle immagini nel server WDS.
-   Utilizzare la funzione [**WdsCliFindNextImage**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclifindnextimage) per incrementare l'enumerazione avviata dalla funzione [**WdsCliFindFirstImage**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclifindfirstimage) . La funzione **WdsCliFindNextImage** Ottiene l'handle per l'immagine successiva.
-   Usare la funzione [**WdsCliGetImageIndex**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimageindex) per ottenere l'indice dell'immagine per l'immagine corrente. Questo valore è valido solo fino a quando le funzioni [**WdsCliFindNextImage**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclifindnextimage) o [**WdsCliClose**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscliclose) non vengono riutilizzate.
-   Usare la funzione [**WdsCliGetEnumerationFlags**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetenumerationflags) per ottenere i flag informativi sul filtro delle immagini.

## <a name="get-information-about-images"></a>Ottenere informazioni sulle immagini

Il client WDS può usare l'API per ottenere informazioni sulle immagini in un server WDS. Le funzioni seguenti ottengono informazioni sull'immagine corrente. Poiché le funzioni [**WdsCliFindFirstImage**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclifindfirstimage) e [**WdsCliFindNextImage**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclifindnextimage) modificano il valore dell'handle dell'immagine corrente, l'applicazione deve archiviare tutte le informazioni ottenute e sarà necessaria in futuro prima di chiamare di nuovo le funzioni **WdsCliFindFirstImage** o **WdsCliFindNextImage** .

-   Utilizzare la funzione [**WdsCliGetImageArchitecture**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagearchitecture) per ottenere l'architettura del processore dell'immagine corrente.
-   Usare la funzione [**WdsCliGetImagePath**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagepath) per ottenere il percorso relativo del file di immagine che contiene l'immagine corrente.
-   Usare la funzione [**WdsCliGetImageSize**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagesize) per ottenere le dimensioni dell'immagine.
-   Usare la funzione [**WdsCliGetImageVersion**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimageversion) per ottenere la versione dell'immagine.
-   Utilizzare la funzione [**WdsCliGetImageLanguage**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagelanguage) per ottenere la lingua predefinita dell'immagine corrente.
-   Usare la funzione [**WdsCliGetImageLanguages**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagelanguages) per ottenere una matrice di linguaggi supportati dall'immagine corrente.
-   Usare [**WdsCliGetImageLastModifiedTime**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagelastmodifiedtime) restituisce l'ora dell'Ultima modifica per l'immagine corrente.
-   Usare la funzione [**WdsCliGetImageName**](/windows/win32/api/WdsClientApi/nf-wdsclientapi-wdscligetimagename) per ottenere il nome dell'immagine corrente.
-   Usare la funzione [**WdsCliGetImageDescription**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagedescription) per ottenere la descrizione dell'immagine corrente.
-   Usare la funzione [**WdsCliGetImageGroup**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagegroup) per ottenere il nome del gruppo di immagini per l'immagine corrente.
-   Usare la funzione [**WdsCliGetImageHalName**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagehalname) per ottenere il nome Hal (Hardware Abstraction Layer) per l'immagine corrente.

## <a name="log-wds-client-events"></a>Registra eventi client WDS

La funzionalità di registrazione della libreria client WDS consente l'invio degli eventi di avanzamento dell'installazione dal client al server WDS.

-   Utilizzare la funzione [**WdsCliInitializeLog**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscliinitializelog) per inizializzare il log della sessione client di WDS.
-   Utilizzare la funzione [**WdsCliLog**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclilog) per scrivere messaggi di evento nel log del server WDS.
-   In Windows Server 2008, il server di servizi di distribuzione Windows scrive gli eventi client in un registro eventi specifico dell'applicazione, visualizzabile tramite eventvwr.exe e il log di traccia di debug. In Windows Server 2003 con la registrazione debug abilitata, il server WDS scriverà gli eventi client nel file di log che si trova in% windir% \\ Tracing \\ WDSServer. log. Per acquisire questi eventi, è necessario abilitare la registrazione del client WDS sul server.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sull'API di servizi di distribuzione Windows](about-the-windows-deployment-services-api.md)
</dt> <dt>

[Uso dell'API server di Servizi di distribuzione Windows](using-the-windows-deployment-services-server-api.md)
</dt> </dl>

 

 