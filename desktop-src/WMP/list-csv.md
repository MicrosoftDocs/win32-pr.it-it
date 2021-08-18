---
title: list.csv
description: list.csv
ms.assetid: 020b213c-826c-430c-8ce7-92b819581de8
keywords:
- Windows Media Player online store,list.csv
- online store, list.csv
- digitare 1 online stores,list.csv
- list.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e754f7985fbf59c23cccae5fd9780ff4b4579205ceaf3ef3cc8f74c768d4e71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135344"
---
# <a name="listcsv"></a>list.csv

Questo file contiene una voce per ognuno degli elenchi contenuti nel catalogo. Gli elenchi possono essere elenchi di tracce, album, artista, generi, sottogeneri o feed radio; o possono essere elenchi di altri elenchi. Ogni voce di elenco è una riga composta dai campi delimitati da tabulazioni descritti nella tabella seguente. I campi devono essere visualizzati nell'ordine elencato.

La colonna Formato nella tabella seguente descrive il modo in cui viene formattato ogni campo di testo Unicode. Non fa riferimento al tipo di dati del contenuto. Ad esempio, se nella colonna Formato è indicato Integer, significa che il campo contiene una stringa Unicode che rappresenta un valore integrale, anziché un intero effettivo.



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Campo</th>
<th>Necessario</th>
<th>Formato</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ListID</td>
<td>Sì</td>
<td>Intero non negativo.</td>
<td>Identificatore di elenco, univoco all'interno list.csv. Deve essere non negativo e minore di 2^32. <strong>Visualizzazione di un nodo elenco nel controllo visualizzazione albero:</strong> Se ListID è 0, 1, 2, 3, 4, 5, 6 o 7, l'elenco verrà visualizzato come nodo personalizzato sotto il nodo di primo livello del negozio online nel controllo visualizzazione albero del lettore. I nodi personalizzati vengono visualizzati prima dei nodi standard nel nodo di primo livello del negozio online e sono posizionati in ordine crescente in base a ListID. Ad esempio, se sono presenti tre nodi personalizzati, con ListID 1, 3 e 5, verranno visualizzati per primo, secondo e terzo sotto il nodo di primo livello dello store online.<br/></td>
</tr>
<tr class="even">
<td>ListTitle</td>
<td>No</td>
<td>Stringa Unicode. Esempio: Top Ten Hits<br/></td>
<td>Titolo dell'elenco.</td>
</tr>
<tr class="odd">
<td>ListSubtitle</td>
<td>No</td>
<td>Stringa Unicode</td>
<td>Titolo alternativo dell'elenco, visualizzato nella seconda riga della visualizzazione Affiancato.</td>
</tr>
<tr class="even">
<td>ListDescription</td>
<td>Sì</td>
<td>Stringa Unicode</td>
<td>Testo visualizzato descrittivo dell'elenco (visualizzato nelle pagine delle proprietà).</td>
</tr>
<tr class="odd">
<td>Linked_ItemType</td>
<td>Sì</td>
<td>Stringa Unicode. Formato: [T| P| A| L|G| S| R]<br/> Esempio: T<br/></td>
<td>Indica il tipo degli elementi collegati.
<ul>
<li>T= Traccia</li>
<li>P = Esecutore</li>
<li>A = Album</li>
<li>L = Elenco</li>
<li>G = Genre</li>
<li>S = Sottogenere</li>
<li>R = Radio</li>
</ul></td>
</tr>
<tr class="even">
<td>ListPrice</td>
<td>Sì</td>
<td>Stringa Unicode. Esempio: $ 9,99<br/></td>
<td>Prezzo dell'elenco. Il simbolo di valuta deve essere incluso. Uno zero indica che l'elenco è gratuito. Nessun valore indica che il prezzo è sconosciuto. Un trattino indica che l'elenco non può essere acquistato.<br/></td>
</tr>
<tr class="odd">
<td>Popolarità</td>
<td>Sì</td>
<td>Valore intero o decimale. Esempio: 1259.3<br/></td>
<td>Indica la classificazione di popolarità quando questo elenco viene visualizzato in altri elenchi. Può essere zero se non applicabile.</td>
</tr>
<tr class="even">
<td>IsRecentlyAdded</td>
<td>Sì</td>
<td>Boolean.Format: [0|1]<br/> Esempio: 0<br/></td>
<td>Indica se l'elenco è stato aggiunto di recente.</td>
</tr>
<tr class="odd">
<td>IsFeatured</td>
<td>Sì</td>
<td>Boolean.Format: [0|1]<br/> Esempio: 0<br/></td>
<td>Indica se l'elenco è in primo piano. Può essere utilizzato per determinare l'ordinamento.</td>
</tr>
<tr class="even">
<td>EditorialGlyph</td>
<td>Sì</td>
<td>Intero non negativo. Deve essere 0.</td>
<td>Non usato in questa versione. Deve essere 0.</td>
</tr>
<tr class="odd">
<td>ViewType</td>
<td>Sì</td>
<td>Stringa Unicode. Formato: [I|T| R| L|O]Esempio: T<br/></td>
<td>Indica il tipo di visualizzazione da utilizzare per l'elenco.
<ul>
<li>I = Icona</li>
<li>T = Riquadro</li>
<li>R = Report</li>
<li>L = Elenco</li>
<li>O = Elenco ordinato</li>
</ul></td>
</tr>
<tr class="even">
<td>ViewImageSize</td>
<td>Sì</td>
<td>Intero non negativo. Esempio: 180<br/></td>
<td>Dimensioni in base alle quali viene visualizzata l'immagine dell'elenco. Se 0, le dimensioni vengono determinate automaticamente.</td>
</tr>
<tr class="odd">
<td>GroupBy</td>
<td>Sì</td>
<td>Stringa Unicode. Formato: [-| P| A| C|R| D]<br/> Esempio: P<br/></td>
<td>Indica il campo utilizzato per raggruppare gli elementi nell'elenco.
<ul>
<li>- = Automatico</li>
<li>P = Esecutore</li>
<li>A = Album</li>
<li>C = Composer</li>
<li>R = Classificazione</li>
<li>D = Data</li>
</ul></td>
</tr>
<tr class="even">
<td>ListItemsAreDynamic</td>
<td>Sì</td>
<td>Proprietà di tipo Boolean. Può essere 0 o 1.</td>
<td>Indica se l'elenco viene generato dinamicamente. Gli elenchi dinamici non hanno elementi in listitem.csv. Se un elenco è contrassegnato come dinamico, i relativi elementi vengono forniti da <a href="/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents">IWMPContentPartner::GetListContents</a></td>
</tr>
</tbody>
</table>



 

 

 





