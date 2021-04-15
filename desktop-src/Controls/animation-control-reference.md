---
title: Controllo animazione
description: Questa sezione contiene informazioni sugli elementi di programmazione usati con i controlli di animazione.
ms.assetid: 16994f93-e0fd-4c71-9c8a-15642408b8de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd2a3fc7377c7258ba49b5a4188e6074270b5862
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474414"
---
# <a name="animation-control"></a>Controllo animazione

Questa sezione contiene informazioni sugli elementi di programmazione usati con i controlli di animazione.

### <a name="overviews"></a>Cenni preliminari



| Argomento                                                      | Contenuto                                                                                                                                                                                                                           |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informazioni sui controlli di animazione](animation-control-overview.md) | Un *controllo di animazione* è una finestra che visualizza un Audio-Video clip con INTERFOLIAZIONE (AVI). Un clip AVI è costituito da una serie di frame bitmap come un film. I controlli di animazione possono visualizzare solo le clip AVI che non contengono audio.<br/> |
| [Uso di controlli di animazione](using-animation-control.md)    | Questa sezione fornisce i dettagli di implementazione e il codice di esempio per i controlli dell'animazione.<br/>                                                                                                                                      |



 

### <a name="macros"></a>Macro



| Argomento                                           | Contenuto                                                                                                                                                                                                                                                          |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Animazione \_ chiusura**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close)         | Chiude un clip AVI. È possibile usare questa macro o inviare in modo esplicito il messaggio di [**\_ apertura ACM**](acm-open.md) , passando i parametri **null** . <br/>                                                                                                              |
| [**Animare \_ Crea**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create)       | Crea un controllo animazione. [**Anima \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) chiama la funzione [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) per creare il controllo dell'animazione. <br/>                                                                                   |
| [**Animare la \_ riproduzione**](/windows/desktop/api/Commctrl/nf-commctrl-animate_isplaying) | Verifica se è in esecuzione un clip AVI. È possibile utilizzare questa macro o inviare un messaggio di [**\_ riproduzione ACM**](acm-isplaying.md) .<br/>                                                                                                                            |
| [**Animazione \_ aperta**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open)           | Apre un clip AVI e ne Visualizza il primo fotogramma in un controllo dell'animazione. È possibile usare questa macro o inviare il messaggio di [**\_ apertura di ACM**](acm-open.md) in modo esplicito. <br/>                                                                                          |
| [**Animare \_ OpenEx**](/windows/desktop/api/Commctrl/nf-commctrl-animate_openex)       | Apre un clip AVI da una risorsa in un modulo specificato e ne Visualizza il primo frame in un controllo Animation. È possibile usare questa macro o inviare il messaggio di [**\_ apertura di ACM**](acm-open.md) in modo esplicito. <br/>                                                    |
| [**Animare \_ Play**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play)           | Riproduce un clip AVI in un controllo dell'animazione. Il controllo riproduce il clip in background mentre il thread continua l'esecuzione. È possibile usare questa macro o inviare il messaggio di [**\_ riproduzione ACM**](acm-play.md) in modo esplicito. <br/>                                    |
| [**Animate \_ Seek**](/windows/desktop/api/Commctrl/nf-commctrl-animate_seek)           | Indica a un controllo di animazione di visualizzare un frame specifico di una clip AVI. Il controllo Visualizza il clip in background mentre il thread continua l'esecuzione. È possibile usare questa macro o inviare il messaggio di [**\_ riproduzione ACM**](acm-play.md) in modo esplicito. <br/> |
| [**\_Interrompi animazione**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop)           | Interrompe la riproduzione di un clip AVI in un controllo Animation. È possibile usare questa macro o inviare il messaggio di [**\_ arresto di ACM**](acm-stop.md) in modo esplicito. <br/>                                                                                                               |



 

### <a name="messages"></a>Messaggi



| Argomento                                   | Contenuto                                                                                                                                                                                                                                   |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RIPRODUZIONE di ACM \_**](acm-isplaying.md) | Verifica se è in esecuzione un clip AVI. È possibile inviare questo messaggio in modo esplicito o utilizzare la macro di [**animazione \_**](/windows/desktop/api/Commctrl/nf-commctrl-animate_isplaying) .<br/>                                                                                   |
| [**apertura di ACM \_**](acm-open.md)           | Apre un clip AVI e ne Visualizza il primo fotogramma in un controllo dell'animazione. È possibile inviare questo messaggio in modo esplicito o usare la macro OpenEx, [**animate \_ Open**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) o [**\_ animate**](/windows/desktop/api/Commctrl/nf-commctrl-animate_openex) . <br/>              |
| [**riproduzione di ACM \_**](acm-play.md)           | Riproduce un clip AVI in un controllo dell'animazione. Il controllo riproduce il clip in background mentre il thread continua l'esecuzione. È possibile inviare questo messaggio in modo esplicito o utilizzando [**\_ la macro animazione**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play) .<br/> |
| [**arresto di ACM \_**](acm-stop.md)           | Interrompe la riproduzione di un clip AVI in un controllo Animation. È possibile inviare questo messaggio in modo esplicito o usando la macro di [**animazione \_ Stop**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop) .<br/>                                                                            |



 

### <a name="notifications"></a>Notifiche



| Argomento                           | Contenuto                                                                                                                                                                                                       |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_avvio ACN**](acn-start.md) | Notifica alla finestra padre di un controllo di animazione che è iniziata la riproduzione del clip AVI associato. Questo codice di notifica viene inviato sotto forma di un messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) . <br/>      |
| [**arresto di ACN \_**](acn-stop.md)   | Notifica alla finestra padre di un controllo di animazione che la riproduzione del clip AVI associato è stata interrotta. Questo codice di notifica viene inviato sotto forma di un messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) . <br/> |



 

### <a name="constants"></a>Costanti



| Argomento                                                        | Contenuto                                                                      |
|--------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**Stili del controllo di animazione**](animation-control-styles.md) | Questa sezione elenca gli stili della finestra usati con i controlli di animazione.<br/> |



 

 

