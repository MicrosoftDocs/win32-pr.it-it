---
description: Ora di arresto. Per impostazione predefinita, il valore è impostato su un numero molto elevato. La classe derivata può reimpostare il valore nel costruttore o quando il filtro viene inizializzato.
ms.assetid: 1fddcf84-fd9a-4dad-892c-1b0abbb0ca55
title: 'Membro CSourceSeeking:: m_rtStop (Ctlutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_rtStop
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 28031f245ef877eca38129df2a86210f90093db4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330201"
---
# <a name="csourceseekingm_rtstop-member"></a>Membro rtStop di CSourceSeeking:: m \_

Ora di arresto. Per impostazione predefinita, il valore è impostato su un numero molto elevato. La classe derivata può reimpostare il valore nel costruttore o quando il filtro viene inizializzato.

## <a name="syntax"></a>Sintassi


```C++
CRefTime m_rtStop;
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

 

 




