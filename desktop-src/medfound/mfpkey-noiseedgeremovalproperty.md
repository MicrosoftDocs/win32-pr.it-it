---
description: Specifica se il codec deve tentare di rilevare i bordi dei fotogrammi rumorosi e rimuoverli.
ms.assetid: fdb4f3a8-1447-4e1e-a208-0f9b717f7626
title: MFPKEY_NOISEEDGEREMOVAL proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 128ab89cd12c31186cf99e0c01454986bfe950a3d0a68b6196db6df205dea02a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118242558"
---
# <a name="mfpkey_noiseedgeremoval-property"></a>Proprietà MFPKEY \_ NOISEEDGEREMOVAL

Specifica se il codec deve tentare di rilevare i bordi dei fotogrammi rumorosi e rimuoverli.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCNoiseEdgeRemoval

## <a name="data-type"></a>Tipo di dati

VT \_ BOOL

## <a name="default-value"></a>Valore predefinito

FALSE

## <a name="remarks"></a>Commenti

Un bordo cornice rumoroso è in genere i dati vbi (Vertical Blanking Interval) da un frame di trasmissione tv. VBI è le prime 21 righe di analisi del frame tv. Queste righe di analisi non contengono dati video, ma dati sulla trasmissione. Quando un segnale televisivo viene registrato da una scheda di acquisizione, l'interfaccia VBI viene in genere rimossa dal frame. Il rilevamento e la correzione dei bordi rumorosi eseguiti dal codec possono correggere solo un bordo con tre o meno righe di disturbo. Se il video acquisito contiene più di tre linee rumorose, si verifica un problema con l'hardware usato per acquisire il video.

Se il codec è impostato per rimuovere i bordi rumorosi, duplica le linee adiacenti al bordo rumoroso per riempire il frame.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 




