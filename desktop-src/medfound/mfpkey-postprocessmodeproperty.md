---
description: Specifica la modalità di post-elaborazione per il decodificatore.
ms.assetid: c6dab7f6-4a3e-45bb-b81c-5f4c39f9e954
title: MFPKEY_POSTPROCESSMODE proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dce916d0b74c25ae2a57a43acde128ce8c45e7eb42860c3d7a2f129ea2d5b3c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973550"
---
# <a name="mfpkey_postprocessmode-property"></a>Proprietà MFPKEY \_ POSTPROCESSMODE

Specifica la modalità di post-elaborazione per il decodificatore.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

**g \_ wszWMVCForcePostProcessMode**

## <a name="data-type"></a>Tipo di dati

**VT \_ I4**

## <a name="remarks"></a>Commenti

Impostare questa proprietà su uno dei valori seguenti.



| Valore | Significato                                                                                |
|-------|----------------------------------------------------------------------------------------|
| -1    | Il decodificatore imposta la modalità di post-elaborazione in modo adattivo in base alle risorse della CPU disponibili. |
| 0     | Il decodificatore non esegue alcuna post-elaborazione.                                               |
| 1     | fIl decodificatore esegue la deblocking veloce.                                                 |
| 2     | Il decodificatore esegue il deblocking completo.                                                  |
| 3     | Il decodificatore esegue la deblocking e la derivazione veloci.                                    |
| 4     | Il decodificatore esegue il deblocking completo e la derivazione.                                    |



 

Con il valore di questa proprietà compreso tra 0 e 4, aumentano la complessità di decodifica, l'uso delle risorse della CPU e la qualità dell'immagine.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows Vista o Windows 7<br/>                                                   |
| Intestazione<br/> | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 




