---
title: ProgressBar
description: Questa sezione contiene informazioni sugli elementi di programmazione utilizzati con i controlli indicatore di stato.
ms.assetid: vs|controls|~\controls\progbar\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03c9cd66326336cd3733f881f3f19d82fedc3bf8d8420f83035bf20dc914c7c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118670652"
---
# <a name="progress-bar"></a>ProgressBar

Questa sezione contiene informazioni sugli elementi di programmazione utilizzati con i controlli indicatore di stato.

### <a name="overviews"></a>Cenni preliminari



| Argomento                                            | Contenuto                                                                                                           |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [Controllo Indicatore di stato](progress-bar-control.md) | Un indicatore di stato è una finestra che può essere utilizzata da un'applicazione per indicare lo stato di avanzamento di un'operazione di lunga durata.<br/> |



 

### <a name="messages"></a>Messaggi



| Argomento                                       | Contenuto                                                                                                                                                                                                                                                              |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PBM \_ DELTAPOS**](pbm-deltapos.md)       | Sposta in avanti la posizione corrente di un indicatore di stato di un incremento specificato e ridisegna l'indicatore per riflettere la nuova posizione. <br/>                                                                                                                                 |
| [**PBM \_ GETBARCOLOR**](pbm-getbarcolor.md) | Ottiene il colore dell'indicatore di stato.<br/>                                                                                                                                                                                                                        |
| [**PBM \_ GETBKCOLOR**](pbm-getbkcolor.md)   | Ottiene il colore di sfondo dell'indicatore di stato.<br/>                                                                                                                                                                                                             |
| [**PBM \_ GETPOS**](pbm-getpos.md)           | Recupera la posizione corrente dell'indicatore di stato. <br/>                                                                                                                                                                                                       |
| [**PBM \_ GETRANGE**](pbm-getrange.md)       | Recupera informazioni sui limiti alti e bassi correnti di un determinato controllo indicatore di stato. <br/>                                                                                                                                                              |
| [**PBM \_ GETSTATE**](pbm-getstate.md)       | Ottiene lo stato dell'indicatore di stato.<br/>                                                                                                                                                                                                                        |
| [**PBM \_ GETSTEP**](pbm-getstep.md)         | Recupera l'incremento del passaggio per un indicatore di stato. L'incremento del passaggio è la quantità in base alla quale l'indicatore di stato aumenta la posizione corrente ogni volta che riceve un [**messaggio \_ STEPIT PBM.**](pbm-stepit.md)<br/>                                               |
| [**PBM \_ SETBARCOLOR**](pbm-setbarcolor.md) | Imposta il colore dell'indicatore di stato nel controllo indicatore di stato. <br/>                                                                                                                                                                                 |
| [**PBM \_ SETBKCOLOR**](pbm-setbkcolor.md)   | Imposta il colore di sfondo nell'indicatore di stato. <br/>                                                                                                                                                                                                            |
| [**PBM \_ SETMARQUEE**](pbm-setmarquee.md)   | Imposta l'indicatore di stato sulla modalità di selezione. In questo modo l'indicatore di stato si sposta come un rettangolo di selezione.<br/>                                                                                                                                                                |
| [**PBM \_ SETPOS**](pbm-setpos.md)           | Imposta la posizione corrente per un indicatore di stato e ridisegna l'indicatore per riflettere la nuova posizione. <br/>                                                                                                                                                             |
| [**PBM \_ SETRANGE**](pbm-setrange.md)       | Imposta i valori minimo e massimo per un indicatore di stato e ridisegna l'indicatore per riflettere il nuovo intervallo.<br/>                                                                                                                                                       |
| [**PBM \_ SETRANGE32**](pbm-setrange32.md)   | Imposta l'intervallo di un controllo indicatore di stato su un valore a 32 bit. <br/>                                                                                                                                                                                               |
| [**PBM \_ SETSTATE**](pbm-setstate.md)       | Imposta lo stato dell'indicatore di stato.<br/>                                                                                                                                                                                                                        |
| [**PBM \_ SETSTEP**](pbm-setstep.md)         | Specifica l'incremento del passaggio per un indicatore di stato. L'incremento del passaggio è la quantità in base alla quale l'indicatore di stato aumenta la posizione corrente ogni volta che riceve un [**messaggio \_ STEPIT PBM.**](pbm-stepit.md) Per impostazione predefinita, l'incremento del passaggio è impostato su 10. <br/> |
| [**PBM \_ STEPIT**](pbm-stepit.md)           | Sposta in avanti la posizione corrente di un indicatore di stato in base all'incremento del passaggio e ridisegna l'indicatore per riflettere la nuova posizione. Un'applicazione imposta l'incremento del passaggio inviando il [**messaggio \_ SETSTEP PBM.**](pbm-setstep.md) <br/>                                |



 

### <a name="structures"></a>Strutture



| Argomento                      | Contenuto                                                                                                                                                                 |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PBRANGE**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) | Contiene informazioni sui limiti alti e bassi di un controllo indicatore di stato. Questa struttura viene usata con il [**messaggio \_ GETRANGE PBM.**](pbm-getrange.md) <br/> |



 

### <a name="constants"></a>Costanti



| Argomento                                                          | Contenuto                                                                            |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [Stili del controllo Indicatore di stato](progress-bar-control-styles.md) | I controlli Indicatore di stato supportano gli **stili di controllo** seguenti:<br/> |



 

 

 





