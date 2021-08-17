---
title: Name Service
description: Questo argomento illustra in che modo Dynamic Data Exchange di gestione locale consente a un'applicazione server di registrare i nomi dei servizi supportati.
ms.assetid: 4b7e7f43-18aa-4c2e-aa2b-5ce7bb18048f
keywords:
- Windows Interfaccia utente,Dynamic Data Exchange (DDE)
- Dynamic Data Exchange (DDE), nome del servizio
- DDE (Dynamic Data Exchange),name service
- scambio di dati, Dynamic Data Exchange (DDE)
- Windows Interfaccia utente,Dynamic Data Exchange Management Library (DDEML)
- Dynamic Data Exchange Management Library (DDEML), name service
- DDEML (Dynamic Data Exchange Management Library), nome del servizio
- scambio di dati, Dynamic Data Exchange Management Library (DDEML)
- Dynamic Data Exchange (DDE), registrazione del nome del servizio
- DDE (Dynamic Data Exchange), registrazione del nome del servizio
- Dynamic Data Exchange Management Library (DDEML), registrazione del nome del servizio
- DDEML (Dynamic Data Exchange Management Library), registrazione del nome del servizio
- Dynamic Data Exchange (DDE), filtro nome servizio
- DDE (Dynamic Data Exchange),filtro nome servizio
- Dynamic Data Exchange Management Library (DDEML), filtro nome servizio
- DDEML (Dynamic Data Exchange Management Library), filtro nome servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7346bd98979e9bd5a4aa0e43493e975d802875cf8fd0fc79d7bd002bcd0c5494
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118811648"
---
# <a name="name-service"></a>Name Service

La libreria di gestione Dynamic Data Exchange (DDEML) consente a un'applicazione server di registrare i nomi dei servizi supportati e di impedire a DDEML di inviare transazioni [**XTYP \_ CONNECT**](xtyp-connect.md) per i nomi di servizio non supportati alla funzione di callback Dynamic Data Exchange (DDE) del server.

Negli argomenti seguenti viene descritto il servizio dei nomi.

-   [Registrazione del nome del servizio](#service-name-registration)
-   [Filtro nome servizio](#service-name-filter)

## <a name="service-name-registration"></a>Registrazione del nome del servizio

Registrando i nomi dei servizi con DDEML, un server informa altre applicazioni DDE nel sistema che è disponibile un nuovo server. Un server registra un nome di servizio chiamando la [**funzione DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) e specificando un handle di stringa che identifica il nome. In risposta, DDEML invia una transazione [**XTYP \_ REGISTER**](xtyp-register.md) alla funzione di callback di ogni applicazione DDEML nel sistema (ad eccezione di quelle che hanno specificato il flag di filtro SKIP REGISTRATIONS CBF nella \_ funzione \_ [**DdeInitialize).**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) La **transazione XTYP \_ REGISTER** passa due handle di stringa a una funzione di callback: il primo identifica la stringa che specifica il nome del servizio di base e il secondo identifica la stringa che specifica il servizio specifico dell'istanza. Un client usa in genere il nome del servizio di base in un elenco di server disponibili, in modo che l'utente possa selezionare un server dall'elenco. Il client usa il nome del servizio specifico dell'istanza per stabilire una conversazione con un'istanza specifica di un'applicazione server, se sono in esecuzione più istanze.

Un server può usare [**DdeNameService per**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) annullare la registrazione di un nome di servizio. Questa funzione fa sì che DDEML invii transazioni [**XTYP \_ UNREGISTER**](xtyp-unregister.md) alle altre applicazioni DDE nel sistema, informandole che non possono più usare il nome per stabilire conversazioni.

Un server deve chiamare [**DdeNameService per**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) registrare i nomi dei servizi subito dopo aver chiamato [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea). Un server deve annullare la registrazione dei nomi dei servizi **usando DdeNameService** subito prima di chiamare la [**funzione DdeUninitialize.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize)

## <a name="service-name-filter"></a>Filtro nome servizio

Oltre a registrare i nomi dei servizi, [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) consente a un server di attivare o disattivare il filtro dei nomi di servizio. Quando un server disattiva il filtro del nome del servizio, DDEML invia la transazione [**XTYP \_ CONNECT**](xtyp-connect.md) alla funzione di callback DDE del server ogni volta che un client chiama la funzione [**DdeConnect,**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) indipendentemente dal nome del servizio specificato nella funzione. Quando un server attiva il filtro del nome del servizio, DDEML invia la transazione **XTYP \_ CONNECT** al server solo quando **DdeConnect** specifica un nome di servizio specificato dal server in una chiamata a **DdeNameService**.

Per impostazione predefinita, il filtro del nome del servizio è on quando un'applicazione chiama [**DdeInitialize.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) Questa impostazione predefinita impedisce a DDEML di inviare la [**transazione XTYP \_ CONNECT**](xtyp-connect.md) a un server prima che il server abbia creato gli handle di stringa di cui necessita. Un server può disattivare il filtro dei nomi di servizio specificando il flag FILTEROFF DNS in una chiamata \_ a [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice). Il \_ flag FILTERON DNS attiva il filtro.

 

 




