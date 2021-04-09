---
title: Come eseguire la ricerca con VLV
description: Active Directory supporta le ricerche VLV (Virtual List View). Questo stile di ricerca è progettato appositamente per set di risultati di grandi dimensioni e consente a un'applicazione di visualizzare un subset di migliaia di voci senza dover recuperare ogni voce.
ms.assetid: fea04190-0846-4b62-99f4-7d8fb35fd510
ms.tgt_platform: multiple
keywords:
- Come eseguire la ricerca con VLV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f4a24250c8e54ccb7917f86b193152c62810b93
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103963461"
---
# <a name="how-to-search-using-vlv"></a>Come eseguire la ricerca con VLV

Active Directory supporta le ricerche VLV (Virtual List View). Questo stile di ricerca è progettato appositamente per set di risultati di grandi dimensioni e consente a un'applicazione di visualizzare un subset di migliaia di voci senza dover recuperare ogni voce.

È possibile utilizzare una ricerca VLV in due modi distinti. Il primo consiste nel recuperare gli attributi per voci specifiche in base a un offset numerico. Questo metodo è utile quando si recuperano i risultati della ricerca in risposta a un'operazione di scorrimento.

Il secondo modo per usare le ricerche VLV consiste nel cercare parte o tutti gli attributi testuali e visualizzare solo i risultati della ricerca. Un esempio di utilizzo di questa è una rubrica. Se l'utente digita una "s", l'applicazione può usare una ricerca VLV per cercare le voci con un nome comune che inizia con "s". Se l'utente aggiunge una "m" alla "s", l'applicazione può usare un'altra ricerca VLV per cercare le voci con un nome comune che inizia con "SM".

Per eseguire una ricerca VLV, indicare a ADSI di usare il controllo VLV. A tale scopo, chiamare il metodo [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) con un'opzione di ricerca **Ads \_ SEARCHPREF \_ VLV** con un valore **specifico di ADSTYPE \_ prov \_** . Il **valore \_ \_ specifico di ADSTYPE prov** è un puntatore a una struttura [**\_ VLV ADS**](/windows/desktop/api/Iads/ns-iads-ads_vlv) che contiene i dati relativi alla ricerca. La funzione di esempio [**GetVLVItemCount**](example-code-for-using-a-vlv-search.md) Mostra come impostare entrambe le preferenze di ricerca.

Tutte le ricerche VLV devono usare l'ordinamento dei risultati sul lato server, che viene eseguito impostando le preferenze di ricerca di **\_ SEARCHPREF \_ \_ per gli annunci** . Per altre informazioni sulle preferenze di ricerca per gli **annunci \_ SEARCHPREF \_ \_** , vedere [ordinamento dei risultati della ricerca con IDirectorySearch](sorting-the-search-results-with-idirectorysearch.md).

Quando viene eseguita una ricerca VLV, una determinata quantità di metadati relativi alla ricerca viene restituita in una colonna recuperata chiamando [**IDirectorySearch:: GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) con l'identificatore **di \_ \_ risposta VLV ADS** . Questi dati sono contenuti in una [**struttura \_ VLV ADS**](/windows/desktop/api/Iads/ns-iads-ads_vlv) . Di particolare importanza sono i membri **dwContentCount** e **lpContextID** . Il membro **dwContentCount** conterrà il numero di risultati che soddisfano i criteri di ricerca VLV. Questo valore può essere utilizzato come stima del numero totale di elementi che verrebbero restituiti per una ricerca di quel tipo. Il membro **lpContextID** contiene un valore definito dal server che può essere passato alla ricerca successiva per identificare la ricerca. L'uso di **lpContextID** può migliorare le prestazioni di ricerca. Tenere presente che **lpContextID** è un valore definito dal server e che la sua lunghezza è contenuta nel membro **dwContextIDLength** . Questo buffer viene liberato quando viene chiamato il metodo [**IDirectorySearch:: FreeColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn) , quindi il chiamante deve allocare un buffer di dimensioni appropriate e copiare e salvare il contenuto del buffer tra le ricerche.

Per ulteriori informazioni sul controllo LDAP VLV, vedere [ricerca con il controllo LDAP VLV](/previous-versions/windows/desktop/ldap/searching-with-the-ldap-vlv-control).

Per altre informazioni, vedere:

-   Recupero del numero di elementi
-   Ricerca per offset
-   Ricerca per stringa
-   [Codice di esempio per l'uso di una ricerca VLV](example-code-for-using-a-vlv-search.md)

## <a name="obtaining-the-number-of-items"></a>Recupero del numero di elementi

**Per ottenere una stima del numero di elementi che verranno restituiti per una particolare ricerca, seguire questa procedura.**

1.  Compilare una struttura [**Ads \_ VLV**](/windows/desktop/api/Iads/ns-iads-ads_vlv) con tutti i valori zero o **null** .
2.  Compilare un [**annuncio \_ SEARCHPREF \_ info**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) con i valori seguenti.

    -   Impostare il membro **dwSearchPref** su **Ads \_ SEARCHPREF \_ VLV**.
    -   Impostare il membro **vValue. dwType** su **ADSTYPE \_ prov \_ specific**.
    -   Impostare il membro **vValue. ProviderSpecific. dwLength** sulla dimensione della struttura [**Ads \_ VLV**](/windows/desktop/api/Iads/ns-iads-ads_vlv) .
    -   Impostare il membro **vValue. ProviderSpecific. lpValue** sull'indirizzo della struttura [**Ads \_ VLV**](/windows/desktop/api/Iads/ns-iads-ads_vlv) del passaggio 1.

3.  Compilare una struttura di [**\_ SORTKEY ADS**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) come illustrato nell' [ordinamento dei risultati della ricerca con IDirectorySearch](sorting-the-search-results-with-idirectorysearch.md) per ordinare l'attributo desiderato.
4.  Compilare un altro [**annuncio \_ SEARCHPREF \_ info**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) per aggiungere la struttura di [**\_ SORTKEY ADS**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) alle preferenze di ricerca, come illustrato nell' [ordinamento dei risultati della ricerca con IDirectorySearch](sorting-the-search-results-with-idirectorysearch.md).
5.  Aggiungere le altre preferenze di ricerca desiderate e chiamare [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) per impostare le preferenze di ricerca.
6.  Eseguire la ricerca con [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch).
7.  Ottenere la prima riga di risultati chiamando [**IDirectorySearch:: GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow).
8.  Chiamare [**IDirectorySearch:: GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) con **Ads \_ VLV \_ Response** per ottenere i metadati di ricerca VLV.
9.  Eseguire il cast di **pADsValues->ProviderSpecific. lpValue** della struttura della [**\_ \_ colonna di ricerca ADS**](/windows/desktop/api/Iads/ns-iads-ads_search_column) a un puntatore alla struttura [**Ads \_ VLV**](/windows/desktop/api/Iads/ns-iads-ads_vlv) . Il membro **dwContentCount** della struttura **Ads \_ VLV** contiene il numero approssimativo di elementi che verrebbero restituiti da una ricerca di quel tipo.
10. Se verranno eseguite altre ricerche VLV dello stesso tipo, creare una copia dei dati **lpContextID** e conservarla per la successiva ricerca VLV.

La funzione di esempio [**GetVLVItemCount**](example-code-for-using-a-vlv-search.md) illustra come eseguire questa operazione.

## <a name="searching-by-offset"></a>Ricerca per offset

Una cosa che rende le ricerche VLV in modo rapido è che è possibile cercare un risultato specifico in base a un offset numerico. Se, ad esempio, una ricerca restituisce 10.000 elementi restituiti, una ricerca di VLV consente di ottenere le informazioni per approssimativamente l'elemento 4072nd senza dover recuperare tutti gli elementi prima dell'elemento in questione.

Gli offset vengono specificati come rapporto tra l'offset e il conteggio del contenuto. I rapporti sono utili perché è possibile che il server non disponga di una stima accurata del numero di voci presenti nell'elenco oppure che le dimensioni dell'elenco possano variare durante il periodo di esplorazione dell'utente. Poiché è necessario indicare l'inizio e la fine dell'elenco, è possibile usare un valore stimato per il conteggio contenuto nella prima richiesta di ricerca, insieme a un valore di offset. Il server usa questi dati per calcolare gli offset corrispondenti all'interno dell'elenco, in base all'idea del conteggio contenuto, che viene inviato in risposta al client tramite il membro **dwContentCount** della struttura [**\_ VLV ADS**](/windows/desktop/api/Iads/ns-iads-ads_vlv) . Se ad esempio si stima che le dimensioni dell'elenco siano pari a 3000 e si desidera che l'offset sia la voce di elenco 1500, è necessario impostare **dwContentCount** su 3000 e **dwOffset** su 1500. Se il server stima le dimensioni effettive dell'elenco come 4500, l'offset verrà ricalcolato a 2250 e verranno restituite le nuove stime in **dwContentCount** e **dwOffset**.

> [!Note]
>
> Tutti i valori numerici in una ricerca VLV sono approssimazioni e non devono essere usati per i valori assoluti. Se, ad esempio, si esegue una ricerca VLV per il cinquantesimo elemento in una razione di 100, non è garantito l'ottenimento dell'elemento intermedio esatto.
>
> **Per cercare un determinato elemento in base all'offset, seguire questa procedura.**
>
> 1.  Compilare una struttura [**Ads \_ VLV**](/windows/desktop/api/Iads/ns-iads-ads_vlv) con i valori seguenti. I membri aggiuntivi della struttura devono essere impostati su zero o **null**.
>
>     -   Impostare il membro **dwContentCount** sul valore massimo del rapporto tra gli elementi da recuperare.
>     -   Impostare il membro **dwOffset** sul rapporto rispetto a **dwContentCount** per l'elemento o gli elementi da recuperare.
>     -   Impostare il membro **lpContextID** sull'indirizzo della copia del buffer dell'ID del contesto e il **dwContextIDLength** sulla lunghezza, in byte, del buffer dell'ID del contesto. Se non è stato salvato alcun ID contesto, entrambi i membri devono essere zero o **null**.
>
> 2.  Impostare le preferenze di ricerca come illustrato nei passaggi da 2 a 5 della procedura recupero del numero di elementi.
> 3.  Eseguire la ricerca con [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch).
> 4.  Ottenere la prima riga di risultati chiamando [**IDirectorySearch:: GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow).
> 5.  Chiamare [**IDirectorySearch:: GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) con il nome dell'attributo da recuperare per ottenere i dati effettivi per l'elemento richiesto.
> 6.  Chiamare [**IDirectorySearch:: GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) con **Ads \_ VLV \_ Response** per ottenere i metadati di ricerca VLV.
> 7.  Eseguire il cast di **pADsValues->ProviderSpecific. lpValue** della struttura della [**\_ \_ colonna di ricerca ADS**](/windows/desktop/api/Iads/ns-iads-ads_search_column) a un puntatore alla struttura [**Ads \_ VLV**](/windows/desktop/api/Iads/ns-iads-ads_vlv) .
> 8.  Creare una copia dei dati di **lpContextID** e conservarla per la successiva ricerca di VLV.

 

La funzione di esempio [**GetVLVItemText**](example-code-for-using-a-vlv-search.md) illustra come eseguire questa operazione.

È anche possibile recuperare più di una riga di dati con una singola chiamata di ricerca. Questa operazione viene eseguita nel passaggio 1 impostando in modo appropriato i membri **dwBeforeCount** e **DwAfterCount** della struttura [**Ads \_ VLV**](/windows/desktop/api/Iads/ns-iads-ads_vlv) . Il membro **dwBeforeCount** contiene il numero di elementi visualizzati nell'elenco prima dell'elemento in questione e il membro **dwAfterCount** contiene il numero di elementi visualizzati nell'elenco dopo l'elemento in questione. Entrambi i conteggi escludono l'elemento stesso, quindi impostando **dwBeforeCount** su 10 e **dwAfterCount** su 10 si otterrà un totale di 21 elementi restituiti. Questa opzione consente di memorizzare nella cache i risultati della ricerca sul lato client.

## <a name="searching-by-string"></a>Ricerca per stringa

È anche possibile usare una ricerca VLV per trovare gli elementi che hanno un attributo di stringa il cui valore corrisponde a tutta o parte di una stringa senza dover recuperare tutti gli elementi. La corrispondenza di stringa viene eseguita in base all'attributo specificato nella struttura [**\_ SORTKEY ADS**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) della **preferenza \_ SEARCHPREF \_ Sort \_ on** search.

**Per cercare un particolare elemento in base alla stringa, seguire questa procedura.**

1.  Compilare una struttura [**Ads \_ VLV**](/windows/desktop/api/Iads/ns-iads-ads_vlv) con i valori seguenti. I membri aggiuntivi della struttura devono essere impostati su zero o **null**.

    -   Impostare il membro **pszTarget verranno rimosse** su un puntatore a una stringa con terminazione null che contiene la stringa da cercare.
    -   Impostare il membro **lpContextID** sull'indirizzo della copia del buffer dell'ID del contesto e il **dwContextIDLength** sulla lunghezza, in byte, del buffer dell'ID del contesto. Se non è stato salvato alcun ID contesto, entrambi i membri devono essere zero o **null**.

2.  Impostare le preferenze di ricerca come illustrato nei passaggi da 2 a 5 della procedura recupero del numero di elementi.
3.  Eseguire la ricerca con [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch).
4.  Ottenere la prima riga di risultati chiamando [**IDirectorySearch:: GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow).
5.  Chiamare [**IDirectorySearch:: GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) con il nome dell'attributo da recuperare per ottenere i dati effettivi per l'elemento richiesto.
6.  Chiamare [**IDirectorySearch:: GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) con **Ads \_ VLV \_ Response** per ottenere i metadati di ricerca VLV.
7.  Eseguire il cast di **pADsValues->ProviderSpecific. lpValue** della struttura della [**\_ \_ colonna di ricerca ADS**](/windows/desktop/api/Iads/ns-iads-ads_search_column) a un puntatore alla struttura [**Ads \_ VLV**](/windows/desktop/api/Iads/ns-iads-ads_vlv) .
8.  Creare una copia dei dati di **lpContextID** e conservarla per la successiva ricerca di VLV. Se necessario, il membro **dwOffset** contiene l'indice in base uno del primo elemento il cui attributo String inizia con il valore specificato in **pszTarget verranno rimosse**.

La funzione di esempio [**GetVLVItemsByString**](example-code-for-using-a-vlv-search.md) illustra come eseguire questa operazione.

Analogamente alla ricerca in base all'indice, è anche possibile recuperare più di una riga di dati con una singola chiamata di ricerca. Questa operazione viene eseguita nello stesso modo impostando in modo appropriato i membri **dwBeforeCount** e **DwAfterCount** della struttura [**Ads \_ VLV**](/windows/desktop/api/Iads/ns-iads-ads_vlv) .

 

 