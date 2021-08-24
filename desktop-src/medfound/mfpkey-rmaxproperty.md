---
description: Specifica la velocità in bit massima, in bit al secondo, usata per la riproduzione con velocità in bit variabile a 2 passi vincolata.
ms.assetid: 51f161d2-f832-48d5-8f16-861e2a98a7f7
title: MFPKEY_RMAX proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e80f679d0ed1213a54a4f22bc5d8bfc79f41b93fa05c446c8b6ed0f589183b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119398401"
---
# <a name="mfpkey_rmax-property"></a>Proprietà MFPKEY \_ RMAX

Specifica la velocità in bit massima, in bit al secondo, usata per la riproduzione con velocità in bit variabile a 2 passi vincolata.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCMaxBitrate

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

Nessuna impostazione predefinita.

## <a name="remarks"></a>Commenti

Questo valore rappresenta la velocità in bit massima per la riproduzione. Il valore [di MFPKEY \_ BMAX](mfpkey-bmaxproperty.md) viene usato per descrivere il buffer in termini di velocità in bit. In effetti, vbr vincolato è simile alla velocità in bit costante (CBR) usando questo valore come velocità in bit. Tuttavia, un flusso VBR vincolato può essere riprodotto a una velocità in bit inferiore, purché il buffer sia aumentato.

È necessario impostare questo valore per la codifica VBR a due passi con limiti di picco. Dopo aver iniziato l'elaborazione degli esempi, è necessario eseguire una query per questo valore solo dopo aver completato la codifica del flusso. Il codificatore interpreta una richiesta per questo valore come un segnale che la sessione di codifica è stata consa. L'esempio successivo che si elabora viene considerato come l'inizio di una nuova sessione.

In genere, questo valore è da due a tre volte maggiore del valore di [MFPKEY \_ RAVG](mfpkey-ravgproperty.md).

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

 

 




