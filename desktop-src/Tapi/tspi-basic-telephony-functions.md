---
description: Tutti i provider di servizi devono implementare le funzioni di telefonia di base.
ms.assetid: 4250f3a0-a66a-4a6e-8566-d71be7463179
title: Funzioni di telefonia di base TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5308def0c94df9fa59f2022bf25c4dbb1843e2f8
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524155"
---
# <a name="tspi-basic-telephony-functions"></a>Funzioni di telefonia di base TSPI

Tutti i provider di servizi devono implementare le funzioni di telefonia di base. Di seguito è riportato un elenco di tali funzioni per categoria. Una funzione viene identificata *come asincrona* se indica il completamento in un messaggio REPLY all'applicazione. Se la funzione restituisce sempre immediatamente il risultato, la funzione viene considerata *sincrona.*

-   [Indirizzi](#addresses)
-   [Risposta alle chiamate in ingresso](#answering-incoming-calls)
-   [Funzioni di rilascio delle chiamate](#call-drop-functions)
-   [Chiamare stati ed eventi](#call-states-and-events)
-   [Stato e funzionalità della riga](#line-status-and-capabilities)
-   [Negoziazione della versione della riga](#line-version-negotiation)
-   [Esecuzione di chiamate](#making-calls)
-   [Apertura e chiusura di dispositivi line](#opening-and-closing-line-devices)
-   [Negoziazione della versione del telefono](#phone-version-negotiation)
-   [Inizializzazione e arresto di TSP](#tsp-initialization-and-shutdown)

## <a name="tsp-initialization-and-shutdown"></a>Inizializzazione e arresto di TSP



|  Funzione                                                         |   Descrizione                                                        |
|-----------------------------------------------------------|-----------------------------------------------------------|
| [**Provider \_ TUISPIInstalla**](/windows/win32/api/tspi/nf-tspi-tuispi_providerinstall) | Installa un TSP. Synchronous.                              |
| [**Provider \_ TSPIInstalla**](/windows/win32/api/tspi/nf-tspi-tspi_providerinstall)     | Installa TSP. Obsoleto con la versione 2.0. Synchronous. |
| [**Provider \_ TSPIInit**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit)           | Inizializza TSP. Synchronous.                         |
| [**Provider \_ TSPIShutdown**](/windows/win32/api/tspi/nf-tspi-tspi_providershutdown)   | Arresta il provider di servizi.                          |
| [**Provider \_ TUISPIRimuovi**](/windows/win32/api/tspi/nf-tspi-tuispi_providerremove)   | Rimuove un TSP. Synchronous.                               |
| [**Provider \_ TSPIRimuovi**](/windows/win32/api/tspi/nf-tspi-tspi_providerremove)       | Rimuove un TSP. Obsoleto con la versione 2.0. Synchronous.    |



 

## <a name="phone-version-negotiation"></a>Negoziazione della versione del telefono



|  Funzione                                                         |   Descrizione                                                        |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**Telefono \_ TSPINegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiatetspiversion) | Restituisce la versione SPI più elevata con cui il provider di servizi può operare per questo dispositivo. |



 

## <a name="line-version-negotiation"></a>Negoziazione della versione della riga



|  Funzione                                                         |   Descrizione                                                        |
|-------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**Riga \_ TSPINegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) | Consente a un'applicazione di negoziare una versione TSPI da usare con un determinato dispositivo di linea. Synchronous. |



 

## <a name="line-status-and-capabilities"></a>Stato e funzionalità della riga



|  Funzione                                                         |   Descrizione                                                        |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Riga \_ TSPIGetDevCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps)                 | Restituisce le funzionalità di un dispositivo linea specificato. Synchronous.                                                                                                  |
| [**Riga \_ TSPIGetDevConfig**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevconfig)             | Restituisce la configurazione di un dispositivo di flusso multimediale. Synchronous.                                                                                                   |
| [**Riga \_ TSPIGetLineDevStatus**](/windows/win32/api/tspi/nf-tspi-tspi_linegetlinedevstatus)     | Restituisce lo stato corrente del dispositivo open line specificato. Synchronous.                                                                                         |
| [**TSPI \_ lineSetDevConfig**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdevconfig)             | Imposta la configurazione del dispositivo del flusso multimediale specificato. Synchronous.                                                                                      |
| [**TSPI \_ lineSetStatusMessages**](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages)   | Specifica le modifiche di stato per cui l'applicazione deve ricevere una notifica. Synchronous.                                                                      |
| [**TSPI \_ lineGetID**](/windows/win32/api/tspi/nf-tspi-tspi_linegetid)                           | Recupera un ID dispositivo associato alla riga aperta, all'indirizzo o alla chiamata specificata. Synchronous.                                                                  |
| [**Riga \_ TSPIGetIcon**](/windows/win32/api/tspi/nf-tspi-tspi_linegeticon)                       | Consente a un'applicazione di recuperare un'icona da visualizzare all'utente. Synchronous.                                                                                |
| [**LineConfigDialog TUISPI \_**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog)         | Fa in modo che il provider del dispositivo linea specificato visualizza una finestra di dialogo che consente all'utente di configurare i parametri correlati al dispositivo linea. Synchronous. |
| [**LINEISPI \_ lineConfigDialogEdit**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialogedit) | Visualizza una finestra di dialogo che consente all'utente di modificare le informazioni di configurazione per un dispositivo linea. Synchronous.                                                    |



 

## <a name="addresses"></a>Indirizzi



|  Funzione                                                         |   Descrizione                                                        |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [**TSPI \_ lineGetAddressCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps)     | Restituisce le funzionalità di telefonia di un indirizzo. Synchronous.                           |
| [**Riga \_ TSPIGetAddressStatus**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressstatus) | Restituisce lo stato corrente di un indirizzo specificato. Synchronous.                              |
| [**TSPI \_ lineGetNumAddressIDs**](/windows/win32/api/tspi/nf-tspi-tspi_linegetnumaddressids) | Recupera il numero di identificatori di indirizzo supportati nella riga indicata.             |
| [**TSPI \_ lineGetAddressID**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressid)         | Recupera l'ID indirizzo di un indirizzo specificato usando un formato alternativo. Synchronous. |



 

## <a name="opening-and-closing-line-devices"></a>Apertura e chiusura di dispositivi line



|  Funzione                                                         |   Descrizione                                                        |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**Riga \_ TSPIApri**](/windows/win32/api/tspi/nf-tspi-tspi_lineopen)   | Apre un dispositivo linea specificato per fornire il monitoraggio e/o il controllo successivi della linea. Synchronous. |
| [**Riga \_ TSPIChiudi**](/windows/win32/api/tspi/nf-tspi-tspi_lineclose) | Chiude un dispositivo di linea aperto specificato. Synchronous.                                                        |



 

## <a name="call-states-and-events"></a>Chiamare stati ed eventi



|  Funzione                                                         |   Descrizione                                                        |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**Riga \_ TSPIGetCallInfo**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallinfo)       | Restituisce informazioni fisse su una chiamata. Synchronous.                                |
| [**TSPI \_ lineGetCallStatus**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallstatus)   | Restituisce informazioni complete sullo stato della chiamata per la chiamata specificata. Synchronous.       |
| [**TSPI \_ lineSetAppSpecific**](/windows/win32/api/tspi/nf-tspi-tspi_linesetappspecific) | Imposta il campo specifico dell'applicazione della struttura delle informazioni di una chiamata. Synchronous. |



 

## <a name="making-calls"></a>Esecuzione di chiamate



|  Funzione                                                         |   Descrizione                                                        |
|-------------------------------------------------|------------------------------------------------------------------------|
| [**Riga \_ TSPIMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall) | Esegue una chiamata in uscita e restituisce un handle di chiamata. Asincrona. |
| [**\_LineDial TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linedial)         | Dial (parti di uno o più) indirizzi dialable. Asincrona.         |



 

## <a name="answering-incoming-calls"></a>Risposta alle chiamate in ingresso



|  Funzione                                                         |   Descrizione                                                        |
|---------------------------------------------|-----------------------------------------|
| [**Riga \_ TSPIAnswer**](/windows/win32/api/tspi/nf-tspi-tspi_lineanswer) | Risponde a una chiamata in ingresso. Asincrona. |



 

## <a name="call-drop-functions"></a>Funzioni di rilascio delle chiamate



|  Funzione                                                         |   Descrizione                                                        |
|-----------------------------------------|---------------------------------------------------------------------------|
| [**LineDrop \_ TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) | Disconnette una chiamata o abbandona un tentativo di chiamata in corso. Asincrona. |



 

 

 
