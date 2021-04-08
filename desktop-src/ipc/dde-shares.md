---
description: Le condivisioni DDE sono una risorsa del computer.
ms.assetid: 98d24300-52cc-4f0d-b74f-c58b823ac5f3
title: Condivisioni DDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 012c219897187c9e68b5b9e662b93678b77974c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882234"
---
# <a name="dde-shares"></a>Condivisioni DDE

\[Il DDE di rete non è più supportato. Nddeapi.dll è presente in Windows Vista, ma tutte le chiamate di funzione restituiscono NDDE \_ non \_ implementate.\]

Le condivisioni DDE sono una risorsa del computer. Sono simili alle condivisioni file perché vengono usate per controllare l'accesso a una risorsa. Con le condivisioni file, la risorsa è un file. Con le condivisioni DDE, la risorsa viene scambiata dinamicamente. Il tipo di dati scambiati è determinato dall'applicazione server che fornisce i dati e l'applicazione client che richiede i dati.

Il server chiama la funzione [**NDDEShareAdd**](nddeshareadd.md) per creare la condivisione DDE, archiviata in gestione database di condivisione DDE (DSDM).

Il client avvia la conversazione DDE connettendosi alla condivisione DDE. Il client deve chiamare la funzione [**DdeInitialize**](/windows/win32/api/ddeml/nf-ddeml-ddeinitializea) per inizializzare DDEML e chiamare la funzione [**DdeConnect**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect) per connettersi alla condivisione DDE. Nella chiamata a **DdeConnect** , il client specifica il nome del servizio come segue:

\\\\*Nomecomputer* \\ NDDE $

dove *nomecomputer* è il nome del computer in cui è in esecuzione l'applicazione server. NDDE $ indica che l'argomento fornito a [**DdeConnect**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect) è il nome della condivisione DDE nel computer remoto denominato *ComputerName*.

Sono disponibili tre tipi di condivisioni DDE: vecchio stile, nuovo stile e statico. È tipico per supportare solo il tipo statico. I nomi delle condivisioni statiche utilizzano la convenzione seguente: *ShareName*$.

 

 
