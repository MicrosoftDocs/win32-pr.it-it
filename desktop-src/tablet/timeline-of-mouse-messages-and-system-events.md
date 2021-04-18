---
description: Quando viene eseguita un'azione specifica, gli eventi di sistema (con prefisso ISG \_ ) vengono inviati e ricevuti quasi istantaneamente dall'applicazione.
ms.assetid: deca6d17-fe2c-4130-88ca-d0605bcb6084
title: Sequenza temporale dei messaggi del mouse e degli eventi di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aee3e6cb7882e1628fee0d2bc40f79ed1e29f55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313912"
---
# <a name="timeline-of-mouse-messages-and-system-events"></a>Sequenza temporale dei messaggi del mouse e degli eventi di sistema

Quando viene eseguita un'azione specifica, gli eventi di sistema (con prefisso ISG \_ ) vengono inviati e ricevuti quasi istantaneamente dall'applicazione. I messaggi del mouse (preceduti da WM \_ ) vengono inviati quando l'azione viene eseguita e vengono ricevuti dall'applicazione dopo il tempo necessario per l'elaborazione dell'evento da parte del servizio di messaggistica Microsoft Windows. Inoltre, **CursorDown** e **CursorUp** sono eventi penna ricevuti dall'hardware Pen. Vengono inviati quando la penna del Tablet PC tocca lo schermo e quando viene sollevata rispettivamente dalla schermata.

Gli eventi penna e i messaggi del mouse non sono sincronizzati. Non vi è alcuna garanzia che i messaggi del mouse e gli eventi penna corrispondenti vengano eseguiti in un ordine particolare. Nel grafico seguente viene illustrata la sequenza di eventi di sistema e mouse prevista, ma non sempre prevedibile, che vengono inviati. Si noti che nel grafico vengono rimandati gli eventi del mouse quando vengono rilevati eventi di movimento del sistema.

![sequenza prevista di eventi di sistema e mouse per l'input penna](images/ccdafa48-13c0-4af7-aec5-ed162be4bbe7.jpg)

## <a name="important-implementation-considerations"></a>Considerazioni importanti sull'implementazione

Quando si sviluppa per i messaggi del mouse e gli eventi di sistema, tenere presente quanto segue:

-   Sia gli eventi penna che i messaggi del mouse vengono inviati a un'applicazione, indipendentemente dal fatto che venga utilizzata la penna o il mouse.
-   Se l'applicazione è in ascolto dei messaggi di penna e del mouse, è difficile prevedere la relazione dei messaggi e quindi il comportamento finale. Gli eventi penna e i messaggi del mouse non sono sincronizzati. Non vi è alcuna garanzia che i messaggi del mouse e gli eventi penna corrispondenti, ad esempio WM \_ LBUTTONDOWN e **ISG \_ Tap**, o WM \_ LBUTTONDBLCLK e **ISG \_ DBLTAP**, vengano eseguiti in un ordine particolare. La relazione tra questi messaggi è complessa.
-   Si consiglia di non combinare gli eventi di mouse e penna nella stessa funzionalità dell'applicazione. Ad esempio, una funzionalità dell'applicazione che risponde a **CursorDown** e **MouseUp** potrebbe non comportarsi come previsto ora o con le versioni future di Tablet PC SDK.
-   Per la sequenza di eventi di attesa tramite, se l'utente trascina la penna del Tablet PC prima che la sequenza venga completata, gli eventi inviati corrispondono al trascinamento a sinistra. Ad esempio, all'avvio del trascinamento, vengono inviati **ISG \_ drag** e WM \_ LBUTTONDOWN. Quando la penna viene revocata, vengono inviati **CursorUp** e WM \_ LBUTTONUP. L'evento del movimento di sistema potrebbe non essere attivato immediatamente perché deve determinare il tipo di evento che si sta verificando.
-   Un doppio tocco con una penna del tablet è spesso meno accurato rispetto a un doppio clic con il mouse. Questo deriva dalla natura intrinseca dell'esecuzione di un doppio tocco con una penna da tablet. Poiché l'utente deve sollevare la penna del tablet per eseguire un doppio tocco, il tempo tra i colpetti è spesso maggiore del tempo corrispondente tra i clic di un doppio clic. Inoltre, è probabile che i due rubinetti della penna del tablet si trovino a coordinate dello schermo che sono ulteriormente separate da quelle per i due clic del mouse. Per risolvere questo problema, in Windows XP Tablet PC Edition sono disponibili impostazioni per la distanza temporale e spaziale tra i due rubinetti di un doppio tocco distinti dalle impostazioni del mouse per un doppio clic. Queste impostazioni possono essere modificate nelle impostazioni del tablet e della penna nel pannello di controllo.

A causa di queste considerazioni, le applicazioni devono restare in ascolto di un solo set di messaggi anziché di entrambi. Se si compila un'applicazione abilitata per la penna, ascoltare solo i messaggi di sistema e di penna. Questi messaggi sono prevedibili e funzionano bene con la penna del Tablet PC. Se si compila un'applicazione che non è abilitata per la penna, ascoltare solo i messaggi del mouse.

 

 



