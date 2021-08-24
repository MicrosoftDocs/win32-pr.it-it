---
description: Le funzioni helper seguenti vengono chiamate dai parser.
ms.assetid: 4e9a9314-8d64-46c0-ad98-bdb9dc4c225a
title: Funzioni del parser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d70c3ad44ad809a323af8acde732af3b142759d3686d78c496f47e92cb8e209
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676841"
---
# <a name="parser-functions"></a>Funzioni del parser

Le funzioni helper seguenti vengono chiamate dai parser.



| Funzione                                                 | Descrizione                                                                                                    |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [AddressToString](addresstostring.md)                   | Converte un indirizzo in una stringa.                                                                               |
| [LookupByteSetString](lookupbytesetstring.md)           | Recupera la stringa corrispondente al valore specificato di un set con etichetta.                                    |
| [SetCCInstPtr](setccinstptr.md)                         | Acquisisce un puntatore all'istanza di contesto.                                                                           |
| [StringToAddress](stringtoaddress.md)                   | Converte una stringa in un indirizzo.                                                                               |
| [VarLenSmallIntToDword](varlensmallinttodword.md)       | Converte un numero intero piccolo a lunghezza variabile in **un valore DWORD**.                                                      |
| [LookupDwordSetString](lookupdwordsetstring.md)         | Recupera la stringa corrispondente al valore specificato di un set con etichetta.                                    |
| [LookupWordSetString](lookupwordsetstring.md)           | Recupera la stringa corrispondente al valore specificato da un set con etichetta.                                      |
| [BERGetHeader](bergetheader.md)                         | Decodifica un'intestazione di scelta.                                                                                       |
| [BERGetInteger](bergetinteger.md)                       | Decodifica un intero con codifica BER.                                                                                 |
| [BERGetString](bergetstring.md)                         | Decodifica una stringa con codifica BER.                                                                                  |
| [CCHeapAlloc](ccheapalloc.md)                           | Alloca la memoria in base all'acquisizione.                                                                |
| [CCHeapFree](ccheapfree.md)                             | Rilascia la memoria allocata dalla **funzione CCHeapAlloc.**                                                 |
| [CCHeapReAlloc](ccheaprealloc.md)                       | Rialloca la memoria allocata dalla **funzione CCHeapAlloc.**                                                  |
| [CCHeapSize](ccheapsize.md)                             | Recupera le dimensioni della memoria allocata dalla **funzione CCHeapAlloc.**                                    |
| [GetCCInstPtr](getccinstptr.md)                         | Recupera il puntatore ai dati dell'istanza aggiunti al contesto di acquisizione.                                       |
| [CreateProtocol](createprotocol.md)                     | Informa l'API Network Monitor che esiste un parser di protocollo specifico.                                        |
| [DestroyProtocol](destroyprotocol.md)                   | Elimina il protocollo creato dalla **funzione CreateProtocol.**                                              |
| [BuildINIPath](buildinipath.md)                         | Recupera un percorso completo del file di inizializzazione (INI) che corrisponde alle informazioni immesse.   |
| [CreateHandoffTable](createhandofftable.md)             | Crea una tabella handoff in base alle informazioni contenute in un file INI specificato.                                             |
| [DestroyHandoffTable](destroyhandofftable.md)           | Elimina una tabella handoff creata con la **funzione CreateHandoffTable.**                                     |
| [GetProtocolFromTable](getprotocolfromtable.md)         | Recupera il protocollo di una determinata tabella handoff.                                                               |
| [AddProperty](/previous-versions/bb251873(v=msdn.10))                           | Aggiunge una **struttura PROPERTYINFO** al database delle proprietà.                                                    |
| [AttachPropertyInstance](attachpropertyinstance.md)     | Associa un'istanza della proprietà a un frame.                                                                       |
| [AttachPropertyInstanceEx](attachpropertyinstanceex.md) | Associa un'istanza della proprietà a un frame.                                                                       |
| [CreatePropertyDatabase](createpropertydatabase.md)     | Crea un database delle proprietà che descrive le proprietà utilizzate dal parser per descrivere i relativi dati.               |
| [DestroyPropertyDatabase](destroypropertydatabase.md)   | Elimina un database delle proprietà creato dalle chiamate alle **funzioni CreatePropertyDatabase** **e AddProperty.** |
| [FindNextFrame](findnextframe.md)                       | Trova il frame successivo nel contesto di acquisizione corrente che corrisponde a un filtro specificato.                               |
| [FindPreviousFrame](findpreviousframe.md)               | Trova il frame precedente nel contesto di acquisizione corrente che corrisponde a un filtro specificato.                           |
| [FormatPropertyInstance](formatpropertyinstance.md)     | Formatta l'istanza della proprietà in modo generico.                                                             |
| [GetFrameDestAddress](getframedestaddress.md)           | Recupera l'indirizzo di destinazione di un frame.                                                                  |
| [GetFrameSourceAddress](getframesourceaddress.md)       | Recupera l'indirizzo di origine di un frame.                                                                       |
| [GetProtocolStartOffset](getprotocolstartoffset.md)     | Recupera l'offset per un protocollo specificato nel frame.                                                         |
| [ParserTemporaryLockFrame](parsertemporarylockframe.md) | Blocca un frame quando entra in un parser e lo sblocca all'uscita.                                     |



 

Per informazioni sulle funzioni di esportazione (funzioni helper che possono essere chiamate da esperti e parser), sulle strutture e sulle enumerazioni, vedere gli argomenti seguenti.



| Per informazioni su                                  | Vedere                                                                          |
|--------------------------------------------------------|------------------------------------------------------------------------------|
| Funzioni esportate dal parser.                         | [Funzioni di esportazione dll del parser](parser-dll-export-functions.md)               |
| Strutture usate da funzioni del parser.                  | [Strutture del parser](parser-structures.md)                                   |
| Funzioni helper comuni chiamate da parser ed esperti. | [Funzioni comuni di Esperti e Parser](expert-and-parser-common-functions.md) |



 

 

 
