---
description: Specifica il numero massimo di frame di riferimento a lungo termine controllati dall'applicazione.
ms.assetid: C34AD867-5F94-4414-A282-ECC392678635
title: CODECAPI_AVEncVideoLTRBufferControl proprietà (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cca2e24e8295969609ba325a2abf24be76fb07c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481927"
---
# <a name="codecapi_avencvideoltrbuffercontrol-property"></a>PROPRIETÀ CODECAPI \_ AVEncVideoLTRBufferControl

Specifica il numero massimo di frame di riferimento a lungo termine controllati dall'applicazione.

## <a name="data-type"></a>Tipo di dati

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVEncVideoLTRBufferControl**

## <a name="property-value"></a>Valore proprietà

Il valore di questo controllo include due campi, in cui ogni campo ha 16 bit.




| valore | Significato | 
|-------|---------|
| <span id="The_first_field"></span><span id="the_first_field"></span><span id="THE_FIRST_FIELD"></span><dl><dt><strong>Il primo campo</strong></dt><dt>Bits[0..15]</dt></dl> | Numero di fotogrammi ATR controllati dall'applicazione.<br /><strong>Codificatori H.264/AVC:</strong><br /> Supponendo che il valore sia N e N sia diverso da zero, in ogni frame IDR il codificatore deve contrassegnare automaticamente i fotogrammi che segue il frame IDR (e incluso il frame IDR) come fotogrammi LTR purché si applino tutti e 3 i seguenti:<ul><li>Il frame non è già impostato per essere contrassegnato come frame di riferimento a lungo termine.</li><li>Il frame è un frame del livello di base. Ad esempio, l'elemento <strong>temporal_id</strong> uguale a 0.</li><li>Il numero di fotogrammi attualmente contrassegnati come LTR è minore di N.</li></ul><br /> | 
| <span id="The_second_field"></span><span id="the_second_field"></span><span id="THE_SECOND_FIELD"></span><dl><dt><strong>Il secondo campo</strong></dt><dt>Bits[16..31]</dt></dl> | Modalità di attendibilità del controllo LTR.<br /><strong>Codificatori H.264/AVC:</strong><br /> 1 (Attendibilità fino a) indica che il codificatore può usare un frame LTR a meno che l'app non lo invalidi in modo esplicito tramite il <a href="codecapi-avencvideouseltrframe.md">CODECAPI_AVEncVideoUseLTRFrame</a> controllo. <br /> Altri valori non sono validi e sono riservati per un uso futuro.<br /> | 




 

## <a name="remarks"></a>Commenti

Si tratta di un'API statica.

Il valore predefinito deve essere 0

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 app desktop \| app UWP\]<br/>                                   |
| Server minimo supportato<br/> | Windows Server 2012 App \[ UWP per app desktop \| R2\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 




