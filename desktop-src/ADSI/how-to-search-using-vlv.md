---
title: Come eseguire ricerche con VLV
description: Active Directory supporta le ricerche VLV (Virtual List View). Questo stile di ricerca è progettato specificamente per set di risultati di grandi dimensioni e consente a un'applicazione di visualizzare un subset di migliaia di voci senza dover recuperare effettivamente ogni voce.
ms.assetid: fea04190-0846-4b62-99f4-7d8fb35fd510
ms.tgt_platform: multiple
keywords:
- Come eseguire ricerche con VLV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 060878f6e7bb21d81556dfce998c5fb311b8f78197312e2a576e121356283c28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118017486"
---
# <a name="how-to-search-using-vlv"></a>Come eseguire ricerche con VLV

Active Directory supporta le ricerche VLV (Virtual List View). Questo stile di ricerca è progettato specificamente per set di risultati di grandi dimensioni e consente a un'applicazione di visualizzare un subset di migliaia di voci senza dover recuperare effettivamente ogni voce.

È possibile usare una ricerca VLV in due modi diversi. Il primo è recuperare gli attributi per voci specifiche in base a un offset numerico. Questo metodo è utile quando si recuperano i risultati della ricerca in risposta a un'operazione di scorrimento.

Il secondo modo per usare le ricerche VLV è cercare parte o tutto un attributo testuale e visualizzare solo i risultati della ricerca. Un esempio di utilizzo è una rubrica. Se l'utente scrive una "s", l'applicazione può usare una ricerca VLV per cercare le voci con un nome comune che inizia con "s". Se l'utente aggiunge quindi una "m" alle "s", l'applicazione può usare un'altra ricerca VLV per cercare le voci con un nome comune che inizia con "sm".

Per eseguire una ricerca VLV, indicare ad ADSI di usare il controllo VLV. A tale scopo, chiamare il metodo [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) con **un'opzione di ricerca \_ \_ VLV ADS SEARCHPREF** con **un valore ADSTYPE \_ PROV \_ SPECIFIC.** Il **valore ADSTYPE \_ PROV \_ SPECIFIC** è un puntatore a [**una struttura \_ ADS VLV**](/windows/desktop/api/Iads/ns-iads-ads_vlv) che contiene i dati sulla ricerca. La [**funzione di esempio GetVLVItemCount**](example-code-for-using-a-vlv-search.md) illustra come impostare entrambe queste preferenze di ricerca.

Tutte le ricerche VLV devono usare l'ordinamento dei risultati sul lato server, che viene eseguito impostando la preferenza di ricerca **ADS \_ SEARCHPREF \_ SORT \_ ON.** Per altre informazioni sulla preferenza di ricerca **ADS \_ SEARCHPREF \_ SORT \_ ON,** vedere Ordinamento dei risultati [della ricerca con IDirectorySearch](sorting-the-search-results-with-idirectorysearch.md).

Quando viene eseguita una ricerca VLV, una determinata quantità di metadati relativi alla ricerca viene restituita in una colonna recuperata chiamando [**IDirectorySearch::GetColumn con**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) l'identificatore **ADS \_ VLV \_ RESPONSE.** Questi dati sono contenuti in una [**struttura ADS \_ VLV.**](/windows/desktop/api/Iads/ns-iads-ads_vlv) Di particolare importanza sono i **membri dwContentCount** **e lpContextID.** Il **membro dwContentCount** conterrà il numero di risultati che soddisfano i criteri di ricerca VLV. Questo valore può essere usato come stima del numero totale di elementi che verrebbero restituiti per una ricerca di quel tipo. Il **membro lpContextID** contiene un valore definito dal server che può essere passato alla ricerca successiva per identificare la ricerca. L'uso **di lpContextID può** migliorare le prestazioni di ricerca. Tenere presente che **lpContextID** è un valore definito dal server e la relativa lunghezza è contenuta nel **membro dwContextIDLength.** Questo buffer viene liberato quando viene chiamato il metodo [**IDirectorySearch::FreeColumn,**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn) quindi il chiamante deve allocare un buffer delle dimensioni appropriate e copiare e salvare il contenuto del buffer tra le ricerche.

Per altre informazioni sul controllo VLV LDAP, vedere [Ricerca con il controllo VLV LDAP](/previous-versions/windows/desktop/ldap/searching-with-the-ldap-vlv-control).

Per altre informazioni, vedere:

-   Recupero del numero di elementi
-   Ricerca in base all'offset
-   Ricerca per stringa
-   [Codice di esempio per l'uso di una ricerca VLV](example-code-for-using-a-vlv-search.md)

## <a name="obtaining-the-number-of-items"></a>Recupero del numero di elementi

**Per ottenere una stima del numero di elementi che verranno restituiti per una ricerca specifica, seguire questa procedura.**

1.  Compilare [**una struttura \_ ADS VLV**](/windows/desktop/api/Iads/ns-iads-ads_vlv) con tutti i valori zero **o NULL.**
2.  Compilare [**ad ADS \_ SEARCHPREF \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) i valori seguenti.

    -   Impostare il **membro dwSearchPref** **su ADS \_ SEARCHPREF \_ VLV**.
    -   Impostare il **membro vValue.dwType** **su ADSTYPE \_ PROV \_ SPECIFIC**.
    -   Impostare il **membro vValue.ProviderSpecific.dwLength** sulla dimensione della [**struttura \_ ADS VLV.**](/windows/desktop/api/Iads/ns-iads-ads_vlv)
    -   Impostare il **membro vValue.ProviderSpecific.lpValue** sull'indirizzo della struttura [**\_ ADS VLV**](/windows/desktop/api/Iads/ns-iads-ads_vlv) del passaggio 1.

3.  Compilare [**una struttura ADS \_ SORTKEY**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) come illustrato in Ordinamento dei risultati della ricerca [con IDirectorySearch](sorting-the-search-results-with-idirectorysearch.md) per ordinare in base all'attributo desiderato.
4.  Compilare [**un'altra struttura ADS \_ SEARCHPREF \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) per aggiungere la struttura [**ADS \_ SORTKEY**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) alle preferenze di ricerca, come illustrato in Ordinamento dei risultati della ricerca [con IDirectorySearch](sorting-the-search-results-with-idirectorysearch.md).
5.  Aggiungere eventuali altre preferenze di ricerca desiderate e chiamare [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) per impostare le preferenze di ricerca.
6.  Eseguire la ricerca con [**IDirectorySearch::ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch).
7.  Ottenere la prima riga di risultati chiamando [**IDirectorySearch::GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow).
8.  Chiamare [**IDirectorySearch::GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) con **ADS \_ VLV \_ RESPONSE** per ottenere i metadati di ricerca VLV.
9.  Eseguire il **cast di pADsValues->ProviderSpecific.lpValue** della struttura [**ADS SEARCH \_ \_ COLUMN**](/windows/desktop/api/Iads/ns-iads-ads_search_column) a un puntatore alla struttura [**ADS \_ VLV.**](/windows/desktop/api/Iads/ns-iads-ads_vlv) Il **membro dwContentCount** di questa **struttura ADS \_ VLV** contiene il numero approssimativo di elementi che verrebbero restituiti da una ricerca di quel tipo.
10. Se verranno eseguite altre ricerche VLV dello stesso tipo, creare una copia dei dati **lpContextID** e conservarla per la ricerca VLV successiva.

La [**funzione di esempio GetVLVItemCount**](example-code-for-using-a-vlv-search.md) illustra come eseguire questa operazione.

## <a name="searching-by-offset"></a>Ricerca in base all'offset

Un aspetto che rende le ricerche VLV così rapide è che è possibile cercare un risultato specifico in base a un offset numerico. Ad esempio, se una ricerca restituisce 10.000 elementi, una ricerca VLV consente di ottenere le informazioni per circa il 4072° elemento senza dover recuperare tutti gli elementi prima dell'elemento in questione.

Gli offset vengono specificati come rapporto tra l'offset e il conteggio del contenuto. I rapporti sono utili perché il server potrebbe non avere una stima accurata del numero di voci presenti nell'elenco o le dimensioni dell'elenco potrebbero cambiare durante l'esplorazione da parte dell'utente. Poiché è necessario indicare l'inizio e la fine dell'elenco, è possibile usare un valore stimato per il conteggio dei contenuti nella prima richiesta di ricerca, insieme a un valore di offset. Il server usa questi dati per calcolare gli offset corrispondenti all'interno dell'elenco, in base all'idea del conteggio dei contenuti, che viene inviato nella risposta al client tramite il membro **dwContentCount** della struttura [**\_ ADS VLV.**](/windows/desktop/api/Iads/ns-iads-ads_vlv) Ad esempio, se si stima che le dimensioni dell'elenco siano 3000 e si vuole che l'offset sia la voce di elenco 1500, impostare **dwContentCount** su 3000 e **dwOffset** su 1500. Se il server stima che le dimensioni effettive dell'elenco siano 4500, ricalcolerà l'offset a 2250 e restituirà le nuove stime in **dwContentCount** e **dwOffset**.

> [!Note]
>
> Tutti i valori numerici in una ricerca VLV sono approssimazioni e non devono essere usati per i valori assoluti. Ad esempio, se si emettere una ricerca VLV per il 50° elemento in una razione di 100, non è garantito ottenere l'elemento intermedio esatto.
>
> **Per cercare un elemento specifico in base all'offset, seguire questa procedura.**
>
> 1.  Compilare [**una struttura \_ ADS VLV**](/windows/desktop/api/Iads/ns-iads-ads_vlv) con i valori seguenti. I membri aggiuntivi della struttura devono essere impostati su zero o **NULL.**
>
>     -   Impostare il **membro dwContentCount** sul valore massimo del rapporto tra gli elementi da recuperare.
>     -   Impostare il **membro dwOffset** sul rapporto, relativo a **dwContentCount**, dell'elemento o degli elementi da recuperare.
>     -   Impostare il **membro lpContextID** sull'indirizzo della copia del buffer dell'ID di contesto e **dwContextIDLength sulla** lunghezza, in byte, del buffer dell'ID di contesto. Se non è stato salvato alcun ID contesto, entrambi i membri devono essere zero o **NULL.**
>
> 2.  Impostare le preferenze di ricerca come illustrato nei passaggi da 2 a 5 della procedura Ottenere il numero di elementi.
> 3.  Eseguire la ricerca con [**IDirectorySearch::ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch).
> 4.  Ottenere la prima riga di risultati chiamando [**IDirectorySearch::GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow).
> 5.  Chiamare [**IDirectorySearch::GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) con il nome dell'attributo da recuperare per ottenere i dati effettivi per l'elemento richiesto.
> 6.  Chiamare [**IDirectorySearch::GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) con **ADS \_ VLV \_ RESPONSE** per ottenere i metadati di ricerca VLV.
> 7.  Eseguire il **cast di pADsValues->ProviderSpecific.lpValue** della struttura [**ADS SEARCH \_ \_ COLUMN**](/windows/desktop/api/Iads/ns-iads-ads_search_column) a un puntatore alla struttura [**ADS \_ VLV.**](/windows/desktop/api/Iads/ns-iads-ads_vlv)
> 8.  Creare una copia dei dati **lpContextID** e conservarla per la successiva ricerca VLV.

 

La [**funzione di esempio GetVLVItemText**](example-code-for-using-a-vlv-search.md) illustra come eseguire questa operazione.

È anche possibile recuperare più righe di dati con una singola chiamata di ricerca. Questa operazione viene eseguita nel passaggio 1 impostando in modo appropriato i membri **dwBeforeCount** e **dwAfterCount** della struttura [**\_ ADS VLV.**](/windows/desktop/api/Iads/ns-iads-ads_vlv) Il **membro dwBeforeCount** contiene il numero di elementi visualizzati nell'elenco prima dell'elemento in questione e il membro **dwAfterCount** contiene il numero di elementi visualizzati nell'elenco dopo l'elemento in questione. Entrambi questi conteggi escludono l'elemento stesso, pertanto l'impostazione di **dwBeforeCount** su 10 e **dwAfterCount** su 10 comporta un totale di 21 elementi restituiti. Questa opzione consente di memorizzare nella cache i risultati della ricerca sul lato client.

## <a name="searching-by-string"></a>Ricerca per stringa

È anche possibile usare una ricerca VLV per trovare gli elementi con un attributo stringa il cui valore corrisponde a tutta o parte di una stringa senza dover recuperare tutti gli elementi. La corrispondenza delle stringhe viene eseguita sull'attributo specificato nella struttura [**ADS \_ SORTKEY**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) della preferenza di ricerca **ADS \_ SEARCHPREF \_ SORT \_ ON.**

**Per cercare un elemento specifico in base alla stringa, seguire questa procedura.**

1.  Compilare [**una struttura \_ ADS VLV**](/windows/desktop/api/Iads/ns-iads-ads_vlv) con i valori seguenti. I membri aggiuntivi della struttura devono essere impostati su zero o **NULL.**

    -   Impostare il **membro pszTarget** su un puntatore a una stringa con terminazione NULL contenente la stringa da cercare.
    -   Impostare il **membro lpContextID** sull'indirizzo della copia del buffer dell'ID di contesto e **dwContextIDLength sulla** lunghezza, in byte, del buffer dell'ID di contesto. Se non è stato salvato alcun ID contesto, entrambi i membri devono essere zero o **NULL.**

2.  Impostare le preferenze di ricerca come illustrato nei passaggi da 2 a 5 della procedura Ottenere il numero di elementi.
3.  Eseguire la ricerca con [**IDirectorySearch::ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch).
4.  Ottenere la prima riga di risultati chiamando [**IDirectorySearch::GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow).
5.  Chiamare [**IDirectorySearch::GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) con il nome dell'attributo da recuperare per ottenere i dati effettivi per l'elemento richiesto.
6.  Chiamare [**IDirectorySearch::GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) con **ADS \_ VLV \_ RESPONSE** per ottenere i metadati di ricerca VLV.
7.  Eseguire il **cast di pADsValues->ProviderSpecific.lpValue** della struttura [**ADS SEARCH \_ \_ COLUMN**](/windows/desktop/api/Iads/ns-iads-ads_search_column) a un puntatore alla struttura [**ADS \_ VLV.**](/windows/desktop/api/Iads/ns-iads-ads_vlv)
8.  Creare una copia dei dati **lpContextID** e conservarla per la successiva ricerca VLV. Se necessario, il **membro dwOffset** contiene l'indice in base uno del primo elemento il cui attributo stringa inizia con il valore specificato in **pszTarget**.

La [**funzione di esempio GetVLVItemsByString**](example-code-for-using-a-vlv-search.md) illustra come eseguire questa operazione.

Analogamente alla ricerca in base all'indice, è anche possibile recuperare più righe di dati con una singola chiamata di ricerca. Questa operazione viene eseguita nello stesso modo impostando in modo appropriato i membri **dwBeforeCount** e **dwAfterCount** della struttura [**\_ ADS VLV.**](/windows/desktop/api/Iads/ns-iads-ads_vlv)

 

 