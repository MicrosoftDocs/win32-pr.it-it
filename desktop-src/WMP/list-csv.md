---
title: list.csv
description: list.csv
ms.assetid: 020b213c-826c-430c-8ce7-92b819581de8
keywords:
- Windows Media Player online, list.csv
- negozi online, list.csv
- tipo 1 negozi online, list.csv
- list.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee7237afb37b30ccf8c96ddac95f0e81e148703d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480787"
---
# <a name="listcsv"></a>list.csv

Questo file contiene una voce per ognuno degli elenchi contenuti nel catalogo. Gli elenchi possono essere elenchi di tracce, album, artisti, generi, sottogeneri o feed radio. oppure possono essere elenchi di altri elenchi. Ogni voce di elenco è una riga composta dai campi delimitati da tabulazioni descritti nella tabella seguente. I campi devono essere visualizzati nell'ordine elencato.

La colonna Formato nella tabella seguente descrive il modo in cui viene formattato ogni campo di testo Unicode. Non fa riferimento al tipo di dati del contenuto. Ad esempio, se Nella colonna Formato è indicato Integer, significa che il campo contiene una stringa Unicode che rappresenta un valore integrale, anziché un numero intero effettivo.




| Campo | Obbligatoria | Formato | Descrizione | 
|-------|----------|--------|-------------|
| ListID | Sì | Intero non negativo. | Identificatore di elenco, univoco all'interno list.csv. Deve essere non negativo e minore di 2^32. <strong>Visualizzazione di un nodo elenco nel controllo visualizzazione albero:</strong> Se ListID è 0, 1, 2, 3, 4, 5, 6 o 7, l'elenco verrà visualizzato come nodo personalizzato sotto il nodo di primo livello del negozio online nel controllo visualizzazione albero di Player. I nodi personalizzati vengono visualizzati prima dei nodi standard nel nodo di primo livello del negozio online e vengono posizionati in ordine crescente in base a ListID. Ad esempio, se sono presenti tre nodi personalizzati, con ListID di 1, 3 e 5, verranno visualizzati per primo, secondo e terzo sotto il nodo di primo livello del negozio online.<br /> | 
| ListTitle | No | Stringa Unicode. Esempio: Primi dieci riscontri<br /> | Titolo dell'elenco. | 
| ListSubtitle | No | Stringa Unicode | Elencare il titolo alternativo, visualizzato nella seconda riga della visualizzazione Riquadro. | 
| ListDescription | Sì | Stringa Unicode | Elencare il testo visualizzato descrittivo (visualizzato nelle pagine delle proprietà). | 
| Linked_ItemType | Sì | Stringa Unicode. Formato: [T|P|A|L|G|S|R]<br /> Esempio: T<br /> | Indica il tipo di elementi collegati.<ul><li>T= Traccia</li><li>P = Esecutore</li><li>A = Album</li><li>L = Elenco</li><li>G = Genere</li><li>S = Sottogenere</li><li>R = Radio</li></ul> | 
| ListPrice | Sì | Stringa Unicode. Esempio: $9,99<br /> | Prezzo dell'elenco. Il simbolo di valuta deve essere incluso. Zero indica che l'elenco è gratuito. Nessun valore indica che il prezzo è sconosciuto. Un trattino indica che l'elenco non può essere acquistato.<br /> | 
| Popolarità | Sì | Valore intero o decimale. Esempio: 1259.3<br /> | Indica la classificazione di popolarità quando questo elenco viene visualizzato in altri elenchi. Può essere zero se non applicabile. | 
| IsRecentlyAdded | Sì | Boolean.Format: [0|1]<br /> Esempio: 0<br /> | Indica se l'elenco è stato aggiunto di recente. | 
| IsFeatured | Sì | Boolean.Format: [0|1]<br /> Esempio: 0<br /> | Indica se l'elenco è in primo piano. Può essere usato per determinare l'ordinamento. | 
| EditorialGlyph | Sì | Intero non negativo. Deve essere 0. | Non usato in questa versione. Deve essere 0. | 
| ViewType | Sì | Stringa Unicode. Formato: [I|T|R|L|O]Esempio: T<br /> | Indica il tipo di visualizzazione da utilizzare per l'elenco.<ul><li>I = Icona</li><li>T = Riquadro</li><li>R = Report</li><li>L = Elenco</li><li>O = Elenco ordinato</li></ul> | 
| ViewImageSize | Sì | Intero non negativo. Esempio: 180<br /> | Dimensioni in base alle quali viene visualizzata l'immagine dell'elenco. Se 0, le dimensioni vengono determinate automaticamente. | 
| GroupBy | Sì | Stringa Unicode. Formato: [-|P|A|C|R|D]<br /> Esempio: P<br /> | Indica il campo utilizzato per raggruppare gli elementi nell'elenco.<ul><li>- = Automatico</li><li>P = Esecutore</li><li>A = Album</li><li>C = Composer</li><li>R = Classificazione</li><li>D = Data</li></ul> | 
| ListItemsAreDynamic | Sì | Proprietà di tipo Boolean. Può essere 0 o 1. | Indica se l'elenco viene generato dinamicamente. Gli elenchi dinamici non hanno elementi in listitem.csv. Se un elenco è contrassegnato come dinamico, i relativi elementi vengono forniti da <a href="/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents">IWMPContentPartner::GetListContents</a> | 




 

 

 





