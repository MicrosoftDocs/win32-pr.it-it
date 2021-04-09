---
title: list.csv
description: list.csv
ms.assetid: 020b213c-826c-430c-8ce7-92b819581de8
keywords:
- Windows Media Player Online Stores, list.csv
- archivi online, list.csv
- digitare 1 Store online, list.csv
- list.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f41ed237c5f4a185f01feace8f09b4615e4922b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104117347"
---
# <a name="listcsv"></a>list.csv

Questo file contiene una voce per ogni elenco contenente il catalogo. Gli elenchi possono essere elenchi di tracce, album, artisti, generi, sottogeneri o feed radiofonici; oppure possono essere elenchi di altri elenchi. Ogni voce di elenco è una riga costituita dai campi delimitati da tabulazioni descritti nella tabella seguente. I campi devono essere visualizzati nell'ordine elencato.

La colonna Format nella tabella seguente descrive la modalità di formattazione di ogni campo di testo Unicode. Non si riferisce al tipo di dati del contenuto. Se, ad esempio, nella colonna formato è indicato Integer, significa che il campo contiene una stringa Unicode che rappresenta un valore integrale, anziché un numero intero effettivo.



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
<td>Integer non negativo.</td>
<td>Identificatore dell'elenco, univoco all'interno list.csv. Deve essere non negativo e minore di 2 ^ 32. <strong>Visualizzazione di un nodo elenco nel controllo di visualizzazione albero:</strong> Se ListID è 0, 1, 2, 3, 4, 5, 6 o 7, l'elenco verrà visualizzato come nodo personalizzato nel nodo di primo livello del negozio online nel controllo di visualizzazione albero del lettore. I nodi personalizzati vengono visualizzati prima dei nodi standard nel nodo di primo livello del negozio online e sono posizionati in ordine crescente in base a ListID. Se ad esempio sono presenti tre nodi personalizzati, con ListId di 1, 3 e 5, verranno visualizzati prima, secondo e terzo nel nodo di primo livello del negozio online.<br/></td>
</tr>
<tr class="even">
<td>Titoloelenco</td>
<td>No</td>
<td>Stringa Unicode. Esempio: primi dieci riscontri<br/></td>
<td>Titolo dell'elenco.</td>
</tr>
<tr class="odd">
<td>ListSubtitle</td>
<td>No</td>
<td>Stringa Unicode</td>
<td>Elenca il titolo alternativo, visualizzato nella seconda riga della visualizzazione affiancata.</td>
</tr>
<tr class="even">
<td>ListDescription</td>
<td>Sì</td>
<td>Stringa Unicode</td>
<td>Elenca il testo visualizzato descrittivo (visualizzato nelle pagine delle proprietà).</td>
</tr>
<tr class="odd">
<td>Linked_ItemType</td>
<td>Sì</td>
<td>Stringa Unicode. Formato: [T | P | A | L | G | S | R<br/> Esempio: T<br/></td>
<td>Indica il tipo degli elementi collegati.
<ul>
<li>T = Track</li>
<li>P = esecutore</li>
<li>A = album</li>
<li>L = elenco</li>
<li>G = genere</li>
<li>S = sottogenere</li>
<li>R = radio</li>
</ul></td>
</tr>
<tr class="even">
<td>ListPrice</td>
<td>Sì</td>
<td>Stringa Unicode. Esempio: $9,99<br/></td>
<td>Prezzo dell'elenco. È necessario includere il simbolo di valuta. Zero indica che l'elenco è gratuito. Nessun valore indica che il prezzo è sconosciuto. Un trattino indica che non è possibile acquistare l'elenco.<br/></td>
</tr>
<tr class="odd">
<td>Popolarità</td>
<td>Sì</td>
<td>Integer o valore decimale. Esempio: 1259,3<br/></td>
<td>Indica la classificazione della popolarità quando questo elenco viene visualizzato in altri elenchi. Può essere zero se non è applicabile.</td>
</tr>
<tr class="even">
<td>IsRecentlyAdded</td>
<td>Sì</td>
<td>Boolean. Format: [0 | 1]<br/> Esempio: 0<br/></td>
<td>Indica se l'elenco è stato aggiunto di recente.</td>
</tr>
<tr class="odd">
<td>Funzionalità di</td>
<td>Sì</td>
<td>Boolean. Format: [0 | 1]<br/> Esempio: 0<br/></td>
<td>Indica se l'elenco è in primo piano. Può essere utilizzato per determinare l'ordinamento.</td>
</tr>
<tr class="even">
<td>EditorialGlyph</td>
<td>Sì</td>
<td>Integer non negativo. Deve essere 0.</td>
<td>Non utilizzato in questa versione. Deve essere 0.</td>
</tr>
<tr class="odd">
<td>ViewType</td>
<td>Sì</td>
<td>Stringa Unicode. Formato: [I | T | R | L | O] esempio: T<br/></td>
<td>Indica il tipo di visualizzazione da utilizzare per l'elenco.
<ul>
<li>I = icona</li>
<li>T = riquadro</li>
<li>R = report</li>
<li>L = elenco</li>
<li>O = elenco ordinato</li>
</ul></td>
</tr>
<tr class="even">
<td>ViewImageSize</td>
<td>Sì</td>
<td>Integer non negativo. Esempio: 180<br/></td>
<td>Dimensione in corrispondenza della quale viene visualizzata l'immagine dell'elenco. Se è 0, la dimensione viene determinata automaticamente.</td>
</tr>
<tr class="odd">
<td>GroupBy</td>
<td>Sì</td>
<td>Stringa Unicode. Formato: [-| P | A | C | R | D<br/> Esempio: P<br/></td>
<td>Indica il campo utilizzato per raggruppare gli elementi nell'elenco.
<ul>
<li>- = Automatico</li>
<li>P = esecutore</li>
<li>A = album</li>
<li>C = Composer</li>
<li>R = classificazione</li>
<li>D = Data</li>
</ul></td>
</tr>
<tr class="even">
<td>ListItemsAreDynamic</td>
<td>Sì</td>
<td>Proprietà di tipo Boolean. Può essere 0 o 1.</td>
<td>Indica se l'elenco viene generato dinamicamente. Gli elenchi dinamici non contengono elementi in listitem.csv. Se un elenco è contrassegnato come dinamico, i relativi elementi vengono forniti da <a href="/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents">IWMPContentPartner:: GetListContents</a></td>
</tr>
</tbody>
</table>



 

 

 





