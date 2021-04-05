---
title: Paging con IDirectorySearch
description: Il paging specifica il numero di righe restituite dal server al client.
ms.assetid: cf4aa56a-c6f7-47c8-956d-512a5cffbf22
ms.tgt_platform: multiple
keywords:
- Paging con IDirectorySearch ADSI
- ADSI, ricerca, IDirectorySearch, altre opzioni di ricerca, paging
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e9fdf001f5908f6c3fc7321c8c94cda09f1b96
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955090"
---
# <a name="paging-with-idirectorysearch"></a>Paging con IDirectorySearch

Il paging specifica il numero di righe restituite dal server al client. È possibile definire una pagina in base al numero di righe o a un limite di tempo. L'oggetto ADSI COM recupera ogni pagina di risultati in base ai valori elencati nella tabella seguente. Il chiamante chiama [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) quando ha raggiunto la fine della pagina e l'oggetto ADSI com recupera la pagina successiva.



| Valore                                   | Descrizione                                                                                                                                                                                                                                          |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_SEARCHPREF Ads \_**           | Specifica il numero massimo di righe da restituire in una pagina.                                                                                                                                                                                            |
| **\_limite di \_ tempo di \_ paging \_ per ADS SEARCHPREF** | Specifica il tempo massimo, in secondi, impiegato dal server per la raccolta di una pagina di risultati prima che la pagina venga restituita al client. Se viene raggiunto il limite, il server interrompe la ricerca e restituisce le righe già recuperate per la pagina. |



 

Se nessuna di queste preferenze di ricerca è impostata, il valore predefinito non è paging. Le ricerche delle Active Directory eseguite senza paging sono limitate alla restituzione di un massimo dei primi 1000 record, pertanto è necessario utilizzare una ricerca di paging se è possibile che il set di risultati contenga più di 1000 elementi.

Un'operazione di ricerca può comportare la restituzione di un numero elevato di oggetti. Se il server restituisce il risultato in un unico set, potrebbe ridurre le prestazioni del client e del server, nonché influenzare il carico di rete. Per evitare questo problema, è possibile utilizzare le ricerche di paging. In una ricerca di paging il client può accettare i risultati in pacchetti più piccoli. Le dimensioni di un pacchetto sono note come dimensioni della pagina di ricerca.

Le ricerche di paging offrono vantaggi sia per il client che per il server. Il client può essere più reattivo nella presentazione dei risultati agli utenti. Questo è particolarmente importante per gli strumenti dell'interfaccia utente grafica che possono iniziare il processo di visualizzazione della finestra mentre l'altro thread riceve contemporaneamente i dati.

Sul lato server, le ricerche di paging rendono l'operazione scalabile. Se, ad esempio, i client 100 inviano richieste di ricerca simultaneamente e, in media, ogni client riceve gli oggetti 200. Se non viene specificata alcuna dimensione di pagina, nello scenario peggiore il server deve disporre di memoria sufficiente per contenere gli oggetti 20.000. Viceversa, se ogni client specifica una dimensione di pagina, ad esempio dieci oggetti, il requisito di memoria sul server viene ridotto di un fattore pari a 20.

Inoltre, l'utilizzo di una ricerca di paging consente a un client di abbandonare l'operazione in corso. Al contrario, in una ricerca non di paging, il client riceve un set di risultati in un pacchetto. Ciò può ridurre le prestazioni della rete.

ADSI gestisce le dimensioni di pagina per il client. Il client non deve contare il numero di oggetti in corso. ADSI incapsula l'interazione del server per il client. Dal punto di vista del client, la ricerca restituisce un set di risultati completo.

Si consiglia di utilizzare il paging.

Per specificare una dimensione massima della pagina, impostare un'opzione di ricerca **Ads \_ SEARCHPREF \_ pageSize** con un valore **\_ Integer ADSTYPE** impostato sul numero massimo di righe per pagina nella matrice [**Ads \_ SEARCHPREF \_ info**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passata al metodo [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .

Nell'esempio di codice riportato di seguito viene illustrato come impostare le dimensioni massime della pagina.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_PAGESIZE;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 1000;
```



Per specificare un'ora di pagina, impostare un'opzione di ricerca per il **\_ limite di tempo di \_ paging \_ \_ ADS SEARCHPREF** con un valore **\_ Integer ADSTYPE** impostato sul numero massimo di secondi che il server deve spendere per recuperare una pagina nella matrice [**Ads \_ SEARCHPREF \_ info**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passata al metodo [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .

Nell'esempio di codice seguente viene illustrato come specificare l'ora della pagina.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_PAGED_TIME_LIMIT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 60;
```



 

 




