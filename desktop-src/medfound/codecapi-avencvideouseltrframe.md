---
description: Specifica che il frame corrente viene codificato utilizzando uno o più fotogrammi di ltr.
ms.assetid: 51FD6E36-9CDF-4005-942F-7A92CA706F38
title: CODECAPI_AVEncVideoUseLTRFrame proprietà (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c438a4e6e2656c5e952062d9e3c1c0000899f2c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473157"
---
# <a name="codecapi_avencvideouseltrframe-property"></a>CODECAPI \_ AVEncVideoUseLTRFrame - proprietà

Specifica che il frame corrente viene codificato utilizzando uno o più fotogrammi di ltr.

## <a name="data-type"></a>Tipo di dati

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVEncVideoUseLTRFrame**

## <a name="property-value"></a>Valore proprietà

Il valore di questo controllo include due campi, in cui ogni campo ha 16 bit.




| valore | Significato | 
|-------|---------|
| <span id="The_first_field"></span><span id="the_first_field"></span><span id="THE_FIRST_FIELD"></span><dl><dt><strong>Primo campo</strong></dt><dt>Bits[0..15]</dt></dl> | Indica quali fotogrammi ditr sono consentiti per la codifica del frame corrente. <br /><strong>Codificatori H.264/AVC:</strong><br /> Si tratta di una bitmap che indica quali fotogrammi LTR possono essere usati come riferimento per questo frame. Il bit meno significativo corrisponde all'indice LTR 0, il secondo bit meno significativo corrisponde all'indice LTR 1 e così via.<br /> Questo valore non deve essere 0.<br /> L'indice più alto specificato da questo valore non deve essere maggiore del numero massimo di fotogrammi LTR specificato nella proprietà CODECAPI_AVEncVideoLTRBufferControl <a href="codecapi-avencvideoltrbuffercontrol.md">minore</a> di uno.<br /> | 
| <span id="The_second_field"></span><span id="the_second_field"></span><span id="THE_SECOND_FIELD"></span><dl><dt><strong>Il secondo campo</strong></dt><dt>Bits[16..31]</dt></dl> | Flag che indica se sono necessarie limitazioni aggiuntive per la codifica dei fotogrammi successivi. <br /><strong>Codificatori H.264/AVC:</strong><br /> 1 è l'unico valore valido per questo campo. Tutti gli altri valori non sono validi e sono riservati per un uso futuro.<br /> Quando il flag è 1, il codificatore deve codificare i fotogrammi successivi in ordine di codifica in base ai vincoli seguenti:<br /><ul><li>Non userà i fotogrammi di riferimento a breve termine in ordine di codifica precedente al frame corrente o alla codifica futura nell'ordine di codifica.</li><li>Non deve usare i fotogrammi LTR non descritti dal controllo CODECAPI_AVEncVideoUseLTRFrame recente.</li><li>Può usare i fotogrammi LTR aggiornati dopo il frame corrente.</li></ul> | 




 

## <a name="remarks"></a>Commenti

**Codificatori H.264/AVC:**

Questa proprietà non deve essere chiamata se è stata emessa una chiamata in sospeso per usare un fotogramma LTR usando la proprietà CODECAPI AVEncVideoUseLTRFrame e il codificatore non ha ancora generato un frame che ha usato la durata \_ (LTR). In altre parole, il codificatore non deve accodarsi le richieste CODECAPI \_ AVEncVideoUseLTRFrame.

Se viene inviata una richiesta CODECAPI \_ AVEncVideoUseLTRFrame mentre un'altra richiesta CODECAPI AVEncVideoUseLTRFrame è ancora in sospeso, la richiesta precedente deve essere \_ eliminata.

La chiamata a CODECAPI AVEncVideoUseLTRFrame su un frame di livello non di base è valida e deve essere applicata al frame del livello non di base, senza ritardi in un frame del livello \_ di base.

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 app desktop \| app UWP\]<br/>                                   |
| Server minimo supportato<br/> | Windows Server 2012 App desktop R2 \[ \| app UWP\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 




