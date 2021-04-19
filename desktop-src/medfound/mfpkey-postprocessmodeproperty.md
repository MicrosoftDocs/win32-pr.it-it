---
description: Specifica la modalità di post-elaborazione per il decodificatore.
ms.assetid: c6dab7f6-4a3e-45bb-b81c-5f4c39f9e954
title: Proprietà MFPKEY_POSTPROCESSMODE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4002deae63f1bdaea09ca31dd95bfec1cb594fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333092"
---
# <a name="mfpkey_postprocessmode-property"></a>\_Proprietà POSTPROCESSMODE di MFPKEY

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
| 1     | il decodificatore della esegue un deblocco rapido.                                                 |
| 2     | Il decodificatore esegue il deblocco completo.                                                  |
| 3     | Il decodificatore esegue una rapida deblocco e una chiamata.                                    |
| 4     | Il decodificatore esegue il blocco e la dechiamata completi.                                    |



 

Poiché il valore di questa proprietà va da 0 a 4, la complessità di decodifica, l'utilizzo delle risorse della CPU e la qualità dell'immagine aumentano.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows Vista o Windows 7<br/>                                                   |
| Intestazione<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




