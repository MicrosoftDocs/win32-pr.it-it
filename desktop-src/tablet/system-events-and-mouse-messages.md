---
description: L'applicazione incorpora la progettazione e l'utilizzo ottimali della penna del Tablet inviando sia i messaggi di sistema che gli eventi di sistema di Microsoft Windows.
ms.assetid: ccd45b68-f037-43da-a7d0-1df9439afd11
title: Eventi di sistema e messaggi del mouse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45c068e30db6ca1a85429667e2a8f1f93c505299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319133"
---
# <a name="system-events-and-mouse-messages"></a>Eventi di sistema e messaggi del mouse

L'applicazione incorpora la progettazione e l'utilizzo ottimali della penna del Tablet inviando sia i messaggi di sistema che gli eventi di sistema di Microsoft Windows. Le applicazioni ricevono entrambi i set di eventi per ogni movimento o azione della penna. L'applicazione sceglie quindi l'evento appropriato da usare in base al contesto dell'azione. I messaggi del mouse Windows funzionano correttamente per puntare e selezionare le attività ed è consigliabile usarli per le attività che coinvolgono l'interazione con gli elementi dell'interfaccia utente. Gli eventi penna funzionano correttamente per l'applicazione Ink in tempo reale, le azioni penna e la grafia.

> [!Note]  
> Sia gli eventi penna che i messaggi del mouse vengono inviati a un'applicazione, indipendentemente dal fatto che venga utilizzata la penna o il mouse.

 

## <a name="distinguishing-pen-input-from-mouse-and-touch"></a>Distinzione dell'input penna da mouse e tocco

Quando l'applicazione riceve un messaggio del mouse, ad esempio WM \_ LBUTTONDOWN, può chiamare la funzione [**GetMessageExtraInfo**](/windows/win32/api/winuser/nf-winuser-getmessageextrainfo) per valutare se il messaggio proviene da una penna o da un dispositivo mouse.

È necessario che il valore restituito da [**GetMessageExtraInfo**](/windows/win32/api/winuser/nf-winuser-getmessageextrainfo) sia mascherato rispetto a 0xffffff00 e quindi confrontato con 0xFF515700. Le seguenti definizioni possono rendere questo più chiaro:


```C++
#define MI_WP_SIGNATURE<entity type="nbsp"/> 0xFF515700
#define SIGNATURE_MASK<entity type="nbsp"/><entity type="nbsp"/> 0xFFFFFF00
#define IsPenEvent(dw)<entity type="nbsp"/><entity type="nbsp"/> (((dw) & SIGNATURE_MASK) == MI_WP_SIGNATURE
```



Se il confronto è true, il messaggio del mouse è stato generato da una penna del Tablet PC o da un touchscreen. In tutti gli altri casi, è possibile presupporre che il messaggio sia stato generato da un dispositivo mouse.

Gli 8 bit inferiori restituiti da [**GetMessageExtraInfo**](/windows/win32/api/winuser/nf-winuser-getmessageextrainfo) sono variabili. Di questi bit, 7 (i 7 inferiori, mascherati da 0x7F) vengono usati per rappresentare l'ID del cursore, zero per il mouse o un valore della variabile per l'ID della penna. Inoltre, in Windows Vista, l'ottavo bit, mascherato da 0x80, viene utilizzato per distinguere l'input tocco dall'input penna (0 = penna, 1 = tocco).

## <a name="supported-system-gestures"></a>Movimenti di sistema supportati

Nella tabella seguente sono elencati i movimenti di sistema attualmente inclusi in Windows XP Tablet PC Edition, vengono descritti in dettaglio le azioni penna corrispondenti e gli eventi di sistema e viene illustrato il modo in cui sono correlati alle azioni tradizionali del mouse.



| Movimento penna                                  | Azione del mouse                                                    | Descrizione movimento penna                                                                                                                                                                                                             | Messaggi di evento                                                                                                                       | Messaggi del mouse                                                                                                                        | Comportamenti nelle applicazioni basate su Windows                                                                                                                                          |
|----------------------------------------------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tocco<br/>                               | Clic con il pulsante sinistro<br/>                                           | Toccare la schermata una volta con la penna.<br/>                                                                                                                                                                                        | \_Tocco ISG inviato quando la penna viene sollevata.<br/>                                                                                         | WM \_ LBUTTONDOWN e WM \_ LBUTTONUP inviati al momento della penna.<br/>                                                                    | Scegliere comando dal menu o dalla barra degli strumenti, intervenire se si sceglie il comando, Imposta punto di inserimento (IP), Mostra feedback selezione.<br/>                                                |
| Doppio tocco<br/>                        | Doppio clic<br/>                                         | Toccare schermata due volte in rapida successione.<br/>                                                                                                                                                                                    | ISG \_ DOUBLETAP inviato al secondo tocco (in basso). \_Evento Tap ISG inviato al primo tocco.<br/>                                           | WM \_ LBUTTONDBLCLK inviati al secondo tocco (in basso). WM \_ LBUTTONDOWN e WM \_ LBUTTONUP inviati al primo tocco (su) come per un singolo tocco.<br/> | Selezionare Word, Apri file o cartella.<br/>                                                                                                                                     |
| Tenere premuto<br/>                    | Fare clic con il pulsante destro del mouse su<br/>                                          | Toccare lo schermo e attendere che venga visualizzata un'icona del mouse, quindi sollevare la penna per visualizzare un menu di scelta rapida. Un'applicazione può scegliere di eseguire un'azione diversa dalla visualizzazione di un menu con il pulsante destro del mouse quando la penna viene sollevata.<br/> | ISG \_ HOLDENTER inviato quando la penna è rimasta inattiva abbastanza a lungo. ISG \_ RIGHTTAP inviato quando la penna viene sollevata e si fa clic con il pulsante destro del mouse.<br/> | WM \_ RBUTTONDOWN e WM \_ RBUTTONUP inviati quando si fa clic con il pulsante destro del mouse (quando la penna viene sollevata).<br/>                                       | Mostra menu di scelta rapida.<br/>                                                                                                                                                   |
| Attesa<br/>                      | Clic con il pulsante sinistro<br/>                                           | Toccare lo schermo e attendere finché non viene visualizzata l'icona del mouse. È probabile che gli utenti eseguano questa operazione quando si verificano incidenti e si vuole ripristinare semplicemente il tocco.<br/>                                                 | \_Tocco ISG inviato quando la penna viene sollevata.<br/>                                                                                         | WM \_ LBUTTONDOWN e WM \_ LBUTTONUP inviati quando la penna viene sollevata.<br/>                                                                 | Fare clic con il pulsante sinistro del mouse per molto tempo. Nessun equivalente del mouse esistente. Si tratta di un fallback per i casi in cui un utente esegue la pressione prolungata. L'evento Ripristina la scelta di un tocco.<br/> |
| Trascinamento<br/>                              | Trascinamento a sinistra<br/>                                            | Toccare la schermata per selezionare l'oggetto da spostare, quindi trascinare dopo la selezione dell'oggetto.<br/>                                                                                                                     | ISG \_ trascina inviato all'avvio del trascinamento.<br/>                                                                                          | WM \_ LBUTTONDOWN inviato all'avvio del trascinamento, seguito da una serie di messaggi di spostamento del mouse e seguito da un \_ evento WM LBUTTONUP.<br/> | Drag-Select, come in Microsoft Word quando si inizia con un indirizzo IP; Seleziona più parole; trascinare, come quando si trascina un oggetto in Windows; scorrimento.<br/>                            |
| Premere e tenere premuto seguito da un trascinamento<br/> | Pulsante destro del mouse<br/>                                           | Toccare la schermata per selezionare l'oggetto da spostare. Attendere finché non viene visualizzata l'icona del mouse, quindi trascinare per spostare l'oggetto. Sollevare la penna per visualizzare un menu di scelta rapida.<br/>                                                   | ISG \_ HOLDENTER inviato quando la penna è rimasta inattiva per un certo periodo di tempo. ISG \_ RightDrag se inviato all'avvio del trascinamento.<br/>                           | WM \_ RBUTTONDOWN inviato all'avvio del trascinamento, seguito da una serie di messaggi di spostamento del mouse, seguiti da un \_ evento WM RBUTTONUP.<br/>     | Trascinare, come quando si trascina un oggetto o una selezione seguito da un menu di scelta rapida.<br/>                                                                                             |
| Cursore penna<br/>                         | Passaggio del mouse<br/>                                          | Mantenere la penna stabile a una distanza ridotta dallo schermo.<br/>                                                                                                                                                                 | \_Evento ISG HOVERENTER inviato inizialmente. Al termine dell'intervallo di passaggio del mouse, ISG \_ HOVERLEAVEis inviato.<br/>                           | Nessun messaggio equivalente del mouse.<br/>                                                                                               | Mostra la descrizione comando, gli effetti di rollforward e altri comportamenti del passaggio del mouse.<br/>                                                                                                     |
| Vibrazione in aria<br/>                      | Mostra **Pannello di input di Tablet PC**. Nessun equivalente del mouse.<br/> | Spostare rapidamente la penna da un lato all'altro, mantenendo il suggerimento sopra, ma all'interno dell'intervallo dello schermo.<br/>                                                                                                                          | L'evento non viene passato all'applicazione.<br/>                                                                                   | Nessun messaggio equivalente del mouse.<br/>                                                                                               | Nuove, specifiche per Tablet PC.<br/>                                                                                                                                           |



 

## <a name="specifying-stylus-and-touch-interactions"></a>Specifica delle interazioni di stilo e tocco

Per impostazione predefinita, la finestra riceverà tutti gli eventi di movimento del sistema e utilizzerà il modello di interazione predefinito. Alcune parti di questo modello possono interferire con l'applicazione, in modo che sia possibile disabilitarle selettivamente rispondendo al [**\_ messaggio WM Tablet \_ QUERYSYSTEMGESTURESTATUS**](wm-tablet-querysystemgesturestatus-message.md) in WndProc.

 

 
