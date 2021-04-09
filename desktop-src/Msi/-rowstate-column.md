---
description: Il nome di colonna riservato \_ RowState rappresenta lo stato non persistente associato a ogni riga della tabella in una tabella di database del programma di installazione.
ms.assetid: ff570b47-7c16-47ae-b1c2-2ecad9266372
title: _RowState colonna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e61a2964d7d11c1c2429ad95e9de2b8bdb148954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049918"
---
# <a name="_rowstate-column"></a>\_RowState-colonna

Il nome di colonna riservato \_ RowState rappresenta lo stato non persistente associato a ogni riga della tabella in una tabella di database del programma di installazione. La pseudo-colonna è di tipo [Integer](integer.md)e il valore è costituito da un set di flag di bit. Tutti i bit sono leggibili, ma è possibile impostare solo UserInfo e BITS temporanei. Questi dati sono disponibili solo se le tabelle sono bloccate o in uso, ovvero quando esiste una vista contenente le tabelle. La tabella seguente Mostra gli attributi che possono essere presenti in una riga.



| Nome           | Valore | Significato                                                        |
|----------------|-------|----------------------------------------------------------------|
| iraUserInfo    | 0x01  | L'attributo è per uso esterno. Questo valore può essere aggiornato.  |
| iraTemporary   | 0x02  | La riga non è persistente. Questo valore può essere aggiornato.          |
| iraModified    | 0x04  | È stata aggiornata una riga.                                        |
| iraInserted    | 0x08  | È stata inserita una riga.                                       |
| iraMergeFailed | 0x0F  | È stato effettuato un tentativo di Unione con dati non identici e non chiave. |



 

I bit da 6 a 8 sono riservati.

 

 



