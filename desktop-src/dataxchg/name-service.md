---
title: Nome servizio
description: In questo argomento viene illustrato il modo in cui la libreria di gestione Dynamic Data Exchange rende possibile a un'applicazione server di registrare i nomi di servizio supportati.
ms.assetid: 4b7e7f43-18aa-4c2e-aa2b-5ce7bb18048f
keywords:
- Interfaccia utente di Windows, Dynamic Data Exchange (DDE)
- Dynamic Data Exchange (DDE), servizio nome
- DDE (Dynamic Data Exchange), servizio nome
- scambio di dati, Dynamic Data Exchange (DDE)
- Interfaccia utente di Windows, libreria di gestione Dynamic Data Exchange (DDEML)
- Libreria di gestione Dynamic Data Exchange (DDEML), servizio nome
- DDEML (libreria di gestione Dynamic Data Exchange), servizio nome
- scambio di dati, libreria di gestione Dynamic Data Exchange (DDEML)
- Dynamic Data Exchange (DDE), registrazione del nome del servizio
- DDE (Dynamic Data Exchange), registrazione del nome del servizio
- Libreria di gestione Dynamic Data Exchange (DDEML), registrazione del nome del servizio
- DDEML (libreria di gestione Dynamic Data Exchange), registrazione del nome del servizio
- Dynamic Data Exchange (DDE), filtro nome servizio
- DDE (Dynamic Data Exchange), filtro nome servizio
- Libreria di gestione Dynamic Data Exchange (DDEML), filtro nome servizio
- DDEML (libreria di gestione Dynamic Data Exchange), filtro nome servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10f958ab73164e70177cb5deeb5f400f44695015
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332628"
---
# <a name="name-service"></a>Nome servizio

La libreria di gestione Dynamic Data Exchange (DDEML) consente a un'applicazione server di registrare i nomi di servizio supportati e di impedire al DDEML di inviare transazioni di [**\_ connessione XTYP**](xtyp-connect.md) per i nomi di servizio non supportati alla funzione di callback di Dynamic Data Exchange (DDE) del server.

Negli argomenti seguenti viene descritto il nome Service.

-   [Registrazione del nome del servizio](#service-name-registration)
-   [Filtro nome servizio](#service-name-filter)

## <a name="service-name-registration"></a>Registrazione del nome del servizio

Registrando i nomi di servizio con DDEML, un server informa altre applicazioni DDE nel sistema che è disponibile un nuovo server. Un server registra un nome di servizio chiamando la funzione [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) e specificando un handle di stringa che identifica il nome. In risposta, il DDEML invia una transazione di [**\_ registrazione XTYP**](xtyp-register.md) alla funzione di callback di ogni applicazione DDEML nel sistema, ad eccezione di quelle che hanno specificato il \_ \_ flag di filtro di CBF Skip registrations nella funzione [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) . La **transazione \_ Register XTYP** passa due handle di stringa a una funzione di callback: il primo identifica la stringa che specifica il nome del servizio di base e la seconda identifica la stringa che specifica il servizio specifico dell'istanza. Un client utilizza in genere il nome del servizio di base in un elenco di server disponibili, in modo che l'utente possa selezionare un server dall'elenco. Il client utilizza il nome del servizio specifico dell'istanza per stabilire una conversazione con un'istanza specifica di un'applicazione server, se è in esecuzione più di un'istanza.

Un server può utilizzare [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) per annullare la registrazione di un nome di servizio. Questa funzione fa in modo che DDEML invii [**XTYP \_ Annulla la registrazione**](xtyp-unregister.md) delle transazioni alle altre applicazioni DDE nel sistema, indicando che non possono più usare il nome per stabilire conversazioni.

Un server deve chiamare [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) per registrare i nomi di servizio subito dopo la chiamata di [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea). Un server deve annullare la registrazione dei nomi di servizio usando **DdeNameService** appena prima di chiamare la funzione [**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) .

## <a name="service-name-filter"></a>Filtro nome servizio

Oltre a registrare i nomi dei servizi, [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) consente a un server di attivare o disattivare il filtro del nome del servizio. Quando un server disattiva il filtro del nome del servizio, DDEML invia la transazione di [**\_ connessione XTYP**](xtyp-connect.md) alla funzione di callback DDE del server ogni volta che un client chiama la funzione [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) , indipendentemente dal nome del servizio specificato nella funzione. Quando un server attiva il filtro del nome del servizio, DDEML invia la transazione di **\_ connessione XTYP** al server solo quando **DdeConnect** specifica un nome di servizio specificato dal server in una chiamata a **DdeNameService**.

Per impostazione predefinita, il filtro del nome del servizio è acceso quando un'applicazione chiama [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea). Questa impostazione predefinita impedisce al DDEML di inviare la transazione di [**\_ connessione XTYP**](xtyp-connect.md) a un server prima che il server abbia creato la stringa di gestione necessaria. Un server può disabilitare il filtro del nome del servizio specificando il \_ flag FILTEROFF DNS in una chiamata a [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice). Il \_ flag FILTERON DNS attiva il filtro.

 

 




