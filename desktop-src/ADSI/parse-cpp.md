---
title: Parse. CPP
description: Nel componente provider di esempio un esempio di codice del parser del percorso del servizio directory si trova in Parse.cpp.
ms.assetid: 5d68065b-0dab-41c9-baf1-f9610656bd6e
ms.tgt_platform: multiple
keywords:
- PARSE.cpp ADSI
- parser di percorso ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 544ab295318ac80ed19df39a7e5837b566615903a8d8bb963b6fdd5435efde8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023289"
---
# <a name="parsecpp"></a>Parse. CPP

Nel componente provider di esempio un esempio di codice del parser del percorso del servizio directory si trova in Parse.cpp. Il parser di percorso è un componente chiave nei componenti del provider ADs. Verifica la validità sintattica di un percorso ADs passato a questo provider. Se la sintassi è valida, viene costruita una struttura **OBJECTINFO** che contiene una versione in componenti di ADspath per questo oggetto.

Tenere presente che si tratta solo di una verifica della sintassi. Invece di creare casi speciali per ogni nuova iterazione del percorso, tutte le verifiche del percorso devono essere conformi alle regole di grammatica stabilite dal parser.

La tabella seguente elenca le funzioni e i metodi implementati in Parse.cpp.



| Elemento                      | Descrizione                                                                                                                                                            |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ADsObject**             | Analizza il percorso ADs passato. Questa funzione segue le regole grammaticali seguenti: <ADsObject>  ->  <ProviderName><SampleDSObject><br/>     |
| **SampleDSObject**        | Analizza le regole grammaticali seguenti: <SampleDSObject> -> " \\ \\ " " <identifier> \\ "<Pathname><br/>                                            |
| **ProviderName**          | Aggiunge il nome del provider sintatticamente corretto, se non è presente.                                                                                                          |
| **PathName**              | Analizza le regole grammaticali seguenti: <Pathname>  ->  <Component> " \\ \\ " <Pathname> OR<br/> <Pathname> -> <Component><br/> |
| **Componente**             | Analizza le regole grammaticali seguenti: <Identifier> OR<br/> <Identifier> "=" <Identifier><br/>                                              |
| **CLexer::CLexer**        | Costruttore standard.                                                                                                                                                  |
| **CLexer::~CLexer**       | Distruttore standard.                                                                                                                                                   |
| **CLexer::GetNextToken**  | Tokenizer.                                                                                                                                                             |
| **CLexer::NextChar**      | Recupera il carattere singolo successivo.                                                                                                                                       |
| **CLexer::P ushBackToken** | Backup all'inizio dell'ultimo token.                                                                                                                               |
| **CLexer::P ushbackChar**  | Backup di un carattere.                                                                                                                                                |
| **CLexer::IsKeyword**     | Verifica l'elenco di parole chiave. Definito in Globals.h).                                                                                                                          |
| **Addcomponent**          | Aggiunge questo componente alla matrice di componenti.                                                                                                                            |
| **AddProviderName**       | Aggiunge un nome di provider sintatticamente corretto alla **struttura OBJECTINFO.**                                                                                            |
| **AddRootRDN**            | Aggiunge il nome RDN (Root Relative Distinguished Name) sintatticamente corretto alla **struttura OBJECTINFO.**                                                            |
| **SetType**               | Imposta il tipo dell'oggetto .                                                                                                                                           |
| **Tipo**                  | Analizza type-> "user" \| "group" e così via.                                                                                                                          |



 

 

 





