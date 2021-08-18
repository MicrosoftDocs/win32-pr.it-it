---
title: Rappresentazione visiva
description: Un controllo supporta il posizionamento e la visualizzazione di se stesso all'interno del contenitore tramite la tecnologia dei documenti composti e la tecnologia di trascinamento ole che coinvolge sia il controllo che il relativo contenitore.
ms.assetid: a7940560-360c-4c0d-9ac1-d051adb0b83e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1037b9f13d3122d19ec5ca429b2189426ac7ff69145e087828571c62aeb6f741
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118549431"
---
# <a name="visual-representation"></a>Rappresentazione visiva

Un controllo supporta il posizionamento e la visualizzazione di se stesso all'interno del contenitore tramite la tecnologia dei documenti composti e la tecnologia di trascinamento ole che coinvolge sia il controllo che il relativo contenitore. Il controllo deve essere in grado di disegnare se stesso mentre il contenitore gestisce la posizione del controllo e le relative dimensioni.

I controlli vengono aggiunti alle funzioni di base fornite dai documenti OLE. Un controllo chiama il metodo [**IOleClientSite::RequestNewObjectLayout**](/windows/desktop/api/OleIdl/nf-oleidl-ioleclientsite-requestnewobjectlayout) del client per indicare al contenitore che vuole modificarne le dimensioni. Il client chiama [**IOleObject::GetExtent**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getextent) del controllo per ottenere le nuove dimensioni e chiama [**IOleInPlaceObject::SetObjectRects**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceobject-setobjectrects) per impostare il controllo sulla nuova dimensione.

I controlli che supportano solo [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) o [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) non supportano la memorizzazione nella cache tramite [**IOleCache2**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache2) perché la cache richiede il supporto [**per IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage). Tuttavia, questi controlli devono consentire al client di eseguire il rendering del controllo tramite [**IDataObject::GetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata) in modo che il client possa facoltativamente creare e gestire la propria cache dei dati di presentazione per il controllo.

I controlli usano il tipo HIMETRIC per le relative coordinate. Tuttavia, contenitori diversi possono usare sistemi di coordinate diversi. Il contenitore vuole ricevere le coordinate nel proprio sistema, ma il controllo non sa necessariamente quali coordinate sta usando il contenitore. Per comunicare correttamente, il controllo deve essere in grado di convertire i valori nelle coordinate del contenitore. Il contenitore fornisce un oggetto sito con il [**metodo IOleControlSite::TransformCoords.**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-transformcoords) Il controllo chiama prima questo metodo nel sito client del contenitore per convertire le coordinate nelle coordinate appropriate per il contenitore. Può quindi passare le coordinate convertite al contenitore.

I controlli possono chiamare [**IOleControlSite::LockInPlaceActive**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-lockinplaceactive) nell'oggetto sito del contenitore per impedire al contenitore di tentare di abbassare di livello il controllo dallo stato attivo sul posto. Abbassando di livello il controllo in questo modo, il controllo viene disattivato e la relativa finestra viene distrutta, quindi se il controllo deve mantenere la finestra per un periodo di tempo noto, può chiamare **LockInPlaceActive** per garantirne lo stato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[ActiveX Controlli](activex-controls.md)
</dt> </dl>

 

 




