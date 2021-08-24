---
description: Le condivisioni DDE sono una risorsa del computer.
ms.assetid: 98d24300-52cc-4f0d-b74f-c58b823ac5f3
title: Condivisioni DDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5e3416235f78e48c68b7d2e35c7ac042f8ff5d6eac79cc2471efa5ea12d82b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602121"
---
# <a name="dde-shares"></a>Condivisioni DDE

\[DDE di rete non è più supportato. Nddeapi.dll è presente in Windows Vista, ma tutte le chiamate di funzione restituiscono NDDE \_ NOT \_ IMPLEMENTED.\]

Le condivisioni DDE sono una risorsa del computer. Sono simili alle condivisioni file perché vengono usate per controllare l'accesso a una risorsa. Con le condivisioni file, la risorsa è un file. Con le condivisioni DDE, la risorsa viene scambiata dinamicamente. Il tipo di dati s scambiati è determinato dall'applicazione server che fornisce i dati e dall'applicazione client che richiede i dati.

Il server chiama la [**funzione NDdeShareAdd**](nddeshareadd.md) per creare la condivisione DDE, archiviata in DDE Share Database Manager (DSDM).

Il client avvia la conversazione DDE connettendosi alla condivisione DDE. Il client deve chiamare la [**funzione DdeInitialize**](/windows/win32/api/ddeml/nf-ddeml-ddeinitializea) per inizializzare DDEML e chiamare la [**funzione DdeConnect**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect) per connettersi alla condivisione DDE. Nella chiamata **DdeConnect** il client specifica il nome del servizio come indicato di seguito:

\\\\*NomeComputer* \\ NDDE$

dove *NomeComputer è* il nome del computer che esegue l'applicazione server. NDDE$ indica che l'argomento fornito a [**DdeConnect**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect) è il nome della condivisione DDE nel computer remoto denominato *ComputerName*.

Esistono tre tipi di condivisioni DDE: stile precedente, nuovo stile e statico. È tipico supportare solo il tipo statico. I nomi delle condivisioni statiche usano la convenzione seguente: *ShareName*$.

 

 
