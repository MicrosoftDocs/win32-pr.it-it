---
description: Specifica un'altezza del fotogramma intermedia per il video codificato.
ms.assetid: 7382ec31-6d59-4e8c-94eb-804786074038
title: MFPKEY_FORCEFRAMEHEIGHT proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6e3d423fe96173829b31a889764d5423db88b5c882d853b3e0f770d17dd4691
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119463451"
---
# <a name="mfpkey_forceframeheight-property"></a>Proprietà MFPKEY \_ FORCEFRAMEHEIGHT

Specifica un'altezza del fotogramma intermedia per il video codificato.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCForceFrameHeight

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="remarks"></a>Commenti

È possibile impostare questo valore e la proprietà [MFPKEY \_ FORCEFRAMEWIDTH](mfpkey-forceframewidthproperty.md) per forzare il codificatore a codificare il flusso video con dimensioni del fotogramma inferiori alle dimensioni dei fotogrammi di input o di output. Una volta decodificato, il video verrà ridimensionato alla risoluzione di input originale.

Le dimensioni valide del frame su entrambi gli assi sono da 2 a 8192 pixel. Le dimensioni del frame devono essere divisibile per 2.

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

 

 




