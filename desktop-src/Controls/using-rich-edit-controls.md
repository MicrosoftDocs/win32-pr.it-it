---
title: Uso di controlli Rich Edit
description: Questa sezione contiene argomenti che illustrano come creare e usare controlli Rich Edit.
ms.assetid: 2c4717c9-3257-42d5-9c36-89b7e524e788
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0489660bb6849d0de76ae7fc2f4e21ca931662a8
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "104474518"
---
# <a name="using-rich-edit-controls"></a>Uso di controlli Rich Edit

Questa sezione contiene argomenti che illustrano come creare e usare controlli Rich Edit.

## <a name="in-this-section"></a>Contenuto della sezione



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Argomento</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="create-rich-edit-controls.md">Come creare controlli Rich Edit</a><br/></td>
<td>Per creare un controllo Rich Edit, chiamare la funzione <a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa"><strong>CreateWindowEx</strong></a> , specificando la classe della finestra Rich Edit. Per Microsoft Rich Edit 4,1 (Msftedit.dll) specificare MSFTEDIT_CLASS come classe della finestra. Per tutte le versioni precedenti, specificare RICHEDIT_CLASS. Per ulteriori informazioni, vedere <a href="about-rich-edit-controls.md">versioni di Rich Edit</a>. <br/> I controlli Rich Edit supportano la maggior parte degli stili della finestra utilizzati con i controlli di modifica e altri stili. È necessario specificare lo stile della finestra <a href="edit-control-styles.md"><strong>ES_MULTILINE</strong></a> se si desidera consentire più di una riga di testo nel controllo. Per altre informazioni, vedere <a href="rich-edit-control-styles.md">stili del controllo Rich Edit</a>. <br/></td>
</tr>
<tr class="even">
<td><a href="format-text-in-rich-edit-controls.md">Come formattare il testo nei controlli Rich Edit</a><br/></td>
<td>Un'applicazione può inviare messaggi a un controllo Rich Edit per formattare i caratteri e i paragrafi e recuperare le informazioni di formattazione. Gli attributi di formattazione dei paragrafi includono l'allineamento, le tabulazioni, i rientri, la numerazione e le tabelle semplici. Per i caratteri, è possibile specificare il nome, la dimensione, il colore e gli effetti del tipo di carattere, ad esempio grassetto, corsivo e protetto. <br/></td>
</tr>
<tr class="odd">
<td><a href="interact-with-the-current-selection.md">Come interagire con la selezione corrente</a><br/></td>
<td>L'utente può selezionare il testo in un controllo Rich Edit utilizzando il mouse o la tastiera. La <em>selezione corrente</em> è l'intervallo di caratteri selezionati o la posizione del punto di inserimento se non è selezionato alcun carattere. Un'applicazione può ottenere informazioni sulla selezione corrente, impostarla, determinare quando viene modificata e mostrare o nascondere l'evidenziazione della selezione. <br/></td>
</tr>
<tr class="even">
<td><a href="use-rich-edit-text-operations.md">Come usare le operazioni Rich Edit Text</a><br/></td>
<td>Un'applicazione può inviare messaggi per recuperare o trovare testo in un controllo Rich Edit. È possibile recuperare il testo selezionato o un intervallo di testo specificato. <br/></td>
</tr>
<tr class="odd">
<td><a href="use-word-and-line-break-information.md">Come usare le informazioni relative a parole e interruzioni di riga</a><br/></td>
<td>Un controllo Rich Edit chiama una funzione chiamata procedura di interruzione di parola per individuare le interruzioni tra le parole e per determinare la posizione in cui è possibile interrompere le righe. Il controllo utilizza queste informazioni quando si eseguono operazioni di ritorno a capo automatico e quando si elaborano le combinazioni di tasti CTRL + freccia sinistra e CTRL + freccia destra. Un'applicazione può inviare messaggi a un controllo Rich Edit per sostituire la routine di Word break predefinita, per recuperare le informazioni sull'interruzioni di parola e per determinare la riga in cui si trova un determinato carattere. <br/></td>
</tr>
<tr class="even">
<td><a href="use-rich-edit-clipboard-operations.md">Come utilizzare le operazioni Rich Edit Clipboard</a><br/></td>
<td>Un'applicazione può incollare il contenuto degli Appunti in un controllo Rich Edit utilizzando il formato degli Appunti disponibile migliore o un formato degli Appunti specifico. È inoltre possibile determinare se un controllo Rich Edit è in grado di incollare un formato degli Appunti. <br/></td>
</tr>
<tr class="odd">
<td><a href="use-streams.md">Come usare i flussi</a><br/></td>
<td>È possibile utilizzare i flussi per trasferire i dati all'interno o all'esterno di un controllo Rich Edit. Un flusso è definito da una struttura <a href="/windows/desktop/api/Richedit/ns-richedit-editstream"><strong>EDITSTREAM</strong></a> , che specifica un buffer e una funzione di callback definita dall'applicazione. <br/></td>
</tr>
<tr class="even">
<td><a href="automatically-resize-rich-edit-controls.md">Come ridimensionare automaticamente i controlli Rich Edit</a><br/></td>
<td>Un'applicazione può ridimensionare un controllo Rich Edit in base alle esigenze, in modo che sia sempre della stessa dimensione del contenuto. Un controllo Rich Edit supporta questa cosiddetta funzionalità senza <em>fondo</em> inviando la finestra padre di un <a href="en-requestresize.md">EN_REQUESTRESIZE</a> codice di notifica ogni volta che viene modificata la dimensione del contenuto del controllo. <br/></td>
</tr>
<tr class="odd">
<td><a href="use-rich-edit-control-notification-codes.md">Come utilizzare i codici di notifica del controllo Rich Edit</a><br/></td>
<td>Una finestra padre di un controllo Rich Edit può elaborare i codici di notifica per monitorare gli eventi che influiscono sul controllo. I controlli Rich Edit supportano tutti i codici di notifica utilizzati con i controlli di modifica, oltre a diversi altri. <br/></td>
</tr>
<tr class="even">
<td><a href="use-font-binding-in-rich-edit-controls.md">Come usare l'associazione di tipi di carattere nei controlli Rich Edit</a><br/></td>
<td>Microsoft Rich Edit 3,0 assegna un set di caratteri a caratteri testo normale a seconda del contesto. Di seguito sono riportati alcuni esempi: <br/>
<ul>
<li>I caratteri greci vengono assegnati <strong>GREEK_CHARSET</strong>.</li>
<li>I simboli Hangul sono assegnati <strong>HANGUL_CHARSET</strong>.</li>
<li>I caratteri cinesi vengono assegnati <strong>SHIFTJIS_CHARSET</strong> se sono presenti caratteri Kana vicini o <strong>GB2312_CHARSET</strong> se non sono stati trovati caratteri Kana nelle vicinanze.</li>
<li>I caratteri ANSI non neutri vengono assegnati <strong>ANSI_CHARSET</strong> in qualsiasi evento.</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="using-rich-edit-com.md">Come utilizzare OLE nei controlli Rich Edit</a><br/></td>
<td>In questa sezione vengono fornite informazioni sull'utilizzo di Object Linking and Embedding (OLE) in controlli Rich Edit. <br/></td>
</tr>
<tr class="even">
<td><a href="printing-rich-edit-controls.md">Come stampare il contenuto dei controlli Rich Edit</a><br/></td>
<td>Questa sezione contiene informazioni su come stampare il contenuto dei controlli Rich Edit. <br/></td>
</tr>
</tbody>
</table>



 

 

