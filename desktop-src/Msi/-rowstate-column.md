---
description: Il nome di colonna riservato RowState rappresenta lo stato \_ non permanente associato a ogni riga di tabella in una tabella del database del programma di installazione.
ms.assetid: ff570b47-7c16-47ae-b1c2-2ecad9266372
title: _RowState colonna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42e0164b76589dfa76deb8754df3e11a8b8250a43d791dec92d0fee65dfb719b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146094"
---
# <a name="_rowstate-column"></a>\_Colonna RowState

Il nome di colonna riservato RowState rappresenta lo stato \_ non permanente associato a ogni riga di tabella in una tabella del database del programma di installazione. La pseudo-colonna è di tipo [Integer](integer.md)e il valore è costituito da un set di flag di bit. Tutti i bit sono leggibili, ma è possibile impostare solo i bit UserInfo e Temporary. Questi dati sono disponibili solo a meno che le tabelle siano bloccate o in uso(ovvero, mentre esiste una vista contenente le tabelle). La tabella seguente illustra gli attributi che una riga può avere.



| Nome           | Valore | Significato                                                        |
|----------------|-------|----------------------------------------------------------------|
| iraUserInfo    | 0x01  | L'attributo è per uso esterno. Questo valore può essere aggiornato.  |
| iraTemporary   | 0x02  | La riga non è persistente. Questo valore può essere aggiornato.          |
| iraModified    | 0x04  | Una riga è stata aggiornata.                                        |
| iraInserted    | 0x08  | È stata inserita una riga.                                       |
| iraMergeFailed | 0x0F  | È stato effettuato un tentativo di unione con dati non identici e non chiave. |



 

I bit da 6 a 8 sono riservati.

 

 



