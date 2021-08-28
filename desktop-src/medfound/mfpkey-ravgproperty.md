---
description: Specifica la velocità in bit media, in bit al secondo, usata per la codifica VBR (Variable-Bit Rate) a 2 passi.
ms.assetid: 88a1888f-7bfb-4e24-9d48-92cfde02a14f
title: MFPKEY_RAVG proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90fd5435498a8a0c247d9363f02e2e767b46c5ab17ce36cc5a41feab54ed5277
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113291"
---
# <a name="mfpkey_ravg-property"></a>Proprietà MFPKEY \_ RAVG

Specifica la velocità in bit media, in bit al secondo, usata per la codifica VBR (Variable-Bit Rate) a 2 passi.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCAvgBitrate

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="remarks"></a>Commenti

In VBR vincolato e non vincolato, questo valore è la velocità in bit media per tutta la durata del contenuto.

È necessario impostare questo valore per entrambe le modalità di codifica VBR a due passi. Dopo aver iniziato a elaborare gli esempi, non è necessario eseguire una query per questo valore fino a quando non è stata completata la codifica del flusso. Il codificatore interpreta una richiesta per questo valore come un segnale che la sessione di codifica è finita; L'esempio successivo che si elabora viene considerato come l'inizio di una nuova sessione.

Questa proprietà può essere letta anche alla fine di una sessione di codifica VBR a 1 passaggio.

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

 

 




