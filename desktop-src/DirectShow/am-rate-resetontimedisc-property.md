---
description: Si applica a Windows Vista e versioni successive.
ms.assetid: 3e342219-341e-49a2-9f8f-4188dd7bf719
title: Proprietà AM_RATE_ResetOnTimeDisc (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5c26763d32513652a08d38b52bf6fb745d3d321
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330328"
---
# <a name="am_rate_resetontimedisc-property"></a>\_Proprietà rate \_ ResetOnTimeDisc

Si applica a Windows Vista e versioni successive.

Questa proprietà esegue una query se il decodificatore risincronizza i timestamp di output ai timestamp di input quando il decodificatore riceve un campione con il flag di discontinuità.

Si tratta di una proprietà di lettura/scrittura.



|                   |                               |
|-------------------|-------------------------------|
| GUID set di proprietà | \_TSRateChange KSPROPSETID \_ |
| ID proprietà       | \_Frequenza \_ ResetOnTimeDisc     |
| Tipo di dati         | **DWORD**                     |



 

## <a name="remarks"></a>Commenti

Questa proprietà supporta le modifiche alla frequenza uniforme. Se il valore di questa proprietà è **true** e il decodificatore riceve un esempio di input con il \_ flag AM Sample \_ TIMEDISCONTINUITY, il fotogramma decodificato deve avere lo stesso timestamp del frame di input.

Per recuperare il \_ flag TIMEDISCONTINUITY di esempio AM \_ , chiamare [**IMediaSample2:: GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) nell'esempio. Il flag viene impostato nel membro **dwSampleFlags** della struttura delle [**\_ \_ Proprietà SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) .

Per ulteriori informazioni, vedere [miglioramenti della riproduzione DVD in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dvdmedia. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Set di proprietà di modifica della frequenza**](rate-change-property-set.md)
</dt> </dl>

 

 




