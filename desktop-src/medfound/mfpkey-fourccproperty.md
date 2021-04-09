---
description: Specifica il FOURCC che identifica il codificatore che si desidera utilizzare.
ms.assetid: c03da576-cb58-4686-af6f-9575520c759c
title: Proprietà MFPKEY_FOURCC (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbe852ad0d7113717428bdd832b8f327f8d0b6e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967170"
---
# <a name="mfpkey_fourcc-property"></a>\_Proprietà FourCC di MFPKEY

Specifica il FOURCC che identifica il codificatore che si desidera utilizzare.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCFOURCC

## <a name="data-type"></a>Tipo di dati

VT \_ I4 (valore fourcc)

## <a name="remarks"></a>Commenti

È necessario impostare questo valore prima di recuperare i valori per le proprietà seguenti utilizzando **IPropertyBag** o **IPropertyStore**:

-   [\_BUFFERFULLNESSINFIRSTBYTE MFPKEY](mfpkey-bufferfullnessinfirstbyteproperty.md)
-   [\_PASSESRECOMMENDED MFPKEY](mfpkey-passesrecommendedproperty.md)

Usare [**IWMCodecProps:: GetCodecProp**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop) per recuperare i valori delle proprietà dipendenti da FourCC elencate in precedenza. Quando si usa **GetCodecProp**, non è necessario impostare **MFPKEY \_ fourcc**.

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

 

 




