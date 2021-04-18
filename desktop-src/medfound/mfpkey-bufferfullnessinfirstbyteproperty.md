---
description: Specifica se il flusso di bit video codificato contiene un valore di completezza del buffer con ogni fotogramma chiave.
ms.assetid: 5574ee3c-ccb3-4ff6-8280-efe5626e6dd6
title: Proprietà MFPKEY_BUFFERFULLNESSINFIRSTBYTE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10fbcdb6306faeb7481f1cc7be20088ff0cedd5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318401"
---
# <a name="mfpkey_bufferfullnessinfirstbyte-property"></a>\_Proprietà BUFFERFULLNESSINFIRSTBYTE di MFPKEY

Specifica se il flusso di bit video codificato contiene un valore di completezza del buffer con ogni fotogramma chiave.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCBufferFullnessInFirstByte

## <a name="data-type"></a>Tipo di dati

\_bool VT

## <a name="remarks"></a>Commenti

Prima di ottenere questo valore, è necessario impostare un tipo di output.

È possibile ottenere il valore di questa proprietà utilizzando [IWMCodecProps:: GetCodecProp](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop). Se si usa **IPropertyBag**, è innanzitutto necessario impostare il valore fourcc del formato compresso desiderato con la proprietà [MFPKEY \_ fourcc](mfpkey-fourccproperty.md) .

La completezza del buffer nel primo byte di tutti i fotogrammi chiave consente di determinare le dimensioni del buffer necessarie per la concatenazione di flussi video compressi.

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

 

 




