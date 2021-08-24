---
description: Specifica le dimensioni del flusso video quando viene decodificato.
ms.assetid: db7b101a-5ff8-4a62-b9e2-d05fcdc44b3d
title: Proprietà AVEncVideoDisplayDimension (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe4c6f6fbcd3f4746b4ee3b807ebb098c1bfce728c9c01614943f05351f5bb18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540721"
---
# <a name="avencvideodisplaydimension-property"></a>AVEncVideoDisplayDimension - proprietà

Specifica le dimensioni del flusso video quando viene decodificato.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVEncVideoDisplayDimension**

## <a name="property-value"></a>Valore proprietà

I 16 bit superiori del valore contengono la larghezza, in pixel. I 16 bit inferiori contengono l'altezza, in pixel.

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

 

 




