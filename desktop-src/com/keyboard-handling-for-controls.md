---
title: Gestione della tastiera per i controlli
description: Un controllo risponde ai tasti di scelta rapida in modo che l'utente finale possa avviare le azioni eseguite dal controllo.
ms.assetid: 59aca5cb-f109-49ee-897d-43610501f7f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26081d36c62b11163ceb8c41421ea0370d18b3ce9bf16be68e4e8a06a5f1a489
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736558"
---
# <a name="keyboard-handling-for-controls"></a>Gestione della tastiera per i controlli

Un controllo risponde ai tasti di scelta rapida in modo che l'utente finale possa avviare le azioni eseguite dal controllo. Il contenitore gestisce l'attività della tastiera per tutti i controlli incorporati. Con i documenti composti, i tasti di scelta rapida si applicano solo all'oggetto attualmente attivo. Con i controlli è stato aggiunto un meccanismo in modo che un controllo possa rispondere ai relativi tasti di scelta rapida anche se non è attualmente attivo dell'interfaccia utente.

I [**metodi IOleControl::GetControlInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo) e [**IOleControl::OnMnemonic**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic) e il metodo [**IOleControlSite::OnControlInfoChanged**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-oncontrolinfochanged) gestiscono i tasti di scelta rapida di un controllo. Una [**struttura CONTROLINFO**](/windows/win32/api/ocidl/ns-ocidl-controlinfo) descrive i tasti di scelta rapida mnemoici di un controllo e i flag passati tramite il metodo **GetControlInfo** descrivono il comportamento dei controlli con i tasti INVIO e ESC. Quando un controllo modifica i relativi mnemonici, chiama **OnControlInfoChanged** in modo che il contenitore possa ricaricare la struttura, se necessario.

Quando un controllo è attivo dell'interfaccia utente, è anche il controllo con lo stato attivo. Quando i controlli vengono attivati e disattivati tra gli stati attivi sul posto e gli stati attivi dell'interfaccia utente, il controllo chiama [**IOleControlSite::OnFocus**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-onfocus) per indicare al contenitore tali modifiche.

Inoltre, quando un controllo è attivo nell'interfaccia utente, avrà la prima possibilità di elaborare eventuali sequenze di tasti. Per offrire a un contenitore la possibilità di elaborare la sequenza di tasti prima del controllo, il controllo chiama [**IOleControlSite::TranslateAccelerator**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-translateaccelerator). Se il contenitore non gestisce la sequenza di tasti, il controllo lo elabora.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[ActiveX Controlli](activex-controls.md)
</dt> </dl>

 

 




