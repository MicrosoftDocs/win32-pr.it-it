---
description: Specifica se il codec deve tentare di rilevare i bordi del frame disturbati e di rimuoverli.
ms.assetid: fdb4f3a8-1447-4e1e-a208-0f9b717f7626
title: Proprietà MFPKEY_NOISEEDGEREMOVAL (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30acd92bae7693d0714e42d6b4f832a521557bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227002"
---
# <a name="mfpkey_noiseedgeremoval-property"></a>\_Proprietà NOISEEDGEREMOVAL di MFPKEY

Specifica se il codec deve tentare di rilevare i bordi del frame disturbati e di rimuoverli.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCNoiseEdgeRemoval

## <a name="data-type"></a>Tipo di dati

\_bool VT

## <a name="default-value"></a>Valore predefinito

FALSE

## <a name="remarks"></a>Commenti

Il bordo di un frame fastidioso è in genere costituito dai dati VBI (Vertical Blanking Interval) di un frame della televisione broadcast. Il VBI è costituito dalle prime 21 righe di analisi del fotogramma televisivo. Queste righe di analisi non contengono dati video, ovvero contengono dati sulla trasmissione. Quando un segnale TV viene registrato da una scheda di acquisizione, il VBI viene in genere rimosso dal frame. Il rilevamento e la correzione dei bordi rumorosi eseguiti dal codec possono correggere solo un bordo con tre o meno righe di disturbo. Se il video acquisito contiene più di tre linee rumorose, si verifica un problema con l'hardware usato per acquisire il video.

Se il codec è impostato in modo da rimuovere i bordi rumorosi, le linee adiacenti al bordo rumoroso vengono duplicate per riempire il frame.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




