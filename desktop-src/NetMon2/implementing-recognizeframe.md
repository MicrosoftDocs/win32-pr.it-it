---
description: Il monitoraggio di rete chiama la funzione RecognizeFrame di un parser per determinare che il parser riconosce i dati non reclamati di un frame.
ms.assetid: 6d0574da-f0ec-4ed9-bfb0-023dff2ac6fe
title: Implementazione di RecognizeFrame
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d970eee80a04168b3fa06b117c2c219c506da7ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348946"
---
# <a name="implementing-recognizeframe"></a>Implementazione di RecognizeFrame

Il monitoraggio di rete chiama la funzione [**RecognizeFrame**](recognizeframe.md) di un parser per determinare che il parser riconosce i dati non reclamati di un frame. I dati non reclamati potrebbero essere all'inizio di un frame, ma in genere i dati non reclamati si trovano al centro di un frame. Nella figura seguente vengono mostrati i dati non recuperati che si trovano al centro di un frame.

![dati non reclamati che si trovano al centro di un frame](images/recognizeframe1.png)

Network Monitor fornisce le informazioni seguenti quando chiama la funzione [**RecognizeFrame**](recognizeframe.md) :

-   Handle per il frame.
-   Puntatore all'inizio del frame.
-   Puntatore all'inizio dei dati non recuperati.
-   Valore MAC del primo protocollo nel frame.
-   Numero di byte nei dati non recuperati; ovvero i byte rimanenti nel frame.
-   Handle per il protocollo precedente.
-   Offset del protocollo precedente.

Quando la DLL del parser determina che i dati non reclamati iniziano con il protocollo del parser, la DLL del parser determina la posizione in cui inizia il protocollo successivo e il protocollo che segue. La DLL del parser funziona nei modi condizionali seguenti:

-   Se la DLL del parser riconosce i dati non recuperati, la DLL del parser imposta il parametro *pProtocolStatus* e restituisce un puntatore al protocollo successivo nel frame o **null**. Se il protocollo corrente è l'ultimo protocollo nel frame, viene restituito **null** .
-   Se la DLL del parser riconosce i dati non attestati e identifica il protocollo che segue (dalle informazioni fornite nel protocollo), la DLL del parser restituisce un puntatore all'handle del protocollo successivo nel parametro *phNextProtocol* della funzione.
-   Se la DLL del parser non riconosce i dati non reclamati, la DLL del parser restituisce il puntatore all'inizio dei dati non attestati e Network Monitor continua a provare ad analizzare i dati non recuperati.

**Per implementare RecognizeFrame**

1.  Eseguire un test per determinare se il protocollo è riconosciuto.
2.  Se si riconoscono i dati non reclamati e si sa quale protocollo segue, impostare *pProtocolStatus* su protocollo \_ status \_ Next \_ Protocol, impostare *phNextProtocol* su un puntatore che punta all'handle per il protocollo successivo, quindi restituire un puntatore al protocollo successivo.

    –oppure–

    Se si riconoscono i dati non reclamati e non si sa quale protocollo segue  , impostare pProtocolStatus \_ sullo stato \_ del protocollo riconosciuto e quindi restituire un puntatore al protocollo successivo.

    –oppure–

    Se si riconoscono i dati non richiesti e il protocollo è l'ultimo protocollo in un frame  , impostare pProtocolStatus \_ sullo stato del protocollo \_ richiesto e quindi restituire **null**.

    –oppure–

    Se non si riconoscono i dati non attestati  , impostare pProtocolStatus \_ sullo stato \_ del protocollo non \_ riconosciuto, quindi restituire il puntatore passato all'utente in *pProtocol*.

Di seguito è riportata un'implementazione di base di [**RecognizeFrame**](recognizeframe.md).

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

 

 



