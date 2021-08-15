---
description: Specifica il metodo da utilizzare per la corrispondenza del movimento.
ms.assetid: 75bbc189-3092-4813-9f45-54e8e48b05cd
title: MFPKEY_MOTIONMATCHMETHOD proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bec0604acc7dc0634be296e5097c3594dc74e5ceb7bdb7563b48a164cd13b164
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119355731"
---
# <a name="mfpkey_motionmatchmethod-property"></a>Proprietà MFPKEY \_ MOTIONMATCHMETHOD

Specifica il metodo da utilizzare per la corrispondenza del movimento.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCMotionMatchMethod

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

0

## <a name="remarks"></a>Commenti

Questa proprietà può essere impostata su uno dei valori seguenti.



| Valore | Metodo usato                       |
|-------|-----------------------------------|
| 0     | somma delle differenze assolute (SAD) |
| 1     | Hadamard                          |
| -1    | Macroblock-adaptive.              |



 

La somma delle differenze assolute è un metodo più veloce ma meno accurato rispetto alla trasformazione Hadamard. La trasformazione Hadamard è più accurata ma a elevato utilizzo di calcolo. La modalità macroblock-adattiva offre un compromesso ragionevole tra i due metodi scegliendo dinamicamente tra le due trasformazioni, selezionando la trasformazione Hadamard solo quando appropriato.

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

 

 




