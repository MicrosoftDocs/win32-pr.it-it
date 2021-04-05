---
title: Analizzare. CPP
description: Nel componente provider di esempio, un esempio di codice del parser del percorso del servizio directory si trova in Parse. cpp.
ms.assetid: 5d68065b-0dab-41c9-baf1-f9610656bd6e
ms.tgt_platform: multiple
keywords:
- ADSI Parse. cpp
- parser percorso ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ee4df5c1c709fde724385fdf5d5cddbafef338
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955089"
---
# <a name="parsecpp"></a>Analizzare. CPP

Nel componente provider di esempio, un esempio di codice del parser del percorso del servizio directory si trova in Parse. cpp. Il parser del percorso è un componente chiave nei componenti del provider ADs. Verifica la validità sintattica di un percorso ADs passato a questo provider. Se la sintassi è valida, viene costruita una struttura **OBJECTINFO** , che contiene una versione con componenti di ADspath per questo oggetto.

Tenere presente che si tratta solo di una verifica della sintassi. Anziché un caso speciale ogni nuova iterazione di path, tutte le verifiche del percorso devono essere conformi alle regole di grammatica stabilite dal parser.

La tabella seguente elenca le funzioni e i metodi implementati in Parse. cpp.



| Elemento                      | Descrizione                                                                                                                                                            |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ADsObject**             | Analizza il ADspath passato. Questa funzione segue le seguenti regole grammaticali: <ADsObject>  ->  <ProviderName><SampleDSObject><br/>     |
| **SampleDSObject**        | Analizza le seguenti regole grammaticali: <SampleDSObject> -> " \\ \\ " <identifier> " \\ "<Pathname><br/>                                            |
| **ProviderName**          | Aggiunge il nome del provider sintatticamente corretto se non è presente.                                                                                                          |
| **PathName**              | Analizza le seguenti regole grammaticali: <Pathname>  ->  <Component> " \\ \\ " <Pathname> o<br/> <Pathname> -> <Component><br/> |
| **Componente**             | Analizza le seguenti regole grammaticali: <Identifier> o<br/> <Identifier> "=" <Identifier><br/>                                              |
| **CLexer::CLexer**        | Costruttore standard.                                                                                                                                                  |
| **CLexer:: ~ CLexer**       | Distruttore standard.                                                                                                                                                   |
| **CLexer:: GetNextToken**  | Tokenizer.                                                                                                                                                             |
| **CLexer::NextChar**      | Recupera il carattere singolo successivo.                                                                                                                                       |
| **CLexer::P ushBackToken** | Esegue il backup fino all'inizio dell'ultimo token.                                                                                                                               |
| **CLexer::P ushbackChar**  | Esegue il backup di un carattere.                                                                                                                                                |
| **CLexer:: la parola chiave**     | Verifica l'elenco di parole chiave. Definito in Globals. h).                                                                                                                          |
| **AddComponent**          | Aggiunge questo componente alla matrice di componenti.                                                                                                                            |
| **AddProviderName**       | Aggiunge un nome di provider sintatticamente corretto alla struttura **OBJECTINFO** .                                                                                            |
| **AddRootRDN**            | Aggiunge il nome del nome distinto relativo (RDN) radice sintatticamente corretto alla struttura **OBJECTINFO** .                                                            |
| **SetType**               | Imposta il tipo dell'oggetto.                                                                                                                                           |
| **Tipo**                  | Analizza il tipo > "User" \| "Group" e così via.                                                                                                                          |



 

 

 





