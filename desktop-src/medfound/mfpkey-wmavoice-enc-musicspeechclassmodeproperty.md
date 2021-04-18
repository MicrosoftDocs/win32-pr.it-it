---
description: Specifica la modalità del codec vocale.
ms.assetid: 8425cdab-e43c-41ca-9c20-09ab6a5f06f4
title: Proprietà MFPKEY_WMAVOICE_ENC_MusicSpeechClassMode (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9776c76f2a8863afe73626f5a2940de2c0ccb7cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309108"
---
# <a name="mfpkey_wmavoice_enc_musicspeechclassmode-property"></a>\_Proprietà MFPKEY WMAVOICE \_ enc \_ MusicSpeechClassMode

Specifica la modalità del codec vocale.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMACMusicSpeechClassMode

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

1

## <a name="remarks"></a>Commenti

Il valore 1 informa il codec che il contenuto è di sola voce, il valore 2 indica che il codec determina automaticamente la modalità e qualsiasi altro valore informa il codec per l'utilizzo della modalità musica.

Se la modalità automatica non codifica la voce mista e la musica in modo corretto, è possibile specificare la codifica per le singole sezioni del file usando la proprietà [MFPKEY \_ WMAVOICE \_ enc \_ EDL](mfpkey-wmavoice-enc-edlproperty.md) .

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

 

 




