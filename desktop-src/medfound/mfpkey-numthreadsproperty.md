---
description: Specifica il numero di thread che il codificatore utilizzerà.
ms.assetid: 2f463cba-2512-455d-9ce1-8797682d4d67
title: Proprietà MFPKEY_NUMTHREADS (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c93f6d38e3bb79bbb692f9bec1b1dc0edb232d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528663"
---
# <a name="mfpkey_numthreads-property"></a>\_Proprietà numThreads di MFPKEY

Specifica il numero di thread che il codificatore utilizzerà.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCNumThreads

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

1

## <a name="remarks"></a>Commenti

Questo valore è destinato a dividere la codifica in più thread per sfruttare i vantaggi dei computer con più processori. Suddividere le attività di codifica in più thread può causare una lieve riduzione della qualità rispetto a un singolo thread.

Per il codificatore video (wmvencod.dll) rilasciato con Windows XP e Windows Vista, questa proprietà deve essere impostata su 1, 2 o 4. Gli altri valori verranno arrotondati per difetto.

Per il codificatore video (wmvencod.dll) rilasciato con Windows 7, questa proprietà deve essere impostata su 1, 2, 4 o 8. Gli altri valori verranno arrotondati per difetto.

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

 

 




