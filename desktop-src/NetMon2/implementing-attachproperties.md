---
description: Chiama la funzione AttachProperties per eseguire il mapping delle proprietà presenti in una parte di dati riconosciuti.
ms.assetid: f1949904-ceb2-4650-847f-01f597ff3620
title: Implementazione di AttachProperties
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbb3571cf655e07b2879513f826192711992fb49a02cc7a4954d5322a948caf5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118365351"
---
# <a name="implementing-attachproperties"></a>Implementazione di AttachProperties

Network Monitor chiama la [**funzione AttachProperties**](attachproperties.md) per eseguire il mapping delle proprietà presenti in una parte di dati riconosciuti. La [**funzione AttachProperties**](attachproperties.md) esegue il mapping delle proprietà a una posizione specifica.

Network Monitor usa il processo seguente per analizzare i dati in un frame.

-   In primo luogo, Network Monitor [recognizeFrame](recognizeframe.md) per riconoscere tutti i protocolli presenti in un frame.
-   Quindi, Network Monitor [**chiama AttachProperties**](attachproperties.md) per ogni parser che riconosce una parte di dati.

Quando Network Monitor chiama la funzione [AttachProperties](attachproperties.md) per i dati riconosciuti, il parser chiamato deve analizzare i dati e quindi eseguire il mapping di ogni proprietà esistente a una posizione nei dati riconosciuti. Il parser determina quali proprietà esistono e dove si trova ogni proprietà nei dati. La figura seguente mostra i dati riconosciuti dal parser.

![dati riconosciuti dal parser](images/attachproperties1.png)

Durante l'implementazione [**di AttachProperties**](attachproperties.md), è necessario chiamare una delle funzioni seguenti per ogni proprietà presente in un frame di dati.

-   Chiamare la [**funzione AttachPropertyInstanceEx**](attachpropertyinstanceex.md) quando si vogliono modificare i dati delle proprietà in un frame.
-   Chiamare la [**funzione AttachPropertyInstance**](attachpropertyinstance.md) quando non si vogliono modificare i dati delle proprietà in un frame.

> [!Note]  
> È consigliabile usare i dati così come sono presenti nell'acquisizione.

 

La procedura seguente identifica i passaggi necessari per implementare [**AttachProperties**](attachproperties.md).

**Per implementare AttachProperties**

1.  Determinare le proprietà esistenti e il percorso della proprietà nei dati.
2.  Chiamare [**AttachPropertyInstanceEx**](attachpropertyinstanceex.md) per ogni proprietà con un valore che si vuole modificare.
3.  Chiamare [**AttachPropertyInstance**](attachpropertyinstance.md) per ogni proprietà con un valore che non si vuole modificare. In genere, questa è l'unica funzione che è necessario chiamare.

Di seguito è riportata un'implementazione di base [**di AttachProperties**](attachproperties.md). Tenere presente che l'esempio non include il codice per determinare quali proprietà esistono o il codice per individuare le proprietà.

``` syntax
#include <windows.h>

LPBYTE BHAPI MyProtocolAttachProperties( HFRAME   hFrame,
                                         LPBYTE   pMacFrame,
                                         LPBYTE   pBLRPLATEFrame,
                                         DWORD    MacType,
                                         DWORD    BytesLeft,
                                         HPROTOCOL  hPreviousProtocol,
                                         DWORD    nPrevProtocolOffset,
                                         DWORD    InstData)
{
  PBLRPLATEHDR pBLRPLATEHdr = (PBLRPLATEHDR)pBLRPLATEFrame;

  // Attach summary property.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_SUMMARY].hProperty,
                          (WORD)BytesLeft,
                          (LPBYTE)pBLRPLATEFrame,
                          0,        // No Help file.
                          0,        // Indent level.
                          0);      // Data flag.

  // Attach signature property.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_SIGNATURE].hProperty,
                          sizeof(DWORD),
                          &(pBLRPLATEHdr->Signature),
                          0,        // No Help file.
                          1,        // Indent level.
                          0);        // Data flag.


  // Attach opcode.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_OPCODE].hProperty,
                          sizeof(WORD),
                          &(pBLRPLATEHdr->Opcode),
                          0,        // No Help file.
                          1,        // Indent level.
                          0);        // Data flag.

  // Attach flags summary.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_FLAGS_SUMMARY].hProperty,
                          sizeof(BYTE),
                          &(pBLRPLATEHdr->Flags),
                          0,        // No Help file.
                          1,        // Indent level.
                          0);       // Data flag.

// Attach flags decode.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_FLAGS_FLAGS].hProperty,
                          sizeof(BYTE),
                          &(pBLRPLATEHdr->Flags),
                          0,        // No Help file.
                          2,        // Indent level.
                          0);       // Data flag.

  RETURN null;

}
```

 

 



