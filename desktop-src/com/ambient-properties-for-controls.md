---
title: Proprietà di ambiente per i controlli
description: Proprietà di ambiente per i controlli
ms.assetid: 19aa3bc2-1605-43e1-acf4-ab782d012539
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e166a7186021b53798150968c9998fed243de00
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396226"
---
# <a name="ambient-properties-for-controls"></a>Proprietà di ambiente per i controlli

Se un controllo supporta tutte le proprietà di ambiente, deve almeno rispettare i valori delle proprietà di ambiente seguenti in base alle condizioni indicate nella tabella seguente usando i DISPID standard.



| Proprietà di ambiente            | DISPID          | Commento/condizioni per l'utilizzo                                                                                                                                                                                                                                                                |
|-----------------------------|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LocaleID<br/>         | -705<br/> | Se le impostazioni locali sono significative per il controllo, ad esempio per l'output di testo<br/>                                                                                                                                                                                                                  |
| UserMode <br/>        | -709<br/> | Se il controllo si comporta in modo diverso in modalità utente (progettazione) e modalità di esecuzione<br/>                                                                                                                                                                                                          |
| UIDead<br/>           | -710<br/> | Se il controllo reagisce agli eventi dell'interfaccia utente, deve rispettare questa proprietà di ambiente<br/>                                                                                                                                                                                                 |
| ShowGrabHandles<br/>  | -711<br/> | Se il controllo supporta il ridimensionamento sul posto di se stesso<br/>                                                                                                                                                                                                                             |
| ShowHatching<br/>     | -712<br/> | Se il controllo supporta l'attivazione sul posto e l'attivazione dell'interfaccia utente<br/>                                                                                                                                                                                                                   |
| DisplayAsDefault<br/> | -713<br/> | Solo se il controllo è contrassegnato \_ come OLEMISC ACTSLIKEBUTTON (il che significa che viene fornito il supporto per i tasti di scelta rapida della tastiera, quindi è necessario implementare [**IOleControl:: GetControlInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo) e [**IOleControl:: onmnemonico**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic) ).<br/> |



 

Come descritto in precedenza, l'uso di ambienti richiede sia [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) (per [**OnAmbientPropertyChange**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange) come minimo) che [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject) (per [**SetClientSite**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setclientsite) e [**GetClientSite**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getclientsite)).

Il \_ bit SETCLIENTSITEFIRST di OLEMISC potrebbe non essere necessariamente supportato da un contenitore. In questi casi, è necessario che un controllo ricorra ai valori predefiniti per le proprietà di ambiente necessarie.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controlli](controls.md)
</dt> </dl>

 

 





