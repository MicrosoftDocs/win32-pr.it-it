---
description: Network Monitors chiama la funzione RecognizeFrame di un parser per determinare che il parser riconosce i dati non reclamati di un frame.
ms.assetid: 6d0574da-f0ec-4ed9-bfb0-023dff2ac6fe
title: Implementazione di RecognizeFrame
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39d3f9a79325c0c75a7a83cfb99a34ff3de1f073573dee13d39a846b575f6285
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890497"
---
# <a name="implementing-recognizeframe"></a>Implementazione di RecognizeFrame

Network Monitors chiama la [**funzione RecognizeFrame**](recognizeframe.md) di un parser per determinare che il parser riconosce i dati non reclamati di un frame. I dati non reclamati possono trovarsi all'inizio di un frame, ma in genere i dati non reclamati si trovano al centro di un frame. La figura seguente mostra i dati non reclamati che si trovano al centro di un frame.

![dati non reclamati che si trovano al centro di un frame](images/recognizeframe1.png)

Network Monitor fornisce le informazioni seguenti quando chiama la [**funzione RecognizeFrame:**](recognizeframe.md)

-   Handle per il frame.
-   Puntatore all'inizio del frame.
-   Puntatore all'inizio dei dati non reclamati.
-   Valore MAC del primo protocollo nel frame.
-   Numero di byte nei dati non reclamati. ciò significa che i byte rimanenti nel frame.
-   Handle per il protocollo precedente.
-   Offset del protocollo precedente.

Quando la DLL del parser determina che i dati non reclamati iniziano con il protocollo del parser, la DLL del parser determina dove viene avviato il protocollo successivo e quale protocollo segue. La DLL del parser funziona nei modi condizionali seguenti:

-   Se la DLL del parser riconosce i dati non dichiarati, la DLL del parser imposta il parametro *pProtocolStatus* e restituisce un puntatore al protocollo successivo nel frame o **NULL.** Se il protocollo corrente è l'ultimo protocollo nel frame, viene restituito **NULL.**
-   Se la DLL del parser riconosce i dati non richieste e identifica il protocollo che segue (dalle informazioni fornite nel protocollo), la DLL del parser restituisce un puntatore all'handle del protocollo successivo nel parametro *phNextProtocol* della funzione.
-   Se la DLL del parser non riconosce i dati non reclamati, la DLL del parser restituisce il puntatore all'inizio dei dati non reclamati e Network Monitor continua a tentare di analizzare i dati non reclamati.

**Per implementare RecognizeFrame**

1.  Eseguire un test per determinare che il protocollo è riconosciuto.
2.  Se si riconoscono i dati non dichiarati e si conosce il protocollo che segue, impostare *pProtocolStatus* su PROTOCOL STATUS NEXT PROTOCOL, impostare \_ \_ \_ *phNextProtocol* su un puntatore che punta all'handle per il protocollo successivo e quindi restituire un puntatore al protocollo successivo.

    –oppure–

    Se si riconoscono i dati non dichiarati e non si conosce il protocollo che segue, impostare *pProtocolStatus* su PROTOCOL STATUS RECOGNIZED e quindi restituire un puntatore al \_ \_ protocollo successivo.

    –oppure–

    Se si riconoscono i dati non dichiarati e il protocollo è l'ultimo protocollo in un frame, impostare *pProtocolStatus* su PROTOCOL STATUS CLAIMED e quindi \_ \_ restituire **NULL.**

    –oppure–

    Se non si riconoscono dati non dichiarati, impostare *pProtocolStatus* su PROTOCOL STATUS NOT RECOGNIZED e quindi restituire il puntatore passato \_ all'utente in \_ \_ *pProtocol*.

Di seguito è riportata un'implementazione di base [**di RecognizeFrame.**](recognizeframe.md)

``` syntax
#include <windows.h>

LPBYTE BHAPI MyProtocol_RecognizeFrame( HFRAME hFrame,
                                        LPBYTE        pMacFrame,
                                        LPBYTE        pProtocol,
                                        DWORD         MacType,
                                        DWORD         BytesLeft,
                                        HPROTOCOL     hPrevProtocol,
                                        DWORD         nPreviuosProtOffset,
                                        LPDWORD       pProtocolStatus,
                                        LPHPROTOCOL   phNextProtocol,
                                        LPDWORD       InstData)
  
  // Test unclaimed data. 
  
  // If unclaimed data is recognized, but you do not know what follows.
  *pProtocolStatus =  PROTOCOL_STATUS_RECOGNIZED;
  return pProtocol + MY_PROTOCOL_LENGTH;
  
  // If unclaimed data is recognized and you know what follows.
  *pProtocolStatus =  PROTOCOL_STATUS_NEXT_PROTOCOL;
  phNextProtocol = GetProtocolFromTable(
                                        hTable,
                                        ItemToFind,
                                        lpInstData);
  return  pProtocol + MY_PROTOCOL_LENGTH;
  
  // If unclaimed data is recognized and the protocol is the last 
  // protocol in the frame.
  *pProtocolStatus =  PROTOCOL_STATUS_CLAIMED;
  return NULL;
  
  // If the unclaimed data is not recognized.
  *pProtocolStatus =  PROTOCOL_STATUS_NOT_RECOGNIZED;
  return *pProtocol;

}
```

 

 



