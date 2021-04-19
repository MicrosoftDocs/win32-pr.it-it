---
description: Specifica il numero di frame predittivi bidirezionali (fotogrammi B).
ms.assetid: 8bd95baa-c130-4616-8ab7-7d902162e4ed
title: Proprietà MFPKEY_NUMBFRAMES (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc3b0655a4a5e24b92f9699b198f10232de8edf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310622"
---
# <a name="mfpkey_numbframes-property"></a>\_Proprietà NUMBFRAMES di MFPKEY

Specifica il numero di frame predittivi bidirezionali (fotogrammi B).

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCNumBFrames

## <a name="data-type"></a>Tipo di dati

VT-I4

## <a name="default-value"></a>Valore predefinito

0

## <a name="remarks"></a>Commenti

Per impostazione predefinita, Windows Media Video 9 utilizza solo i fotogrammi (I-frame), noti anche come fotogrammi chiave o frame di ancoraggio, che sono frame completamente codificati e frame predittivi (fotogrammi P), che vengono codificati come differenza rispetto al frame I precedente. I frame B sono diversi dai fotogrammi P perché archiviano le differenze rispetto al frame precedente e le differenze rispetto al frame seguente.

Quando si configura il codec per l'utilizzo di fotogrammi B, verrà utilizzato il numero specificato di fotogrammi B tra ogni coppia di frame del tipo I o P.

Se, ad esempio, una sequenza di frame senza fotogrammi B è "IPPPPPPPPI", la stessa codifica di sequenza con due fotogrammi B sarà "IBBPBBPBBI".

Per la maggior parte del contenuto, uno o due fotogrammi B sono appropriati. Con una frequenza dati più elevata, un frame B è in genere la scelta ottimale. Sono raramente utili tre o più.

L'intervallo valido di valori per questa proprietà è compreso tra 0 e 7.

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

 

 




