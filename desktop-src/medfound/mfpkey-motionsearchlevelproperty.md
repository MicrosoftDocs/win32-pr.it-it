---
description: Specifica il modo in cui le informazioni sui colori vengono usate nelle operazioni di ricerca di movimento.
ms.assetid: a625b103-0a55-4268-a01a-6a464a56fec2
title: Proprietà MFPKEY_MOTIONSEARCHLEVEL (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 231c2c0ae70466d41f4bf348ec47ee0a74cb135b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049838"
---
# <a name="mfpkey_motionsearchlevel-property"></a>\_Proprietà MOTIONSEARCHLEVEL di MFPKEY

Specifica il modo in cui le informazioni sui colori vengono usate nelle operazioni di ricerca di movimento.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCMotionSearchLevel

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

0

## <a name="remarks"></a>Commenti

Questa proprietà può essere impostata su uno dei valori seguenti.



| Valore | Informazioni video utilizzate                           |
|-------|--------------------------------------------------|
| 0     | Solo luminanza.                                       |
| 1     | Luma con Chroma integer più vicino.                |
| 2     | Luminanza con crominanza vera.                           |
| -1    | Macroblocco-Adaptive con Chroma true.            |
| -2    | Macroblocco-Adaptive con Chroma integer più vicino. |



 

Per impostazione predefinita, il codec esegue la ricerca di movimento solo nel canale luma. Includere le informazioni sulla crominanza nella stima del movimento può migliorare significativamente la qualità del video codificato. La ricerca di movimento con luma e la Croma vera produrrà la migliore qualità del video, ma con il costo massimo delle prestazioni. Le due modalità dinamiche (-1 e-2) e la Luma con la modalità Chroma con valori integer più vicino forniranno compromessi ragionevoli tra qualità e prestazioni.

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

 

 




