---
title: Uso dei controlli Rich Edit
description: Questa sezione contiene argomenti che illustrano come creare e usare controlli Rich Edit.
ms.assetid: 2c4717c9-3257-42d5-9c36-89b7e524e788
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce4d6565160babc896ea9affe2d5c0c772c5b77e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466180"
---
# <a name="using-rich-edit-controls"></a>Uso dei controlli Rich Edit

Questa sezione contiene argomenti che illustrano come creare e usare controlli Rich Edit.

## <a name="in-this-section"></a>Contenuto della sezione




| Argomento | Descrizione | 
|-------|-------------|
| <a href="create-rich-edit-controls.md">Come creare controlli Rich Edit</a><br /> | Per creare un controllo Rich Edit, chiamare la <a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa"><strong>funzione CreateWindowEx,</strong></a> specificando la classe della finestra Rich Edit. Per Microsoft Rich Edit 4.1 (Msftedit.dll), specificare MSFTEDIT_CLASS come classe della finestra. Per tutte le versioni precedenti, specificare RICHEDIT_CLASS. Per altre informazioni, vedere <a href="about-rich-edit-controls.md">Versioni di Rich Edit.</a> <br /> I controlli Rich Edit supportano la maggior parte degli stili di finestra usati con i controlli di modifica e altri stili. È necessario specificare lo <a href="edit-control-styles.md"><strong>stile ES_MULTILINE</strong></a> finestra se si desidera consentire più righe di testo nel controllo . Per altre informazioni, vedere <a href="rich-edit-control-styles.md">Stili di controllo Rich Edit</a>. <br /> | 
| <a href="format-text-in-rich-edit-controls.md">Come formattare il testo nei controlli Rich Edit</a><br /> | Un'applicazione può inviare messaggi a un controllo Rich Edit per formattare caratteri e paragrafi e recuperare informazioni di formattazione. Gli attributi di formattazione dei paragrafi includono allineamento, tabulazioni, rientri, numerazione e tabelle semplici. Per i caratteri, è possibile specificare il nome, la dimensione, il colore e gli effetti del tipo di carattere, ad esempio grassetto, corsivo e protetto. <br /> | 
| <a href="interact-with-the-current-selection.md">Come interagire con la selezione corrente</a><br /> | L'utente può selezionare il testo in un controllo Rich Edit usando il mouse o la tastiera. La <em>selezione corrente</em> è l'intervallo di caratteri selezionati o la posizione del punto di inserimento se non è selezionato alcun carattere. Un'applicazione può ottenere informazioni sulla selezione corrente, impostarla, determinare quando cambia e mostrare o nascondere l'evidenziazione della selezione. <br /> | 
| <a href="use-rich-edit-text-operations.md">Come usare operazioni rich edit text</a><br /> | Un'applicazione può inviare messaggi per recuperare o trovare testo in un controllo Rich Edit. È possibile recuperare il testo selezionato o un intervallo di testo specificato. <br /> | 
| <a href="use-word-and-line-break-information.md">Come usare le informazioni sulle parole e sulle interruzioni di riga</a><br /> | Un controllo Rich Edit chiama una funzione denominata routine di interruzione di parola per trovare le interruzioni tra le parole e per determinare dove può interrompere le righe. Il controllo usa queste informazioni quando si eseguono operazioni di ritorno a capo automatico e durante l'elaborazione di combinazioni di tasti CTRL+FRECCIA SINISTRA e CTRL+FRECCIA DESTRA. Un'applicazione può inviare messaggi a un controllo Rich Edit per sostituire la routine di interruzione di parola predefinita, recuperare informazioni sull'interruzione di parola e determinare la riga su cui si trova un determinato carattere. <br /> | 
| <a href="use-rich-edit-clipboard-operations.md">Come usare le operazioni degli Appunti rich edit</a><br /> | Un'applicazione può incollare il contenuto degli Appunti in un controllo Rich Edit usando il formato degli Appunti migliore disponibile o un formato degli Appunti specifico. È anche possibile determinare se un controllo Rich Edit è in grado di incollare un formato degli Appunti. <br /> | 
| <a href="use-streams.md">Come usare Flussi</a><br /> | È possibile usare i flussi per trasferire dati da o verso un controllo Rich Edit. Un flusso è definito da una <a href="/windows/desktop/api/Richedit/ns-richedit-editstream"><strong>struttura EDITSTREAM,</strong></a> che specifica un buffer e una funzione di callback definita dall'applicazione. <br /> | 
| <a href="automatically-resize-rich-edit-controls.md">Come ridimensionare automaticamente i controlli Rich Edit</a><br /> | Un'applicazione può ridimensionare un controllo Rich Edit in base alle esigenze in modo che sia sempre delle stesse dimensioni del relativo contenuto. Un controllo Rich Edit supporta <em></em> questa cosiddetta funzionalità senza fondo inviando alla finestra padre un codice di notifica <a href="en-requestresize.md">EN_REQUESTRESIZE</a> ogni volta che le dimensioni del contenuto del controllo cambiano. <br /> | 
| <a href="use-rich-edit-control-notification-codes.md">Come usare i codici di notifica del controllo Rich Edit</a><br /> | La finestra padre di un controllo Rich Edit può elaborare i codici di notifica per monitorare gli eventi che influiscono sul controllo. I controlli Rich Edit supportano tutti i codici di notifica usati con i controlli di modifica, oltre a diversi altri. <br /> | 
| <a href="use-font-binding-in-rich-edit-controls.md">Come usare l'associazione di tipi di carattere nei controlli Rich Edit</a><br /> | Microsoft Rich Edit 3.0 assegna un set di caratteri a caratteri non crittografati a seconda del contesto. Di seguito sono riportati alcuni esempi: <br /><ul><li>I caratteri greche vengono assegnati <strong>GREEK_CHARSET</strong>.</li><li>I simboli hangul vengono assegnati <strong>HANGUL_CHARSET</strong>.</li><li>I caratteri cinesi vengono <strong>assegnati SHIFTJIS_CHARSET</strong> se i caratteri kana vengono trovati nelle vicinanze o GB2312_CHARSET <strong>se</strong> non viene trovato alcun carattere kana nelle vicinanze.</li><li>I caratteri ANSI non neutri vengono assegnati <strong>ANSI_CHARSET</strong> in qualsiasi evento.</li></ul> | 
| <a href="using-rich-edit-com.md">Come usare OLE nei controlli Rich Edit</a><br /> | Questa sezione contiene informazioni sull'uso del collegamento e dell'incorporamento di oggetti (OLE) nei controlli Rich Edit. <br /> | 
| <a href="printing-rich-edit-controls.md">Come stampare il contenuto dei controlli Rich Edit</a><br /> | Questa sezione contiene informazioni su come stampare il contenuto dei controlli Rich Edit. <br /> | 




 

 

