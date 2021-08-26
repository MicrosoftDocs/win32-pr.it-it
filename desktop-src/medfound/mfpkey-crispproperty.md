---
description: Specifica una rappresentazione numerica del compromesso tra l'uniformità del movimento e la qualità dell'immagine dell'output del codec.
ms.assetid: 63915450-71c5-4097-91d7-5817249c1cda
title: MFPKEY_CRISP proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 177ae5e9d1c8a9aba359000e04483c8e45c44f823c9db924155dd5ef3d5989a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954261"
---
# <a name="mfpkey_crisp-property"></a>Proprietà MFPKEY \_ CRISP

Specifica una rappresentazione numerica del compromesso tra l'uniformità del movimento e la qualità dell'immagine dell'output del codec.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCCrisp

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

75

## <a name="remarks"></a>Commenti

Questo valore intero può essere compreso tra 0 e 100. Più alto è il valore, più il codec ottimizza la codifica per la qualità dell'immagine dei singoli fotogrammi, riducendo in genere l'uniformità del movimento.

Questa proprietà deve essere impostata solo per la codifica CBR (Constant-Bit-Rate). Le ottimizzazioni per la codifica vbr (variable-bit-rate) funzionano in modo diverso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 




