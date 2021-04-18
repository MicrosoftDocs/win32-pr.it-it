---
description: Specifica il livello di risparmio energia di un decodificatore video.
ms.assetid: 7e2ff8be-b21f-4833-a165-0112d4220677
title: Proprietà AVDecVideoSWPowerLevel (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1196c45cf038085856b1d63a5cd3a1c7dc350d0d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304167"
---
# <a name="avdecvideoswpowerlevel-property"></a>Proprietà AVDecVideoSWPowerLevel

Specifica il livello di risparmio energia di un decodificatore video.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVDecVideoSWPowerLevel**

## <a name="property-value"></a>Valore proprietà

L'intervallo dei valori possibili è \[ 0.. 100 \] , inclusivo, con il significato seguente.



| Valore | Descrizione                 |
|-------|-----------------------------|
| 0     | Ottimizza per la durata della batteria.  |
| 100   | Ottimizza per la qualità del video. |



 

L'enumerazione [**eAVDecVideoSWPowerLevel**](/windows/desktop/api/codecapi/ne-codecapi-eavdecvideoswpowerlevel) definisce alcune costanti specifiche all'interno di questo intervallo.

## <a name="remarks"></a>Commenti

È possibile impostare questa proprietà durante la riproduzione per modificare il livello di risparmio energia.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App UWP di Windows 2000 Professional \[ desktop apps \|\]<br/>                     |
| Server minimo supportato<br/> | App desktop di Windows 2000 Server \[ \| UWP\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapis. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà dell'API codec](codec-api-properties.md)
</dt> <dt>

[**Interfaccia ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




