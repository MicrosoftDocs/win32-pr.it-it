---
title: PARSE. CPP
description: Nel componente provider di esempio un esempio di codice del parser del percorso del servizio directory si trova in Parse.cpp.
ms.assetid: 5d68065b-0dab-41c9-baf1-f9610656bd6e
ms.tgt_platform: multiple
keywords:
- PARSE.cpp ADSI
- parser di percorso ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 518db6857f9b7018a0dbf3e1e97ac60ed654447d
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880282"
---
# <a name="parsecpp"></a>PARSE. CPP

Nel componente provider di esempio un esempio di codice del parser del percorso del servizio directory si trova in Parse.cpp. Il parser di percorso è un componente chiave nei componenti del provider ADs. Verifica la validità sintattica di un percorso ADs passato a questo provider. Se la sintassi è valida, viene costruita una struttura **OBJECTINFO** che contiene una versione in componenti di ADspath per questo oggetto.

Tenere presente che si tratta solo di una verifica della sintassi. Invece di creare casi speciali per ogni nuova iterazione del percorso, tutte le verifiche del percorso devono essere conformi alle regole di grammatica stabilite dal parser.

La tabella seguente elenca le funzioni e i metodi implementati in Parse.cpp.



| Elemento                      | Descrizione                                                                                                                                                            |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ADsObject**             | Analizza il percorso ADs passato. Questa funzione segue le regole grammaticali seguenti: &lt; ADsObject &gt;  ->  &lt; ProviderName &gt; &lt; SampleDSObject&gt;<br/>     |
| **SampleDSObject**        | Analizza le regole grammaticali seguenti: &lt; SampleDSObject &gt; -> " \\ \\ identificatore " " &lt; &gt; \\ &lt; Pathname&gt;<br/>                                            |
| **ProviderName**          | Aggiunge il nome del provider sintatticamente corretto, se non è presente.                                                                                                          |
| **PathName**              | Analizza le regole di grammatica seguenti: &lt; Componente Pathname &gt;  ->  &lt; " " &gt; \\ \\ &lt; Pathname &gt; OR<br/> &lt;Componente &gt; Pathname  ->  &lt;&gt;<br/> |
| **Componente**             | Analizza le regole grammaticali seguenti: &lt; Identificatore &gt; OR<br/> &lt;Identificatore &gt; "=" &lt; Identificatore&gt;<br/>                                              |
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



 

 

 





