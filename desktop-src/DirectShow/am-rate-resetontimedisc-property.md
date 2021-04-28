---
description: 'AM_RATE_ResetOnTimeDisc proprietà : si applica a Windows Vista e versioni successive.'
ms.assetid: 3e342219-341e-49a2-9f8f-4188dd7bf719
title: AM_RATE_ResetOnTimeDisc proprietà (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e867bff1f344e80ffd06c9c40276515f2cd4920c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096609"
---
# <a name="am_rate_resetontimedisc-property"></a>Am \_ RATE \_ ResetOnTimeDisc - proprietà

Si applica a Windows Vista e versioni successive.

Questa proprietà esegue una query se il decodificatore risincronizza i timestamp di output nei timestamp di input quando il decodificatore riceve un campione con il flag di discontinuità.

Si tratta di una proprietà di lettura/scrittura.



| Label | Valore |
|-------------------|-------------------------------|
| GUID set di proprietà | AM \_ KSPROPSETID \_ TSRateChange |
| ID proprietà       | AM \_ RATE \_ ResetOnTimeDisc     |
| Tipo di dati         | **Dword**                     |



 

## <a name="remarks"></a>Commenti

Questa proprietà supporta le modifiche della velocità uniforme. Se il valore di questa proprietà è **TRUE** e il decodificatore riceve un esempio di input con il flag AM \_ SAMPLE TIMEDISCONTINUITY, il frame decodificato deve avere lo stesso timestamp del \_ frame di input.

Per recuperare il flag AM \_ SAMPLE \_ TIMEDISCONTINUITY, chiamare [**IMediaSample2::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) nell'esempio. Il flag viene impostato nel **membro dwSampleFlags** della [**struttura AM \_ SAMPLE2 \_ PROPERTIES.**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties)

Per altre informazioni, vedere [Miglioramenti della riproduzione DVD in Windows Vista.](dvd-playback-enhancements-in-windows-vista.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dvdmedia.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Impostare le proprietà di modifica della frequenza**](rate-change-property-set.md)
</dt> </dl>

 

 




