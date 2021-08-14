---
description: Specifica se il flusso di bit video codificato contiene un valore di completezza del buffer con ogni fotogramma chiave.
ms.assetid: 5574ee3c-ccb3-4ff6-8280-efe5626e6dd6
title: MFPKEY_BUFFERFULLNESSINFIRSTBYTE proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 087b505680dfc3c51fe2cb50cdae76a425ca2ff5798356e9893794d47a7e22e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118243000"
---
# <a name="mfpkey_bufferfullnessinfirstbyte-property"></a>Proprietà MFPKEY \_ BUFFERFULLNESSINFIRSTBYTE

Specifica se il flusso di bit video codificato contiene un valore di completezza del buffer con ogni fotogramma chiave.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCBufferFullnessInFirstByte

## <a name="data-type"></a>Tipo di dati

VT \_ BOOL

## <a name="remarks"></a>Commenti

È necessario impostare un tipo di output prima di ottenere questo valore.

È possibile ottenere il valore di questa proprietà [usando IWMCodecProps::GetCodecProp](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop). Se si usa **IPropertyBag,** è necessario innanzitutto impostare il valore FOURCC del formato compresso desiderato con la [proprietà MFPKEY \_ FOURCC.](mfpkey-fourccproperty.md)

La presenza del livello di completezza del buffer nel primo byte di tutti i fotogrammi chiave consente di determinare le dimensioni del buffer necessarie per la concatenazione di flussi video compressi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 




