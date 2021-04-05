---
title: Rappresentazione visiva
description: Un controllo supporta il posizionamento e la visualizzazione all'interno del contenitore tramite la tecnologia di documenti compositi e la tecnologia di trascinamento della selezione OLE che coinvolge sia il controllo che il relativo contenitore.
ms.assetid: a7940560-360c-4c0d-9ac1-d051adb0b83e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9711dccbc7aa17f0b4a2ff228b2e2e4421e5083b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714419"
---
# <a name="visual-representation"></a>Rappresentazione visiva

Un controllo supporta il posizionamento e la visualizzazione all'interno del contenitore tramite la tecnologia di documenti compositi e la tecnologia di trascinamento della selezione OLE che coinvolge sia il controllo che il relativo contenitore. Il controllo deve essere in grado di creare se stesso mentre il contenitore gestisce la posizione del controllo e le relative dimensioni.

I controlli vengono aggiunti alle funzioni di base fornite dai documenti OLE. Un controllo chiama il metodo [**IOleClientSite:: RequestNewObjectLayout**](/windows/desktop/api/OleIdl/nf-oleidl-ioleclientsite-requestnewobjectlayout) del client per indicare al contenitore che desidera modificare le dimensioni. Il client chiama l'oggetto [**IOleObject:: GetExtent**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getextent) del controllo per ottenere la nuova dimensione e chiama [**IOleInPlaceObject:: SetObjectRects**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceobject-setobjectrects) per impostare il controllo sulle nuove dimensioni.

I controlli che supportano solo [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) o [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) non supportano la memorizzazione nella cache tramite [**IOleCache2**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache2) , perché la cache richiede il supporto per [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage). Tuttavia, questi controlli dovrebbero consentire al client di eseguire il rendering del controllo tramite [**IDataObject:: GetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata) , in modo che il client possa eventualmente creare e gestire la propria cache dei dati di presentazione per il controllo.

I controlli utilizzano il tipo HIMETRIC per le coordinate. Tuttavia, contenitori diversi possono utilizzare sistemi di coordinate diversi. Il contenitore vuole ricevere le coordinate nel proprio sistema, ma il controllo non conosce necessariamente le coordinate usate dal contenitore. Per comunicare correttamente, il controllo richiede un modo per convertire i valori nelle coordinate del relativo contenitore. Il contenitore fornisce un oggetto sito con il metodo [**IOleControlSite:: TransformCoords**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-transformcoords) . Il controllo chiama innanzitutto questo metodo sul sito client del contenitore per convertire le coordinate nelle coordinate appropriate per il contenitore. Quindi, può passare le coordinate convertite al contenitore.

I controlli possono chiamare [**IOleControlSite:: LockInPlaceActive**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-lockinplaceactive) nell'oggetto sito del contenitore per evitare che il contenitore provi a abbassare di grado il controllo dallo stato attivo sul posto. Abbassamento il controllo in questo modo causa la disattivazione del controllo e la sua finestra distrutta, pertanto se il controllo deve mantenere la finestra per una durata nota, può chiamare **LockInPlaceActive** per garantirne lo stato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controlli ActiveX](activex-controls.md)
</dt> </dl>

 

 




