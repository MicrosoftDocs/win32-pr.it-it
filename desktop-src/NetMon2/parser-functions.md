---
description: Le funzioni di supporto seguenti vengono chiamate dai parser.
ms.assetid: 4e9a9314-8d64-46c0-ad98-bdb9dc4c225a
title: Funzioni del parser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db9a502778247a3daad5f11dd8d0e2a3312d586d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128318"
---
# <a name="parser-functions"></a>Funzioni del parser

Le funzioni di supporto seguenti vengono chiamate dai parser.



| Funzione                                                 | Descrizione                                                                                                    |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [AddressToString](addresstostring.md)                   | Converte un indirizzo in una stringa.                                                                               |
| [LookupByteSetString](lookupbytesetstring.md)           | Recupera la stringa corrispondente al valore specificato di un set con etichetta.                                    |
| [SetCCInstPtr](setccinstptr.md)                         | Acquisisce un puntatore all'istanza del contesto.                                                                           |
| [StringToAddress](stringtoaddress.md)                   | Converte una stringa in un indirizzo.                                                                               |
| [VarLenSmallIntToDword](varlensmallinttodword.md)       | Converte un valore integer di lunghezza variabile, piccolo, in un valore **DWORD**.                                                      |
| [LookupDwordSetString](lookupdwordsetstring.md)         | Recupera la stringa corrispondente al valore specificato di un set con etichetta.                                    |
| [LookupWordSetString](lookupwordsetstring.md)           | Recupera la stringa che corrisponde al valore specificato da un set con etichetta.                                      |
| [BERGetHeader](bergetheader.md)                         | Decodifica un'intestazione Choice.                                                                                       |
| [BERGetInteger](bergetinteger.md)                       | Decodifica un integer con codifica BER.                                                                                 |
| [BERGetString](bergetstring.md)                         | Decodifica una stringa con codifica BER.                                                                                  |
| [CCHeapAlloc](ccheapalloc.md)                           | Alloca la memoria in base a un'acquisizione per acquisizione.                                                                |
| [CCHeapFree](ccheapfree.md)                             | Rilascia la memoria allocata dalla funzione **CCHeapAlloc** .                                                 |
| [CCHeapReAlloc](ccheaprealloc.md)                       | Consente di riallocare la memoria allocata dalla funzione **CCHeapAlloc** .                                                  |
| [CCHeapSize](ccheapsize.md)                             | Recupera le dimensioni della memoria allocata dalla funzione **CCHeapAlloc** .                                    |
| [GetCCInstPtr](getccinstptr.md)                         | Recupera il puntatore ai dati dell'istanza aggiunti al contesto di acquisizione.                                       |
| [CreateProtocol](createprotocol.md)                     | Informa l'API Network Monitor che esiste un parser di protocollo specifico.                                        |
| [DestroyProtocol](destroyprotocol.md)                   | Elimina definitivamente il protocollo creato dalla funzione **CreateProtocol** .                                              |
| [BuildINIPath](buildinipath.md)                         | Recupera il percorso completo del file di inizializzazione (INI) che corrisponde alle informazioni immesse.   |
| [CreateHandoffTable](createhandofftable.md)             | Crea una tabella di continuità in base alle informazioni contenute in un determinato file INI.                                             |
| [DestroyHandoffTable](destroyhandofftable.md)           | Elimina definitivamente una tabella di continuità creata con la funzione **CreateHandoffTable** .                                     |
| [GetProtocolFromTable](getprotocolfromtable.md)         | Recupera il protocollo di una tabella di continuità specificata.                                                               |
| [AddProperty](/previous-versions/bb251873(v=msdn.10))                           | Aggiunge una struttura **PROPERTYINFO** al database della proprietà.                                                    |
| [AttachPropertyInstance](attachpropertyinstance.md)     | Connette un'istanza di proprietà a un frame.                                                                       |
| [AttachPropertyInstanceEx](attachpropertyinstanceex.md) | Connette un'istanza di proprietà a un frame.                                                                       |
| [CreatePropertyDatabase](createpropertydatabase.md)     | Crea un database di proprietà che descrive le proprietà utilizzate dal parser per descrivere i dati.               |
| [DestroyPropertyDatabase](destroypropertydatabase.md)   | Elimina un database di proprietà creato dalle chiamate alle funzioni **CreatePropertyDatabase** e **AddProperty** . |
| [FindNextFrame](findnextframe.md)                       | Trova il frame successivo nel contesto di acquisizione corrente che corrisponde a un filtro specificato.                               |
| [FindPreviousFrame](findpreviousframe.md)               | Trova il frame precedente nel contesto di acquisizione corrente che corrisponde a un filtro specificato.                           |
| [FormatPropertyInstance](formatpropertyinstance.md)     | Formatta l'istanza della proprietà in modo generico.                                                             |
| [GetFrameDestAddress](getframedestaddress.md)           | Recupera l'indirizzo di destinazione di un frame.                                                                  |
| [GetFrameSourceAddress](getframesourceaddress.md)       | Recupera l'indirizzo di origine di un frame.                                                                       |
| [GetProtocolStartOffset](getprotocolstartoffset.md)     | Recupera l'offset a un protocollo specificato nel frame.                                                         |
| [ParserTemporaryLockFrame](parsertemporarylockframe.md) | Blocca un frame quando immette un parser e sblocca il frame alla chiusura.                                     |



 

Per informazioni sulle funzioni di esportazione (funzioni helper che possono essere chiamate da esperti e parser), da strutture ed enumerazioni, vedere gli argomenti seguenti.



| Per informazioni su                                  | Vedere                                                                          |
|--------------------------------------------------------|------------------------------------------------------------------------------|
| Funzioni che vengono esportate dai parser.                         | [Funzioni di esportazione DLL del parser](parser-dll-export-functions.md)               |
| Strutture utilizzate dalle funzioni del parser.                  | [Strutture del parser](parser-structures.md)                                   |
| Funzioni helper comuni chiamate da parser ed esperti. | [Funzioni comuni di esperti e parser](expert-and-parser-common-functions.md) |



 

 

 
