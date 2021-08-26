---
description: Specifica il numero di thread che verranno utilizzati dal codificatore.
ms.assetid: 2f463cba-2512-455d-9ce1-8797682d4d67
title: MFPKEY_NUMTHREADS proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ac8b6ec040ba07a2e38b1e9d8e2df6cf0fcbfcdbba14481e9b50379ecc10df5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953911"
---
# <a name="mfpkey_numthreads-property"></a>Proprietà NUMTHREADS MFPKEY \_

Specifica il numero di thread che verranno utilizzati dal codificatore.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCNumThreads

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

1

## <a name="remarks"></a>Commenti

Questo valore è progettato per dividere la codifica in più thread per sfruttare i vantaggi dei computer con più processori. La suddivisione delle attività di codifica in più thread può causare una lieve riduzione della qualità rispetto a un singolo thread.

Per il codificatore video (wmvencod.dll) rilasciato con Windows XP e Windows Vista, questa proprietà deve essere impostata su 1, 2 o 4. Gli altri valori verranno arrotondati per ese.

Per il codificatore video (wmvencod.dll) rilasciato con Windows 7, questa proprietà deve essere impostata su 1, 2, 4 o 8. Gli altri valori verranno arrotondati per ese.

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

 

 




