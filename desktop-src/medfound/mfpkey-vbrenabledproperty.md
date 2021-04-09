---
description: Specifica se il codificatore utilizza la codifica con velocità in bit variabile (VBR).
ms.assetid: e6826802-99b7-4a38-9b58-8a9cb8b753fb
title: Proprietà MFPKEY_VBRENABLED (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab9061abcc6ac7d7338b63eb5a7cd1a13ad22bf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880773"
---
# <a name="mfpkey_vbrenabled-property"></a>\_Proprietà VBRENABLED di MFPKEY

Specifica se il codificatore utilizza la codifica con velocità in bit variabile (VBR). Lettura/scrittura.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

**g \_ wszWMVCVBREnabled**, **g \_ wszWMCPAudioVBRSupported**

## <a name="data-type"></a>Tipo di dati

**\_bool VT**

## <a name="default-value"></a>Valore predefinito

**VARIANTE \_ false**

## <a name="remarks"></a>Commenti

Questo valore deve essere impostato su **Variant \_ true** per qualsiasi altra proprietà VBR che verrà usata dal codec.

Dopo aver impostato questo valore su **Variant \_ true** nel codificatore audio, i tipi di output recuperati usando il metodo [**IMediaObject:: GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype) sono tipi VBR.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MFPKEY \_ vincolato \_ VBRQUALITY enumerato \_**](mfpkey-constrain-enumerated-vbrqualityproperty.md)
</dt> <dt>

[**MFPKEY \_ desired \_ VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md)
</dt> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
