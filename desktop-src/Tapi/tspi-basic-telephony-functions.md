---
description: Tutti i provider di servizi devono implementare funzioni di telefonia di base.
ms.assetid: 4250f3a0-a66a-4a6e-8566-d71be7463179
title: Funzioni di telefonia Basic TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6276be51482620af32650ad1625eea97bddb8e5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885242"
---
# <a name="tspi-basic-telephony-functions"></a>Funzioni di telefonia Basic TSPI

Tutti i provider di servizi devono implementare funzioni di telefonia di base. Di seguito è riportato un elenco di tali funzioni per categoria. Una funzione viene identificata come *asincrona* se indica il completamento in un messaggio di risposta all'applicazione. Se la funzione restituisce sempre il risultato immediatamente, la funzione viene considerata *sincrona*.

-   [Indirizzi](#addresses)
-   [Risposta alle chiamate in ingresso](#answering-incoming-calls)
-   [Funzioni drop di chiamata](#call-drop-functions)
-   [Stati e eventi di chiamata](#call-states-and-events)
-   [Stato e funzionalità della linea](#line-status-and-capabilities)
-   [Negoziazione della versione della linea](#line-version-negotiation)
-   [Esecuzione di chiamate](#making-calls)
-   [Apertura e chiusura di dispositivi linea](#opening-and-closing-line-devices)
-   [Negoziazione della versione del telefono](#phone-version-negotiation)
-   [Inizializzazione e arresto di un TSP](#tsp-initialization-and-shutdown)

## <a name="tsp-initialization-and-shutdown"></a>Inizializzazione e arresto di un TSP



|                                                           |                                                           |
|-----------------------------------------------------------|-----------------------------------------------------------|
| [**\_PROVIDERINSTALL TUISPI**](/windows/win32/api/tspi/nf-tspi-tuispi_providerinstall) | Installa un TSP. Synchronous.                              |
| [**\_PROVIDERINSTALL TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_providerinstall)     | Installa il TSP. Obsoleto con la versione 2,0. Synchronous. |
| [**\_PROVIDERINIT TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit)           | Inizializza il TSP. Synchronous.                         |
| [**\_PROVIDERSHUTDOWN TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_providershutdown)   | Arresta il provider di servizi.                          |
| [**\_PROVIDERREMOVE TUISPI**](/windows/win32/api/tspi/nf-tspi-tuispi_providerremove)   | Rimuove un TSP. Synchronous.                               |
| [**\_PROVIDERREMOVE TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_providerremove)       | Rimuove un TSP. Obsoleto con la versione 2,0. Synchronous.    |



 

## <a name="phone-version-negotiation"></a>Negoziazione della versione del telefono



|                                                                           |                                                                                         |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**\_PHONENEGOTIATETSPIVERSION TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiatetspiversion) | Restituisce la versione SPI più elevata con cui il provider di servizi può operare per questo dispositivo. |



 

## <a name="line-version-negotiation"></a>Negoziazione della versione della linea



|                                                                         |                                                                                                 |
|-------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**\_LINENEGOTIATETSPIVERSION TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) | Consente a un'applicazione di negoziare una versione di TSPI da usare con un dispositivo a linee specificato. Synchronous. |



 

## <a name="line-status-and-capabilities"></a>Stato e funzionalità della linea



|                                                                     |                                                                                                                                                                |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_LINEGETDEVCAPS TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps)                 | Restituisce le funzionalità di una determinata periferica di linea. Synchronous.                                                                                                  |
| [**\_LINEGETDEVCONFIG TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevconfig)             | Restituisce la configurazione di un dispositivo del flusso multimediale. Synchronous.                                                                                                   |
| [**\_LINEGETLINEDEVSTATUS TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linegetlinedevstatus)     | Restituisce lo stato corrente del dispositivo a linee aperte specificato. Synchronous.                                                                                         |
| [**\_LINESETDEVCONFIG TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdevconfig)             | Imposta la configurazione del dispositivo del flusso multimediale specificato. Synchronous.                                                                                      |
| [**\_LINESETSTATUSMESSAGES TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages)   | Specifica le modifiche dello stato per le quali l'applicazione deve ricevere una notifica. Synchronous.                                                                      |
| [**\_LINEGETID TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linegetid)                           | Recupera un ID dispositivo associato alla riga aperta, all'indirizzo o alla chiamata specificata. Synchronous.                                                                  |
| [**\_LINEGETICON TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linegeticon)                       | Consente a un'applicazione di recuperare un'icona da visualizzare all'utente. Synchronous.                                                                                |
| [**\_LINECONFIGDIALOG TUISPI**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog)         | Fa in modo che il provider del dispositivo a linee specificato visualizzi una finestra di dialogo che consenta all'utente di configurare i parametri correlati al dispositivo della linea. Synchronous. |
| [**\_LINECONFIGDIALOGEDIT TUISPI**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialogedit) | Visualizza una finestra di dialogo che consente all'utente di modificare le informazioni di configurazione per un dispositivo a linee. Synchronous.                                                    |



 

## <a name="addresses"></a>Indirizzi



|                                                                 |                                                                                          |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [**\_LINEGETADDRESSCAPS TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps)     | Restituisce le funzionalità di telefonia di un indirizzo. Synchronous.                           |
| [**\_LINEGETADDRESSSTATUS TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressstatus) | Restituisce lo stato corrente di un indirizzo specificato. Synchronous.                              |
| [**\_LINEGETNUMADDRESSIDS TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linegetnumaddressids) | Recupera il numero di identificatori di indirizzo supportati sulla riga indicata.             |
| [**\_LINEGETADDRESSID TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressid)         | Recupera l'ID di un indirizzo specificato utilizzando un formato alternativo. Synchronous. |



 

## <a name="opening-and-closing-line-devices"></a>Apertura e chiusura di dispositivi linea



|                                           |                                                                                                            |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**\_LINEOPEN TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_lineopen)   | Apre un dispositivo a linee specificato per fornire il monitoraggio e/o il controllo successivo della riga. Synchronous. |
| [**\_LINECLOSE TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_lineclose) | Chiude un dispositivo a linee aperte specificato. Synchronous.                                                        |



 

## <a name="call-states-and-events"></a>Stati e eventi di chiamata



|                                                             |                                                                                     |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**\_LINEGETCALLINFO TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallinfo)       | Restituisce informazioni fisse su una chiamata. Synchronous.                                |
| [**\_LINEGETCALLSTATUS TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallstatus)   | Restituisce informazioni complete sullo stato della chiamata per la chiamata specificata. Synchronous.       |
| [**\_LINESETAPPSPECIFIC TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linesetappspecific) | Imposta il campo specifico dell'applicazione della struttura di informazioni di una chiamata. Synchronous. |



 

## <a name="making-calls"></a>Esecuzione di chiamate



|                                                 |                                                                        |
|-------------------------------------------------|------------------------------------------------------------------------|
| [**\_LINEMAKECALL TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall) | Esegue una chiamata in uscita e restituisce un handle di chiamata per l'oggetto. Asincrona. |
| [**\_LINEDIAL TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linedial)         | Dials (parti di uno o più) indirizzi di connessione. Asincrona.         |



 

## <a name="answering-incoming-calls"></a>Risposta alle chiamate in ingresso



|                                             |                                         |
|---------------------------------------------|-----------------------------------------|
| [**\_LINEANSWER TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_lineanswer) | Risponde a una chiamata in ingresso. Asincrona. |



 

## <a name="call-drop-functions"></a>Funzioni drop di chiamata



|                                         |                                                                           |
|-----------------------------------------|---------------------------------------------------------------------------|
| [**\_LINEDROP TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) | Disconnette una chiamata o abbandona un tentativo di chiamata in corso. Asincrona. |



 

 

 
