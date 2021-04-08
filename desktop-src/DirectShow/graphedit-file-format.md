---
description: Formato di file GraphEdit
ms.assetid: 84c2de05-6c8f-45f1-b789-04a24cfa3ea1
title: Formato di file GraphEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a75421ff75c9bb26901eddf423448bbd9e4f478
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747631"
---
# <a name="graphedit-file-format"></a>Formato di file GraphEdit

Quando l'utilità GraphEdit salva un grafo di filtro DirectShow, viene creato un file di archiviazione con estensione. GRF. Il file di archiviazione contiene un singolo flusso denominato ActiveMovieGraph. Questo flusso contiene informazioni su tutti i filtri, i nomi dei filtri, i nomi file, le connessioni e così via.

La grammatica seguente descrive la sintassi del grafico all'interno del flusso, usando una sintassi BNF (Backus-Naur Form) modificata:


```C++
<graph> ::= 
0003\r\n<filters><connections><clock>
END | 
0002\r\n<filters><connections>
END
<filters> ::= 
FILTERS<b> 
[<filter list><b>
]
<filter list> ::= <filter><b> 
[<filter list>
]
<filter> ::= <filter id><b><name><b><class id><b>
[<file>
]<length><b1><filter data>
<class id> ::= <guid>
<file> ::= 
SOURCE <name><b> | 
SINK <name><b>
<connections> ::= 
CONNECTIONS<b> 
{<connection><b>
}
<connection> ::= <filter id><b><pin id><b><filter id><b><pin id><b><media type>
<filter id> ::= <id>
<pin id> ::= <name>
<media type> ::= <sample size><major type><b><subtype><b><flags><format>
<major type> ::= <guid>
<subtype> ::= <guid>
<flags> ::= <fixed sample size><b><temporal compression><b>
<fixed sample size> ::= 1 
| 0
<temporal compression> ::= 1 
| 0
<format> ::= <length><b1><format type><b><length><b1><format data>
<format type> ::= <guid>
<format data> ::= 
{ binary_data 
}
<clock> ::= 
CLOCK <b><required><b><clockid>
\r\n
<required> ::= 1 
| 0
<clockid> ::= <filter id> 
| <class id>
<name> ::= quote_symbol 
{ any_non_quote_character 
} quote_symbol
<length> ::= unsigned decimal number (as a string), indicating the number 
             of bytes of data in the following token.
<guid> ::= GUID in string format. for example: {CF49D4E0-1115-11CE-B03A-0020AF0BA770}
<b> ::= 
{ space_character 
} 
{ \t 
} 
{ \r 
} 
{ \n 
} { <b> 
}
<b1> ::= space_character
<id> ::= integer (as a string), such as 0001
```



Nell'output sarà presente una nuova riga (" \\ r \\ n") per filtro, una per connessione e una per ciascuna delle parole chiave filtri e connessioni. Tutti gli altri casi di saranno costituiti da <b> uno spazio singolo. Le parole chiave FILTERs, CONNECTIONs e END non sono localizzabili. Si noti inoltre che i dati del filtro e i dati di formato sono binari, quindi potrebbero contenere interruzioni di riga, valori null e così via. Il flusso usa caratteri wide.

Di seguito viene illustrato un grafico tipico. (Le linee di connessione sono state interrotte per maggiore chiarezza e i dati binari sono stati omessi).


```C++
003
FILTERS
0001 "C:\SomeFile.avi" {E436EBB5-524F-11CE-9F53-0020AF0BA770} SOURCE "C:\SomeFile.avi" 0000000000 
0002 "AVI Splitter" {1B544C20-FD0B-11CE-8C63-00AA0044B51E} 0000000000 
0003 "AVI Decompressor" {CF49D4E0-1115-11CE-B03A-0020AF0BA770} 0000000000
0004 "Video Renderer" {70E102B0-5556-11CE-97C0-00AA0055595A} 0000000000
CONNECTIONS
0001 "Output" 0002 "input pin" 0000000288 
   {E436EB83-524F-11CE-9F53-0020AF0BA770} 
   {E436EB88-524F-11CE-9F53-0020AF0BA770} 1 0 0000000001 
   {00000000-0000-0000-0000-000000000000} 0000000000  
0002 "Stream 00" 0003 "In" 0000000376 
   {73646976-0000-0010-8000-00AA00389B71} 
   {64697663-0000-0010-8000-00AA00389B71} 0 0 0000000001 
   {05589F80-C356-11CE-BF01-00AA0055595A} 0000000088 <binary data>
0003 "Out" 0004 "In" 0000000376 
    {73646976-0000-0010-8000-00AA00389B71} 
    {E436EB7D-524F-11CE-9F53-0020AF0BA770} 1 0 0000129600 
    {05589F80-C356-11CE-BF01-00AA0055595A} 0000000088 <binary data> 
CLOCK 1 0000
END
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Simulazione della creazione di grafici con GraphEdit](simulating-graph-building-with-graphedit.md)
</dt> </dl>

 

 



