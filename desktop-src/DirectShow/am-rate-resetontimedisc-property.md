---
description: Si applica a Windows Vista e versioni successive.
ms.assetid: 3e342219-341e-49a2-9f8f-4188dd7bf719
title: AM_RATE_ResetOnTimeDisc proprietà (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d465329c2c8de1a66f04a830d183b8cba88c0728
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910249"
---
# <a name="am_rate_resetontimedisc-property"></a>Am \_ RATE \_ ResetOnTimeDisc - proprietà

Si applica a Windows Vista e versioni successive.

Questa proprietà esegue una query per determinare se il decodificatore risincronizza i timestamp di output nei timestamp di input quando il decodificatore riceve un campione con il flag di discontinuità.

Si tratta di una proprietà di lettura/scrittura.



| Label | Valore |
|-------------------|-------------------------------|
| GUID set di proprietà | AM \_ KSPROPSETID \_ TSRateChange |
| ID proprietà       | AM \_ RATE \_ ResetOnTimeDisc     |
| Tipo di dati         | **Dword**                     |



 

## <a name="remarks"></a>Commenti

Questa proprietà supporta le modifiche della velocità uniforme. Se il valore di questa proprietà è **TRUE** e il decodificatore riceve un campione di input con il flag AM \_ SAMPLE TIMEDISCONTINUITY, il frame decodificato deve avere lo stesso timestamp del frame di \_ input.

Per recuperare il flag AM \_ SAMPLE \_ TIMEDISCONTINUITY, chiamare [**IMediaSample2::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) nell'esempio. Il flag è impostato nel **membro dwSampleFlags** della [**struttura AM \_ SAMPLE2 \_**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) PROPERTIES.

Per altre informazioni, vedere [DVD Playback Enhancements in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dvdmedia.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Rate Change Property Set**](rate-change-property-set.md)
</dt> </dl>

 

 




