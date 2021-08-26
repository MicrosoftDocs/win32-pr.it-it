---
description: Specifica una larghezza di fotogramma intermedia per il video codificato.
ms.assetid: 805bd587-31af-49b8-b5ab-2dcf2a3f81c5
title: MFPKEY_FORCEFRAMEWIDTH proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8d04e30f5fd5d2ecc7055553e17eaf86199b62be8d3dd861b9f82246947212f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939837"
---
# <a name="mfpkey_forceframewidth-property"></a>Proprietà MFPKEY \_ FORCEFRAMEWIDTH

Specifica una larghezza di fotogramma intermedia per il video codificato.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCForceFrameWidth

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="remarks"></a>Commenti

È possibile impostare questo valore e la proprietà [MFPKEY \_ FORCEFRAMEHEIGHT](mfpkey-forceframeheightproperty.md) per forzare il codificatore a codificare il flusso video con dimensioni del fotogramma inferiori alle dimensioni dei fotogrammi di input o di output. Una volta decodificato, il video verrà ridimensionato alla risoluzione di input originale.

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

 

 




