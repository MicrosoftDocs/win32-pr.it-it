---
title: Controllo Animation
description: Questa sezione contiene informazioni sugli elementi di programmazione usati con i controlli di animazione.
ms.assetid: 16994f93-e0fd-4c71-9c8a-15642408b8de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7241199dc92004f9b3616e2666dd96eadbf43fc6c4dfe9081369e13cca26e082
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921781"
---
# <a name="animation-control"></a>Controllo Animation

Questa sezione contiene informazioni sugli elementi di programmazione usati con i controlli di animazione.

### <a name="overviews"></a>Cenni preliminari



| Argomento                                                      | Contenuto                                                                                                                                                                                                                           |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informazioni sui controlli di animazione](animation-control-overview.md) | Un *controllo animazione* è una finestra che visualizza Audio-Video clip AVI (Interleaved). Un clip AVI è una serie di fotogrammi bitmap come un film. I controlli di animazione possono visualizzare solo clip AVI che non contengono audio.<br/> |
| [Uso dei controlli di animazione](using-animation-control.md)    | In questa sezione vengono fornite informazioni dettagliate sull'implementazione e codice di esempio per i controlli di animazione.<br/>                                                                                                                                      |



 

### <a name="macros"></a>Macro



| Argomento                                           | Contenuto                                                                                                                                                                                                                                                          |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Anima \_ chiusura**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close)         | Chiude un clip AVI. È possibile usare questa macro o inviare il [**messaggio ACM \_ OPEN**](acm-open.md) in modo esplicito, passando **parametri NULL.** <br/>                                                                                                              |
| [**Aggiungere \_ un'animazione a Create**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create)       | Crea un controllo animazione. [**Animare \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) chiama la [**funzione CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) per creare il controllo di animazione. <br/>                                                                                   |
| [**Animare \_ IsPlaying**](/windows/desktop/api/Commctrl/nf-commctrl-animate_isplaying) | Verifica se è in esecuzione un clip AVI. È possibile usare questa macro o inviare un [**messaggio \_ ACM ISPLAYING.**](acm-isplaying.md)<br/>                                                                                                                            |
| [**Animare \_ l'apertura**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open)           | Apre un clip AVI e visualizza il primo fotogramma in un controllo di animazione. È possibile usare questa macro o inviare il messaggio [**OPEN di ACM \_ in**](acm-open.md) modo esplicito. <br/>                                                                                          |
| [**Animare \_ OpenEx**](/windows/desktop/api/Commctrl/nf-commctrl-animate_openex)       | Apre un clip AVI da una risorsa in un modulo specificato e visualizza il primo fotogramma in un controllo di animazione. È possibile usare questa macro o inviare il messaggio [**OPEN di ACM \_ in**](acm-open.md) modo esplicito. <br/>                                                    |
| [**Aggiungere \_ un'animazione alla riproduzione**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play)           | Riproduce un clip AVI in un controllo di animazione. Il controllo riproduce il clip in background mentre il thread continua l'esecuzione. È possibile usare questa macro o inviare il messaggio [**PLAY ACM \_ in**](acm-play.md) modo esplicito. <br/>                                    |
| [**Animare \_ Seek**](/windows/desktop/api/Commctrl/nf-commctrl-animate_seek)           | Indica a un controllo di animazione di visualizzare un frame specifico di un clip AVI. Il controllo visualizza il clip in background mentre il thread continua l'esecuzione. È possibile usare questa macro o inviare il messaggio [**PLAY ACM \_ in**](acm-play.md) modo esplicito. <br/> |
| [**Animare \_ Stop**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop)           | Interrompe la riproduzione di un clip AVI in un controllo di animazione. È possibile usare questa macro o inviare il messaggio [**STOP di ACM \_**](acm-stop.md) in modo esplicito. <br/>                                                                                                               |



 

### <a name="messages"></a>Messaggi



| Argomento                                   | Contenuto                                                                                                                                                                                                                                   |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ACM \_ ISPLAYING**](acm-isplaying.md) | Controlla se un clip AVI è in riproduzione. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ Animate IsPlaying.**](/windows/desktop/api/Commctrl/nf-commctrl-animate_isplaying)<br/>                                                                                   |
| [**ACM \_ OPEN**](acm-open.md)           | Apre un clip AVI e visualizza il primo fotogramma in un controllo di animazione. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ Animate Open o**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) Animate [**\_ OpenEx.**](/windows/desktop/api/Commctrl/nf-commctrl-animate_openex) <br/>              |
| [**ACM \_ PLAY**](acm-play.md)           | Riproduce un clip AVI in un controllo di animazione. Il controllo riproduce il clip in background mentre il thread continua l'esecuzione. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**Animate \_ Play.**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play)<br/> |
| [**ARRESTO \_ di ACM**](acm-stop.md)           | Interrompe la riproduzione di un clip AVI in un controllo di animazione. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**Animate \_ Stop.**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop)<br/>                                                                            |



 

### <a name="notifications"></a>Notifiche



| Argomento                           | Contenuto                                                                                                                                                                                                       |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ACN \_ START**](acn-start.md) | Notifica alla finestra padre di un controllo di animazione che è stata avviata la riproduzione del clip AVI associato. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ COMMAND.**](/windows/desktop/menurc/wm-command) <br/>      |
| [**ACN \_ STOP**](acn-stop.md)   | Notifica alla finestra padre di un controllo di animazione che la riproduzione del clip AVI associato è stata interrotta. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ COMMAND.**](/windows/desktop/menurc/wm-command) <br/> |



 

### <a name="constants"></a>Costanti



| Argomento                                                        | Contenuto                                                                      |
|--------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**Stili del controllo Animation**](animation-control-styles.md) | Questa sezione elenca gli stili delle finestre usati con i controlli di animazione.<br/> |



 

 

