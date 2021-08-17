---
description: Specifica il livello di risparmio energia di un decodificatore video.
ms.assetid: 7e2ff8be-b21f-4833-a165-0112d4220677
title: Proprietà AVDecVideoSWPowerLevel (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7c362e066a16e333cda402704a720b5e1b0b8534f1b56536d32009e6fa29663
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117824221"
---
# <a name="avdecvideoswpowerlevel-property"></a>AVDecVideoSWPowerLevel - proprietà

Specifica il livello di risparmio energia di un decodificatore video.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVDecVideoSWPowerLevel**

## <a name="property-value"></a>Valore proprietà

L'intervallo di valori possibili \[ è 0..100, \] inclusi, con il significato seguente.



| Valore | Descrizione                 |
|-------|-----------------------------|
| 0     | Ottimizzare per la durata della batteria.  |
| 100   | Ottimizzare per la qualità video. |



 

[**L'enumerazione eAVDecVideoSWPowerLevel**](/windows/desktop/api/codecapi/ne-codecapi-eavdecvideoswpowerlevel) definisce alcune costanti specifiche all'interno di questo intervallo.

## <a name="remarks"></a>Commenti

È possibile impostare questa proprietà durante la riproduzione per modificare il livello di risparmio energia.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[ app desktop \| UWP\]<br/>                     |
| Server minimo supportato<br/> | app \[ desktop UWP di Windows 2000 Server \|\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà dell'API Codec](codec-api-properties.md)
</dt> <dt>

[**Interfaccia ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




