---
title: Modello a oggetti testo
description: Questa sezione contiene informazioni sugli elementi di programmazione usati con il modello a oggetti di testo (TOM).
ms.assetid: vs|controls|~\controls\richedit\textobjectmodel.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7625ca7772da7f4e10aa7d64159971ee0e259d2a
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "103873061"
---
# <a name="text-object-model"></a>Modello a oggetti testo

Questa sezione contiene informazioni sugli elementi di programmazione usati con il modello a oggetti di testo (TOM).

Il TOM definisce un set sostanziale di interfacce di manipolazione del testo. Le soluzioni di testo, ad esempio Microsoft Word e i controlli Rich Edit supportano il set di funzionalità di TOM. TOM è stato fortemente influenzato da WordBasic (il linguaggio di programmazione usato per Word) ed è facile da usare da Microsoft Visual Basic, Applications Edition (VBA). Questa compatibilità presenta diversi vantaggi:

-   Il codice può essere migrato abbastanza facilmente da una soluzione a un'altra.
-   Una lingua può essere usata per condividere le informazioni di testo tra diversi motori di testo.
-   Riduce la necessità di documentazione e codice rispetto alle interfacce COM (Component Object Model di basso livello) e VBA separate.

Tuttavia, può essere meno efficiente per gli scopi C/C++ rispetto all'uso di interfacce COM più generali di livello inferiore.

TOM è un set semplice di interfacce da implementare per le soluzioni di testo principale, i controlli Word e Rich Edit. Tuttavia, per le applicazioni che inseriscono un'enfasi secondaria sul testo, è preferibile fornire le interfacce TOM trasferendo il testo in un controllo di modifica che supporta TOM. Poiché i controlli Rich Edit vengono forniti con i sistemi operativi Microsoft, sono i metodi standard per ottenere la funzionalità TOM.

### <a name="overviews"></a>Cenni preliminari



| Argomento                                                          | Contenuto                                                                                                                                                                                                         |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informazioni sul modello a oggetti di testo](about-text-object-model.md)         | L'oggetto TOM (Text Object Model) di primo livello è definito dall'interfaccia [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) , che dispone di metodi per la creazione e il recupero di oggetti di livello inferiore nella gerarchia di oggetti.<br/> |
| [Uso del modello a oggetti di testo](using-the-text-object-model.md) | Negli esempi di codice di questo documento vengono illustrati i vari aspetti dell'utilizzo del modello a oggetti di testo (TOM).<br/>                                                                                                          |



 

### <a name="interfaces"></a>Interfacce



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Argomento</th>
<th>Contenuto</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a></td>
<td>L'interfaccia <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> è l'interfaccia di primo livello di Tom, che recupera gli oggetti selezione e intervallo attivi per qualsiasi storia del documento, indipendentemente dal fatto che sia attiva o meno. Consente all'applicazione di:
<ul>
<li>Aprire e salvare i documenti.</li>
<li>Controllare il comportamento di annullamento e l'aggiornamento dello schermo.</li>
<li>Trovare un intervallo da una posizione dello schermo.</li>
<li>Ottiene un enumeratore di <a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>ITextStoryRanges</strong></a> Story.</li>
</ul>
<br/> <strong>Quando implementare</strong><br/> Le applicazioni in genere non implementano l'interfaccia <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> . Le soluzioni Microsoft Text, ad esempio i controlli Rich Edit, implementano <strong>ITextDocument</strong> come parte dell'implementazione di Tom. <br/> <strong>Quando usare</strong><br/> Le applicazioni possono recuperare un puntatore <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> da un controllo Rich Edit. A tale scopo, inviare un messaggio di <a href="em-getoleinterface.md"><strong>EM_GETOLEINTERFACE</strong></a> per recuperare un oggetto <a href="/windows/desktop/api/Richole/nn-richole-iricheditole"><strong>IRichEditOle</strong></a> da un controllo Rich Edit. Chiamare quindi il metodo <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)"><strong>IUnknown:: QueryInterface</strong></a> dell'oggetto per recuperare un puntatore <strong>ITextDocument</strong> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>ITextFont</strong></a></td>
<td>È possibile accedere agli attributi di intervallo RTF di TOM con una coppia di interfacce duali, <a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>ITextFont</strong></a> e <a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>ITextPara</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>ITextPara</strong></a></td>
<td>È possibile accedere agli attributi di intervallo RTF di TOM con una coppia di interfacce duali, <a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>ITextFont</strong></a> e <a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>ITextPara</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Tom/nn-tom-itextrange"><strong>ITextRange</strong></a></td>
<td>Gli oggetti <a href="/windows/desktop/api/Tom/nn-tom-itextrange"><strong>ITextRange</strong></a> sono strumenti avanzati per la modifica e il data binding che consentono a un programma di selezionare il testo in una storia, quindi di esaminare o modificare il testo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Tom/nn-tom-itextselection"><strong>ITextSelection</strong></a></td>
<td>Una selezione di testo è un intervallo di testo con evidenziazione della selezione.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>ITextStoryRanges</strong></a></td>
<td>Lo scopo dell'interfaccia <a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>ITextStoryRanges</strong></a> è enumerare le storie in un <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a>.<br/></td>
</tr>
</tbody>
</table>



 

 

