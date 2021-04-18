---
description: Specifica il metodo di costo utilizzato dal codec per determinare la modalità di macroblocco da utilizzare.
ms.assetid: 2ba9b943-0daa-40c1-87ea-2fa647fb7095
title: Proprietà MFPKEY_MACROBLOCKMODECOSTMETHOD (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 289219300a79c67565891c48cec848851c17bd7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310624"
---
# <a name="mfpkey_macroblockmodecostmethod-property"></a>\_Proprietà MACROBLOCKMODECOSTMETHOD di MFPKEY

Specifica il metodo di costo utilizzato dal codec per determinare la modalità di macroblocco da utilizzare.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCMacroblockModeCostMethod

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

0

## <a name="remarks"></a>Commenti

Questa proprietà può essere impostata su uno dei valori seguenti.



| Valore | Metodo utilizzato                                                                                            |
|-------|--------------------------------------------------------------------------------------------------------|
| 0     | TRISTE/Hadamard. Questa opzione consente di configurare il codec in modo da usare solo la distorsione durante il calcolo dei costi.             |
| 1     | Costo RD. Questa opzione consente di configurare il codec per tenere conto della velocità e della distorsione durante il calcolo dei costi. |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[\_MOTIONMATCHMETHOD MFPKEY](mfpkey-motionmatchmethodproperty.md)
</dt> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




