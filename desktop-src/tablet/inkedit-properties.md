---
description: Questa sezione contiene le proprietà appartenenti al controllo InkEdit.
ms.assetid: 6aa476b3-97ad-4289-836b-f46fe4d04280
title: Proprietà InkEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4e7fa3156ef38013ab099e6440b6796505f21d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313466"
---
# <a name="inkedit-properties"></a>Proprietà InkEdit

Questa sezione contiene le proprietà appartenenti al controllo InkEdit.



| Proprietà                                                 | Descrizione                                                                                                                                                                                            |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Aspetto**](/windows/desktop/api/inked/nf-inked-iinkedit-get_appearance)                 | Ottiene o imposta un valore che determina se il controllo [InkEdit](inkedit-control-reference.md) viene visualizzato come flat o 3D.<br/>                                                                      |
| [**BackColor**](/windows/desktop/api/inked/nf-inked-iinkedit-get_backcolor)                   | Ottiene o imposta il colore di sfondo per il controllo [InkEdit](inkedit-control-reference.md) .<br/>                                                                                                 |
| [**BorderStyle**](/windows/desktop/api/inked/nf-inked-iinkedit-get_borderstyle)               | Ottiene o imposta un valore che determina se il controllo [InkEdit](inkedit-control-reference.md) dispone di un bordo.<br/>                                                                             |
| [**DisableNoScroll**](/windows/desktop/api/inked/nf-inked-iinkedit-get_disablenoscroll)       | Ottiene o imposta un valore che determina se le barre di scorrimento nel controllo [InkEdit](inkedit-control-reference.md) sono disabilitate.<br/>                                                              |
| [**DrawingAttributes**](/windows/desktop/api/inked/nf-inked-iinkedit-get_drawingattributes)   | Ottiene o imposta gli attributi di disegno per l'input penna ancora da disegnare sul controllo [InkEdit](inkedit-control-reference.md) .<br/>                                                                |
| [**Abilitato**](/windows/desktop/api/inked/nf-inked-iinkedit-get_enabled)                       | Ottiene o imposta un valore che determina se il controllo [InkEdit](inkedit-control-reference.md) può rispondere agli eventi generati dall'utente.<br/>                                                     |
| [**Factoid**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid)                       | Ottiene o [imposta la costante del controllo del controllo](factoid-constants.md) utilizzata da un oggetto [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) per limitare la ricerca del risultato del riconoscimento.<br/>                  |
| [**Carattere**](/windows/desktop/api/inked/nf-inked-iinkedit-get_font)                             | Ottiene o imposta il tipo di carattere del testo visualizzato dal controllo [InkEdit](inkedit-control-reference.md) .<br/>                                                                                       |
| [**hWnd**](/windows/desktop/api/inked/nf-inked-iinkedit-get_hwnd)                             | Ottiene l'handle di finestra a cui è associato il controllo [**InkDisp**](inkdisp-class.md) .<br/>                                                                                                      |
| [**InkInsertMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkinsertmode)           | Ottiene o imposta un valore che specifica la modalità di inserimento dell'input penna sul controllo [InkEdit](inkedit-control-reference.md) , come testo o come input penna.<br/>                                                |
| [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode)                       | Ottiene o imposta un valore che specifica se la raccolta di input penna è disabilitata, l'input penna viene raccolto o viene raccolto input penna e movimenti.<br/>                                                                |
| [**Bloccato**](/windows/desktop/api/inked/nf-inked-iinkedit-get_locked)                         | Ottiene o imposta un valore che specifica se il controllo [InkEdit](inkedit-control-reference.md) è di sola lettura o meno.<br/>                                                                       |
| [**MaxLength**](/windows/desktop/api/inked/nf-inked-iinkedit-get_maxlength)                   | Ottiene o imposta un valore che indica se un controllo [InkEdit](inkedit-control-reference.md) può conservare un numero massimo di caratteri e, in tal caso, specifica il numero massimo di caratteri.<br/> |
| [**MouseIcon**](/windows/desktop/api/inked/nf-inked-iinkedit-get_mouseicon)                   | Ottiene o imposta l'icona del mouse personalizzata corrente.<br/>                                                                                                                                                 |
| [**MousePointer**](/windows/desktop/api/inked/nf-inked-iinkedit-get_mousepointer)             | Ottiene o imposta un valore che indica il tipo di puntatore del mouse visualizzato quando il mouse si trova su una particolare parte del controllo [InkEdit](inkedit-control-reference.md) .<br/>                |
| [**MultiLine**](/windows/desktop/api/inked/nf-inked-iinkedit-get_multiline)                   | Ottiene o imposta un valore che indica se si tratta di un controllo [InkEdit](inkedit-control-reference.md) su più righe.<br/>                                                                           |
| [**RecognitionTimeout**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout)        | Ottiene o imposta il periodo di tempo, in millisecondi, tra l'ultimo oggetto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) raccolto e l'inizio del riconoscimento del testo.<br/>                         |
| [**Sistema di riconoscimento**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognizer)                 | Ottiene o imposta l'oggetto [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) da utilizzare per il riconoscimento.<br/>                                                                                                    |
| [**BarreScorrimento**](/windows/desktop/api/inked/nf-inked-iinkedit-get_scrollbars)                 | Ottiene o imposta il tipo di barre di scorrimento visualizzate nel controllo [InkEdit](inkedit-control-reference.md) .<br/>                                                                                   |
| [**SelAlignment**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selalignment)             | Ottiene o imposta l'allineamento da applicare alla selezione o al punto di inserimento corrente (solo in fase di esecuzione).<br/>                                                                                            |
| [**SelBold**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selbold)                       | Ottiene o imposta un valore che specifica se lo stile del tipo di carattere del testo attualmente selezionato nel controllo [InkEdit](inkedit-control-reference.md) è in grassetto (solo in fase di esecuzione).<br/>                  |
| [**SelCharOffset**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selcharoffset)           | Ottiene o imposta un valore che indica se il testo nel controllo [InkEdit](inkedit-control-reference.md) viene visualizzato nella linea di base, come apice o come indice (solo in fase di esecuzione).<br/>                             |
| [**SelColor**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selcolor)                     | Ottiene o imposta il colore del testo della selezione di testo o del punto di inserimento corrente (solo in fase di esecuzione).<br/>                                                                                               |
| [**SelFontName**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selfontname)               | Ottiene o imposta il nome del tipo di carattere del testo selezionato all'interno del controllo [InkEdit](inkedit-control-reference.md) (solo in fase di esecuzione).<br/>                                                                |
| [**SelFontSize**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selfontsize)               | Ottiene o imposta la dimensione del carattere del testo selezionato all'interno del controllo [InkEdit](inkedit-control-reference.md) (solo in fase di esecuzione).<br/>                                                                |
| [**SelInks**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selinks)                       | Ottiene o imposta la matrice di oggetti [**InkDisp**](inkdisp-class.md) incorporati (se visualizzati come input penna) contenuti nella selezione corrente.<br/>                                                      |
| [**SelInksDisplayMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selinksdisplaymode) | Ottiene o imposta un valore che consente di alternare l'aspetto della selezione tra input penna e testo.<br/>                                                                                             |
| [**SelItalic**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selitalic)                   | Ottiene o imposta un valore che specifica se lo stile del tipo di carattere del testo attualmente selezionato nel controllo [InkEdit](inkedit-control-reference.md) è in corsivo (solo in fase di esecuzione).<br/>                |
| [**SelLength**](/windows/desktop/api/inked/nf-inked-iinkedit-get_sellength)                   | Ottiene o imposta il numero di caratteri selezionati nel controllo [InkEdit](inkedit-control-reference.md) (solo in fase di esecuzione).<br/>                                                            |
| [**SelRTF**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selrtf)                         | Ottiene o imposta il testo formattato RTF (Rich Text Format) attualmente selezionato nel controllo [InkEdit](inkedit-control-reference.md) (solo in fase di esecuzione).<br/>                                          |
| [**SelStart**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selstart)                     | Ottiene o imposta il punto iniziale del testo selezionato nella casella di testo (solo in fase di esecuzione).<br/>                                                                                               |
| [**SelText**](/windows/desktop/api/inked/nf-inked-iinkedit-get_seltext)                       | Ottiene o imposta il testo selezionato all'interno del controllo [InkEdit](inkedit-control-reference.md) (solo in fase di esecuzione).<br/>                                                                                 |
| [**SelUnderline**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selunderline)             | Ottiene o imposta un valore che specifica se lo stile del tipo di carattere del testo attualmente selezionato nel controllo [InkEdit](inkedit-control-reference.md) è sottolineato (solo in fase di esecuzione).<br/>            |
| [**Stato**](/windows/desktop/api/inked/nf-inked-iinkedit-get_status)                         | Ottiene un valore che specifica se il controllo [InkEdit](inkedit-control-reference.md) è inattivo, raccogliendo input penna o riconoscendo l'input penna (solo in fase di esecuzione).<br/>                                       |
| [**Text**](/windows/desktop/api/inked/nf-inked-iinkedit-get_text)                             | Ottiene o imposta il testo corrente nella casella di testo.<br/>                                                                                                                                              |
| [**TextRTF**](/windows/desktop/api/inked/nf-inked-iinkedit-get_textrtf)                       | Ottiene o imposta il testo del controllo [InkEdit](inkedit-control-reference.md) , inclusi tutti i codici RTF.<br/>                                                                                     |
| [**UseMouseForInput**](/windows/desktop/api/inked/nf-inked-iinkedit-get_usemouseforinput)     | Ottiene o imposta un valore che indica se il mouse può essere utilizzato come dispositivo di input.<br/>                                                                                                       |



 

 

 




