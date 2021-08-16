---
title: Paging con IDirectorySearch
description: Il paging specifica il numero di righe restituite dal server al client.
ms.assetid: cf4aa56a-c6f7-47c8-956d-512a5cffbf22
ms.tgt_platform: multiple
keywords:
- Paging con IDirectorySearch ADSI
- ADSI, Ricerca, IDirectorySearch, Altre opzioni di ricerca, Paging
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48494c01831e6b69931fc6b6f779ed9b042b7fecaaf17fa62286c094a926ba73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838941"
---
# <a name="paging-with-idirectorysearch"></a>Paging con IDirectorySearch

Il paging specifica il numero di righe restituite dal server al client. Una pagina può essere definita dal numero di righe o da un limite di tempo. L'oggetto ADSI COM recupera ogni pagina di risultati in base ai valori elencati nella tabella seguente. Il chiamante [**chiama IDirectorySearch::GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) quando ha raggiunto la fine della pagina e l'oggetto ADSI COM recupera la pagina successiva.



| Valore                                   | Descrizione                                                                                                                                                                                                                                          |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ADS \_ SEARCHPREF \_ PAGESIZE**           | Specifica il numero massimo di righe da restituire in una pagina.                                                                                                                                                                                            |
| **ADS SEARCHPREF PAGED TIME LIMIT (LIMITE DI TEMPO DI PAGINAZIONE DI ADS \_ \_ \_ \_ SEARCHPREF)** | Specifica il tempo massimo, in secondi, che il server deve dedicare alla raccolta di una pagina di risultati prima di restituire la pagina al client. Se viene raggiunto il limite, il server arresta la ricerca e restituisce le righe già recuperate per la pagina. |



 

Se nessuna di queste preferenze di ricerca è impostata, il valore predefinito è no paging. Le ricerche di Active Directory eseguite senza paging sono limitate alla restituzione di un massimo dei primi 1000 record, pertanto è necessario usare una ricerca di paging se esiste la possibilità che il set di risultati conterrà più di 1000 elementi.

Un'operazione di ricerca può comportare la restituita di un numero elevato di oggetti. Se il server restituisce il risultato in un set, potrebbe ridurre le prestazioni del client e del server, nonché influire sul carico di rete. Per evitare questo problema, è possibile usare ricerche di pagine. In una ricerca di pagine, il client può accettare risultati in pacchetti più piccoli. Le dimensioni di un pacchetto sono note come dimensioni della pagina di ricerca.

Le ricerche di pagine offrono vantaggi sia per il client che per il server. Il client può essere più reattivo nella presentazione dei risultati agli utenti. Ciò è particolarmente rilevante per gli strumenti dell'interfaccia utente grafica che possono avviare il processo di visualizzazione della finestra mentre l'altro thread riceve contemporaneamente i dati.

Sul lato server, le ricerche di pagine rendono scalabile l'operazione. Ad esempio, se uncento client emettere richieste di ricerca contemporaneamente e, in media, ogni client riceve duecento oggetti. Se non vengono specificate dimensioni di pagina, nello scenario peggiore, il server deve avere memoria sufficiente per contenere 20.000 oggetti. Viceversa, se ogni client specifica una dimensione di pagina come, ad esempio, dieci oggetti, il requisito di memoria nel server viene quindi ridotto di un fattore di 20.

Inoltre, usando una ricerca di pagine, un client può abbandonare l'operazione in corso. Al contrario, in una ricerca non di pagina il client riceve un set di risultati in un pacchetto. Ciò può ridurre le prestazioni di rete.

ADSI gestisce le dimensioni della pagina per il client. Il client non deve contare il numero di oggetti in corso. ADSI incapsula l'interazione del server per il client. Dal punto di vista del client, la ricerca restituisce un set di risultati completo.

È consigliabile usare il paging.

Per specificare le dimensioni massime della pagina, impostare un'opzione di ricerca **ADS \_ SEARCHPREF \_ PAGESIZE** con un valore **ADSTYPE \_ INTEGER** impostato sul numero massimo di righe per pagina nella matrice [**ADS \_ SEARCHPREF \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passata al metodo [**IDirectorySearch::SetSearchPreference.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference)

Nell'esempio di codice seguente viene illustrato come impostare le dimensioni massime della pagina.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_PAGESIZE;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 1000;
```



Per specificare un tempo di pagina, impostare un'opzione di ricerca **ADS \_ SEARCHPREF \_ PAGED \_ TIME \_ LIMIT** con un valore **ADSTYPE \_ INTEGER** impostato sul numero massimo di secondi che il server deve dedicare al recupero di una pagina nella matrice [**ADS \_ SEARCHPREF \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passata al metodo [**IDirectorySearch::SetSearchPreference.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference)

Nell'esempio di codice seguente viene illustrato come specificare l'ora della pagina.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_PAGED_TIME_LIMIT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 60;
```



 

 




