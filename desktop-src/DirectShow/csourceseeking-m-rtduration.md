---
description: 'Durata del flusso. Per impostazione predefinita, il valore viene impostato sul valore della variabile membro CSourceSeeking:: m \_ rtStop.'
ms.assetid: a87b321e-3179-4485-969b-bf12cb634b43
title: 'Membro CSourceSeeking:: m_rtDuration (Ctlutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_rtDuration
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e188a29689a6dd1a54ef401f8bd2677e30989972
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329485"
---
# <a name="csourceseekingm_rtduration-member"></a>Membro rtDuration di CSourceSeeking:: m \_

Durata del flusso. Per impostazione predefinita, il valore viene impostato sul valore della variabile membro [**CSourceSeeking:: m \_ rtStop**](csourceseeking-m-rtstop.md) .

## <a name="syntax"></a>Sintassi


```C++
CRefTime m_rtDuration;
```



## <a name="remarks"></a>Osservazioni

Prima di accedere a questa variabile, mantenere la sezione **\_ pLock critico m** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




