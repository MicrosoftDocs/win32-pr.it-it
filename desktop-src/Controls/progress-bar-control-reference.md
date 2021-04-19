---
title: ProgressBar
description: Questa sezione contiene informazioni sugli elementi di programmazione usati con i controlli indicatore di stato.
ms.assetid: vs|controls|~\controls\progbar\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b99a31bbbd3b80de0d528d5232c79c28af1e1f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297967"
---
# <a name="progress-bar"></a>ProgressBar

Questa sezione contiene informazioni sugli elementi di programmazione usati con i controlli indicatore di stato.

### <a name="overviews"></a>Cenni preliminari



| Argomento                                            | Contenuto                                                                                                           |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [Controllo indicatore di stato](progress-bar-control.md) | Un indicatore di stato è una finestra che può essere utilizzata da un'applicazione per indicare lo stato di avanzamento di un'operazione di lunga durata.<br/> |



 

### <a name="messages"></a>Messaggi



| Argomento                                       | Contenuto                                                                                                                                                                                                                                                              |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_DELTAPOS PBM**](pbm-deltapos.md)       | Sposta in avanti la posizione corrente di un indicatore di stato in base a un incremento specificato e ridisegnato la barra per riflettere la nuova posizione. <br/>                                                                                                                                 |
| [**\_GETBARCOLOR PBM**](pbm-getbarcolor.md) | Ottiene il colore dell'indicatore di stato.<br/>                                                                                                                                                                                                                        |
| [**\_GETBKCOLOR PBM**](pbm-getbkcolor.md)   | Ottiene il colore di sfondo dell'indicatore di stato.<br/>                                                                                                                                                                                                             |
| [**\_GETPOS PBM**](pbm-getpos.md)           | Recupera la posizione corrente dell'indicatore di stato. <br/>                                                                                                                                                                                                       |
| [**GetRange PBM \_**](pbm-getrange.md)       | Recupera le informazioni sui limiti massimo e minimo correnti di un determinato controllo indicatore di stato. <br/>                                                                                                                                                              |
| [**PBM \_ GETstate**](pbm-getstate.md)       | Ottiene lo stato dell'indicatore di stato.<br/>                                                                                                                                                                                                                        |
| [**getstep di PBM \_**](pbm-getstep.md)         | Recupera l'incremento del passaggio per un indicatore di stato. L'incremento del passaggio è la quantità in base alla quale l'indicatore di stato aumenta la posizione corrente ogni volta che viene ricevuto un messaggio [**\_ STEPIT PBM**](pbm-stepit.md) .<br/>                                               |
| [**\_SETBARCOLOR PBM**](pbm-setbarcolor.md) | Imposta il colore della barra indicatore di stato nel controllo indicatore di stato. <br/>                                                                                                                                                                                 |
| [**\_SETBKCOLOR PBM**](pbm-setbkcolor.md)   | Imposta il colore di sfondo nell'indicatore di stato. <br/>                                                                                                                                                                                                            |
| [**\_rettangolo di selezione**](pbm-setmarquee.md)   | Imposta l'indicatore di stato sulla modalità marquee. Questo fa sì che l'indicatore di stato si sposti come un Marquee.<br/>                                                                                                                                                                |
| [**\_SETPOS PBM**](pbm-setpos.md)           | Imposta la posizione corrente di un indicatore di stato e ridisegnato la barra in modo da riflettere la nuova posizione. <br/>                                                                                                                                                             |
| [**\_SEtrange PBM**](pbm-setrange.md)       | Imposta i valori minimo e massimo per un indicatore di stato e ridisegnato la barra in modo da riflettere il nuovo intervallo.<br/>                                                                                                                                                       |
| [**\_SETRANGE32 PBM**](pbm-setrange32.md)   | Imposta l'intervallo di un controllo indicatore di stato su un valore a 32 bit. <br/>                                                                                                                                                                                               |
| [**PBM ( \_ stato)**](pbm-setstate.md)       | Imposta lo stato dell'indicatore di stato.<br/>                                                                                                                                                                                                                        |
| [**operazione in fase di esecuzione PBM \_**](pbm-setstep.md)         | Specifica l'incremento del passaggio per un indicatore di stato. L'incremento del passaggio è la quantità in base alla quale l'indicatore di stato aumenta la posizione corrente ogni volta che viene ricevuto un messaggio [**\_ STEPIT PBM**](pbm-stepit.md) . Per impostazione predefinita, l'incremento del passaggio è impostato su 10. <br/> |
| [**\_STEPIT PBM**](pbm-stepit.md)           | Sposta in avanti la posizione corrente di un indicatore di stato in base all'incremento del passaggio e ridisegnato la barra per riflettere la nuova posizione. Un'applicazione consente di impostare l'incremento del passaggio inviando il messaggio di [**\_ sepasso PBM**](pbm-setstep.md) . <br/>                                |



 

### <a name="structures"></a>Strutture



| Argomento                      | Contenuto                                                                                                                                                                 |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PBRANGE**](/windows/desktop/api/Commctrl/ns-commctrl-pbrange) | Contiene informazioni sui limiti massimo e minimo di un controllo indicatore di stato. Questa struttura viene utilizzata [**con il messaggio \_**](pbm-getrange.md) della gestione basata su criteri. <br/> |



 

### <a name="constants"></a>Costanti



| Argomento                                                          | Contenuto                                                                            |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [Stili del controllo indicatore di stato](progress-bar-control-styles.md) | Gli stili di controllo seguenti sono supportati dai controlli **indicatore di stato** :<br/> |



 

 

 





