---
description: Specifica se il codec utilizzerà il filtro rumore durante la codifica.
ms.assetid: 9e099378-bb77-4dca-9171-7fe58e0139de
title: Proprietà MFPKEY_DENOISEOPTION (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7f318e294f69095758fe300fce19043c23cf376
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310636"
---
# <a name="mfpkey_denoiseoption-property"></a>\_Proprietà DENOISEOPTION di MFPKEY

Specifica se il codec utilizzerà il filtro rumore durante la codifica.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCDenoiseOption

## <a name="data-type"></a>Tipo di dati

\_bool VT

## <a name="default-value"></a>Valore predefinito

FALSE

## <a name="remarks"></a>Commenti

Il filtro rumore può migliorare la qualità delle origini video rumorose, ad esempio film che contengono un numero elevato di granularità o video in basso. Questo filtro può essere usato negli scenari di codifica live in cui la pre-elaborazione esterna non è un'opzione.

Questo filtro deve essere disabilitato per le origini video pulite perché può ridurre la qualità dell'immagine quando la qualità è ottima per iniziare.

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

 

 




