---
title: Proprietà di ambiente per i controlli
description: Proprietà di ambiente per i controlli
ms.assetid: 19aa3bc2-1605-43e1-acf4-ab782d012539
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 421a643873e818d8f5c0e006b4bb9049c1230c5f4e18525cdf7ed2b4175797bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119994061"
---
# <a name="ambient-properties-for-controls"></a>Proprietà di ambiente per i controlli

Se un controllo supporta tutte le proprietà di ambiente, deve rispettare almeno i valori delle proprietà di ambiente seguenti in base alle condizioni riportate nella tabella seguente usando i dispid standard.



| Proprietà Ambient            | Dispid          | Commento/Condizioni per l'uso                                                                                                                                                                                                                                                                |
|-----------------------------|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LocaleID<br/>         | -705<br/> | Se le impostazioni locali sono significative per il controllo, ad esempio per l'output di testo<br/>                                                                                                                                                                                                                  |
| Usermode <br/>        | -709<br/> | Se il controllo si comporta in modo diverso in modalità utente (progettazione) e in modalità di esecuzione<br/>                                                                                                                                                                                                          |
| UIDead<br/>           | -710<br/> | Se il controllo reagisce agli eventi dell'interfaccia utente, deve rispettare questa proprietà di ambiente<br/>                                                                                                                                                                                                 |
| ShowGrabHandles<br/>  | -711<br/> | Se il controllo supporta il ridimensionamento sul posto di se stesso<br/>                                                                                                                                                                                                                             |
| ShowHatching<br/>     | -712<br/> | Se il controllo supporta l'attivazione sul posto e l'attivazione dell'interfaccia utente<br/>                                                                                                                                                                                                                   |
| DisplayAsDefault<br/> | -713<br/> | Solo se il controllo è contrassegnato come OLEMISC ACTSLIKEBUTTON (il che significa che viene fornito il supporto per i tasti di scelta rapida, è quindi necessario implementazione di \_ [**IOleControl::GetControlInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo) e [**IOleControl::OnMnemonic).**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic)<br/> |



 

Come descritto in precedenza, l'uso di ambiente richiede sia [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) (per [**OnAmbientPropertyChange**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange) come minimo) che [**IOleObject**](/windows/desktop/api/OleIdl/nn-oleidl-ioleobject) (per [**SetClientSite**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setclientsite) e [**GetClientSite).**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getclientsite)

Il bit OLEMISC \_ SETCLIENTSITEFIRST potrebbe non essere necessariamente supportato da un contenitore. In questi casi, un controllo deve ricorrere ai valori predefiniti per le proprietà di ambiente necessarie.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controlli](controls.md)
</dt> </dl>

 

 





