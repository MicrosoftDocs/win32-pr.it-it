---
description: Specifica il metodo da usare per la corrispondenza di movimento.
ms.assetid: 75bbc189-3092-4813-9f45-54e8e48b05cd
title: Proprietà MFPKEY_MOTIONMATCHMETHOD (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09496e714633dd394f55122b7461f29a2daa3656
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967168"
---
# <a name="mfpkey_motionmatchmethod-property"></a>\_Proprietà MOTIONMATCHMETHOD di MFPKEY

Specifica il metodo da usare per la corrispondenza di movimento.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCMotionMatchMethod

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

0

## <a name="remarks"></a>Commenti

Questa proprietà può essere impostata su uno dei valori seguenti.



| Valore | Metodo utilizzato                       |
|-------|-----------------------------------|
| 0     | somma delle differenze assolute (SAD) |
| 1     | Hadamard                          |
| -1    | Macroblocco-Adaptive.              |



 

La somma delle differenze assolute (SAD) è un metodo più veloce ma meno accurato rispetto alla trasformazione Hadamard. La trasformazione Hadamard è più accurata ma a elevato utilizzo di calcolo. La modalità adattiva macroblocco fornisce un ragionevole compromesso tra i due metodi scegliendo dinamicamente tra le due trasformazioni, selezionando la trasformazione Hadamard solo quando appropriato.

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

 

 




