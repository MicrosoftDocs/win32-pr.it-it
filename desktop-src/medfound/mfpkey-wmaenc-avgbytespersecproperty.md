---
description: Specifica i byte medi al secondo in un flusso audio VBR (Variable-Bit Rate) basato sulla qualità.
ms.assetid: dcee969a-617e-4045-a468-8158afb06356
title: MFPKEY_WMAENC_AVGBYTESPERSEC proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfadc41e9f2c9f4410bc84c6d8bf23f30c559b96c83abba80beb719e8ccb8eba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953301"
---
# <a name="mfpkey_wmaenc_avgbytespersec-property"></a>Proprietà MFPKEY \_ WMAENC \_ AVGBYTESPERSEC

Specifica i byte medi al secondo in un flusso audio VBR (Variable-Bit Rate) basato sulla qualità.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMACAvgBytesPerSecond

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="remarks"></a>Commenti

È possibile ottenere questo valore dal decodificatore dopo la codifica del flusso.

Questo valore è richiesto dal decodificatore audio per decomprimere correttamente il contenuto.

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

 

 




