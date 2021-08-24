---
description: Quando viene eseguita una determinata azione, gli eventi di sistema (con prefisso ISG) vengono inviati e ricevuti quasi istantaneamente \_ dall'applicazione.
ms.assetid: deca6d17-fe2c-4130-88ca-d0605bcb6084
title: Sequenza temporale dei messaggi del mouse e degli eventi di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 635147b3f30b8746c75901de78336102ac8d1b41a685919c27f990496f5f225d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119819606"
---
# <a name="timeline-of-mouse-messages-and-system-events"></a>Sequenza temporale dei messaggi del mouse e degli eventi di sistema

Quando viene eseguita una determinata azione, gli eventi di sistema (con prefisso ISG) vengono inviati e ricevuti quasi istantaneamente \_ dall'applicazione. I messaggi del mouse (con prefisso WM) vengono inviati quando l'azione viene eseguita e vengono ricevuti dall'applicazione dopo il tempo necessario per l'elaborazione dell'evento da parte del servizio di \_ messaggistica microsoft Windows. Inoltre, **CursorDown** e **CursorUp** sono eventi penna ricevuti dall'hardware della penna. Vengono inviati rispettivamente quando la penna del tablet tocca lo schermo e quando viene sollevata dallo schermo.

Gli eventi penna e i messaggi del mouse non vengono sincronizzati. Non è garantito che i messaggi del mouse e gli eventi della penna corrispondenti si verificheranno in un ordine specifico. Il grafico seguente mostra la sequenza prevista, ma non sempre prevedibile, di eventi di sistema e mouse inviati. Si noti nel grafico che gli eventi del mouse vengono ritardati quando vengono rilevati eventi movimento di sistema.

![sequenza prevista di eventi di sistema e mouse per l'input penna](images/ccdafa48-13c0-4af7-aec5-ed162be4bbe7.jpg)

## <a name="important-implementation-considerations"></a>Considerazioni importanti sull'implementazione

Quando si sviluppano messaggi del mouse ed eventi di sistema, tenere presente quanto segue:

-   Sia gli eventi penna che i messaggi del mouse vengono inviati a un'applicazione, indipendentemente dal fatto che la penna o il mouse siano usati.
-   Se l'applicazione è in ascolto di messaggi con penna e mouse, è difficile prevedere la relazione dei messaggi e quindi il comportamento finale. Gli eventi penna e i messaggi del mouse non vengono sincronizzati. Non è garantito che i messaggi del mouse e gli eventi di penna corrispondenti (ad esempio WM \_ LBUTTONDOWN e **ISG \_ TAP** o WM \_ LBUTTONDBLCLK e **ISG \_ DBLTAP)** si verificheranno in un ordine specifico. La relazione tra questi messaggi è complessa.
-   È consigliabile non combinare eventi mouse e penna nella stessa funzionalità dell'applicazione. Ad esempio, una funzionalità dell'applicazione che risponde a **CursorDown** e **MouseUp** potrebbe non comportarsi come previsto ora o con le versioni future di Tablet PC SDK.
-   Per il blocco attraverso la sequenza di eventi, se l'utente trascina la penna del tablet prima del completamento della sequenza, gli eventi inviati corrispondono al trascinamento a sinistra. Ad esempio, all'avvio del trascinamento, vengono inviati **ISG \_ DRAG** e WM \_ LBUTTONDOWN. Quando la penna viene infine sollevata, **vengono inviati CursorUp** e WM \_ LBUTTONUP. L'evento movimento di sistema potrebbe non essere generato immediatamente perché deve determinare il tipo di evento in corso.
-   Un doppio tocco con una penna del tablet è spesso meno accurato rispetto a un doppio clic con il mouse. Questo deriva dalla natura intrinseca dell'esecuzione di un doppio tocco con una penna del tablet. Poiché l'utente deve elevare la penna del tablet per eseguire un doppio tocco, il tempo tra i tocchi è spesso maggiore del tempo corrispondente tra i clic di un doppio clic. Inoltre, è probabile che i due tocchi della penna del tablet si verifichino in corrispondenza di coordinate dello schermo più distanti da quelle dei due clic del mouse. Per soddisfare questo problema, Windows XP Tablet PC Edition include impostazioni per la distanza temporale e spaziale tra i due tocchi di un doppio tocco separati dalle impostazioni del mouse per un doppio clic. Queste impostazioni possono essere modificate in Tablet PC e Penna Impostazioni in Pannello di controllo.

Per queste considerazioni, le applicazioni devono restare in ascolto di un solo set di messaggi anziché di entrambi. Se si compila un'applicazione abilitata per la penna, restare in ascolto solo dei messaggi di sistema e penna. Questi messaggi sono prevedibili e funzionano bene con la penna del tablet. Se si compila un'applicazione non abilitata per la penna, restare in ascolto solo dei messaggi del mouse.

 

 



