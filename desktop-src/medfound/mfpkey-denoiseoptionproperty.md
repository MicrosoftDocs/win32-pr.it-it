---
description: Specifica se il codec userà il filtro del rumore durante la codifica.
ms.assetid: 9e099378-bb77-4dca-9171-7fe58e0139de
title: MFPKEY_DENOISEOPTION proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0483edbda1c2eb3ec929fb662fe4544cb09e7d43dfd1b30421d14eb06d2a365b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954071"
---
# <a name="mfpkey_denoiseoption-property"></a>Proprietà MFPKEY \_ DENOISEOPTION

Specifica se il codec userà il filtro del rumore durante la codifica.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCDenoiseOption

## <a name="data-type"></a>Tipo di dati

VT \_ BOOL

## <a name="default-value"></a>Valore predefinito

FALSE

## <a name="remarks"></a>Commenti

Il filtro del rumore può migliorare la qualità delle sorgenti video rumorose, ad esempio film contenenti molta granularità o video scattato in condizioni di scarsa luce. Questo filtro può essere usato in scenari di codifica live in cui la pre-elaborazione esterna non è un'opzione.

Questo filtro deve essere disabilitato per le origini video pulite perché può ridurre la qualità delle immagini quando la qualità è buona per iniziare.

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

 

 




