---
title: Gestione della tastiera per i controlli
description: Un controllo risponde agli acceleratori della tastiera, in modo che l'utente finale possa avviare le azioni eseguite dal controllo.
ms.assetid: 59aca5cb-f109-49ee-897d-43610501f7f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbe03058fdb0192a0f8f7b13032612288045775b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332495"
---
# <a name="keyboard-handling-for-controls"></a>Gestione della tastiera per i controlli

Un controllo risponde agli acceleratori della tastiera, in modo che l'utente finale possa avviare le azioni eseguite dal controllo. Il contenitore gestisce l'attività della tastiera per tutti i controlli incorporati. Con i documenti composti, i tasti di scelta rapida si applicano solo all'oggetto attualmente attivo. Con i controlli, è stato aggiunto un meccanismo che consente a un controllo di rispondere ai tasti di scelta rapida anche se attualmente non è attiva l'interfaccia utente.

I metodi [**IOleControl:: GetControlInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo) e [**IOleControl:: onmnemonico**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic) e il metodo [**IOleControlSite:: OnControlInfoChanged**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-oncontrolinfochanged) gestiscono i tasti di scelta rapida di un controllo. Una struttura [**CONTROLINFO**](/windows/win32/api/ocidl/ns-ocidl-controlinfo) descrive i tasti di scelta rapida di un controllo e i flag passati tramite il metodo **GetControlInfo** descrivono il comportamento dei controlli con i tasti Enter e ESC. Quando un controllo modifica i tasti di scelta, chiama **OnControlInfoChanged** , in modo che il contenitore possa ricaricare la struttura, se necessario.

Quando un controllo è un'interfaccia utente attiva, è anche il controllo con lo stato attivo. Quando i controlli vengono attivati e disattivati tra l'oggetto attivo sul posto e gli Stati attivi dell'interfaccia utente, il controllo chiama [**IOleControlSite:: onfocus**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-onfocus) per indicare al contenitore le modifiche di questo tipo.

Inoltre, quando un controllo è un'interfaccia utente attiva, avrà la prima possibilità di elaborare tutte le sequenze di tasti. Per fornire a un contenitore la possibilità di elaborare la sequenza di tasti prima del controllo, il controllo chiama [**IOleControlSite:: TranslateAccelerator**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-translateaccelerator). Se il contenitore non gestisce la sequenza di tasti, il controllo lo elabora.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controlli ActiveX](activex-controls.md)
</dt> </dl>

 

 




